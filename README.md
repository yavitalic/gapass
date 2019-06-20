# gapass
Command line wrapper for auto submit TOTP/HOTP verification code and password

## Quick Start
- [Download](https://github.com/yavitalic/gapass.git) the current release of `gapass`
- Copy to `$HOME/bin/gapass` or wherever you want
- Make it executable: `chmod 755 $HOME/bin/gapass`
- Create `$HOME/.gapass`
- Set the configuration file permissions: `chmod 600 $HOME/.gapass`
- ...and execute: `gapass <command> <params>`

### Configuration File
The general format is:
```
name=key
```
An example file would be
```
[gapass]
secret=1234567890123
password=9876543210
```

### Using
```
$ gapass ssh myhost
```
