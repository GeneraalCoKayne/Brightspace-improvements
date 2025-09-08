# Brightspace Improvements

[![GitHub release](https://img.shields.io/github/v/release/GeneraalCoKayne/Brightspace-improvements?style=for-the-badge)](https://github.com/GeneraalCoKayne/Brightspace-improvements/releases)[![Tampermonkey](https://img.shields.io/badge/Tampermonkey-Compatible-brightgreen?style=for-the-badge&logo=google-chrome)](https://www.tampermonkey.net/)

Een **Tampermonkey-userscript** dat de gebruikservaring van D2L Brightspace verbetert met performance-optimalisaties en handige verbeteringen.

---

## ✨ Features

- **Meer vakken op de homepage**  
  Op de homepage worden meer vakken weergegeven, zodat je snel en gemakkelijk toegang hebt tot de vakken waar je aan werkt.

- **Directe toegang tot vakinhoud**  
  Bij het selecteren van een vak word je direct naar de inhoud van dat vak geleid, zonder tussenkomst van een tussenpagina. Dit bespaart tijd en maakt de navigatie eenvoudiger.

- **Verbeterde PDF-viewer**  
  De pdf-viewer wordt vergroot, zodat je documenten gemakkelijker kunt lezen en bekijken.

- **UI-verbeteringen**  
  Kleine aanpassingen zoals:
  - Compactere navigatiebalk  
  - Verwijdering van overbodige banners  
  - Bredere widgets  
  - Schonere en efficiëntere layout  

---

## 🚀 Verbeterd vanaf het originele project

Dit script is gebaseerd op het originele project:  
👉 [ELO Usability Improvement (MartGroothuis)](https://github.com/MartGroothuis/ELO-usability-improvement)

### 🔧 Major Changes

1. **MutationObserver-based Element Detection**
   - Vervangt al het poll-gedrag door MutationObserver (±60–80% CPU-reductie)  
   - Fallback timeout-systeem voor betrouwbaarheid  
   - Directe resolutie als element al bestaat  

2. **Enhanced Caching System**
   - Repository base class met intelligent caching  
   - Cache-validatie (checkt of element nog in de DOM staat)  
   - Automatische cleanup om memory leaks te voorkomen  

3. **Robust Shadow DOM Handling**
   - Generiek path traversal systeem  
   - Correcte error handling voor kapotte DOM chains  
   - Shadow root readiness detection  

4. **Batched DOM Operations**
   - Eén enkele className-update i.p.v. meerdere losse operaties  
   - Parallelle uitvoering waar mogelijk  
   - Betere foutisolatie  

5. **Architectural Improvements**
   - Strakkere separation of concerns  
   - Singleton pattern met correcte cleanup  
   - Debounced operations  
   - Promise-based async handling  

---

### ⚡ Performance Benefits

- **Memory**: Cache management voorkomt herhaalde DOM-queries  
- **CPU**: MutationObserver elimineert constant polling  
- **Reliability**: Error boundaries zorgen dat één fout niet alles breekt  
- **Maintainability**: Modulair design maakt debuggen makkelijker  

---

### 🔑 Key Features

- Alle operaties draaien parallel waar mogelijk  
- Graceful degradation als elementen niet gevonden worden  
- Correcte cleanup bij page unload  
- Console logging voor debugging  
- Zelfde visuele verbeteringen als het originele project  

✅ Het script behoudt alle originele functionaliteit, maar is nu veel efficiënter en robuuster.  
De polling-intervallen die elke 10ms draaiden, zijn volledig verwijderd en vervangen door event-driven element-detectie.  

---

## 📦 Installatie

1. Installeer eerst **Tampermonkey** in je browser:  
   👉 [Tampermonkey](https://www.tampermonkey.net/)

2. Installeer vervolgens dit script via de GitHub release:  
   👉 [Brightspace Improvements Script](https://github.com/GeneraalCoKayne/Brightspace-improvements/releases/latest/download/Brightspace-improvements.user.js)

---

## ⚡ Gebruik

Na installatie worden de verbeteringen automatisch toegepast wanneer je Brightspace bezoekt op:

- `https://leren.windesheim.nl`  
- `https://s.brightspace.com`

Er is geen verdere configuratie nodig.  

---
