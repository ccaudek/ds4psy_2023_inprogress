# Prefazione 

Questo libro ti insegnerà i principi base della Data Science, con esempi pratici.

## Struttura del corso 

La dispensa si compone di sette parti. La parte I copre ciò che viene spesso chiamato statistica descrittiva. La parte II fornisce alcune nozioni di base della teoria delle probabilità. La parte III presenta le variabili casuali continue e le principali distribuzioni di densità. Qui verrà anche introdotta la funzione di verosimiglianza. La parte IV copre i concetti teorici di base dell'analisi bayesiana dei dati. La Parte V introduce i modelli di regressione. La parte VI affronta il problema del confronto tra modelli. La parte VII introduce le idee di base dell'inferenza frequentista e mette a confronto l'approccio frequentista e quello bayesiano.

Le caratteristiche generali di questo insegnamento sono le seguenti.

-   In primo luogo, utilizzeremo un approccio incentrato sui modelli, ovvero rappresenteremo e parleremo esplicitamente dei modelli statistici come di un insieme formalizzato di ipotesi che stanno alla base di una specifica analisi dei dati.
-   In secondo luogo, utilizzeremo un approccio computazionale, ovvero promuoveremo la comprensione delle nozioni matematiche mediante simulazioni al computer.
-   In terzo luogo, adotteremo un approccio duplice, in quanto introdurremo sia l'approccio frequentista all'inferenza statistica che quello bayesiano. Inizieremo con l'approccio bayesiano, perché è quello più intuitivo. Inoltre, la discussione dell'approccio bayesiano aiuta anche a comprendere meglio i concetti di base del paradigma frequentista. Presenteremo poi l'inferenza frequentista e ne metteremo in evidenza i limiti.

Questa dispensa contiene anche delle appendici con informazioni aggiuntive. Tra le altre cose, le appendici forniscono un ripasso della teoria degli insiemi e della notazione matematica e, soprattutto, introducono Python, il principale linguaggio di programmazione che utilizzeremo.

## L'analisi dei dati psicologici 

Sembra sensato dire qualche parola su una domanda che è importante per gli studenti: perché dobbiamo spendere tanto tempo per studiare le tecniche di analisi dei dati quando in realtà, quello che ci interessa, in psicologia, è tutt'altro? Questa è una bella domanda. Ma c'è una ragione molto semplice che dovrebbe farci capire perché la Data Science sia così importante per la psicologia. Infatti, a ben pensarci, la psicologia è una disciplina intrinsecamente statistica, se per statistica intendiamo quella disciplina che studia la variazione delle caratteristiche degli individui nella popolazione. La psicologia studia *gli individui* ed è proprio la variabilità inter- e intra-individuale ciò che vogliamo descrivere e, in certi casi, predire. In questo senso, la psicologia è molto diversa dall'ingegneria, per esempio. Le proprietà di un determinato ponte sotto certe condizioni, ad esempio, sono molto simili a quelle di un altro ponte, sotto le medesime condizioni. Quindi, per un ingegnere la statistica è poco importante: le proprietà dei materiali sono unicamente dipendenti dalla loro composizione e restano costanti. Ma lo stesso non può dirsi degli individui: ogni individuo è unico e cambia nel tempo. E le variazioni tra gli individui, e di un individuo nel tempo, sono proprio l'oggetto di studio della psicologia: è dunque chiaro che i problemi che la psicologia si pone sono molto diversi da quelli affrontati, ad esempio, dagli ingegneri. Questa è la ragione per cui abbiamo bisogno della Data Science in psicologia: la Data Science ci consente di descrivere la variazione e il cambiamento. E queste sono le caratteristiche di base dei fenomeni psicologici.

Sono sicuro che, leggendo queste righe, a molti studenti sarà venuta in mente la seguente domanda: perché non chiediamo a qualche esperto di fare il "lavoro sporco" (ovvero le analisi statistiche) per noi, mentre noi (gli psicologi) ci occupiamo solo di ciò che ci interessa, ovvero dei problemi psicologici slegati dai dettagli "tecnici" della Data Science? La risposta a questa domanda è che non è possibile progettare uno studio psicologico sensato senza avere almeno una comprensione rudimentale della Data Science. Le tematiche della Data Science non possono essere ignorate né dai ricercatori in psicologia, né da coloro che svolgono la professione di psicologo al di fuori dell'Università. Infatti, anche i professionisti al di fuori dall'università devono essere in graedo di leggere la letteratura psicologica più recente: il continuo aggiornamento delle conoscenze è infatti richiesto dalla deontologia della professione. Ma per potere fare questo è necessario conoscere un bel po' di Data Science! Basta aprire a caso una rivista specialistica di psicologia per rendersi conto di quanto ciò sia vero: gli articoli che riportano i risultati delle ricerche psicologiche sono zeppi di analisi statistiche e di modelli formali. Ed è ovvio che la comprensione della letteratura psicologica rappresenti un requisito minimo nel bagaglio professionale dello psicologo.

Le considerazioni precedenti cercano di chiarire il seguente punto: la Data Science non è qualcosa da studiare a malincuore, in un singolo insegnamento universitario, per poi poterla tranquillamente dimenticare. Nel bene e nel male, gli psicologi usano gli strumenti della Data Science in tantissimi ambiti della loro attività professionale: in particolare quando costruiscono, somministrano e interpretano i test psicometrici. È dunque chiaro che la Data Science è un tassello imprescindibile del bagaglio professionale dello psicologo.

## Come studiare 

Il metodo di studio che consiglio agli studenti è quello di seguire attivamente le lezioni, di assimilare i concetti via via che essi vengono presentati e di verificare in autonomia le procedure presentate a lezione.

La prima fase dello studio, che è sicuramente individuale, è quella in cui lo studente deve acquisire le conoscenze teoriche relative ai problemi che saranno presentati all'esame. La seconda fase di studio, che può essere facilitata da scambi con altri e da incontri di gruppo, porta lo studente ad acquisire la capacità di applicare le conoscenze: è necessario sapere usare un software (nel nostro caso, Python) per risolvere i problemi che verranno presentati all'esame. Le due fasi non sono però separate: in questa materia è molto utile adottare un approccio di *learning by doing*.

Per tutte queste ragioni, incoraggio gli studenti

-   a farmi domande per chiarire ciò che non è stato capito appieno;
-   a svolgere gli esercizi proposti su Moodle seguendo il calendario indicato; tali problemi rappresentano il livello di difficoltà richiesto per superare l'esame e consentono allo studente di capire se le competenze sviluppate fino a quel punto siano sufficienti rispetto alle richieste dell'esame;
-   a partecipare attivamente alle chat sui forum che sono stati predisposti.
