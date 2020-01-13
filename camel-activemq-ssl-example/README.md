# Sample Jboss Fuse AMQ client SSL #

Run locally

``` mvn clean package spring-boot:run```

Deploy on openshift

STEP:

1. Create build config & set base image 


```oc new-build --name=$APP_NAME openshift/java:8 --binary=true```

2. Upload jar 


``` oc start-build $APP_NAME --from-file="camel-activemq-example-0.0.1-SNAPSHOT.jar " --follow ```


3. Create new application . 

``` oc new-app $APP_NAME ```


