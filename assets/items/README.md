# Item art

35 original SVG illustrations authored for 유하의 후쿠오카 여행. No third-party game art,
emoji images, brand logos, or reference photographs are embedded. 128 × 128 viewBox,
transparent background, muted palette, outlined silhouettes, soft contact shadows.

Regenerate with `python3 scripts/generate-item-art.py` from the repository root.
Item names resolve through `src/data/items.ts`; saved inventory strings remain unchanged.
The same artwork is used in shop listings and inventory. All SVGs are precached by the
production service worker. Additional network APIs are not required.

- Food/drink: ramen, bento, sandwich, water, coffee, green-tea, juice, egg,
  gyoza, hotpot, curry, bread, cookies, chocolate, cake
- Goods: pouch, bag, handkerchief, mug, bear, pencils, notebook, puzzle, top, gift
- Records: meal-record; card-sea, card-flower, card-park, card-city, card-animal,
  card-robot, card-food, card-play, card-map

These are game illustrations, not photographs of products sold at actual venues.
