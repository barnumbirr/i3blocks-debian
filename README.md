# i3blocks-debian

This repository contains the source to build a Debian package for [i3blocks](https://github.com/vivien/i3blocks).

**The [i3blocks Debian package hasn't been update recently](https://packages.debian.org/search?keywords=i3blocks)
which is a shame considering `v1.5` [is compatible with `i3-gaps`](https://github.com/Airblader/i3blocks-gaps).
As soon as the Debian package is updated this repository can be archived.**

## Usage

If you have [Docker](https://www.docker.com/) installed locally, just run the following:

```bash
user@hostname$ ./build.sh
```
By default this will build i3blocks 1.5 on Debian Buster.

If you want to customize the build at runtime, use the following:

```bash
user@hostname$ ./build.sh -i debian:unstable-slim -v 1.4
```
Don't forget to update `debian/changelog` so your package is generated with the correct version.

## Release

To publish a new package version to Github, follow these steps:
  * update the `VERSION` variable in `build.sh`
  * add a new entry in `debian/changelog`
  * create a new tag with the Debian package version

## License

```
Copyright (c) 2020, Martin Simon

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.
```

## References

* [ayosec/polybar-debian](https://github.com/ayosec/polybar-debian)
* [jpleau-guest/i3blocks](https://salsa.debian.org/jpleau-guest/i3blocks)
