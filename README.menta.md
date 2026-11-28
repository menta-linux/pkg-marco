# pkg-marco (Menta Linux)

Debian packaging of marco 1.29.1 (from debian-mate-team/marco on Salsa, 1.26.2-6).
Needed because mate-control-center master requires `libmarco-private >= 1.29.0`
and Debian unstable only has 1.26.2.

Changes versus Debian: new upstream, Debian patches 0001/0002/0003/1001 dropped
(already upstream), symbols file updated, libmate-desktop-dev (>= 1.27.1)
build-dependency. marco is an X11 window manager: it has no Wayland or in-process
build options, so none are set.

Versioning: `<upstream>-<debian rev>mentaN` (e.g. `1.29.1-1menta1`).

CI builds on every push to `master` (needs the menta mate-desktop `latest` release)
and publishes the .debs as the rolling `latest` release. Pushing a tag
`menta/<version>` also creates a tagged release.
