---
jupytext:
  cell_metadata_filter: -all
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: '0.8'
    jupytext_version: 1.5.0
kernelspec:
  display_name: 'Python 3.8.15 64-bit (''codeforecon'': conda)'
  language: python
  name: python3
---
(join-probability)=
# Probabilità congiunta 

La probabilità congiunta è la probabilità che due o più eventi si verifichino contemporaneamente. In questo Capitolo verrà esaminato il caso discreto.

(sec-fun-join-prob)=
## Funzione di probabilità congiunta 

Dopo aver trattato della distribuzione di probabilità di una variabile casuale, la quale associa ad ogni evento elementare dello spazio campione uno ed un solo numero reale, è naturale estendere questo concetto al caso di due o più variabili casuali. Iniziamo a descrivere il caso discreto con un esempio. Consideriamo l'esperimento casuale corrispondente al lancio di tre monete equilibrate. Lo spazio campione è

$$
\Omega = \{TTT, TTC, TCT, CTT, CCT, CTC, TCC, CCC\}.
$$

Dato che i tre lanci sono tra loro indipendenti, non c'è ragione di aspettarsi che uno degli otto risultati possibili dell'esperimento sia più probabile degli altri, dunque possiamo associare a ciascuno degli otto eventi elementari dello spazio campione la stessa probabilità, ovvero 1/8.

Definiamo sullo spazio campione $\Omega$ le seguenti variabili casuali:

-   $X \in \{0, 1, 2, 3\}$ = "numero di realizzazioni con il risultato testa nei tre lanci",
-   $Y \in \{0, 1\}$ = "numero di realizzazioni con il risultato testa nel primo lancio".

Indicando con T = 'testa' e C = 'croce', si ottiene la situazione riportata nella {numref}`tbl-tre-monete-distr-cong-1`.

```{table} Spazio campione dell'esperimento consistente nel lancio di tre monete equilibrate su cui sono state definite le variabili aleatorie $X$ = 'numero di realizzazioni con il risultato testa nei tre lanci' e $Y$ = 'numero di realizzazioni con il risultato testa nel primo lancio'.
:name: tbl-tre-monete-distr-cong-1

|     $\omega$     | $X$ | $Y$ | $P(\omega)$ |
|:----------------:|:---:|:---:|:-----------:|
| $\omega_1$ = TTT |  3  |  1  |     1/8     |
| $\omega_2$ = TTC |  2  |  1  |     1/8     |
| $\omega_3$ = TCT |  2  |  1  |     1/8     |
| $\omega_4$ = CTT |  2  |  0  |     1/8     |
| $\omega_5$ = CCT |  1  |  0  |     1/8     |
| $\omega_6$ = CTC |  1  |  0  |     1/8     |
| $\omega_7$ = TCC |  1  |  1  |     1/8     |
| $\omega_8$ = CCC |  0  |  0  |     1/8     |
```

Ci poniamo il problema di associare un valore di probabilità ad ogni coppia $(x, y)$ definita su $\Omega$. La coppia $(X = 0, Y = 0)$ si realizza in corrispondenza di un solo evento elementare, ovvero CCC; avrà dunque una probabilità pari a

$$
P(X=0, Y=0) = P(CCC) = 1/8.
$$

Nel caso della coppia $(X = 1, Y = 0)$ ci sono due eventi elementari che danno luogo al risultato considerato, ovvero, CCT e CTC. La probabilità dell'evento composto $P(X=1, Y=0)$ è dunque uguale alla somma delle probabilità dei due eventi elementari che lo costituiscono, cioé

$$
P(X=1, Y=0) = P(\mbox{CCT}) + P(\mbox{CTC}) = 1/8 + 1/8 = 1/4.
$$

Di seguito sono riportati i calcoli per tutte le possibili coppie $X, Y$:

$$
\begin{align}
P(X = 0, Y = 0) &= P(\omega_8 = CCC) = 1/8; \notag\\
P(X = 1, Y = 0) &= P(\omega_5 = CCT) + P(\omega_6 = CTC) = 2/8; \notag\\
P(X = 1, Y = 1) &= P(\omega_7 = TCC) = 1/8; \notag\\
P(X = 2, Y = 0) &= P(\omega_4 = CTT) = 1/8; \notag\\
P(X = 2, Y = 1) &= P(\omega_3 = TCT) + P(\omega_2 = TTC) = 2/8; \notag\\
P(X = 3, Y = 1) &= P(\omega_1 = TTT) = 1/8; \notag
\end{align}
$$

Le probabilità così trovate sono riportate nella {numref}`tbl-distr-cong-biv-1` che descrive la *distribuzione di probabilità congiunta* delle variabili casuali $X$ ("numero di realizzazioni con il risultato testa nei tre lanci") e $Y$ ("numero di realizzazioni con il risultato testa nel primo lancio") per l'esperimento casuale che consiste nel lancio di tre monete equilibrate.

```{table} Distribuzione di probabilità congiunta per i risultati dell'esperimento consistente nel lancio di tre monete equilibrate. 
:name: tbl-distr-cong-biv-1

| $x /\ y$ |  0  |  1  |
|:--------------------:|:---:|:---:|
|          0           | 1/8 |  0  |
|          1           | 2/8 | 1/8 |
|          2           | 1/8 | 2/8 |
|          3           |  0  | 1/8 |
```

In generale, possiamo dire che, dato uno spazio campione discreto $\Omega$, è possibile associare ad ogni evento elementare $\omega_i$ dello spazio campione una coppia di numeri reali $(x, y)$, essendo $x = X(\omega)$ e $y = Y(\omega)$, il che ci conduce alla seguente definizione.

```{admonition} Definizione
Siano $X$ e $Y$ due variabili casuali. La funzione che associa ad ogni coppia $(x, y)$ un valore di probabilità prende il nome di funzione di probabilità congiunta:

$$
P(x, y) = P(X = x, Y = y).
$$
```

Il termine "congiunta" deriva dal fatto che questa probabilità è legata al verificarsi di una coppia di valori, il primo associato alla variabile casuale $X$ ed il secondo alla variabile casuale $Y$. Nel caso di due sole variabili casuali si parla di *distribuzione bivariata*, mentre nel caso di più variabili casuali si parla di *distribuzione multivariata*.

### Proprietà

Una distribuzione di massa di probabilità congiunta bivariata deve soddisfare due proprietà:

1.  $0 \leq P(x_i, y_j) \leq 1$;
2.  la probabilità totale deve essere uguale a 1: $\sum_{i} \sum_{j} P(x_i, y_j) = 1.$

### Eventi

Si noti che dalla probabilità congiunta possiamo calcolare la probabilità di qualsiasi evento definito in base alle variabili aleatorie $X$ e $Y$. Per capire come questo possa essere fatto, consideriamo nuovamente l'esperimento casuale discusso in precedenza.

Per fare un esempio, consideriamo la distribuzione di massa di probabilità congiunta riportata nella {numref}`tbl-distr-cong-biv-1` si trovi la probabilità dell'evento $X+Y \leq 1$.

Per trovare la probabilità richiesta dobbiamo sommare le probabilità associate a tutte le coppie $(x,y)$ che soddisfano la condizione $X+Y \leq 1$, ovvero

$$
P_{XY}(X+Y \leq 1) = P_{XY}(0, 0)+ P_{XY}(0, 1) + P_{XY}(1, 0) = 3/8.
$$

### Funzioni di probabilità marginali {#sec-marg-distr-discr}

La distribuzione marginale di un sottoinsieme di variabili casuali è la distribuzione di probabilità delle variabili contenute nel sottoinsieme. Come spiegato da [Wikipedia](https://it.wikipedia.org/wiki/Distribuzione_marginale): \> il termine variabile marginale è usato per riferirsi a quelle variabili nel sottoinsieme delle variabili che vengono trattenute ovvero utilizzate. Questo termine, marginale, è attribuito ai valori ottenuti ad esempio sommando in una tabella di valori lungo le righe oppure lungo le colonne, trascrivendo il risultato appunto a margine rispettivamente della riga o colonna sommata. La distribuzione delle variabili marginali (la distribuzione marginale) è ottenuta mediante marginalizzazione sopra le variabili da "scartare", e le variabili scartate sono dette fuori marginalizzate.

Nel caso di due variabili casuali discrete $X$ e $Y$ di cui conosciamo la distribuzione congiunta, la distribuzione marginale di $X$, $P(X=x)$, è dunque

$$
P(X = x) = \sum_y P(X, Y = y) = \sum_y P(X \mid Y = y) P(Y = y),
$$

dove $P(X = x,Y = y)$ è la distribuzione congiunta di $X, Y$, mentre $P(X = x \mid Y = y)$ è la distribuzione condizionata di $X$ dato $Y$.

Le probabilità bivariate marginali e congiunte di variabili casuali discrete sono spesso rappresentate mediante tabelle di contingenza. Si noti che $P(X = x)$ e $P(Y = y)$ sono normalizzate:

$$
\sum_x P(X=x) = 1.0, \quad \sum_y P(Y=y) = 1.0.
$$

Nel caso continuo si sostituisce l'integrazione alla somma.

Per l'esperimento casuale descritto nella {ref}`sec-fun-join-prob`, si calcolino le probabilità marginali di $X$ e $Y$.

Come indicato nella {numref}`tbl-ditr-cong-biv`, $P_X$ si ottiene sommando su ciascuna riga fissata la colonna $j$, $P_X(X = j) = \sum_y p_{xy}(x = j, y)$ e $P_Y$ si trova sommando su ciascuna colonna fissata la riga $i,$ $P_Y (Y = i) = \sum_x p_{xy}(x, y = i)$.

```{table} Distribuzione di probabilità congiunta $P(X,Y)$ per i risultati dell'esperimento consistente nel lancio di tre monete equilibrate e probabilità marginali $P(X)$ e $P(Y)$.
:name: tbl-ditr-cong-biv

| $x /\ y$ |  0  |  1  | $P(x)$ |
|:--------------------:|:---:|:---:|:------:|
|          0           | 1/8 |  0  |  1/8   |
|          1           | 2/8 | 1/8 |  3/8   |
|          2           | 1/8 | 2/8 |  3/8   |
|          3           |  0  | 1/8 |  1/8   |
|        $P(y)$        | 4/8 | 4/8 |  1.0   |
```

(sec-margin-vc-cont)=
### Marginalizzazione di variabili casuali continue 

Nella trattazione della statistca bayesiana useremo spesso il concetto di "marginalizzazione" e vedremo equazioni come la seguente:

$$
p(y) = \int_{\theta} p(y, \theta) = \int_{\theta} p(y \mid \theta) p(\theta),
$$ (eq-ex-marg-cont)

laddove $y$ e $\theta$ sono due variabili casuali continue -- nello specifico, con $y$ denoteremo i dati e con $\theta$ i parametri di un modello statistico. Alla luce di quanto detto sopra, è possibiile pensare al caso continuo indicato nell'eq. {eq}`eq-ex-marg-cont` come all'estensione dell'esempio discusso in questo capitolo ad un numero infinito di valori delle due variabili continue (qui $y$ e $\theta$).

## Valore atteso di una funzione di una variabile casuale

A volte ci viene data una variabile casuale \$ X\$e dobbiamo lavorare con una funzione di $X$. Se $X$ è una variabile casuale e $h(X)$ è una funzione di $X$, allora anche $h(X)$ è una variabile casuale. Se si vuole calcolare il valore atteso di $h(X)$, lo si può fare usando la funzione di massa di probabilità o la funzione di densità di probabilità di $X$; non è necessario conoscere la funzione di massa di probabilità (o la funzione di densità di probabilità) di $h(X)$.

Consideriamo un esempio. Sia $X$ una variabile casuale discreta. Si trovi $\mathbb{E}(aX + b)$.

$\mathbb{E}(aX + b) = a\mathbb{E}(X) + b = a \sum_{x \in \Omega} xP(x) + b.$ Si noti che la soluzione ha richiesto l'uso $P(x)$, e non di $P(aX + b)$.

```{admonition} Nota
Il risultato precedente è valido per variabili casuali continua dove la somma viene sostituita da un integrale.
```

## Valore atteso di una funzione di molteplici variabili casuali

A volte ci vengono fornite due variabili casuali $X$ e $Y$ e dobbiamo lavorare con una funzione di $X$ e $Y$. Se $X$ e $Y$ sono variabili casuali e $h(X, Y)$ è una funzione di $X$ e $Y$, allora anche $h( X, Y)$ è una variabile casuale. Se si desidera calcolare la media di $h(X, Y)$, lo si può fare utilizzando la funzione di massa di probabilità congiunta (o la funzione di densità di probabilità congiunta di $X$ e $Y$); non è necessario conoscere la funzione di massa di probabilità congiunta (o la funzione di massa congiunta funzione di densità di probabilità) di $h(X, Y)$.

Facciamo un esempio. Siano $X$ e $Y$ due variabili casuali discrete con distribuzione di massa di probabilità congiunta

$$
P_{XY} (1,1) = 1/3; \quad P_{XY}  (1,2) = 1/8; \quad P_{XY} (2,1) = 1/2; \quad P_{XY} (2,2) = 1/24.
$$

Troviamo il valore atteso di $g(X, Y) = XY$.

$$
\begin{align}
\mathbb{E}g(X, Y) &= \mathbb{E}(XY) \notag\\
&= \sum_{x=1}^2 \sum_{y=1}^2 x y P_{XY}(x, y) \notag\\
&= 1 \cdot 1 \cdot \frac{1}{3} +  
   1 \cdot 2 \cdot \frac{1}{8} +
   2 \cdot 1 \cdot \frac{1}{2} +
   2 \cdot 2 \cdot \frac{1}{24}\notag\\
&= \frac{7}{4}.\notag
\end{align}
$$

Consideriamo un altro esempio. Sia $X_1, X_2, \dots, X_n$ una sequenza di variabili casuali i.i.d., ciascuna con media $\mu$ e varianza $\sigma^2$. Si trovi il valore atteso di $X = X_1 + X_2 + \dots + X_n$.

$\mathbb{E}(X) = \mathbb{E}(X_1) + \mathbb{E}(X_2) + \dots + \mathbb{E}(X_n) = \sum_{i=1}^n \mathbb{E}(X_i) = n \mu.$

Esaminiamo un terzo esempio. Sia $X_1, X_2, \dots, X_n$ una sequenza di variabili casuali i.i.d., ciascuna con media $\mu$ e varianza $\sigma^2$. Si definisca una nuova variabile casuale

$$
\bar{X} = \frac{X_1 + X_2 + \dots + X_n}{n}
$$

detta media campionaria. Troviamo il valore atteso di $\bar{X}$.

$\mathbb{E}(\bar{X}) = \frac{1}{n} \sum_{i=1}^n \mathbb{E}(X_i) = \mu.$

## Distribuzioni condizionali

Se $X$ e $Y$ sono variabili casuali distribuite congiuntamente, conoscere il valore di $X$ può modificare le probabilità relative alla variabile casuale $Y$. Per calcolare questa nuova probabilità, è necessaria l'idea di una *distribuzione condizionale*.

```{admonition} Definizione
Siano $X$ e $Y$ variabili casuali discrete distribuite congiuntamente. Definiamo la funzione di massa di probabilità condizionata di $X$ dato che $Y = y$ nei termini seguenti:

$$
P_{X \mid Y} (x \mid y) = P(X = x \mid Y = y) = \frac{P_{XY} (x, y)}{P_Y(y)}
$$
```

Per esempio, supponiamo che $X$ e $Y$ siano variabili casuali discrete con valori 1, 2, 3, 4 e che per $x,y = 1, 2, 3, 4$ la funzione di massa di probabilità congiunta sia data da

$$
  P_{XY}(x,y) =
    \begin{cases}
      \frac{1}{16} & \text{se $x = y$}\\
      \frac{2}{16} & \text{se $x < y$}\\
      0 & \text{se $x > y$}
    \end{cases}       
$$

Troviamo la funzione di probabilità condizionata di $Y$ dato che $X = 3$.

La distribuzione congiunta di massa di probabilità è la seguente.

```{table}
| $x /\ y$ | 1    | 2    | 3    | 4    | $P_X(x)$ |
|----------------------|------|------|------|------|----------|
| 1                    | 1/16 | 2/16 | 2/16 | 2/16 | 7/16     |
| 2                    | 0    | 1/16 | 2/16 | 2/16 | 5/16     |
| 3                    | 0    | 0    | 1/16 | 2/16 | 3/16     |
| 4                    | 0    | 0    | 0    | 1/16 | 1/16     |
| $P_Y(y)$             | 1/16 | 3/16 | 5/16 | 7/16 | 1.0      |
```

Dunque otteniamo

$$
P_{Y\mid X}(1 \mid 3) =  \frac{P_{XY}(3,1)}{P_X(3)} = 0 
$$

$$
P_{Y\mid X}(2 \mid 3) =  \frac{P_{XY}(3,2)}{P_X(3)} = 0 
$$

$$
P_{Y\mid X}(3 \mid 3) =  \frac{P_{XY}(3,3)}{P_X(3)} = \frac{(1/16)}{(3/16)} = \frac{1}{3}
$$

$$
P_{Y\mid X}(4 \mid 3) =  \frac{P_{XY}(3,4)}{P_X(3)} = \frac{(2/16)}{(3/16)} = \frac{2}{3}
$$

## Valore atteso condizionato

Un valore atteso condizionato è un valore atteso, o media, calcolato utilizzando una funzione di massa di probabilità condizionale (o una funzione di densità di probabilità condizionale).

```{admonition} Definizione
Siano $X$ e $Y$ variabili casuali discrete congiunte. Definiamo il valore atteso condizionato di $X$ dato che $Y = y$ come

$$
\begin{align}
\mathbb{E} (X \mid Y = y) &= \sum_x x P(X = x \mid Y = y)\notag\\
 &= \sum_x x P_{X \mid Y}(x \mid y) \notag
\end{align}
$$
```

Per fare un esempio, troviamo il valore atteso condizionato dell'esercizio precedente, dato che $X = 3$. Abbiamo che

$$
\begin{align}
\mathbb{E} (X \mid Y = 3) &= \sum_x x P(X = x \mid Y = 3)\notag\\
&= \frac{1 \cdot P_{XY}(3,1)}{P_X(3)} + \frac{2 \cdot P_{XY}(3,2)}{P_X(3)} + 
\frac{3 \cdot P_{XY}(3,3)}{P_X(3)} + \frac{4 \cdot P_{XY}(3,4)}{P_X(3)} \notag\\
&= 3 \cdot \frac{1}{3} + 4 \cdot \frac{2}{3} \notag\\
&= \frac{11}{3} \notag
\end{align}
$$

## Indipendenza

La nozione di indipendenza per le variabili casuali è molto simile alla nozione di indipendenza per gli eventi. Due variabili casuali sono indipendenti se la conoscenza relativa a una di esse non influisce sulle probabilità dell'altra. Nel caso di due variabili casuali discrete, presentiamo qui una definizione di indipendenza formulatanei termini della loro distribuzione di massa di probabilità congiunta.

```{admonition} Definizione
Due variabili casuali $X$ e $Y$ distribuite congiuntamente si dicono indipendenti se e solo se

$$
P_{X, Y}(x, y) = P_X(x) P_Y(y).
$$
```

A parole, se due variabili discrete $X$ e $Y$ non si influenzano, ovvero se sono statisticamente indipendenti, allora la distribuzione di massa di probabilità congiunta si ottiene come prodotto delle funzioni di probabilità marginali di $X$ e $Y$. Se $P_{X, Y}(x, y) \neq P_X(x) P_Y(y)$, allora le due variabili si dicono associate.

Vedremo in seguito come una misura del grado di associazione lineare tra due variabili casuali è fornita dalla covarianza (o dalla correlazione).

## Commenti e considerazioni finali 

In alcuni casi, diverse variabili casuali possono essere associate a ciascuna unità statistica della popolazione. Ad esempio, immaginiamo di scegliere uno studente a caso dall'elenco di tutti gli studenti iscritti a un'università e di misurare l'altezza e il peso di quello studente. A ogni individuo nella popolazione degli studenti corrispondono dunque due variabili casuali, altezza e peso. Quando due o più variabili casuali sono associate a ciascun elemento di una popolazione, si dice che le variabili casuali sono distribuite congiuntamente. In questo capitolo abbiamo visto come si possa rappresentare la distribuzione di massa di probabilità congiunta di due variabili casuali discrete e come si possano ottenere le distribuzioni marginali delle due variabili. Abbiamo anche esaminato i concetti di distribuzione marginale, distribuzione condizionata e indipendenza.
