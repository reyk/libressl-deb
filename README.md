LibreSSL's libtls for Debian
============================

The [LibreSSL] project provides a free TLS and crypto stack that was
forked from [OpenSSL] in 2014.  The goals are to provide a modernized
codebase, improved security, and to apply best practice development
processes.

[LibreSSL] provides C APIs that are compatible to [OpenSSL]'s [libssl]
and [libcrypto] libraries.  It also provides [libtls], a new TLS
library that is designed to make it easier to write foolproof
applications.

[LibreSSL] conflicts with [OpenSSL] on [Debian] and [Ubuntu] as both
provide the [libssl] and [libcrypto] libraries.  This package only
provides [libtls] as a library, statically linked with the [LibreSSL]
versions of [libssl] and [libcrypto].

This allows to build install programs that use [libtls] without
conflicts.  One example is [OpenBSD]'s TLS-enabled version of
[netcat].

**It includes the [libtls] library but not [libssl] or [libcrypto].**

## Copyright and license

See [COPYING] for details.

[Debian]: https://www.debian.org/
[LibreSSL]: https://www.libressl.org
[OpenSSL]: https://wiki.openssl.org/index.php/Code_Quality
[Ubuntu]: https://www.ubuntu.com/
[libssl]: https://man.openbsd.org/ssl.3
[libtls]: https://man.openbsd.org/tls_init.3
[libcrypto]: https://man.openbsd.org/crypto.3
[netcat]: https://man.openbsd.org/nc.1
