# Image Credits

All photographs in `italy-trip-family.html` are loaded dynamically from the
**Wikipedia REST API** — specifically `en.wikipedia.org/api/rest_v1/page/summary/<article>`
which returns the lead image of each article. Wikipedia lead images are typically
licensed CC BY-SA 4.0 (or compatible) and live on Wikimedia Commons; full
attribution is on each Commons file page.

## How it works

Each `<img>` tag carries a `data-wiki` attribute with one or more comma-separated
Wikipedia article slugs. The script tries each slug in turn:

1. Fetches the article summary
2. If the lead image hasn't already been used elsewhere on the page, uses it
3. Probes the image URL to confirm it loads
4. Falls back to the next slug on failure
5. Falls back to a typographic placeholder if every slug fails

This is more resilient than hard-coding filenames — articles get re-illustrated
on Wikipedia, files move on Commons, but the lead image always resolves.

## Articles used per day

| Day | Place | Article slugs (in priority order) |
|---|---|---|
| 2 | Sirmione | `Scaliger_Castle_(Sirmione)` · `Sirmione` · `Lake_Garda` |
| 2 | Lake Garda | `Lake_Garda` · `Sirmione` |
| 2 | Parco Natura Viva | `Parco_Natura_Viva` · `Bussolengo` |
| 2 | Desenzano | `Desenzano_del_Garda` · `Lake_Garda` |
| 3 | Isola di San Biagio | `Isola_di_San_Biagio` · `Manerba_del_Garda` · `Lake_Garda` |
| 3 | Manerba | `Manerba_del_Garda` · `Lake_Garda` |
| 3 | Castelrotto | `Castelrotto` · `Kastelruth` · `Schlern` |
| 3 | Sciliar | `Schlern` · `Sciliar-Catinaccio_Nature_Park` · `Sassolungo` |
| 4 | Alpe di Siusi | `Sassolungo` · `Seiser_Alm` · `Alpe_di_Siusi` · `Schlern` |
| 4 | Seiser Alm | `Seiser_Alm` · `Alpe_di_Siusi` |
| 4 | Lago di Fiè | `Völser_Weiher` · `Fiè_allo_Sciliar` · `Schlern` |
| 4 | Schlern massif | `Schlern` · `Sciliar-Catinaccio_Nature_Park` |
| 5 | Lago di Carezza | `Karersee` · `Latemar` · `Lago_di_Carezza` |
| 5 | Latemar | `Latemar` · `Karersee` |
| 5 | Trauttmansdorff | `Trauttmansdorff_Castle` · `Merano` |
| 5 | Merano | `Merano` · `Texel_Group` |
| 6 | Etsch valley | `Adige` · `Burgraviato` · `Lana,_South_Tyrol` |
| 6 | Lana | `Lana,_South_Tyrol` · `Burgraviato` |
| 6 | Texel Group | `Texel_Group` · `Naturpark_Texelgruppe` |
| 6 | Orchards | `Apple_(South_Tyrol)` · `Vinschgau` · `Adige` |
| 7 | Texel Group | `Texel_Group` · `Meran_2000` · `Mutspitze` |
| 7 | Merano 2000 | `Meran_2000` · `Mutspitze` |
| 7 | Tappeiner | `Tappeinerweg` · `Merano` |
| 7 | Merano old town | `Merano` · `Burgraviato` |
| 8 | Castel Tirolo | `Tirol_Castle` · `Schloss_Tirol` · `Tirolo,_South_Tyrol` |
| 8 | Therme Meran | `Therme_Meran` · `Merano` |
| 8 | Tirolo village | `Tirolo,_South_Tyrol` · `Schloss_Tirol` |
| 8 | Merano valley | `Burgraviato` · `Texel_Group` · `Merano` |
| 9 | Riva del Garda | `Riva_del_Garda` · `Lake_Garda` · `Monte_Brione` |
| 9 | Cascate del Varone | `Cascate_del_Varone` · `Tenno` |
| 9 | Bastione di Riva | `Bastione_di_Riva` · `Riva_del_Garda` |
| 9 | Lake Garda north | `Lake_Garda` · `Monte_Brione` · `Trentino` |
| 10 | Lago di Tenno | `Lago_di_Tenno` · `Tenno` |
| 10 | Torbole | `Torbole` · `Lake_Garda` |
| 10 | Canale di Tenno | `Tenno` · `Canale_di_Tenno` · `Lago_di_Tenno` |
| 10 | Lake Garda cliffs | `Lake_Garda` · `Monte_Brione` · `Riva_del_Garda` |
| 11 | Riva morning | `Riva_del_Garda` · `Lake_Garda` |
| 11 | Limone sul Garda | `Limone_sul_Garda` · `Lake_Garda` |
| 11 | Lake Garda | `Lake_Garda` · `Sirmione` |

## Licensing

Images served via the Wikipedia REST API resolve to files on
`upload.wikimedia.org`, which are hosted on Wikimedia Commons. The
overwhelming majority of Wikipedia article lead images are licensed
**CC BY-SA 4.0**, **CC BY-SA 3.0**, **CC BY 4.0**, or **public domain**.
Each individual file's exact license is on its Commons file page —
follow the image URL upstream to find it.

Use of these images in this private trip page (a non-commercial,
single-recipient page shared with my partner) falls within the spirit
of those licenses. If this page were ever made public-facing or
commercial, each photo would need explicit attribution per its license
terms.

## If an image fails to load

The page falls back gracefully — a typographic placeholder shows the
place name in serif type over a rust → moss → water gradient. The
schedule itself remains fully readable.

To swap a failed image, find the corresponding `<img data-wiki="...">`
tag in `italy-trip-family.html` and add a different Wikipedia slug to
the comma-separated list.
