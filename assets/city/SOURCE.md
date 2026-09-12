# Fukuoka / Hakata LOD2 extract

Source: Fukuoka City 2024 3D city model, distributed by MLIT Project PLATEAU.
https://www.mlit.go.jp/plateau/
https://docs.plateauview.mlit.go.jp/datasets/3d-tiles/

Canal City tile:
https://assets.cms.plateau.reearth.io/assets/15/c3e22e-aa0a-411c-b34d-d40035ae940b/40130_fukuoka-shi_city_2024_citygml_2_op_bldg_3dtiles_40132_hakata-ku_lod2/data/data112.b3dm

Usage policy / attribution: https://www.mlit.go.jp/plateau/site-policy/
Used under the site's CC BY 4.0-compatible public-data terms.

Adapted for this game: decoded Draco geometry, converted ECEF/glTF axes to local
meters, each building grounded at y=0, colors assigned by the game, metadata
reduced to building envelopes and draw ranges. Not an official MLIT visualization.
No photographic textures; vertical terrain datum is deliberately not preserved.
Canal City: 533 buildings, 14,736 triangles.
Hakata Station: data96.b3dm, 216 buildings, 7,362 triangles.
Airport international terminal: data35.b3dm, 1 building, 236 triangles.
The latter two tiles use the same source directory as the Canal City URL.
Total: 750 buildings, 22,334 triangles. Source downloaded 2026-09-12.

Regenerate:
node scripts/decode-plateau.cjs input.b3dm /tmp/canal-decoded.json
python3 scripts/build-plateau.py /tmp/canal-decoded.json public/assets/city/canal data112.b3dm

Architectural accents and facade patterns are original illustrative reconstructions,
not surveyed detail. Station clock dimension reference:
https://tic.citizen.co.jp/sample/hakata.html
Canal City concept (colors, curved architecture):
https://canalcity.co.jp/service/concept
Airport: the surveyed 2024 shell predates the 2025 international terminal expansion.
https://www.fukuoka-airport.jp/information/grandopen-international.html
The model does not claim an exact current terminal layout or photographic fidelity.
