# Shibboleth Server and SAML Service Provider

It's well known that [CAS](https://github.com/CenterForOpenScience/cas-overlay) serves as the authentication and authorization server for [OSF](https://github.com/CenterForOpenScience/osf.io/) and its services. However, not many of us are aware that there is a [Shibboleth2](https://wiki.shibboleth.net/confluence/display/SHIB2/Home) server (Apache) running on top of CAS (Jetty). This SP server has three primary roles:

* Handles SSL for CAS
* Serves as a SAML2 service provider, which is the vital part of OSF institution login.
* Foward non-SAML2 requests from/to CAS
