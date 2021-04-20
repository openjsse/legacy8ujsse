Legacy8uJSSE
----------------------------------------------
Legacy8uJSSE : Fallback JSSE provider for legacy TLS 1.2 protocol implementation on Java SE 8

The Legacy8uJSSE project was created to preserve OpenJDK8 TLS 1.2 protocol
implementation as a separate JSSE provider. This provider could be used
us a fallback option for the new TLS 1.3 implementation for Java SE 8.

----
### Code origins and evolution

The project code is comprised primarily of the OpenJDK 8 implementations
of various components that together comprise of a TLS 1.2 JSSE provider.
The structure of the OpenJDK 8 code has been kept mostly intact, with
associated packages placed under the org.openjsse.legacy8ujsse* namespace
to avoid collisions.

The code for this project is licensed under the OpenJDK GPLv2 + CPE
license, as described in the LICENSE file at the base of this repository
and in notices found in the various source files.

----
### Installation

Copy provider into you Java SE 8 directory:

    cp target/legacy8ujsse-<version>.jar $JAVA_HOME/jre/lib/ext/legacy8ujsse.jar

Copy provider security properties:

    cp conf/security/legacy8ujsse.security $JAVA_HOME/jre/lib/ext/legacy8ujsse.jar

----
### Enabling Legacy8uJSSE provider
 
Add the Legacy8uJSSE provider to your list of registered security providers
using the following cmdline option:

    -Djava.security.properties=$JAVA_HOME/jre/lib/security/legacy8ujsse.security
    
The Legacy8uJSSE provider replaces the SunJSSE provider.

----
### OpenJDK 8 to Legacy8uJSSE version mapping

| OpenJDK8u | Legacy8uJSSE |
|-----------|--------------|
| 1.8.0_262 | 1.1.0        |
| 1.8.0_271 | 1.1.1        |
| 1.8.0_272 | 1.1.1        |
| 1.8.0_281 | 1.1.1        |
| 1.8.0_282 | 1.1.1        |
| 1.8.0_291 | 1.1.2        |
| 1.8.0_292 | 1.1.2        |
