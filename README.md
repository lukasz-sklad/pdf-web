# PDFCraft Web (`pdf.lmk.one`)

Webowa wersja programu **PDFCraft v0.8.0** (zaawansowany czytnik i edytor dokumentów PDF klasy Adobe Acrobat Pro z wbudowanym polskim syntezatorem mowy **Lektor PL**, napisany w Rust + WebAssembly) działająca bezpośrednio w przeglądarce pod adresem:

👉 **[https://pdf.lmk.one](https://pdf.lmk.one)**  
*(oraz przez przekierowania: `https://lmk.one/pdf` i `https://lmk.one/pdfcraft`)*

## Najważniejsze cechy tego wydania
- **Język polski domyślnie (`pl`)** – pełne polskie tłumaczenie interfejsu (ponad 2 410 fraz menu, narzędzi, paneli, formularzy, podpisów i dostępności PDF/UA).
- **Domyślny ciemny motyw (`Dark`)** – komfortowy tryb ciemny aktywny od pierwszego uruchomienia.
- **Wbudowany Lektor PL (Syntezator mowy TTS)**:
  - W wersji webowej wykorzystuje natywne **Web Speech API (`speechSynthesis`, `pl-PL`)** działające w przeglądarce Google Chrome.
  - W wersji desktopowej (Flatpak / AppImage) wykorzystuje lokalny silnik neuronowy **Piper TTS** (`/home/deck/Applications/piper/piper` + model `pl_PL-gosia-medium.onnx`).
  - **Skrót `Shift + Kliknięcie LPM`** na dowolnym tekście lub komentarzu PDF natychmiast odczytuje wybrane zdanie lub akapit na głos.
  - **Przycisk `🔊 Lektor` na górnym pasku** oraz możliwość minimalizacji okienka lektora do paska (`🗕 Minimalizuj do paska`). W przeglądarkach bez obsługi Web Speech TTS (np. Firefox / Brave) okienko lektora startuje domyślnie zminimalizowane do górnego paska, aby nie zasłaniać dokumentu.
- **Obsługa klikalnych linków zewnętrznych** bezpośrednio w treści dokumentów PDF.
- **Domyślny dokument startowy (`podroz_na_marsa.pdf`)** – dwustronicowe kompendium *Podróż na Marsa — Kompendium Misji* z klikalnymi odnośnikami do Wikipedii oraz gotowym tekstem do przetestowania Lektora PL.

## Parametry URL
- **Domyślnie:** [https://pdf.lmk.one/](https://pdf.lmk.one/) – otwiera przykładowy dokument PDF *Podróż na Marsa*.
- **Czysty edytor:** [https://pdf.lmk.one/?new](https://pdf.lmk.one/?new) – otwiera pusty obszar roboczy bez domyślnego pliku PDF.
- **Dowolny plik PDF bezpośrednio z sieci:** `https://pdf.lmk.one/?file=adres_do_pliku.pdf` – pobiera i otwiera dokument PDF bezpośrednio z adresu URL (z automatycznym fallbackiem przez mostek CORS `https://lmk.one/api/cors`).
