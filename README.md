# archlinux-initcpio-hooks

## Overview
This hook has been derived from the official "encrypt" hook in archlinux.
This hook allows to type a single passphrase at startup to decrypt multiple
LUKS encrypted devices using dmcrypt. For this to work all devices must have
been configured using the same passphrase.

## How to use
This file needs to be copied to /usr/lib/initcpio/hooks and the "fdencrypt"
hook must be listed in the HOOKS variable in /etc/mkinitcpio.conf for it to take
effect. The kernel boot command line needs to have "cryptdevice=auto"

