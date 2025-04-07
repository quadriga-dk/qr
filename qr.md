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
```{code-cell} ipython3
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
  "text-fs-2": {
    "url": "https://quadriga-dk.github.io/Text-Fallstudie-2"
  },
  "bild-fs-1": {
    "url": "https://quadriga-dk.github.io/Bewegtes-Bild-Fallstudie-1/"
  },
  "bild-fs-2": {
    "url": "https://quadriga-dk.github.io/Bewegtes-Bild-Fallstudie-2/"
  },
  "tabelle-fs-1": {
    "url": "https://quadriga-dk.github.io/Tabelle-Fallstudie-1/"
  },
  "tabelle-fs-2": {
    "url": "https://quadriga-dk.github.io/Tabelle-Fallstudie-2/"
  },
  "dkf": {
    "url": "https://doi.org/10.5281/zenodo.14747822"
  },
  "qr-codes": {
    "url": "https://quadriga-dk.github.io/qr"
  },
  "navigator": {
    "url": "https://quadriga.fokus.fraunhofer.de/datasets?locale=de"
  },
  "isi2025-poster-feedback": {
    "url": "https://umfrage.hu-berlin.de/index.php/871645?lang=de"
  },
  "zenodo-community": {
    "url": "https://zenodo.org/communities/quadriga/"
  }
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
:figwidth: 400px
:name: "qr-website"

https://quadriga-dk.de
```


## Text

### 1 _Quantitative Analyse der Medienwellen der Spanischen Grippe (1918/19). Eine Fallstudie_
```{glue:figure} qr-text-fs-1
:figwidth: 400px
:name: "qr-text-fs-1"

https://dh-network.github.io/quadriga
```
### 2 _Quantitative diachrone Analyse der kommunikativen Barrierefreiheit des Berliner Senats (2011-2024). Eine Fallstudie_
```{glue:figure} qr-text-fs-2
:figwidth: 400px
:name: "qr-text-fs-2"

https://dh-network.github.io/quadriga-fs-2
```

## Bewegtes Bild
### 1 _Affektrhetorik in Online-Videos zur Klimakrise. Datengestützte Analysen audiovisueller Muster_
```{glue:figure} qr-bild-fs-1
:figwidth: 400px
:name: "qr-bild-fs-1"

https://quadriga-dk.github.io/Bewegtes-Bild-Fallstudie-1/
```
### 2 _Studentische Filme an der Filmuniversität zur Wendezeit (1985-1999)_
```{glue:figure} qr-bild-fs-2
:figwidth: 400px
:name: "qr-bild-fs-2"

https://quadriga-dk.github.io/Bewegtes-Bild-Fallstudie-2/
```

## Tabelle
### 1 _Reproduzierbarkeit von Datenanalysen: Ein Fallbeispiel aus dem Nationalen Bildungsbericht_
```{glue:figure} qr-tabelle-fs-1
:figwidth: 400px
:name: "qr-tabelle-fs-1"

https://quadriga-dk.github.io/Tabelle-Fallstudie-1/
```
### 2 _Erfragen von Metadaten: Ein Fallbeispiel aus dem Europäischen/Deutschen Metadatenportal_
```{glue:figure} qr-tabelle-fs-2
:figwidth: 400px
:name: "qr-tabelle-fs-2"

https://quadriga-dk.github.io/Tabelle-Fallstudie-2/
```

## Weitere Ressourcen

### QUADRIGA Datenkompetenzframework
```{glue:figure} qr-dkf
:figwidth: 400px
:name: "qr-dkf"

https://doi.org/10.5281/zenodo.14747822
```

### QUADRIGA Navigator (Beta)
```{glue:figure} qr-navigator
:figwidth: 400px
:name: "qr-navigator"

https://quadriga.fokus.fraunhofer.de/datasets?locale=de
```

### ISI 2025 Poster Feedback
```{glue:figure} qr-isi2025-poster-feedback
:figwidth: 400px
:name: "qr-isi2025-poster-feedback"

https://umfrage.hu-berlin.de/index.php/871645?lang=de
```

### QUADRIGA Community auf zenodo.org
```{glue:figure} qr-zenodo-community
:figwidth: 400px
:name: "qr-zenodo-community"

https://zenodo.org/communities/quadriga/
```

### QR-Codes (diese Seite)
```{glue:figure} qr-qr-codes
:figwidth: 400px
:name: "qr-qr-codes"

https://quadriga-dk.github.io/qr/
```