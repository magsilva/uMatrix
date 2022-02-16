## Building uMatrix

### Requirements

* bash
* python 3

You will need both `uMatrix` and the community managed `uAssets` repositories in
the same directory:
```
git clone https://github.com/uBlockOrigin/uAssets.git
git clone https://github.com/ibhagwan/uMatrix.git
cd uMatrix
```

### Packaging / Installation
You can now run the scripts that package everything up.
These are bash scripts. They have only been tested on Linux and MacOS.

#### For Firefox
```
tools/make-firefox.sh all
cp ./dist/build/uMatrix.firefox.xpi ~/Downloads
```

Open Firefox and navigate to
`file:///home/bhagwan/Downloads/uMatrix.firefox.xpi`

> To enable unverified add-on installation, navigate to `about:config` and set
> `xpinstall.signatures.required` to `false`.

#### For Chrome/Chromium
```
tools/make-chromium.sh all
cp -pR ./dist/build/uMatrix.chromium ~/Downloads
```

- In Chromium navigate to `chrome://extensions/` and enable "Devloper Mode"
- Click "Load Unpacked" and select the folder `~/Downloads/uMatrix.chromium`

#### For Opera
```
tools/make-opera.sh
```

The installation package should now be found in dist/build/

### Installing

Follow the instructions in [README.md](README.md) to install it.
