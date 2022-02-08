# oem-info

Unofficial/community-maintained repo of OEM info for elementary OS System Settings

![Screenshot](screenshot.png) | ![Screenshot Dark](screenshot-dark.png)
------------------------------|----------------------------------------

## To use:

1. Find your device in the list of folders
2. Copy the device's folder's contents to `/etc/` (on elementary OS, open Files as Administrator or use `sudo` from Terminal)
3. Open _System Settings_ → _System_ → _Hardware_ on elementary OS 6 to see the prettiness

## Contributing

I made this for the various devices I use/have used that didn't provide good data out of the box, but pull requests are welcome for more hardware!

See the [Switchboard About Plug's OEM Configuration section](https://github.com/elementary/switchboard-plug-about/#oem-configuration) for more info.

### Images

Images should:

- Be an OEM logo, or represent the hardware itself
  - Previously we recommended it represent the hardware itself, but a logo is simpler and requires less updating over time
  - For hardware with a display, a generic wallpaper or a default screenshot of the latest release of elementary OS is acceptable
- Have a square aspect ratio
- Have a transparent background
- Be at least 256×256 to ensure they show well on HiDPI displays
- Be 512×512 at the largest for filesize concerns
- Work on both light and dark backgrounds
  - or, provide a variant for a dark background with the optional `LogoDark` key

#### To make an image:

Start with a high-resolution version of the OEM logo with a transparent background. Alternatively, find the highest-resolution representative image of the hardware you can with a transparent background. 

1. Open in GIMP
2. Crop the image to the content
3. If the image is larger than 512 in either dimension, scale it down to 512 on the longest side
4. If the canvas is not square, resize the canvas to a square and center the image
5. Export as a PNG

File name does not strictly matter as long as it matches what is in the `oem.conf`, but convention is to name the image a kebab-case version of the OEM name if it is an OEM logo, or the device model number if it is a photo of hardware. E.g. `star-labs.png` or `starbook-mk-v.png`.
