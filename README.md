
# This is a proof of concept for a local rpm mirroring #

## Googls ##

- Hard control of rpm versions pinning
- Speed up download
- Independence from external sources

## concept ##

A server loads all packages locally. This server shares its RPMs with all other
servers via nfs. RPM versions pinning will be done via rsync exclude flag.
