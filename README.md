# copy
This is the simple version of a script using scp to copy over network.

## Usage:
```fish
./copy $WHAT $WHERE_TO_SEND $WHERE_TO_LAND
```

For sample:

```fish
tar cfz songs.tar.gz songs
./copy songs.tar.gz 192.168.8.100 /home/lukaszwieczorek/Music/
```

## Predisposition
### Enabled SSH
Check under Sharing in MacOS if remote login is enabled.

### Keys

First we need a public key to a pendrive.

```fish
cat ~/.ssh/$PUBLIC_KEY /Volumes/$DRIVE/
```

Then we need to add the public key to `authorized_keys`,
under the user to which we will be logging using scp.

```fish
cat /Volumes/$PUBLIC_KEY >> ~/.ssh/authorized_keys
```
