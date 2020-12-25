# mx-puppet-steam

Matrix <-> Steam puppeting bridge based on [mx-puppet-bridge](https://github.com/Sorunome/mx-puppet-bridge)

## Status

- [x] login with steam guard support
- [x] 1<->1 messaging
- [x] group messaging
- [x] steam <-> matrix typing notifications
- [x] online/offline status
- [x] retrieve nickname and avatar from steam
- [x] listing of steam users
- [ ] listing of steam group chats
- [ ] listing of members within group chat
- [x] bridging embedded images in 1<->1 chats
- [x] receiving embedded images from steam in group chats
- [ ] sending embedded images to steam in group chats
- [x] steam -> matrix emotes 

## Linking

Start a chat with @_steampuppet_bot:yourserver.com

```
link <username> <password>
```

If a steam guard (mobile or email) code is required, you will be asked for the code.

## Ephemeral events

To enable bridging ephemeral events from matrix to steam (typing notification, read markers and presence)
you'll need to enable the experimental support in synapse for pushing these events to the bridge by setting

```yaml
"de.sorunome.msc2409.push_ephemeral": true
```

in your registration file.
