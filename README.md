# Atlassian Plugins
## OneLogin Authenticators for Confluence and Jira
-----
Overview

The included projects are for the purpose of autheticating with Atlassian's Jira and Confluence. Documentation for setting up a particular project for a particular purposes is included in each project. That is to say documentation for setting up and configuring Confluence is in the confluence directory. Documentation for Jira is in the Jira directories.

-----
Builds

These projects are written in Java and the builds are based on Maven. Requirements for building include a) a current version of Java and b) a current version of Maven. For details on Maven seen https://maven.apache.org/. Builds have been tested with Java version 1.8.0_60 and Maven 3.3.3. The version of Java you choose to build with will be dependent on the requirements of your use case.

The build for Jira version6 has an additional dependency, the latest OneLogin java-saml jar (java-saml-1.1.2.jar), from the onelogin/java-saml project on GitHub. So for building Jira version6 the steps are: sync onelogin/java-saml, build onelogin/java-saml (it's also a Maven/Java project). Run 'mvn clean install' to place the java-saml-1.1.2.jar in your local Maven repository. Next pull the lastest from onelogin/atlassian and run 'mvn clean install' from version6 to bulid your Jira version6 artifacts.  

