# phone-photos-cdn

Rendus produits officiels de telephones, servis en CDN pour des sites e-commerce.

- **333 images**, **53 modeles**
- `apple/` — 151 rendus Apple officiels, **PNG a fond transparent**, un par coloris, plus les vues de dos et de profil quand elles existent
- `android/` — 182 rendus Samsung, Redmi, TECNO, Infinix, itel
- `index.json` — la carte complete : modele -> fichiers + URLs CDN
- `phonePhotos.ts` — module pret a importer dans un projet React/TypeScript

## Utiliser une image

Via jsDelivr (recommande, CDN mondial) :

```
https://cdn.jsdelivr.net/gh/fresnelbusiness/phone-photos-cdn@main/apple/iphone-15-pro-max/iphone-15-pro-max-blacktitanium.png
```

Ou directement depuis GitHub :

```
https://raw.githubusercontent.com/fresnelbusiness/phone-photos-cdn/main/apple/iphone-15-pro-max/iphone-15-pro-max-blacktitanium.png
```

## Provenance

Chaque image provient du site officiel du constructeur ou de son CDN produit
(`store.storeimages.cdn-apple.com`, `images.samsung.com`, `mi.com`,
`tecno-mobile.com`, `itel-life.com`). Ce sont les visuels que les marques
diffusent a leurs revendeurs. Le champ `source` de `index.json` indique l'origine
pour chaque modele. Les marques et les produits appartiennent a leurs detenteurs
respectifs.

## Nommage

```
apple/<modele-slug>/<modele-slug>-<coloris>[-dos|-profil].png
android/<modele-slug>/<modele-slug>-<NN>.png
```

## Variantes d'image

Chaque visuel existe en trois formats, meme chemin, prefixe different :

| Variante | Chemin | Taille | Usage |
|---|---|---|---|
| Miniature | `thumb/<dossier>/<nom>.webp` | 420 px, ~9 Ko | cartes du catalogue |
| Pleine taille | `webp/<dossier>/<nom>.webp` | 900 px, ~25 Ko | fiche detaillee |
| PNG | `<dossier>/<nom>.png` | 900 px, ~180 Ko | repli, navigateurs sans WebP |

Le WebP est 90 % plus leger que le PNG, les miniatures 96 %.

## Assets Chez Manaf

`chez-manaf/logo.png` · `logo.webp` · `logo-180.png` (favicon) · `fondateur.jpg` · `fondateur.webp`
