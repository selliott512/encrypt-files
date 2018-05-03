encrypt-files
=============

A simple utility that can be used to encrypt individual files while preserving
file names. This can be used when the file names are helpful and not sensitive.

To encrypt "/tmp/src" to "/tmp/enc" something like:
    encrypt-files -ruvx /tmp/src /tmp/enc

To decrypt "/tmp/enc" to "/tmp/dec" something like:
    encrypt-files -duvx /tmp/enc /tmp/dec

Also "remote-encrypted-backup" is included as a cron job wrapper for creating
encrypted backups on a remote system. Copy to it to something like 
"/etc/cron.daily".

For both "encrypt-files" and "remote-encrypted-backup" the corresponding 
configuration file should be copied from the "etc" subdirectory to "/etc" and
then edited. Make sure that "encrypt-files.conf" is not world readable since
it contains a password that should be changed.

GPLv2, as per the license file, or any later GPL license may be used.
