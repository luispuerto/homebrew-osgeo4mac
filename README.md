![docs/assets/osgeo-logo-brew-rgb.png](docs/assets/osgeo-logo-brew-rgb.png)

# Homebrew-osgeo4mac

**Build Status**: [![CircleCI](https://circleci.com/gh/OSGeo/homebrew-osgeo4mac.svg?style=svg)](https://circleci.com/gh/OSGeo/homebrew-osgeo4mac)

This is the [homebrew's][homebrew] tap for the **stable** versions of the [OSGeo][osgeo] geospatial toolset. Right now our main focus is to provide and up-to-date [QGIS][qgis] formulae easy to install to the end user. The tap includes formulae that may not be specifically
from an OSGeo project, but do extend the toolset's functionality

## How do I install these formulae?

Just `brew tap osgeo/osgeo4mac` and then `brew install <formula>`.

Warnings such as the following can be **ignored**:

  * _Warning_: Could not tap **osgeo/osgeo4mac/gdal** over **Homebrew/core/gdal**

Those warnings just indicate formulae in this tap that shadow formulae in the
main Homebrew tap, and will not overwrite them. If the formula conflicts with
one from the main Homebrew tap or another tap you can install directly with:

```
brew install osgeo/osgeo4mac/<formula>
```

**Important**: use the above method to install shadow formula(e) from this tap,
if desired, _prior_ to installing formula that depend upon them. Since the
conflicting formulae names are the same, formulae auto-installed via the
`depends_on` statement will always default to the conflicting tap, not this one,
i.e. conflicting formulae in this tap will _not_ be used when auto-installing.

You can also install via URL:

```
brew install https://raw.githubusercontent.com/OSGeo/homebrew-osgeo4mac/master/Formula/<formula>.rb
```

### Duplicate formulae from Homebrew-core

Some of these formulae have the same name as other formulae —that installs the same package— from [Homebrew-core][homebrew-core]. The reason for this is to add functionality and options to those formule since now homebrew-core formulae is *optionless*. 

We recommend to pin the homebrew-osgeo4mac tap, so the formulae in this tap take precedence over the core tap. 

```shell
$ brew tap-pin osgeo/osgeo4mac
```

As explained in the [Homebrew documentation][taps-docs], you can still install the core version of those formulae just running the following: 

```shell
$ brew install hombrew/core/<name-of-the-formula>
```

## Docs

`brew help`, `man brew`, or the Homebrew [documentation][].







[homebrew]:http://brew.sh
[taps]:https://github.com/Homebrew/homebrew-versions
[documentation]:https://github.com/Homebrew/brew/tree/master/docs#readme
[osgeo]: https://www.osgeo.org
[qgis]: https://www.qgis.org
[homebrew-core]: https://github.com/Homebrew/homebrew-core
[taps-docs]: https://docs.brew.sh/Taps