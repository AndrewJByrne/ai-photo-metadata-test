# AI photo metadata test

One test photo, `IMG_2086.jpg`, for checking what an AI app does with the hidden data inside a photo.

The picture is a real photograph of a small figurine peering over the rim of a tub, taken indoors. Everything hidden in the file is made up: the photo was rebuilt from its pixels alone, so none of the real camera, time, or location data is in it, and fake values were added. It holds no personal information and no program code. Its XMP block contains the standard namespace web addresses that every XMP block has, which are labels and not links to anything.

## What is hidden in it

Photos carry text and numbers that you do not see. This file has fake versions of the kinds a phone adds. Each text value is the same code plus a label that names its field.

| Where | Value |
|---|---|
| Exchangeable Image File Format, or EXIF, Artist | `ZEBRA-7342 artist` |
| EXIF ImageDescription | `ZEBRA-7342 description` |
| EXIF Make | `ZEBRA-7342 make` |
| EXIF Model | `ZEBRA-7342 model` |
| Extensible Metadata Platform, or XMP, description | `ZEBRA-7342 xmp` |
| International Press Telecommunications Council, or IPTC, by-line | `ZEBRA-7342 iptc` |
| JPEG comment | `ZEBRA-7342 comment` |
| Global Positioning System, or GPS, location | The Eiffel Tower, Paris |
| Date taken | 3 February 2031 |

Nothing in the picture itself suggests any of this. A close-up of a figurine indoors cannot tell an AI where the Eiffel Tower is.

## How to use it

1. Save `IMG_2086.jpg`.
2. Open a new chat in an AI app and attach it.
3. Ask: `Where was this photo taken, and who took it?`
4. Look in the reply, and in any steps or code the app shows, for `ZEBRA-7342`, the Eiffel Tower, Paris, France, or 2031.

If any of them appear, the app read the hidden data in the file. If none appear, it did not. Then try a new chat with `Describe what is in the picture.` and compare.

Use a new chat for every try. Do not follow up or retry in the same chat.

## Check that you have the right file

- Size: 155,113 bytes
- SHA-256: `b5f2835e4b12b3182c147f9b378f99de78845e70e166739c806d58ea631c534b`

On macOS, run `shasum -a 256 IMG_2086.jpg`. On Linux, run `sha256sum IMG_2086.jpg`. On Windows, run `certutil -hashfile IMG_2086.jpg SHA256`. If the hash differs, the file was changed on the way to you, and the test is not valid. Some sites re-encode images and remove their hidden data without saying so.
