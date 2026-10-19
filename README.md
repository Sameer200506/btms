# btms (Battery thermal management system — COMSOL models)

COMSOL Multiphysics models of a lithium-ion battery pack with a battery thermal
management system (BTMS). The models are used to study heat generation, cell
temperature distribution and cooling performance under different pack layouts.

## Files

| File | Description |
| --- | --- |
| `4 battery.mph` | 4-cell pack model (included in this repository) |
| `BTMS (1).mph` | Full BTMS model, ~3.4 GB (not committed — see below) |
| `BTMS (2).mph` | Extended BTMS model, ~12.7 GB (not committed — see below) |
| `BTMS (1).lock` | COMSOL lock file |

## Requirements

- **COMSOL Multiphysics** (the models were authored in a recent 6.x release)
  with the Heat Transfer and Battery Design modules.
- Enough RAM/disk for the large `.mph` files — they are multi-gigabyte
  recovery/model files.

## Opening

1. Copy the large `.mph` files next to `4 battery.mph` (they are intentionally
   excluded from Git because GitHub rejects files over 100 MB).
2. Open COMSOL → **File → Open** → select the `.mph`.
3. Inspect the geometry, materials, heat-source and cooling boundary conditions
   in the model tree, then run the study.

## Why the big files are missing

GitHub's hard limit is 100 MB per file. The two full BTMS models exceed that by
orders of magnitude. Keep them on disk, in cloud storage, or track them with
[Git LFS](https://git-lfs.com/) if you need versioned copies.
