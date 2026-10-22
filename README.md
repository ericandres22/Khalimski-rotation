# Rotation on the Khalimsky Grid — Interactive Demo

Interactive web demo accompanying the paper **"Rotations on the Khalimsky grid"** by Ede Troll, Benedek Nagy, Eric Andres and Gaëlle Largeteau-Skapin.

**Live demo:** https://<username>.github.io/khalimsky-rotation/

## About

The Khalimsky grid (truncated quadrille tiling) alternates octagonal and square pixels. It avoids the topological paradox of the square grid, since octagons have 8 neighbours and squares only 4. Because it is not a point lattice, rotating digital images on it raises specific questions: bijectivity, preservation of cell types, and positional error.

This demo lets you rotate a digital image on the Khalimsky grid and compare several digital rotation methods.

## Rotation methods

| Method | Frame | Operation | Bijective | Preserves cell type |
|---|---|---|:---:|:---:|
| N<sup>lat</sup> | 45° lattice (i, j) | nearest lattice point | no | no |
| C<sup>lat</sup><sub>a</sub> | 45° lattice (i, j) | containing cell of the *a*-grid | no | no |
| Q<sup>lat</sup> | 45° lattice (i, j) | quasi-shear rotation | yes | no |
| N<sup>ind</sup> | octagon grid O(m, n) and square grid S(m, n) | nearest node of the same grid | no | yes |
| Q<sup>ind</sup> | octagon grid O(m, n) and square grid S(m, n) | quasi-shear rotation per grid | yes | yes |

- **Lattice approach (lat):** the whole grid is treated as one lattice, cell types are only labels.
- **Independent approach (ind):** octagons and squares each form an upright square grid; both are rotated separately about the same centre and the results are merged.

The grid parameter *a* (0 < *a* < 2) controls the relative size of octagons and squares; the regular grid corresponds to *a* = 2√2 − 2.

## Usage

Open the live demo in a browser, or run it locally:

```bash
git clone https://github.com/<username>/khalimsky-rotation.git
cd khalimsky-rotation
# open index.html in a web browser
```

No installation or server is required.

## Citation

If you use this demo, please cite:

> E. Troll, B. Nagy, E. Andres, G. Largeteau-Skapin. *Rotations on the Khalimsky grid*. In preparation.

## Authors

- Ede Troll — Eszterházy Károly Catholic University, Eger, Hungary
- Benedek Nagy — Eszterházy Károly Catholic University, Eger, Hungary; Eastern Mediterranean University, Famagusta, North Cyprus
- Eric Andres — XLIM UMR CNRS 7252, Asali team, University of Poitiers
- Gaëlle Largeteau-Skapin — XLIM UMR CNRS 7252, Asali team, University of Poitiers

## License

This project is released under the MIT License — see [LICENSE](LICENSE).
