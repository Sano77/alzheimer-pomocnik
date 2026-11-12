# PROMPT: Fáza 1 – Alzheimer Pomocník (PWA Web Aplikácia)

## 1. Cieľ a Kontext Projektu
Vytvoriť intuitívnu, maximálne zjednodušenú a vysoko prístupnú Progressive Web Application (PWA) pre pacientov s počiatočným až stredným štádiom Alzheimerovej choroby / demencie a ich opatrovateľov (rodinných príslušníkov).

Aplikácia musí byť optimalizovaná pre dotykové zariadenia (tablety, smartfóny) a fungovať plne **offline**.

---

## 2. Technologický Stack
- **Framework:** React 19 + TypeScript (Vite)
- **Styling:** Tailwind CSS (veľké dotykové plochy, vysoký kontrast, jasná typografia)
- **Offline / PWA:** `vite-plugin-pwa` (Service Worker, Web App Manifest)
- **Ikony:** Lucide React (jednoznačné a rozpoznateľné symboly)
- **Perzistencia dát:** LocalStorage / IndexedDB (dáta zostávajú bezpečne v zariadení používateľa)

---

## 3. UI/UX Princípy pre seniorov s kognitívnym znevýhodnením
- **Žiadne preplnené rozhranie:** Na obrazovke sú vždy len najdôležitejšie informácie.
- **Veľké písmo a dotykové terče:** Tlačidlá minimálne 56px až 72px na výšku, text minimálne 18px–24px.
- **Vysoký kontrast:** Svetlé pozadie, tmavý čitateľný text, jasné farby pre stav (zelená = hotovo, modrá = informácia, červená = SOS).
- **Zrozumiteľný jazyk:** Žiadny technický žargón, len priame vety v prvej osobe ("Vypil som vodu", "Zavolať dcére").

---

## 4. Kľúčové Moduly pre Fázu 1 (Web MVP)

### Modul A: Orientácia v čase (Kognitívna kotva)
- Veľký prehľadný panel:
  - Deň v týždni (napr. **ŠTVRTOK**)
  - Dátum a rok (napr. **12. november 2026**)
  - Denná doba v ľudskej reči: **RÁNO / DOOBEDA / OBED / POPOLUDNIE / VEČER / NOC**
  - Aktuálny čas (veľké digitálne hodiny)

### Modul B: Denný režim & Lieky (Today Checklist)
- Zoznam úloh rozdelených podľa dennej doby (Ráno, Obed, Večer).
- Každá úloha má:
  - Čas, ikonu, jasný názov (napr. *Ranné lieky po raňajkách*, *Pohár vody*, *Obed*).
  - Veľké tlačidlo na odškrtnutie s pozitívnou zvukovou/vizuálnou spätnou väzbou (konfety).
  - Možnosť pre opatrovateľa jednoducho pridať/upraviť úlohu.

### Modul C: Moja rodina a blízki (Album pamäti)
- Karty blízkych s veľkou fotografiou:
  - Meno (napr. *Zuzana*)
  - Vzťah (napr. *Vaša dcéra*)
  - Krátka osobná pripomienka (napr. *Má dvoch synov, býva v Bratislave*)
  - Tlačidlo **"Zavolať"** (`tel:...`) na priame vytočenie hovoru.

### Modul D: Bezpečnostný profil & SOS karta (Kto som)
- Karta identity pacienta:
  - Moje meno a priezvisko,
  - Moja domáca adresa (s tlačidlom zobrazenia na mape / návratu domov),
  - Núdzové kontakty na rodinu a lekára (SOS tlačidlo volania).
- Režim Opatrovateľa (PIN chránené nastavenia pre rodinu).

---

## 5. Akceptačné kritériá Fázy 1
1. Aplikácia sa načíta bleskovo a funguje bez internetového pripojenia (Offline PWA).
2. Možnosť pridať aplikáciu na domovskú obrazovku telefónu/tabletu s vlastnou ikonou.
3. Testované na dotykovom rozhraní s nulovou chybovosťou preklepov.
4. Možnosť predvyplniť ukážkové dáta (demo profil) jedným klikom pre okamžité testovanie.
