# custom void packages

This is a custom xbps-src repo that contains packages/changes to existing packages.

Connman now uses iwd by default and the bgra patch is applied onto libXft, numix-solarized-gtk-theme uses the DarkMagenta variant.

All suckless programs are my own builds.

The rest is probably unchanged.

# How to install
1. Clone void-packages
```
git clone --depth 1 https://github.com/void-linux/void-packages
```

2. Clone this repo
```
git clone --depth 1 https://github.com/notchtc/custom-void-packages
```

3. Merge them both
```
cp -r custom-void-packages/srcpkgs/* void-packages/srcpkgs/
```

If you haven't used xbps-src before and don't know what to do next, here's what you have to do
```
cd void-packages
./xbps-src binary-bootstrap
```

To build a package you need to do this in the void-packages directory
```
./xbps-src pkg <pkgname>
```

Now you can either use `xbps-install --repository=/hostdir/binpkgs/ <pkgname>` or `xi <pkgname>` (if you have xtools installed) to install the package.
