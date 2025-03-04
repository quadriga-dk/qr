---
lang: de-DE
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---
```{code-cell}
:tags: ["remove-cell"]
import qrcode
from myst_nb import glue

qr_dict = {
  "website": {
    "url": "https://quadriga-dk.de"
  },
  "text-fs-1": {
    "url": "https://dh-network.github.io/quadriga"
  },
  "bild-fs-1": {
    "url": "https://quadriga-dk.github.io/Bewegtes-Bild-Fallstudie-1/"
  },
  "tabelle-fs-1": {
    "url": "https://quadriga-dk.github.io/Tabelle-Fallstudie-1/"
  },
  "dkf": {
    "url": "https://doi.org/10.5281/zenodo.14747822"
  },
  "qr-codes": {
    "url": "https://quadriga-dk.github.io/qr"
  },
}
for key, value in qr_dict.items():
  print(f"{key=}; {value=}")
  qr_gen = qrcode.QRCode(
    version=1,
    error_correction=qrcode.constants.ERROR_CORRECT_L,
    box_size=10,
    border=4,
  )
  qr_gen.add_data(value["url"])
  qr_gen.make(fit=True)

  value["qr"] = qr_gen.make_image(fill_color="black", back_color="white")
  print("qr-"+key)
  glue("qr-"+key, value["qr"])
```
# QUADRIGA QR-Codes

## Website
```{glue:figure} qr-website
:figwidth: 450px
:name: "qr-website"

https://quadriga-dk.de
```


## Text

### 1 _Quantitative Analyse der Medienwellen der Spanischen Grippe (1918/19). Eine Fallstudie_
```{glue:figure} qr-text-fs-1
:figwidth: 450px
:name: "qr-text-fs-1"

https://dh-network.github.io/quadriga
```

## Bewegtes Bild
### 1 _Affektrhetorik in Online-Videos zur Klimakrise. Datengestützte Analysen audiovisueller Muster_
```{glue:figure} qr-bild-fs-1
:figwidth: 450px
:name: "qr-bild-fs-1"

https://quadriga-dk.github.io/Bewegtes-Bild-Fallstudie-1/
```

## Tabelle
### 1 _Reproduzierbarkeit von Datenanalysen: Ein Fallbeispiel aus dem Nationalen Bildungsbericht_
```{glue:figure} qr-tabelle-fs-1
:figwidth: 450px
:name: "qr-tabelle-fs-1"

https://quadriga-dk.github.io/Tabelle-Fallstudie-1/
```


## Weitere Ressourcen

### QUADRIGA Datenkompetenzframework
```{glue:figure} qr-dkf
:figwidth: 450px
:name: "qr-dkf"

https://doi.org/10.5281/zenodo.14747822
```

### QR-Codes (diese Seite)
```{glue:figure} qr-qr-codes
:figwidth: 450px
:name: "qr-qr-codes"

https://quadriga-dk.github.io/qr/
```