# Progetto Computer Graphics 2024 - Flappy Plane

![Static Badge](https://img.shields.io/badge/status-completed-brightgreen)
![Static Badge](https://img.shields.io/badge/WebGL-3D-blue)
![Static Badge](https://img.shields.io/badge/license-MIT-green)

Benvenuti nel repository del progetto per il corso di **Computer Graphics A.A. 2023/2024**. L'obiettivo era sviluppare un'applicazione 3D interattiva utilizzando WebGL, JavaScript e GLSL.

Il risultato è un **videogioco "endless runner"** in 3D dal titolo "The Aviator", in cui il giocatore pilota un aereo attraverso un mondo low-poly, raccogliendo monete ed evitando ostacoli.

👉 **[Gioca ora!](https://benedetta2199.github.io/Flappy-Plane-CG/)** 👈

## 📖 Panoramica del Gioco

Il progetto si basa sull'idea del gioco [The Aviator](https://tympanus.net/Tutorials/TheAviator/index.html) il cui obiettivo principale è pilotare un aereo evitando gli ostacoli e raccogliendo monete lungo il percorso.

- **Genere:** Endless runner 3D.
- **Obiettivo:** Sopravvivere il più a lungo possibile, collezionare monete (ognuna vale 1 punto) e raggiungere il punteggio più alto. Se si tocca un ostacolo, il gioco termina. Raccogliere 999 punti è una condizione di vittoria che conclude la partita.
- **Stile Grafico:** Low-poly, con texture e normal map opzionali per un effetto più realistico.

## 🎮 Comandi di Gioco

Il gioco è progettato per essere accessibile su più piattaforme.

| Azione | Mouse | Tastiera | Mobile (Touch) |
| :--- | :--- | :--- | :--- |
| **Salire** | Muovi il mouse verso l'alto | Tasto Freccia SU (↑) | Tieni premuto il bottone ▲ |
| **Scendere**| Muovi il mouse verso il basso| Tasto Freccia GIÙ (↓) | Tieni premuto il bottone ▼ |
| **Avvia/Pausa** | - | Barra spaziatrice | - |

## ✨ Funzionalità Implementate

Il progetto dimostra l'uso di diverse tecniche di computer graphics:

- **Gestione della Scena:** Due scene distinte (gioco e schermata finale) con telecamere, luci e matrici di proiezione differenti.
- **Modelli 3D:** Importazione di oggetti in formato `.obj` con relativi materiali `.mtl`, creati con Blender e Nomad Sculpt.
- **Texture Mapping:** Applicazione di texture (da ambientCG) attivabili/disattivabili dinamicamente tramite una flag globale `enableTextureMap`.
- **Normal Mapping:** Implementazione del normal mapping per aggiungere dettagli superficiali senza aumentare la complessità geometrica, controllato dalla flag `enableNormalMap`.
- **Trasparenze:** Gestione dell'alpha blending per elementi come nuvole e acqua, attivabile con `alphaEnable`.
- **Ombre Dinamiche:** Sistema di ombre proiettate, con una luce ortografica per la scena di gioco e prospettica per la schermata finale.
- **Illuminazione:** Modello di illuminazione di **Blinn-Phong** per effetti di luce ambientale, diffusa e speculare su superfici lucide.
- **Illuminazione Dinamica:** Nella schermata finale, è possibile cambiare l'atmosfera (Alba/Giorno/Notte), regolando il colore di sfondo e l'intensità della luce.
- **Personalizzazione:** L'utente può modificare la velocità di gioco, la frequenza di spawn degli oggetti, la direzione della luce e abilitare/disabilitare le feature grafiche.
- **Dinamicità:** Generazione procedurale di nuvole con parametri casuali e variazione del colore degli ostacoli per aumentare la varietà visiva.
- **Audio:** Musica di sottofondo ed effetti sonori per la raccolta di monete e il game over.

## 🗂️ Struttura del Progetto

La struttura delle cartelle è organizzata per separare chiaramente codice, risorse e documentazione.
/
├── index.html # Pagina principale del gioco
├── endGame.html # Pagina della schermata finale
├── style.css # Foglio di stile globale
├── 📁 doc/ # Documentazione del progetto
│ ├── documentazione.html # Documentazione dettagliata
│ └── 📁 img/ # Immagini per la documentazione
├── 📁 js/ # Codice JavaScript principale
│ ├── cameraAndLight.js # Configurazione di telecamere e luci
│ ├── cloud.js # Generazione e rendering delle nuvole
│ ├── collectibles.js # Gestione di monete e ostacoli
│ ├── createObj.js # Caricamento di modelli OBJ/MTL
│ ├── drawScene.js # Logica di disegno per le scene
│ ├── endGame.js # Gestione della logica di fine gioco
│ ├── mousePosition.js # Input da mouse, tastiera e touch
│ ├── objLoad.js # Parsing di file OBJ e MTL
│ ├── renderObj.js # Render e trasformazioni degli oggetti
│ ├── renderScene.js # Setup del rendering con matrici e ombre
│ ├── script.js # Inizializzazione della scena di gioco
│ ├── scriptEnd.js # Inizializzazione della scena finale
│ ├── utils.js # Funzioni di utilità varie
│ └── vsfs.js # Vertex e Fragment Shaders
└── 📁 src/ # Risorse del gioco (assets)
├── (modelli .obj e .mtl)
├── 📁 sound/ # File audio (musica, effetti)
└── 📁 texture/ # Texture e normal map


## 📚 Documentazione Completa

Per una descrizione approfondita di tutte le scelte progettuali, l'implementazione delle funzionalità e la struttura del codice, consulta la **[documentazione dedicata](./doc/documentazione.html)**.

**Cosa troverai nella documentazione:**

- Descrizione dettagliata del gioco e dell'interfaccia.
- Motivazioni dietro le scelte di design e implementazione.
- Spiegazione approfondita delle funzionalità grafiche con esempi di codice.
- Esempi di come sono stati creati i modelli 3D.
- Spunti per sviluppi futuri.

## 🔮 Sviluppi Futuri

Il progetto ha ampi margini di miglioramento. Alcune idee:

- Implementare una classifica dei punteggi.
- Introdurre livelli di difficoltà crescente.
- Aggiungere nuovi tipi di ostacoli e power-up.
- Migliorare la resa delle ombre (soft shadows).
- Simulare un ciclo giorno-notte dinamico.
- Aggiungere scenari alternativi (spazio, fondale marino).

## 📜 Riconoscimenti e Riferimenti

- **Idea di Gioco:** Ispirato a [The Aviator](https://tympanus.net/Tutorials/TheAviator/index.html).
- **Documentazione WebGL:** [WebGL Fundamentals](https://webglfundamentals.org).
- **Illuminazione:** [LearnOpenGL](https://learnopengl.com/Advanced-Lighting/Advanced-Lighting).
- **Software di Modellazione:** [Blender](https://www.blender.org/), [Nomad Sculpt](https://nomadsculpt.com/).
- **Risorse Grafiche:** [ambientCG](https://ambientcg.com/) per le texture, [Poly Pizza](https://poly.pizza/) per il modello della moneta.

## 👤 Autore

**Benedetta Bottari** - 0001144057

---

**Nota:** Le immagini presenti in questa repository sono soggette a copyright. I modelli 3D e le texture sono utilizzati secondo le rispettive licenze (vedi [Poly Pizza](https://poly.pizza/) e [ambientCG](https://ambientcg.com/)).
