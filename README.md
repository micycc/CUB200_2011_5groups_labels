# CUB-200-2011 five look-alike groups (labels pack)

Filtered CUB-200-2011 metadata for COMP5523: five look-based coarse groups.

| Group | Species | Images |
|---|---:|---:|
| warbler | 30 | 1790 |
| sparrow | 21 | 1244 |
| gull | 9 | 522 |
| woodpecker | 7 | 408 |
| hummingbird | 4 | 240 |
| **total** | **71** | **4204** |

## Layout (CUB-style)

- `classes.txt`, `images.txt`, `image_class_labels.txt`, `bounding_boxes.txt`, `train_test_split.txt`
- `coarse_groups.txt` — remapped class id → species → group
- `attributes.txt` — original attrs + `has_group::{warbler,sparrow,gull,woodpecker,hummingbird}` (ids 313–317)
- `attributes/`, `parts/` — filtered to these images
- **Labels/metadata only** — no image files. Point paths at your local CUB `images/` tree.

## Grouping rule

Last-word species filter, plus 8 look-alike extras: Northern Flicker → woodpecker; Green Violetear → hummingbird; Red-legged Kittiwake → gull; Ovenbird, American Redstart, both Waterthrushes, Common Yellowthroat → warbler.

Dual PASS: Checky + Picky (2026-11-04).
