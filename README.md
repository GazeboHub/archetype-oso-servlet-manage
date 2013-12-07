archetype-oso-servlet-manage
============================

## Summary

This project defines a [Maven _Archetype_][mvn-archetypes] for purpose
of creating a project such as would be used to manage the development
and publishing of a Java web application onto a Java web application
container -- whether a Java application server or directly, a servlet
engine -- such that the Java web application container would be
provided via the [OpenShift][openshift] application platform.

## Design Goals

This artifact was designed originally for purpose of providing a means
for structured reuse of a _pattern_ or _model_ developed originally in
the [Gazebo web portal][portal-gproj], such that the model is
comprised of the following components:

1. A _web archive_, published as a `.war` file from a trusted source.

2. An [OpenShift][openshift] _application_ implementing
  [JBoss AS7 on OpenShift][as7-oso] as a container, via the `jbossas`
  [OpenShift][openshift] _cartridge_.

3. A set of resources that must be applied commensurately, for the
   installation of the usptream _web archive_ into `jbossas`,
   including:

    * An _overlay_ that the application must provide onto the upstream
   `  .war` file.

    * A set of _module definitions_ that the application must provide
      onto the application's _jbossas_ instance.

The goal in this _model_ is to install the modified _web archive_ as
the application server's `ROOT.war` application.


[mvn-archetypes]: http://maven.apache.org/guides/introduction/introduction-to-archetypes.html
[openshift]: https://www.openshift.com/
[portal-gproj]: portal-gproj.rhcloud.com
[as7-oso]: https://www.openshift.com/developers/jboss
