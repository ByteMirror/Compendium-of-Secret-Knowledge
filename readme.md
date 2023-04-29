# Mac Spellbook of Secrets

> 👋🏻 Disclaimer
>
> I really love Mac OS but some things about it are quite annoying. For that reason I wanted to create a list of changes I make to Mac OS to make it more productive and fun to use. I thought sharing this list might help other Developers struggling with the same issues.


## Useful Settings

### Faster Dock Hiding

`defaults write com.apple.dock autohide-delay -float 0; defaults write com.apple.dock autohide-time-modifier -int 0;killall Dock`

#### Undo:

`defaults write com.apple.dock autohide-delay -float 0.5; defaults write com.apple.dock autohide-time-modifier -int 0.5 ;killall Dock`

### Add Spacer to Dock

`defaults write com.apple.dock persistent-apps -array-add '{tile-data={}; tile-type="spacer-tile";}' && killall Dock`

> ⚠️ Attention
>
> To remove the spacer, simply drag and drop it out of your dock, like an application.

### Add Half-Height Spacer to Dock

`defaults write com.apple.dock persistent-apps -array-add '{"tile-type"="small-spacer-tile";}' && killall Dock`


### Disable annoying warning when removing USB from Mac

`sudo defaults write /Library/Preferences/SystemConfiguration/com.apple.DiskArbitration.diskarbitrationd.plist DADisableEjectNotification -bool YES && sudo pkill diskarbitrationd`

> ⚠️ Attention
>
> This change to qlist requires a restart of your Mac

### Re-Enable Annoying Disk Warning (Why would you though?)

`sudo defaults delete /Library/Preferences/SystemConfiguration/com.apple.DiskArbitration.diskarbitrationd.plist DADisableEjectNotification && sudo pkill diskarbitrationd`

### Change Screenshot Default to JPG (Replace with png to undo)

`defaults write com.apple.screencapture type jpg`


### Make Hidden Apps Transparent

`defaults write com.apple.Dock showhidden -bool TRUE && killall Dock`

