# Blood Supply Chain Optimization – Campania

Questo repository contiene il progetto di riorganizzazione della rete dei centri trasfusionali regionali in Campania, basato sul modello MILP pubblicato in letteratura:

**Antonio Diglio, Andrea Mancuso, Adriano Masone, Carmela Piccolo, Claudio Sterle, "A MILP Formulation for the Reorganization of the Blood Supply Chain in Italian Regions", 2021.**

Abbiamo esteso il modello originale applicando **euristiche Greedy** e Drop Heuristic per ottenere soluzioni rapide e scalabili, confrontandole con le soluzioni ottimali calcolate tramite **Gurobi**.

---

## Contenuto della repository

- `notebook.ipynb` – Notebook Python con implementazione del modello MILP, euristiche Greedy e Drop Heuristic.  
- `paper.pdf` – Documento descrittivo del progetto.  

---

## Tecnologie e strumenti

- **Python** – implementazione del modello e delle euristiche.  
- **Gurobi** – risoluzione del modello MILP esatto.  
- **OpenStreetMap / OSMnx** – generazione dei dati geospaziali e centroidi dei comuni.  
- **Matplotlib, Pandas, NumPy** – gestione dati e visualizzazione.  
- **Algoritmi euristici** – Greedy e Drop Heuristic per ottimizzazione approssimata.  

---

## Descrizione del progetto

L’obiettivo del progetto è ottimizzare la posizione e il numero di **Blood Center (BC)** e **Blood Station (BS)** nella regione, minimizzando:

- I costi logistici di trasferimento del sangue.  
- Le penalità per mancata autosufficienza e superamento dei limiti di capacità.  

La funzione di valutazione implementata calcola la qualità di una configurazione della rete, gestendo:

1. **Assegnazione dei comuni ai centri** – tramite strutture attive o unità mobili.  
2. **Gestione delle eccedenze** – riallocazione dei donatori quando le capacità dei centri sono superate.  
3. **Trasferimento da BS a BC** – instradamento del sangue raccolto.  
4. **Calcolo della funzione obiettivo Z** – somma di costi logistici e penalità.

---

## Come usare

1. Aprire `notebook.ipynb` in **Google Colab** o **Jupyter Notebook**.  
2. Installare le librerie richieste (`gurobipy`, `osmnx`, `pandas`, `numpy`, `matplotlib`).  
3. Eseguire le celle per replicare la generazione dei dati, l’esecuzione delle euristiche e l’analisi dei risultati.  

---

## Confronto risultati

Il repository include una sezione di confronto tra le soluzioni esatte (Gurobi) e le euristiche implementate, evidenziando:

- Performance e gap della Greedy classica.  
- Miglioramenti ottenuti con la Drop Heuristic.  
- Analisi dei costi logistici, autosufficienza e produttività dei BC.  

---

## Licenza

Questo progetto è fornito a scopo **didattico e professionale**. Per l’uso commerciale, contattare l’autore.
