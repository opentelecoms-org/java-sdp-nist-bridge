Java SDP NIST Bridge
====================

Rationale
---------
This little project provides a free, Apache 2.0 licensed, implementation of the
JSR 141 `SdpFactory` interface against NIST's public domain reference
implementation of the JSR 141 classes and interfaces.

The entire `javax.sdp` package, including the `SdpFactory` class of the NIST RI
cannot be used because:

- it has a non-free, non-OSI approved, expired, proprietary license
- the interface references the implementation and vice-versa

Usage
-----
Replace the reference to the JAIN RI jar with one that does not include
the `javax.sdp` headers (e.g. `org.jitsi:jain-sip-ri-plain`), then:

- reference `org.opentelecoms.sdp:sdp-api`
- reference `org.opentelecoms.sdp:java-sdp-nist-bridge` (this project)
- replace calls to `SdpFactory.getInstance()` with `new NistSdpFactory()`
