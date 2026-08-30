# WingRadar map styles v1

These styles are the Phase 3, application-owned visual policy. They are not
wired into the production application.

## Provenance

- Upstream style: OpenFreeMap Liberty, MapLibre style specification v8
- Retrieved: 2026-08-30 from `https://tiles.openfreemap.org/styles/liberty`
- OpenFreeMap repository reference:
  `8892fc6e1dd7433826c9e9b88f3b9915c7e7e135`
- Unmodified response:
  `upstream/openfreemap-liberty.json`
- Upstream license record: `licenses/OpenFreeMap-LICENSE.md`

OpenFreeMap does not expose a style-response commit identifier. The repository
commit records the reviewed project/license state on the retrieval date; the
unmodified HTTP response is therefore retained as the exact style snapshot.

## Published styles

- `published/wingradar-day.json` retains the Liberty visual baseline.
- `published/wingradar-night.json` is derived from the same Liberty layer set,
  with a dark palette and high-contrast labels. It intentionally retains all
  25 symbol layers, including road, locality and four POI layers.

Both styles initially use replaceable OpenFreeMap public delivery for vector
tiles, raster relief, glyphs and sprites. Both include required OpenMapTiles,
OpenStreetMap and Natural Earth attribution in their sources.

Run `dart run tool/validate_map_styles.dart` before publishing or changing a
style. Generated output must also pass `test/map_styles/map_style_validation_test.dart`.

