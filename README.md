# LibreSSL's libtls for Debian/Ubuntu

> EXPERIMENTAL!!!

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

**It packages the [libtls] library but not [libssl] or [libcrypto].**

## Package List

* libtls-dev: LibreSSL libtls headers
* libtls-doc: LibreSSL libtls manual pages
* libtls19: LibreSSL libtls
* netcat-libressl: TCP/IP swiss army knife with TLS support

## Installation

```bash
$ sudo apt install dpkg-dev devscripts
$ dpkg-source -x libressl_3.0.2-1.dsc
$ ( cd libressl-3.0.2 && dpkg-buildpackage --no-sign )
$ sudo dpkg -i *.deb
```

The `libressl_3.0.2.orig.tar.gz` source file is directly from
[LibreSSL], you can verify it with the official [signify] or [PGP]
public key.  The format of this repository might change in the future,
including the official release tarball here is to simplify the `.deb`
build.

## Copyright and license

See [COPYING] for details.

[COPYING]: COPYING
[Debian]: https://www.debian.org/
[LibreSSL]: https://www.libressl.org
[OpenBSD]: https://www.openbsd.org/
[OpenSSL]: https://wiki.openssl.org/index.php/Code_Quality
[PGP]: https://ftp.openbsd.org/pub/OpenBSD/LibreSSL/libressl.asc
[Ubuntu]: https://www.ubuntu.com/
[libssl]: https://man.openbsd.org/ssl.3
[libtls]: https://man.openbsd.org/tls_init.3
[libcrypto]: https://man.openbsd.org/crypto.3
[netcat]: https://man.openbsd.org/nc.1
[signify]: https://ftp.openbsd.org/pub/OpenBSD/LibreSSL/libressl.pub
