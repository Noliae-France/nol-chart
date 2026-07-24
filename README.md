# nol.chart

Plans comptables (PCG français) : classes, comptes, validation en pur [Nolc](https://noliae-nolc.s3.gra.io.cloud.ovh.net/nolc-latest-linux-x86_64.tar.gz), sans dépendance.

## Installation

```toml
[dependances]
"nol-chart" = { git = "https://github.com/Noliae-France/nol-chart" }
```

## API
`compte_valide`, `compte_classe`, `classe_nom`, `compte_bilan`, `compte_gestion`, `compte_charge`, `compte_produit`, `compte_sous_compte(sous, parent)`.

```nol
compte_classe("607")     // 6
classe_nom(6)            // "Comptes de charges"
compte_charge("607")     // true
compte_sous_compte("4011", "401")  // true
```

Classes PCG : 1 Capitaux · 2 Immobilisations · 3 Stocks · 4 Tiers · 5 Financiers · 6 Charges · 7 Produits · 8 Spéciaux.

## Licence

MIT © 2026 Bastien LANGUEDOC.
