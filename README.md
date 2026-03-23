Short script to clear Spotify cache run by systemd.

# Setup
Files have to be moved to specific location on your machine:

`~/.config/systemd/user/`

After moving them reload the daemon and enable the timer

`systemctl --user daemon-reload`

`systemctl --user endable --now clear-spotify-cache.timer`

