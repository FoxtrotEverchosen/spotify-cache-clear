Short script to clear Spotify cache run by systemd (linux) or task scheduler (windows).

# Setup - Linux (requires systemd)
The .service and .timer (.bat does not concern you) files have to be moved to specific location on your machine (this directories might not yet exist, in which case you will have to create them):

`~/.config/systemd/user/`

After moving them reload the daemon and enable the timer

`systemctl --user daemon-reload`

`systemctl --user endable --now clear-spotify-cache.timer`

# Setup - Microslop Windows
After downloading the files (or just the .bat file since .service and .timer do not concern you) follow those instructions:

1. Open Task Scheduler
2. Click `Create Basic Task`
3. Set trigger to a desired period
4. Set action to `Start a program` and point it to the .bat file
5. Click `Finish`

If you want it to run efen if scheduled start is missed, you can edit the task settings and check the `Run task as soon as possible after a scheduled start is missed` checkbox.
