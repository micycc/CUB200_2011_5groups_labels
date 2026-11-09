# CUB-200-2011 five look-alike groups (labels + filtered images)

Filtered CUB-200-2011 pack for COMP5523: five look-based coarse groups.

| Group | Species | Images |
|---|---:|---:|
| warbler | 30 | 1790 |
| sparrow | 21 | 1244 |
| gull | 9 | 522 |
| woodpecker | 7 | 408 |
| hummingbird | 4 | 240 |
| **total** | **71** | **4204** |

## Quick start (teammates — one click for images)

You do **not** need the full CUB-200-2011 ~10k-image dump for this 5-group demo.

1. **Clone this labels repo**
   ```bash
   git clone https://github.com/micycc/CUB200_2011_5groups_labels.git
   cd CUB200_2011_5groups_labels
   ```
2. **Download the filtered images** (71 species / 4204 jpgs only) from Google Drive:  
   **[CUB200_2011_5groups_images](https://drive.google.com/drive/folders/1ybkAXBORUaiRyYlNygv5AkaQiJTjns77)**  
   Download **all five** part zips (`part01` … `part05`) plus `README_DOWNLOAD.txt`.
3. **Unzip every part into the same folder** so the `images/` trees merge:
   ```bash
   mkdir -p images_tmp && cd images_tmp
   # unzip all five part*.zip here (Explorer / Archive Utility / unzip)
   # you should get: images/<species>/*.jpg  (71 folders)
   mv images ../images
   cd ..
   ```
4. Paths in `images.txt` already look like `036.Northern_Flicker/….jpg`, so they resolve under `./images/` with no remapping.

### Direct part links (if the folder needs sharing)

- [part01](https://drive.google.com/file/d/1xdCYHD0PNox6V3ISMLvIBQIK0IUhFVH2/view?usp=drivesdk) (~85 MB, 992 jpgs)
- [part02](https://drive.google.com/file/d/1bmeFrj7y5DM-vuptw7L8BuJhbY23HjaO/view?usp=drivesdk) (~87 MB, 894 jpgs)
- [part03](https://drive.google.com/file/d/1C7siNdlPH6i1HJEVkn2rhYHS7eQfkBrG/view?usp=drivesdk) (~86 MB, 898 jpgs)
- [part04](https://drive.google.com/file/d/19D8nQMrGOKTaq44W-fE96MTCJV9Oy45W/view?usp=drivesdk) (~85 MB, 892 jpgs)
- [part05](https://drive.google.com/file/d/1_042YjEh_nThgJ5LFmTcflaLYz3w-Z86/view?usp=drivesdk) (~56 MB, 528 jpgs)

If a link asks for access, ask the repo owner to set the Drive folder to **Anyone with the link → Viewer**.

## What’s in this repo (labels only)

- `classes.txt`, `images.txt`, `image_class_labels.txt`, `bounding_boxes.txt`, `train_test_split.txt`
- `coarse_groups.txt` — remapped class id → species → group
- `attributes.txt` — original attrs + `has_group::{warbler,sparrow,gull,woodpecker,hummingbird}` (ids 313–317)
- `attributes/`, `parts/` — filtered to these images
- **No image bytes in GitHub** (too large). Use the Drive filtered pack above — not the full CUB tarball.

## Grouping rule

Last-word species filter, plus 8 look-alike extras: Northern Flicker → woodpecker; Green Violetear → hummingbird; Red-legged Kittiwake → gull; Ovenbird, American Redstart, both Waterthrushes, Common Yellowthroat → warbler.

Dual PASS: Checky + Picky (2026-11-04). Images pack added 2026-11-09.
