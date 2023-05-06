# Consolas Nerd Fonts

**For learning and communication only, do not use for business purposes !!!!!**

This repo is patch to [Nerd Fonts](https://github.com/ryanoasis/nerd-fonts) for **Consolas**.

# Font Apply Name: `'Consolas Nerd Font'`

[Latest FontPatcher](https://github.com/ryanoasis/nerd-fonts/releases/latest/download/FontPatcher.zip)

If you can adjust [Inconsolatas](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/Inconsolata) & [Inconsolatas-go](https://github.com/ryanoasis/nerd-fonts/blob/master/patched-fonts/InconsolataGo). Pleases use [Nerd Fonts](https://github.com/ryanoasis/nerd-fonts) first.

## [tutorials](https://github.com/ryanoasis/nerd-fonts/blob/master/readme.md#font-patcher):
## Steps:
### Use Script:
- Download script and its helper files as [archive](https://github.com/ryanoasis/nerd-fonts/releases/latest/download/FontPatcher.zip) and extract
- Requires: Fontforge, Python 3, python-fontforge and argparse packages
    - Fontforge can be installed as package
    - or on OSX via brew install fontforge
    - or as [AppImage](https://github.com/fontforge/fontforge/releases)
- Usage, recommended:  
`fontforge -script font-patcher PATH_TO_FONT`
- Usage, direct (more convenient call, if it works for you):
`./font-patcher PATH_TO_FONT`
- Usage, with Fontforge AppImage  
_Note_: `chmod u+x` the AppImage after download. All supplied paths need to be **absolute** and an explicit output path is required! If everything is located in the same directory, you can use the `$PWD` shorthand.

  ```
  ./FontForge.AppImage -script $PWD/font-patcher $PWD/BaseFont.ttf -out /tmp
  ```

## Examples:

```
# font-patcher is script in folder
fontforge -script PATH_TO_'font-patcher' <path_to_base_font>/Consolas.ttf

./font-patcher Droid\ Sans\ Mono\ for\ Powerline.otf
./font-patcher Droid\ Sans\ Mono\ for\ Powerline.otf -s -q
./font-patcher Droid\ Sans\ Mono\ for\ Powerline.otf --use-single-width-glyphs --quiet

./font-patcher Inconsolata.otf --fontawesome
./font-patcher Inconsolata.otf --fontawesome --octicons --pomicons
./font-patcher Inconsolata.otf

./FontForge.AppImage -script /tmp/nerdfonts/font-patcher /tmp/nerdfonts/CascadiaMonoPL-Semibold.ttf --fontawesome -out /tmp
./FontForge.AppImage -script $PWD/font-patcher $PWD/CascadiaMonoPL-Semibold.ttf --octicons -out $HOME

docker run --rm -v ~/myfont/patchme:/in -v ~/myfont/patched:/out nerdfonts/patcher
docker run --rm -v ~/Desktop/myfont/patchme:/in -v ~/Desktop/myfont/patched:/out nerdfonts/patcher --fontawesome
```

# TODO
- [ ] Use latest release Patchers to auto patch `Consolas` by Actions (Auto patch to `Consolas` when latest Patcher releases)