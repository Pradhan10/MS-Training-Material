# MS-Training-Material
Material used for ms training at amdocs.

Join Fun Code on WhatsApp : 
https://chat.whatsapp.com/JYt7MIA5qdgKJIkhagiJWn


Running the application locally

There are several ways to run a Spring Boot application on your local machine. One way is to execute the main method in the de.codecentric.springbootsample.Application class from your IDE.

Alternatively you can use the Spring Boot Maven plugin like so:

mvn spring-boot:run

Deploying the application to OpenShift

The easiest way to deploy the sample application to OpenShift is to use the OpenShift CLI:

oc new-app codecentric/springboot-maven3-centos~https://github.com/codecentric/springboot-sample-app

This will create:

    An ImageStream called "springboot-maven3-centos"
    An ImageStream called "springboot-sample-app"
    A BuildConfig called "springboot-sample-app"
    DeploymentConfig called "springboot-sample-app"
    Service called "springboot-sample-app"

If you want to access the app from outside your OpenShift installation, you have to expose the springboot-sample-app service:

oc expose springboot-sample-app --hostname=www.example.com
