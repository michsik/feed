# Kadr

Prywatny feed zamiast scrollowania: teledyski, filmy modowe i krótkie artykuły (PL/EN). Codziennie rano Claude dopisuje nową porcję do `feed.json`.

- `index.html` – aplikacja (pełnoekranowy pionowy feed, filtry, zapisane, karta „Na dziś to wszystko”)
- `feed.json` – treści; najnowsza data = dzisiejsza porcja, starsze trafiają do „Starsze”
- Na telefonie: otwórz stronę → Udostępnij → „Dodaj do ekranu początkowego”

## Format pozycji w feed.json

| pole | znaczenie |
|---|---|
| `id` | unikalny, `RRRR-MM-DD-krótki-slug` |
| `date` | data porcji `RRRR-MM-DD` |
| `type` | `photo` · `video` · `article` · `news` |
| `title`, `by`, `text` | tytuł, autor, opis własnymi słowami (max ~2 zdania) |
| `kind` | (video) np. „Teledysk”, „Film krótkometrażowy · dokument” |
| `embed` | (video) `{ "p": "yt" \| "vimeo", "id": "..." }` |
| `img` | zdjęcie lub plakat filmu (URL) |
| `lang` | `pl` / `en` dla tekstów |
| `src`, `srcName` | link do źródła i jego nazwa |
