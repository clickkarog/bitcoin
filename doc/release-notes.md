<<<<<<< HEAD
(note: this is a temporary file, to be added-to by anybody, and moved to
release-notes at release time)

Bitcoin Core version *version* is now available from:

  <https://bitcoin.org/bin/bitcoin-core-*version*/>

This is a new major version release, including new features, various bugfixes
and performance improvements, as well as updated translations.

Please report bugs using the issue tracker at github:

  <https://github.com/bitcoin/bitcoin/issues>

To receive security and update notifications, please subscribe to:

  <https://bitcoincore.org/en/list/announcements/join/>

Compatibility
==============

Microsoft ended support for Windows XP on [April 8th, 2014](https://www.microsoft.com/en-us/WindowsForBusiness/end-of-xp-support),
an OS initially released in 2001. This means that not even critical security
updates will be released anymore. Without security updates, using a bitcoin
wallet on a XP machine is irresponsible at least.

In addition to that, with 0.12.x there have been varied reports of Bitcoin Core
randomly crashing on Windows XP. It is [not clear](https://github.com/bitcoin/bitcoin/issues/7681#issuecomment-217439891)
what the source of these crashes is, but it is likely that upstream
libraries such as Qt are no longer being tested on XP.

We do not have time nor resources to provide support for an OS that is
end-of-life. From 0.13.0 on, Windows XP is no longer supported. Users are
suggested to upgrade to a newer verion of Windows, or install an alternative OS
that is supported.

No attempt is made to prevent installing or running the software on Windows XP,
you can still do so at your own risk, but do not expect it to work: do not
report issues about Windows XP to the issue tracker.

Notable changes
===============

0.14.0 Change log
=================

Detailed release notes follow. This overview includes changes that affect
behavior, not code moves, refactors and string updates. For convenience in locating
the code changes and accompanying discussion, both the pull request and
git merge commit are mentioned.

### RPC and REST

### Configuration and command-line options

### Block and transaction handling

### P2P protocol and network code

### Validation

### Build system

### Wallet

### GUI

### Tests

### Miscellaneous

Credits
=======

Thanks to everyone who directly contributed to this release:

=======
Bitcoin Core version 0.9.5 is now available from:

  https://bitcoin.org/bin/0.9.5/

This is a new minor version release, bringing only bug fixes and updated
translations. Upgrading to this release is recommended.

Please report bugs using the issue tracker at github:

  https://github.com/bitcoin/bitcoin/issues

How to Upgrade
===============

If you are running an older version, shut it down. Wait until it has completely
shut down (which might take a few minutes for older versions), then run the
installer (on Windows) or just copy over /Applications/Bitcoin-Qt (on Mac) or
bitcoind/bitcoin-qt (on Linux).

Notable changes
================

Mining and relay policy enhancements
------------------------------------

Bitcoin Core's block templates are now for version 3 blocks only, and any mining
software relying on its `getblocktemplate` must be updated in parallel to use
libblkmaker either version 0.4.2 or any version from 0.5.1 onward.
If you are solo mining, this will affect you the moment you upgrade Bitcoin
Core, which must be done prior to BIP66 achieving its 951/1001 status.
If you are mining with the stratum mining protocol: this does not affect you.
If you are mining with the getblocktemplate protocol to a pool: this will affect
you at the pool operator's discretion, which must be no later than BIP66
achieving its 951/1001 status.

0.9.5 changelog
================

- `74f29c2` Check pindexBestForkBase for null
- `9cd1dd9` Fix priority calculation in CreateTransaction
- `6b4163b` Sanitize command strings before logging them.
- `3230b32` Raise version of created blocks, and enforce DERSIG in mempool
- `989d499` Backport of some of BIP66's tests
- `ab03660` Implement BIP 66 validation rules and switchover logic
- `8438074` build: fix dynamic boost check when --with-boost= is used

Credits
--------

Thanks to who contributed to this release, at least:

- 21E14
- Alex Morcos
- Cory Fields
- Gregory Maxwell
- Pieter Wuille
- Wladimir J. van der Laan
>>>>>>> refs/remotes/karogkung/0.9

As well as everyone that helped translating on [Transifex](https://www.transifex.com/projects/p/bitcoin/).
