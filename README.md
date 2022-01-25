# DiceBear Py Wrapper
[`dicebear`](https://pypi.org/project/dicebear/) is an API wrapper for https://dicebear.com. Using this wrapper you can get custom avatars for your program.
\
For an example go to [`examples/dicebear.py`](https://github.com/jvherck/dicebear/tree/main/examples).

## Useful links
* PyPI: https://pypi.org/project/dicebear/
* GitHub: https://github.com/jvherck/dicebear

## How to install
Run `pip install dicebear`\
If that doesn't work try `py -m pip install dicebear`

## Usage
```python
from dicebear import DAvatar, DStyle, DOptions, DColor

options = DOptions(backgroundColor=DColor("#00ddd0"))

av = DAvatar(style=DStyle.pixel_art, seed="John Apple", options=options)
# this returns a URL to the avatar

print(av)
# str(DAvatar) returns the png url to the avatar

print(av.style, av.seed, av.options)

av.edit(extra_options=DOptions(flip=True))
# edit the avatar more to your liking
# using `extra_options` you add/replace these options to the old ones
# using `blank_options` you reset the old options and add these new options

print(av.url_png, av.url_svg)

print(av.full_svg)
# using `DAvatar.avatar_svg` you can get the svg code for the avatar
```


### Styles
All the possible avatar styles. \
https://avatars.dicebear.com/styles

* `adventurer`
* `adventurer-neutral`
* `avataaars`
* `big-ears`
* `big-ears-neutral`
* `big-smile`
* `bottts`
* `croodles`
* `croodles-neutral`
* `identicon`
* `initials`
* `micah`
* `miniavs`
* `open-peeps`
* `personas`
* `pixel-art`
* `pixel-art-neutral`

### Base Options
All the possible options for the avatar. These options work for all the styles.

* `seed` (type: `str`) - the seed for the avatar generator (determine its basic looks)
* `dataUri` (type: `bool`) - whether to give the dataUri 
* `flip` (type: `bool`) - flips the image vertically
* `rotate` (type: `int`) - rotates the avatar
* `scale` (type: `int`) - the scale of the avatar
* `radius` (type: `int`) - the radius of the avatar
* `size` (type: `int`) - the size of the avatar
* `backgroundColor` (type: `DColor( " #ffffff " )` ) - the background color of the avatar
* `translateX` (type: `int`) - move the avatar horizontally
* `translateY` (type: `int`) - move the avatar vertically

### Specific Style Options 
Specific options to get a more detailed avatar. This is different for every style.

* [adventurer](https://avatars.dicebear.com/styles/adventurer#style-options)
* [adventurer-neutral](https://avatars.dicebear.com/styles/adventurer-neutral#style-options)
* [avataaars](https://avatars.dicebear.com/styles/avataaars#style-options)
* [big-ears](https://avatars.dicebear.com/styles/big-ears#style-options)
* [big-ears-neutral](https://avatars.dicebear.com/styles/big-ears-neutral#style-options)
* [big-smile](https://avatars.dicebear.com/styles/big-smile#style-options)
* [bottts](https://avatars.dicebear.com/styles/bottts#style-options)
* [croodles](https://avatars.dicebear.com/styles/croodles#style-options)
* [croodles-neutral](https://avatars.dicebear.com/styles/croodles-neutral#style-options)
* [identicon](https://avatars.dicebear.com/styles/identicon#style-options)
* [initials](https://avatars.dicebear.com/styles/initials#style-options)
* [micah](https://avatars.dicebear.com/styles/micah#style-options)
* [miniavs](https://avatars.dicebear.com/styles/miniavs#style-options)
* [open-peeps](https://avatars.dicebear.com/styles/open-peeps#style-options)
* [personas](https://avatars.dicebear.com/styles/personas#style-options)
* [pixel-art](https://avatars.dicebear.com/styles/pixel-art#style-options)
* [pixel-art-neutral](https://avatars.dicebear.com/styles/pixel-art-neutral#style-options)