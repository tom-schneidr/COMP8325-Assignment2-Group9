# COMP8325 Assignment 2

Group project repo for the BODMAS malware category classification assignment.

## Repo layout

- `notebooks/`: the three assignment notebooks.
- `docs/`: short project notes, such as model choice rationale.
- `report/`: final report files.
- `slides/`: final presentation slides.
- `results/`: generated local outputs, such as metrics and figures.
- `data/`: local BODMAS files. This folder is ignored by git.

## How to get the data files

1. Download all files from the assignment Google Drive folder:
   https://drive.google.com/drive/folders/1Uf-LebLWyi9eCv97iBal7kL1NgiGEsv_

2. Create a folder called `data/` in the repo root.

3. Put the BODMAS files in `data/`:
   - `bodmas.npz`
   - `bodmas_metadata.csv`
   - `bodmas_malware_category.csv`

Do not commit the data files. They are too large for GitHub and are ignored by `.gitignore`.
