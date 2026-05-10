# Image Credits

All photographs used in `italy-trip-family.html` are sourced from Wikimedia
Commons via the `Special:FilePath` redirect, which always resolves to the
current location of the original file. Captions in the HTML credit the
source.

## A note on URL verification

Image URLs **were not pre-verified** in this build because the build
environment had no outbound network access. The `Special:FilePath` URL
pattern is used because it is the most resilient option — it does not depend
on the MD5 hash prefix used by direct `upload.wikimedia.org` thumbnail URLs,
and it survives file moves on Commons.

If any image fails to load when the page is opened in a browser, the page
falls back gracefully to a typographic placeholder showing the place name.
To replace a failing image, open the day's `<img>` in `italy-trip-family.html`
and swap the filename portion of the URL with one of the alternates suggested
below.

**To verify each URL once you have a network**, run:

```sh
for f in \
  "Sirmione%20Castello%20Scaligero%20Aerial%20View.jpg" \
  "Isola%20di%20San%20Biagio%20Lago%20di%20Garda.jpg" \
  "Bolzano%20Piazza%20delle%20Erbe.jpg" \
  "Alpe%20di%20Siusi%20panorama.jpg" \
  "Lago%20di%20Carezza%20Karersee.jpg" \
  "Castel%20Tirolo%20panorama.jpg" \
  "Terme%20Merano.jpg" \
  "Seilbahn%20Meran%202000.jpg" \
  "Riva%20del%20Garda%20panorama.jpg" \
  "Limone%20sul%20Garda.jpg" ; do
  echo "$f:"
  curl -sILo /dev/null -w "  %{http_code} → %{url_effective}\n" \
    "https://commons.wikimedia.org/wiki/Special:FilePath/$f?width=1600"
done
```

Any URL that returns a 4xx should be replaced by browsing the relevant
Wikimedia Commons category and copying a different filename.

---

## Image list

### Day 1 · Jun 25 — Land MXP → Desenzano
No image. A thin terracotta divider is used in place of a photograph.

### Day 2 · Jun 26 — Sirmione

- **Subject:** Castello Scaligero, Sirmione, on its peninsula in Lake Garda
- **URL:** `https://commons.wikimedia.org/wiki/Special:FilePath/Sirmione Castello Scaligero Aerial View.jpg?width=1600`
- **License:** Wikimedia Commons (typically CC BY-SA 4.0; see file page for the exact author/license)
- **Source category:** [Castello Scaligero (Sirmione)](https://commons.wikimedia.org/wiki/Category:Castello_Scaligero_(Sirmione))
- **Alternates if broken:**
  - `Sirmione_-_Castello_Scaligero_-_panorama.jpg`
  - `Castello_Scaligero_Sirmione.jpg`
  - `Sirmione_aerial_view.jpg`

### Day 3 · Jun 27 — Rabbit Island

- **Subject:** Isola di San Biagio (Isola dei Conigli), Lake Garda
- **URL:** `https://commons.wikimedia.org/wiki/Special:FilePath/Isola di San Biagio Lago di Garda.jpg?width=1600`
- **License:** Wikimedia Commons (typically CC BY-SA 4.0)
- **Source category:** [Isola di San Biagio (Manerba del Garda)](https://commons.wikimedia.org/wiki/Category:Isola_di_San_Biagio_(Manerba_del_Garda))
- **Alternates if broken:**
  - `Isola_dei_Conigli_Manerba.jpg`
  - `San_Biagio_island_Garda.jpg`

### Day 4 · Jun 28 — Bolzano

- **Subject:** Piazza delle Erbe, Bolzano, with the open-air market
- **URL:** `https://commons.wikimedia.org/wiki/Special:FilePath/Bolzano Piazza delle Erbe.jpg?width=1600`
- **License:** Wikimedia Commons (typically CC BY-SA 4.0)
- **Source category:** [Piazza delle Erbe (Bolzano)](https://commons.wikimedia.org/wiki/Category:Piazza_delle_Erbe_(Bolzano))
- **Alternates if broken:**
  - `Piazza_delle_Erbe_Bolzano.jpg`
  - `Bozen_Obstplatz.jpg`

### Day 5 · Jun 29 — Alpe di Siusi

- **Subject:** Alpe di Siusi / Seiser Alm meadow under the Sassolungo
- **URL:** `https://commons.wikimedia.org/wiki/Special:FilePath/Alpe di Siusi panorama.jpg?width=1600`
- **License:** Wikimedia Commons (typically CC BY-SA 4.0)
- **Source category:** [Seiser Alm](https://commons.wikimedia.org/wiki/Category:Seiser_Alm)
- **Alternates if broken:**
  - `Seiser_Alm_Panorama.jpg`
  - `Alpe_di_Siusi_-_Seiser_Alm.jpg`
  - `Sassolungo_from_Seiser_Alm.jpg`

### Day 6 · Jun 30 — Lago di Carezza

- **Subject:** Lago di Carezza / Karersee, with the Latemar reflected
- **URL:** `https://commons.wikimedia.org/wiki/Special:FilePath/Lago di Carezza Karersee.jpg?width=1600`
- **License:** Wikimedia Commons (typically CC BY-SA 4.0)
- **Source category:** [Karersee](https://commons.wikimedia.org/wiki/Category:Karersee)
- **Alternates if broken:**
  - `Karersee_Latemar.jpg`
  - `Lago_di_Carezza.jpg`
  - `Karersee_reflection.jpg`

### Day 7 · Jul 1 — Tirolo

- **Subject:** Castel Tirolo / Falknerpromenade above Merano
- **URL:** `https://commons.wikimedia.org/wiki/Special:FilePath/Castel Tirolo panorama.jpg?width=1600`
- **License:** Wikimedia Commons (typically CC BY-SA 4.0)
- **Source category:** [Schloss Tirol](https://commons.wikimedia.org/wiki/Category:Schloss_Tirol)
- **Alternates if broken:**
  - `Schloss_Tirol_panorama.jpg`
  - `Tirolo_Castel_Tirolo.jpg`
  - `Falknerpromenade_Tirolo.jpg`

### Day 8 · Jul 2 — Terme Merano

- **Subject:** Terme Merano outdoor pools
- **URL:** `https://commons.wikimedia.org/wiki/Special:FilePath/Terme Merano.jpg?width=1600`
- **License:** Wikimedia Commons (typically CC BY-SA 4.0)
- **Source category:** [Therme Meran](https://commons.wikimedia.org/wiki/Category:Therme_Meran)
- **Alternates if broken:**
  - `Therme_Meran_Aussenpool.jpg`
  - `Terme_di_Merano.jpg`
- **Note:** Wikimedia coverage of Terme Merano is sparse. If none of these work, fall back to an Unsplash search photo (see "Unsplash fallback" below).

### Day 9 · Jul 3 — Merano 2000

- **Subject:** Merano 2000 cable car
- **URL:** `https://commons.wikimedia.org/wiki/Special:FilePath/Seilbahn Meran 2000.jpg?width=1600`
- **License:** Wikimedia Commons (typically CC BY-SA 4.0)
- **Source category:** [Meran 2000](https://commons.wikimedia.org/wiki/Category:Meran_2000)
- **Alternates if broken:**
  - `Meran_2000_Seilbahn.jpg`
  - `Funivia_Merano_2000.jpg`
  - `Meran_2000_panorama.jpg`

### Day 10 · Jul 4 — Riva del Garda

- **Subject:** Riva del Garda lakefront with the Monte Brione cliffs
- **URL:** `https://commons.wikimedia.org/wiki/Special:FilePath/Riva del Garda panorama.jpg?width=1600`
- **License:** Wikimedia Commons (typically CC BY-SA 4.0)
- **Source category:** [Riva del Garda](https://commons.wikimedia.org/wiki/Category:Riva_del_Garda)
- **Alternates if broken:**
  - `Riva_del_Garda_lake.jpg`
  - `Riva_del_Garda_Lago.jpg`
  - `Riva_panorama.jpg`

### Day 11 · Jul 5 — Limone sul Garda

- **Subject:** Limone sul Garda, lemon groves on the opposite shore
- **URL:** `https://commons.wikimedia.org/wiki/Special:FilePath/Limone sul Garda.jpg?width=1600`
- **License:** Wikimedia Commons (typically CC BY-SA 4.0)
- **Source category:** [Limone sul Garda](https://commons.wikimedia.org/wiki/Category:Limone_sul_Garda)
- **Alternates if broken:**
  - `Limone_sul_Garda_panorama.jpg`
  - `Limone_sul_Garda_lake.jpg`

### Day 12 · Jul 6 — MXP departure
No image.

---

## Unsplash fallback pattern

If Wikimedia is sparse for a given subject (most likely on Day 8: Terme
Merano), grab a photo from Unsplash. Browse to the photo page on
unsplash.com, copy the photo ID from the URL, and use it like this:

```html
<img src="https://images.unsplash.com/photo-<PHOTO_ID>?w=1600&q=80" />
```

Do **not** use the deprecated `source.unsplash.com/featured/?query=...`
redirect — it no longer resolves reliably.

When using Unsplash, credit the photographer in the caption (their handle
appears on the photo page) and add their name to this file.
