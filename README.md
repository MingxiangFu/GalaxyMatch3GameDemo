# Galaxy classification match-3 demo



Educational match-3 from `GalaxyImages4Class/` (**unzip** from **GalaxyImages4Class.zip**, face-on spiral, edge-on disk, irregular, smooth). Matching is by **class** (subfolder), not identical pixels. After a clear, survivors fall and new images enter from the top.

这是一个用四类星系形态目录做成的科普消消乐：按类别匹配，不按同一张图匹配。

## Play

打开方式 / how to play:

1. Open `index.html` in a browser (double-click, or drag into Chrome/Safari).
2. Optional local server:
   `python3 -m http.server 43147 --bind 127.0.0.1`
3. Swap adjacent tiles. Three or more galaxies of the **same morphological class** clear even when the photos differ.

`index.html` is a single portable file (inline CSS/JS, JPEG data URIs).

`index.html` 可单独打开；图像以 JPEG 的 data URI 嵌入。

## Rebuild

改图或改玩法后，用当前四类目录重建：

```bash
python3 tools/build_index.py
```

This reads `GalaxyImages4Class/` (default 12 unique JPEGs per class) and writes a new portable `index.html`. Template: `tools/game.template.html`. Checks: `node tools/verify_rules.cjs`.

## Dataset

- **Included:** `GalaxyImages4Class/` — FaceOnSpirals, EdgeOnDisk, Irregular, Smooth.

