# G834JY Audio Fix

Easy Effects output preset for the ASUS ROG Strix G18 G834JY running CachyOS.

On Linux, this laptop can sound overly bassy and muffled compared with Windows because the Windows/Dolby/vendor audio processing is missing. This preset is a practical correction profile that gets the built-in speakers much closer to a normal sound on my setup.

It is not perfect or universal. Speaker response, firmware, PipeWire settings, Easy Effects versions, and personal preference can all change the result. If you find improvements, please open an issue or PR so the profile can get better.

## What It Uses

The preset chain is:

```text
Equalizer -> Multiband Compressor -> Crystalizer -> Limiter
```

The EQ reduces low-end boom, restores upper-mid and treble clarity, and the limiter/multiband compressor help control harshness and clipping.

## Install

Install Easy Effects, then copy the preset into your Easy Effects output preset directory:

```bash
mkdir -p ~/.local/share/easyeffects/output
cp presets/output/G834JY-CachyOS-Audio-Fix.json ~/.local/share/easyeffects/output/G834JY-CachyOS-Audio-Fix.json
```

Restart Easy Effects if it is already open, then load the output preset named `G834JY-CachyOS-Audio-Fix`.

## Device

Tested on:

```text
Laptop: ASUS ROG Strix G18 G834JY
OS: CachyOS
Audio stack: PipeWire + Easy Effects
Preset type: Easy Effects output preset
```

## Disclaimer

Use this as a starting point, not a guaranteed perfect correction. It was tuned by ear on one laptop. If it sounds too sharp, too quiet, distorted, or still too bassy on your machine, adjust it and share what worked.
