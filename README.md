# Ansible role for Mopidy

Installs and configures [Mopidy](https://www.mopidy.com/).

## Requirements

<!-- Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required. -->


## Role Variables

<!-- A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well. -->

Variable | Description
--- | ---
`mopidy_audio_output` | The audio output to use. Default: `autoaudiosink`. For [Snapcast](https://github.com/badaix/snapcast), use `output = audioresample ! audioconvert ! audio/x-raw,rate=48000,channels=2,format=S16LE ! wavenc ! filesink location=/tmp/snapfifo`.

Use https://www.mopidy.com/authenticate/ to generate tokens for SoundCloud and/or Spotify.


## Dependencies

None


## Example Playbook

See included `playbook.yml`.
