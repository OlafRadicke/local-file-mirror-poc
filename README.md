
# This is a proof of concept for a local rpm mirroring #

## Googls ##

- Hard control of rpm versions pinning
- Speed up download
- Independence from external sources

## concept ##

A server loads all packages locally. This server shares its RPMs with all other
servers via nfs. RPM versions pinning will be done via rsync exclude flag.


## Sync diffs ##

The sync logs will written in /var/log/mirror-sync.<repo name>.log


## Exclude rpm updates ##

Edit this file:

```bash
[oradicke@aux-01 local-file-mirror-poc]$ cat ./roles/sync_mirror/files/mirror-exclude-list.txt
*selinux-policy*.rpm
*NetworkManager*.rpm
*kernel*.rpm
```
