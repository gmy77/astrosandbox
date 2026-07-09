# 🚀 AstroSandbox

**Simulatore di sostanze in stile "falling sand" con fisica spaziale — tutto in un singolo file HTML, zero dipendenze.**

Disegna materiali su un canvas, costruisci muri e contenitori, e guarda come fluidi, gas, fuoco e calore interagiscono tra loro — sulla Terra, sulla Luna, o in **assenza di gravità**.

▶️ **[Provalo online](https://gmy77.github.io/astrosandbox/)** — nessuna installazione, funziona nel browser.

## ✨ Caratteristiche

### 17 materiali interattivi

| Categoria | Materiali |
|-----------|-----------|
| 🧱 Muri e solidi | Cemento, Ferro, Legno, Vetro, Pietra |
| 💧 Liquidi | Acqua, Olio, Lava, Acido |
| 🏖️ Polveri | Sabbia, Polvere da sparo, Ghiaccio |
| 💨 Gas | Gas infiammabile, Vapore, Fumo |
| 🔥 Energia | Fuoco + pennelli Calore/Freddo |

### Fisica simulata

- **Sistema di temperatura per cella** — ogni pixel ha la sua temperatura in °C, visibile nella barra di stato
- **Conduzione termica realistica** — il ferro conduce il calore attraverso i muri, il cemento isola
- **Cambi di stato**: l'acqua bolle a 100°C → vapore → condensa e ripiove; congela sotto 0°C; il ferro fonde a 1538°C
- **Densità**: l'olio galleggia sull'acqua, la sabbia affonda
- **Combustione**: il fuoco accende gas, olio, legno e polvere da sparo (che esplode!)
- **Reazioni**: lava + acqua → pietra + vapore; l'acido corrode tutto tranne il vetro

### Tre modalità di gravità

- 🌍 **Terra** — fisica classica
- 🌙 **Luna** — caduta rallentata
- 🛰️ **Spazio (zero-g)** — i liquidi fluttuano in deriva browniana, i gas si espandono in modo isotropo

## 🎮 Come si usa

1. Apri `index.html` in qualsiasi browser moderno (o usa la [demo online](https://gmy77.github.io/astrosandbox/))
2. Scegli un materiale dal pannello a destra
3. **Click sinistro** per disegnare, **click destro** per cancellare
4. Regola la dimensione del pennello con lo slider

### Esperimenti consigliati

- 🏗️ Costruisci una vasca di cemento, riempila di acqua e olio, poi dai fuoco all'olio
- 🔥 Metti un muro di ferro tra fuoco e ghiaccio e guarda il calore attraversarlo — poi riprova col cemento
- 💥 Una vena di polvere da sparo che attraversa la mappa + una scintilla
- 🛰️ Riempi tutto d'acqua, poi passa a gravità Spazio
- 🌋 Versa lava nell'acqua e costruisci isole di pietra

## 🛠️ Tecnica

- Singolo file HTML (~700 righe), **nessuna dipendenza**
- Automa cellulare su griglia 220×150 con typed arrays (`Uint8Array`/`Float32Array`)
- Rendering via `ImageData` + upscaling pixelato su canvas
- Doppio step di simulazione per frame a 60 FPS

## 📄 Licenza

[MIT](LICENSE) — fai quello che vuoi, divertiti.

---

*Creato con [Claude Code](https://claude.com/claude-code)* 🤖
