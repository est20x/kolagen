# Kolagen HelpVit — landing

Statyczny landing page (czysty HTML/CSS/JS, bez build-u).

## Struktura
- `index.html` — landing z formularzem (imię + telefon)
- `dziekujemy.html` — strona podziękowania (otwiera się po wysłaniu zgłoszenia)
- `assets/kolagen-helpvit.jpg` — zdjęcie produktu
- `vercel.json` — konfiguracja Vercel (clean URLs, cache dla assets)

## Jak działa formularz
Zgłoszenie (`name`, `phone`, `product`, `price`, `page`, `date` + parametry UTM) trafia POST-em
na webhook Make (stała `HOOK` na dole `index.html`), potem przeglądarka przechodzi na `dziekujemy.html`.

## Piksele
W `index.html` i `dziekujemy.html` zamień `META_PIXEL_ID` i `TIKTOK_PIXEL_ID` na swoje ID.
Zdarzenia Lead / SubmitForm odpalają się na `dziekujemy.html`.

## Deploy
1. GitHub: utwórz repo, wrzuć wszystkie pliki z tego folderu (z `index.html` w katalogu głównym).
2. Vercel: Add New → Project → wybierz repo → Framework Preset: **Other** → Deploy
   (Build Command i Output Directory zostaw puste).
3. Domena: Project → Settings → Domains.
