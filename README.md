# macOS Mojave Set Desktop Image

## Purpose
Set a user's Desktop image in macOS Mojave 10.14 from the command line. See [Limitations](#limitations)

## Background
An explanation for why this script does what it does can be found at [Setting the Desktop Image in Macos Mojave From the Command Line](https://www.tech-otaku.com/mac/setting-desktop-image-macos-mojave-from-command-line)

## Usage
`[bash] /path/to/set-desktop-mojave.sh <desktop image>`

## Examples

#### HEIF (.heic) images

###### Mojave Dynamic
`[bash] /path/to/set-desktop-mojave.sh mojave`

###### Mojave Light (Still)
`[bash] /path/to/set-desktop-mojave.sh light`

###### Mojave Dark (Still)
`[bash] /path/to/set-desktop-mojave.sh dark`

###### Solar Gradients
`[bash] /path/to/set-desktop-mojave.sh solar`

#### non-HEIF (.heic) images

###### High Sierra
`[bash] /path/to/set-desktop-mojave.sh "/Library/Desktop Pictures/High Sierra.jpg"`

###### Ink Cloud
`[bash] /path/to/set-desktop-mojave.sh "/Library/Desktop Pictures/Ink Cloud.jpg"`

#### Other

###### Default
`[bash] /path/to/set-desktop-mojave.sh default`

## Error Messages

###### Not running macOS Mojave
`ERROR: For use with macOS Mojave 10.14.x only.`

###### No Desktop image passed on the command line
`ERROR: No image was specified.`

###### Supplied Desktop image is a file that doesn't exist
`ERROR: '/path/to/desktop/image.jpg' doesn't exist.`

###### Invalid option passed on the command line
`ERROR: 'option' is not a valid option.`

###### Attempt to reset a database other than desktoppicture.db to the default
`ERROR: The 'default' option is only appropriate when the database is ~/Library/Application Support/Dock/desktoppicture.db`

###### Possible dual-monitor environment detected
`ERROR: This script should not be used in a dual-monitor environment.`

###### Two or more Desktops (Spaces) detected
`ERROR: This script should not be used when multiple Desktops (Spaces) are configured.`


## Limitations
Works only with a single Desktop (Space) in a single-display environment.

__Not for use with multiple Desktops (Spaces) or in a dual-display environment.__
