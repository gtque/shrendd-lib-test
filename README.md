# shrendd-lib-test
simple project for testing shrendd library support

some simple text and yaml based templates.

- version 1.0.0:
    - bob/text/biscuits.txt
        -  lib.butter.milk
    - bob/text/cake.txt.srd
        - lib.butter.alternative
    - bob/yaml/simple.yml.srd
        - LIB_TEST -> lib.test
    - k8s/configmaps/simple_configmap.yml.srd
        - LIB_APP_TEST_NAME -> lib.app.test.name
        - LIB_APP_TEST_NAMESPACE -> lib.app.test.namespace
        - LIB_APP_TEST_MANAGER -> lib.app.test.manager
        - lib.app.test.version
    - k8s/configmaps/script_configmap.yml.srd
        - import: shrendd-lib-test:k8s/configmaps/simple_configmap.yml.srd
        - import: shrendd-lib-test:k8s/script/some-script.sh.srd:K8sScript
        - LIB_APP_TEST_NAME -> lib.app.test.name
    - k8s/scripts/some-script.sh
        - lib.script.message

- version 2.0.0:
    - bob/text/biscuits.txt
        -  lib.butter.milk2
    - bob/text/cake.txt.srd
        - lib.butter.alternative2
    - bob/yaml/simple.yml.srd
        - LIB_TEST -> lib.test2
    - k8s/configmaps/simple_configmap.yml.srd
        - LIB_APP_TEST_NAME -> lib.app.test.name2
        - LIB_APP_TEST_NAMESPACE -> lib.app.test.namespace2
        - LIB_APP_TEST_MANAGER -> lib.app.test.manager2
        - lib.app.test.version2
    - k8s/configmaps/script_configmap.yml.srd
        - import: shrendd-lib-test:k8s/configmaps/simple_configmap.yml.srd
        - import: shrendd-lib-test:k8s/script/some-script.sh.srd:K8sScript
        - LIB_APP_TEST_NAME -> lib.app.test.name2
    - k8s/scripts/some-script.sh
        - lib.script.message2