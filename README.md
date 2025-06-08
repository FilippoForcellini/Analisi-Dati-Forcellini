Oggi presenterò un progetto di analisi dati che ho realizzato utilizzando diverse librerie Python, tra cui NumPy, Pandas, Statsmodels, Scikit-learn e TensorFlow. L'obiettivo di questo progetto era di esplorare un dataset di motociclette Husqvarna per comprenderne le caratteristiche, identificare eventuali relazioni tra queste caratteristiche e, infine, tentare di prevedere il prezzo di una motocicletta basandosi su di esse.

FONTE DEI DATI E OBIETTIVO:
Come punto di partenza, ho utilizzato un dataset sintetico che ho creato per questo esercizio. Questo dataset include informazioni chiave come il modello della motocicletta, l'anno di produzione, la cilindrata, la potenza, il tipo e il prezzo. In un contesto reale, idealmente, si utilizzerebbe un dataset più ampio e dettagliato, magari proveniente da listini prezzi, siti di vendita o dati di mercato. L'obiettivo principale era duplice: in primo luogo, ottenere una panoramica descrittiva delle motociclette Husqvarna presenti nel dataset e, in secondo luogo, valutare la possibilità di costruire un modello predittivo per il prezzo.

ESPLORAZIONE E PULIZIA DEI DATI:
La prima fase del progetto è stata dedicata all'esplorazione e alla pulizia dei dati utilizzando la librerie Pandas. Ho esaminato le prime righe del dataset per familiarizzare con la sua struttura e ho calcolato statistiche descrittive per ottenere un'idea della distribuzione delle variabili numeriche come l'anno, la cilindrata, la potenza e il prezzo. Ho anche verificato la presenza di valori mancanti e duplicati, anche se nel dataset sintetico questi erano assenti.
Successivamente, ho utilizzato librerie di visualizzazione come Matplotlib e Seaborn per rappresentare graficamente i dati. Ho creato istogrammi per visualizzare la distribuzione delle variabili numeriche e grafici a barre per mostrare la frequenza dei diversi modelli e tipi di motociclette. Un passaggio cruciale è l'analisi della correlazione tra le variabili numeriche, visualizzata tramite una heatmap. Questo ci ha permesso di osservare, ad esempio, una potenziale relazione positiva tra la cilindrata e il prezzo, o tra la potenza e il prezzo. È importante notare che, per calcolare correttamente la correlazione, ho selezionato solo le colonne numeriche del dataset, escludendo le colonne di testo come 'Modello' e 'Tipo'.

ANALISI STATISTICA E MACHINE LEARNING:
Nella fase successiva, ho applicato tecniche di analisi statistica e machine learning. Ho utilizzato la libreria Statsmodels per costruire un modello di regressione lineare, che ci ha fornito un'analisi più formale della relazione tra le variabili indipendenti (anno, cilindrata, potenza) e la variabile dipendente (prezzo).
L'output di Statsmodels ci ha dato informazioni importanti sulla significatività statistica delle variabili e sulla bontà di adattamento del modello.

RISULTATI E CONCLUSIONI:
Confrontando le prestazioni dei diversi modelli in base all'errore quadratico medio sul set di test, ho osservato che il modello Random Forest ha fornito i risultati migliori in termini di accuratezza predittiva per questo dataset specifico. Questo suggerisce che le relazioni tra le caratteristiche delle motociclette e il loro prezzo potrebbero essere non lineari e complesse, e un modello più flessibile come la Random Forest è in grado di catturarle meglio rispetto a modelli lineari o polinomiali di basso grado. Il modello di rete neurale, date le dimensioni limitate del dataset, non ha superato le prestazioni del Random Forest.

PROSSIMI PASSI:
Questo progetto rappresenta un'analisi iniziale. In futuro, sarebbe interessante:
	- Ampliare il dataset: utilizzare un dataset più grande e rappresentativo del mercato delle motociclette Husqvarna.
	- Includere ulteriori caratteristiche: aggiungere variabili come il chilometraggio, le condizioni della moto, la presenza di accessori, la storia delle manutenzioni e fattori di mercato regionali.
	- Ottimizzare i modelli: eseguire una ricerca più approfondita degli iperparametri dei modelli di machine learning per migliorarne le prestazioni.
	- Esplorare modelli più avanzati: considerare l'utilizzo di modelli di deep learning più complessi con un dataset più ampio.
	- Implementare la feature engineering: creare nuove variabili a partire da quelle esistenti che potrebbero avere un potere predittivo maggiore.
