![](../images/header.png)

+-----------------------------------------------------------------------+
| **SPECIFICHE ATTUATIVE DEI CODICI IDENTIFICATIVI DI VERSAMENTO,       |
| RIVERSAMENTO E RENDICONTAZIONE**                                      |
|                                                                       |
| *Allegato A alle \"Linee guida per l\'effettuazione dei pagamenti     |
| elettronici a favore delle* *pubbliche amministrazioni e dei gestori  |
| di pubblici servizi\"*                                                |
|                                                                       |
| **Versione 1.3.1 - gennaio 2018**                                     |
+-----------------------------------------------------------------------+

::: {#flusso-di-rendicontazione}
7\. Flusso di Rendicontazione
![](../images/image7.png)
============================
:::

Le informazioni che devono essere messe a disposizione dell\'Ente
Creditore sono organizzate in flussi omogenei di dati e devono essere
rese disponibili ai soggetti interessati a cura del prestatore di
servizi di pagamento che ha effettuato l'operazione di pagamento.

Entro e non oltre le ore 24 della seconda giornata lavorativa successiva
alla ricezione dell'ordine di pagamento (T+2), il prestatore di servizi
di pagamento che ha effettuato l'operazione provvede ad inviare al Nodo
dei Pagamenti-SPC il flusso di rendicontazione predisposto secondo lo
schema riportato nella successiva Tabella 4.

Le colonne *Liv*, *Gen*, *Occ* e *Len* della citata tabella assumono il
seguente significato:

+--------+------+-----------------------------------------------------+
| **col  | *    | indica il livello di indentazione del dato al fine  |
| onna** | Liv* | di rendere evidenti le strutture che contengono     |
|        |      | ulteriori informazioni (colonna \"Gen\" uguale ad   |
|        |      | *s*): esempio, le strutture di livello 1 sono       |
|        |      | formate da tutti i dati di livello superiore ad 1,  |
|        |      | quelle di livello 2 sono formate da tutti i dati di |
|        |      | livello superiore a 2, e così via.                  |
+--------+------+-----------------------------------------------------+
| **col  | *    | indica il genere (tipo) del dato da utilizzare; può |
| onna** | Gen* | assumere i seguenti valori:                         |
|        |      |                                                     |
|        |      | -   s - struttura che può contenere altre strutture |
|        |      |     o dati,                                         |
|        |      | -   an - dato alfanumerico                          |
|        |      | -   n - dato numerico.                              |
+--------+------+-----------------------------------------------------+
| **col  | *    | indica le "occorrenze" del dato nel formato         |
| onna** | Occ* | **min..max.**                                       |
+--------+------+-----------------------------------------------------+
| **col  | *    | indica la lunghezza massima del dato nel formato    |
| onna** | Len* | **min..max;** nel caso si tratti di una lunghezza   |
|        |      | fissa comparirà solo il dato *len*, nel caso di     |
|        |      | lunghezze fisse in alternativa la notazione sarà    |
|        |      | *len1 / len2.*                                      |
+--------+------+-----------------------------------------------------+

**Tabella** **4 - Flusso per la rendicontazione - Schema dati**

+-------------------+----+----+----+----+----------------------------+
| **Dato**          | *  | *  | *  | *  | **Contenuto**              |
|                   | *L | *G | *O | *L |                            |
|                   | iv | en | cc | en |                            |
|                   | ** | ** | ** | ** |                            |
+-------------------+----+----+----+----+----------------------------+
| versioneOggetto   | 1  | an | 1. | 1  | Versione che identifica    |
|                   |    |    | .1 | .. | l'oggetto scambiato.       |
|                   |    |    |    | 16 |                            |
|                   |    |    |    |    | Valori ammessi: **"1.0" e  |
|                   |    |    |    |    | "1.1"**                    |
+-------------------+----+----+----+----+----------------------------+
| ide               | 1  | an | 1. | 1  | Identificativo legato alla |
| ntificativoFlusso |    |    | .1 | .. | generazione e trasmissione |
|                   |    |    |    | 35 | del flusso di              |
|                   |    |    |    |    | riversamento.              |
|                   |    |    |    |    |                            |
|                   |    |    |    |    | Deve essere univoco        |
|                   |    |    |    |    | nell'ambito dell'anno di   |
|                   |    |    |    |    | riferimento delle          |
|                   |    |    |    |    | operazioni di pagamento    |
|                   |    |    |    |    | cui si riferisce il        |
|                   |    |    |    |    | flusso.                    |
|                   |    |    |    |    |                            |
|                   |    |    |    |    | Per la composizione del    |
|                   |    |    |    |    | dato si faccia riferimento |
|                   |    |    |    |    | al successivo paragrafo    |
|                   |    |    |    |    | `7.2 <sta                  |
|                   |    |    |    |    | nd-del-dato-identificativo |
|                   |    |    |    |    | flusso>`{.interpreted-text |
|                   |    |    |    |    | role="ref"}                |
+-------------------+----+----+----+----+----------------------------+
| dataOraFlusso     | 1  | an | 1. | 19 | Indica la data e ora di    |
|                   |    |    | .1 |    | creazione del flusso,      |
|                   |    |    |    |    | secondo il formato ISO     |
|                   |    |    |    |    | 8601                       |
|                   |    |    |    |    |                            |
|                   |    |    |    |    | **\[YYYY\]-\[MM\]-\[D      |
|                   |    |    |    |    | D\]T\[hh\]:\[mm\]:\[ss\]** |
+-------------------+----+----+----+----+----------------------------+
| identificativoU   | 1  | an | 1. | 1  | Riferimento assegnato dal  |
| nivocoRegolamento |    |    | .1 | .. | prestatore di servizi di   |
|                   |    |    |    | 35 | pagamento all'operazione   |
|                   |    |    |    |    | di trasferimento fondi con |
|                   |    |    |    |    | la quale viene regolato    |
|                   |    |    |    |    | contabilmente il           |
|                   |    |    |    |    | riversamento delle somme   |
|                   |    |    |    |    | incassate ovvero           |
|                   |    |    |    |    | l'accumulo degli accrediti |
|                   |    |    |    |    | disposti dai clienti.      |
+-------------------+----+----+----+----+----------------------------+
| dataRegolamento   | 3  | an | o  | 10 | Indica la data di          |
|                   |    |    |    |    | esecuzione dell'operazione |
|                   |    |    |    |    | di trasferimento fondi con |
|                   |    |    |    |    | la quale viene regolato    |
|                   |    |    |    |    | contabilmente il           |
|                   |    |    |    |    | riversamento delle somme   |
|                   |    |    |    |    | incassate, nel formato ISO |
|                   |    |    |    |    | 8601                       |
|                   |    |    |    |    | \[YYYY\]-\[MM\]-\[DD\].    |
+-------------------+----+----+----+----+----------------------------+
| istitutoMittente  | 1  | s  | 1. |    | Aggregazione relativa al   |
|                   |    |    | .1 |    | prestatore di servizi di   |
|                   |    |    |    |    | pagamento mittente che     |
|                   |    |    |    |    | genera il presente flusso. |
+-------------------+----+----+----+----+----------------------------+
| identificati      | 2  | s  | 1. |    | Aggregazione che riporta   |
| voUnivocoMittente |    |    | .1 |    | le informazioni            |
|                   |    |    |    |    | concernenti                |
|                   |    |    |    |    | l'identificazione          |
|                   |    |    |    |    | dell'Istituto mittente del |
|                   |    |    |    |    | flusso.                    |
+-------------------+----+----+----+----+----------------------------+
| tipoIden          | 3  | an | 1. | 1  | Campo alfanumerico che     |
| tificativoUnivoco |    |    | .1 |    | descrive la codifica       |
|                   |    |    |    |    | utilizzata per individuare |
|                   |    |    |    |    | l'Istituto Mittente; se    |
|                   |    |    |    |    | presente può assumere i    |
|                   |    |    |    |    | seguenti valori:           |
|                   |    |    |    |    |                            |
|                   |    |    |    |    | -   **'G'** = persona      |
|                   |    |    |    |    |     giuridica              |
|                   |    |    |    |    | -   **'A'** = Codice ABI   |
|                   |    |    |    |    | -   **'B'** = Codice BIC   |
|                   |    |    |    |    |     (standard ISO 9362)    |
+-------------------+----+----+----+----+----------------------------+
| codiceIden        | 3  | an | 1. | 1  | Campo alfanumerico che può |
| tificativoUnivoco |    |    | .1 | .. | contenere il codice        |
|                   |    |    |    | 35 | fiscale o la partita IVA,  |
|                   |    |    |    |    | il codice ABI o il codice  |
|                   |    |    |    |    | BIC del prestatore di      |
|                   |    |    |    |    | servizi di pagamento       |
|                   |    |    |    |    | mittente, in funzione del  |
|                   |    |    |    |    | dato                       |
|                   |    |    |    |    | tipoIdentificativoUnivoco. |
+-------------------+----+----+----+----+----------------------------+
| deno              | 2  | an | 0. | 1  | Contiene la denominazione  |
| minazioneMittente |    |    | .1 | .. | del prestatore di servizi  |
|                   |    |    |    | 70 | di pagamento mittente che  |
|                   |    |    |    |    | genera il flusso.          |
+-------------------+----+----+----+----+----------------------------+
| codiceBicBa       | 2  | an | 0. | 1  | Contiene il codice BIC del |
| ncaDiRiversamento |    |    | .1 | .. | PSP che ha generato il     |
|                   |    |    |    | 35 | SEPA Credit Transfer di    |
|                   |    |    |    |    | riversamento. Corrisponde  |
|                   |    |    |    |    | al dato AT-09 del SCT.     |
+-------------------+----+----+----+----+----------------------------+
| istitutoRicevente | 1  | s  | 1. |    | Aggregazione relativa      |
|                   |    |    | .1 |    | all'Ente Creditore         |
|                   |    |    |    |    | destinatario del flusso.   |
+-------------------+----+----+----+----+----------------------------+
| identificativ     | 2  | s  | 1. |    | Aggregazione che riporta   |
| oUnivocoRicevente |    |    | .1 |    | le informazioni            |
|                   |    |    |    |    | concernenti                |
|                   |    |    |    |    | l'identificazione fiscale  |
|                   |    |    |    |    | dell'Ente Creditore che    |
|                   |    |    |    |    | riceve il flusso.          |
+-------------------+----+----+----+----+----------------------------+
| tipoIden          | 3  | an | 1. | 1  | Campo alfanumerico che     |
| tificativoUnivoco |    |    | .1 |    | indica la natura dell'Ente |
|                   |    |    |    |    | Creditore; se presente     |
|                   |    |    |    |    | deve assumere il valore    |
|                   |    |    |    |    | **'G'**, Identificativo    |
|                   |    |    |    |    | fiscale Persona Giuridica. |
+-------------------+----+----+----+----+----------------------------+
| codiceIden        | 3  | an | 1. | 1  | Campo alfanumerico         |
| tificativoUnivoco |    |    | .1 | .. | contenente il codice       |
|                   |    |    |    | 35 | fiscale dell'Ente          |
|                   |    |    |    |    | Creditore destinatario del |
|                   |    |    |    |    | flusso.                    |
+-------------------+----+----+----+----+----------------------------+
| denom             | 2  | an | 0. | 1  | Contiene la denominazione  |
| inazioneRicevente |    |    | .1 | .. | dell'Ente Creditore che    |
|                   |    |    |    | 70 | riceve il flusso.          |
+-------------------+----+----+----+----+----------------------------+
| nume              | 1  | n  | 1. | 1  | Numero dei pagamenti       |
| roTotalePagamenti |    |    | .1 | .. | presenti nel flusso.       |
|                   |    |    |    | 15 |                            |
+-------------------+----+----+----+----+----------------------------+
| impor             | 1  | n  | 1. | 1  | Importo totale dei         |
| toTotalePagamenti |    |    | .1 | .. | pagamenti presenti nel     |
|                   |    |    |    | 18 | flusso. Deve coincidere    |
|                   |    |    |    |    | con la somma dei dati      |
|                   |    |    |    |    | singoloImportoPagato       |
|                   |    |    |    |    | presenti nel flusso.       |
|                   |    |    |    |    |                            |
|                   |    |    |    |    | **Deve essere maggiore di  |
|                   |    |    |    |    | 0.**                       |
+-------------------+----+----+----+----+----------------------------+
| dat               | 1  | s  | 1  |    | Aggregazione con un numero |
| iSingoliPagamenti |    |    | n  |    | di occorrenze pari         |
|                   |    |    |    |    | all'elemento               |
|                   |    |    |    |    | numeroTotalePagamenti      |
+-------------------+----+----+----+----+----------------------------+
| identificativo    | 2  | an | 1. | 1  | Riporta il dato codice IUV |
| UnivocoVersamento |    |    | .1 | .. | cui si riferisce il        |
|                   |    |    |    | 35 | pagamento rendicontato nel |
|                   |    |    |    |    | flusso.                    |
+-------------------+----+----+----+----+----------------------------+
| identificativoU   | 2  | an | 1. | 1  | Riferimento univoco        |
| nivocoRiscossione |    |    | .1 | .. | dell'operazione assegnato  |
|                   |    |    |    | 35 | al pagamento dal           |
|                   |    |    |    |    | Prestatore dei servizi di  |
|                   |    |    |    |    | Pagamento                  |
+-------------------+----+----+----+----+----------------------------+
| indiceDat         | 2  | n  | 0. | 1  | Indice dell'occorrenza del |
| iSingoloPagamento |    |    | .1 |    | pagamento all'interno      |
|                   |    |    |    |    | della struttura            |
|                   |    |    |    |    | datiSingoloPagamento della |
|                   |    |    |    |    | Ricevuta Telematica.       |
+-------------------+----+----+----+----+----------------------------+
| sin               | 2  | an | 1. | 3  | Campo numerico indicante   |
| goloImportoPagato |    |    | .1 | .. | l'importo relativo alla    |
|                   |    |    |    | 12 | somma pagata o revocata.   |
|                   |    |    |    |    | Deve essere diverso da 0.  |
|                   |    |    |    |    |                            |
|                   |    |    |    |    | Qualora il singolo importo |
|                   |    |    |    |    | pagato è riferito ad un    |
|                   |    |    |    |    | pagamento revocato (dato   |
|                   |    |    |    |    | c                          |
|                   |    |    |    |    | odiceEsitoSingoloPagamento |
|                   |    |    |    |    | =3) deve assumere un       |
|                   |    |    |    |    | valore negativo.           |
+-------------------+----+----+----+----+----------------------------+
| codiceEsit        | 2  | n  | 1. | 1  | Campo numerico indicante   |
| oSingoloPagamento |    |    | .1 |    | l'esito del pagamento. Può |
|                   |    |    |    |    | assumere i seguenti        |
|                   |    |    |    |    | valori:                    |
|                   |    |    |    |    |                            |
|                   |    |    |    |    | -   **0** = Pagamento      |
|                   |    |    |    |    |     eseguito               |
|                   |    |    |    |    | -   **3** = Pagamento      |
|                   |    |    |    |    |     revocato               |
|                   |    |    |    |    | -   **9** = Pagamento      |
|                   |    |    |    |    |     eseguito in assenza di |
|                   |    |    |    |    |     RPT                    |
+-------------------+----+----+----+----+----------------------------+
| dataEsit          | 2  | an | 1. | 10 | Indica la data in cui è    |
| oSingoloPagamento |    |    | .1 |    | stato disposto o revocato  |
|                   |    |    |    |    | il pagamento, nel formato  |
|                   |    |    |    |    | ISO 8601                   |
|                   |    |    |    |    | \[YYYY\]-\[MM\]-\[DD\].    |
+-------------------+----+----+----+----+----------------------------+

Per quanto riguarda gli Enti Creditori, tali flussi omogenei di dati
sono messi a loro disposizione attraverso l'infrastruttura di cui
all'articolo 5, comma 2 del CAD alla quale sono tenuti a collegarsi i
prestatori di servizi di pagamento che effettuano il riversamento, con
le modalità riportate nelle (Allegato B alle Linee guida).

Lo schema XML (XSD) descrittivo del contenuto dei file XML utilizzati
per trasferire le informazioni del flusso di rendicontazione è fornito
in formato elettronico nell'apposita sezione del sito dell'Agenzia per
l'Italia Digitale.

Si precisa che le Ricevute Telematiche soggette a "storno" o "revoca"
([vedi rispettivamente §§
2.1.4](http://pagopa-specifichepagamenti.readthedocs.io/it/latest/_docs/Capitolo2.html#storno-del-pagamento)
e
[2.3](http://pagopa-specifichepagamenti.readthedocs.io/it/latest/_docs/Capitolo2.html#revoca-della-ricevuta-telematica)
delle *"Specifiche attuative del Nodo dei Pagamenti-SPC"*) devono essere
sempre presenti nel flusso di rendicontazione: il recupero di tali somme
può avvenire contestualmente nello stesso flusso o in un flusso
successivo, in funzione del momento di ricezione da parte del PSP
dell'oggetto ER ("Esito Revoca") avente esito positivo.

Si sottolinea infine che, essendo il flusso di rendicontazione associato
ad un singolo SCT di riversamento, detto flusso è ovviamente sempre
correlato ad un unico codice IBAN di accredito.

::: {#precisazioni-sulla-colonna-contenutodella-tabella-4}
7.1 Precisazioni sulla colonna "contenuto"della Tabella 4
![](../images/image7.png)
\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--
:::

Tenuto presente che il significato dei dati richiesti per il flusso di
rendicontazione è riportato nella colonna "contenuto" della Tabella 4,
di seguito sono riportate alcune precisazioni sui dati presenti nel
flusso di rendicontazione:

**identificativoFlusso:** deve essere lo stesso riportato nel componente
**\< idFlusso\>** della causale del SEPA Credit Transfer di Riversamento
(dato "*Unstructured Remittance Information*" -attributo AT-05,
`vedi capitolo 6 <riversamento-agli-enti-creditori>`{.interpreted-text
role="ref"});

**identificativoUnivocoMittente:** la struttura deve coincidere con
quella presente nell'elemento identificativoUnivocoAttestante indicato
della RT rendicontata ([cfr. §
5.3.2](http://pagopa-specifichepagamenti.readthedocs.io/it/latest/_docs/Capitolo5.html#ricevuta-telematica-rt)
dell'Allegato B alle Linee guida *"Specifiche Attuative del Nodo dei
Pagamenti-SPC"*).

**identificativoUnivocoRegolamento:** ulteriore dato 'non ambiguo'
utilizzato per abbinare il flusso di rendicontazione con l'accredito
ricevuto. Può contenere, in alternativa, uno dei seguenti dati presenti
nel SCT di riversamento (cfr. *SEPA Credit Transfert Scheme Rulebook*):

-   a)  *Transaction Reference Number* (TRN, attributo AT-43 Originator
        Bank's Reference), qualora il PSP, al momento della generazione
        del flusso di rendicontazione, disponga di tale dato;

-   b)  *EndToEndId* (attributo AT-41 Originator's Reference), in caso
        contrario.

**identificativoUnivocoRiscossione:** rappresenta l'identificativo con
il quale il prestatore di servizi di pagamento individua la singola
operazione. Nel caso di utilizzo dell'infrastruttura di cui all'articolo
81, comma 2-bis del CAD, tale informazione si riferisce all'omonimo dato
presente nella "Ricevuta Telematica" di cui alla Sezione II delle , alle
quali si rimanda per i dettagli;

**indiceDatiSingoloPagamento:** dato facoltativo che rappresenta la
i-esima occorrenza di pagamento all'interno della struttura
datiSingoloPagamento presente nell'oggetto RT ("Ricevuta Telematica") di
cui alla Sezione II dell'Allegato B alle Linee guida;

**dataEsitoSingoloPagamento:** tale data deve coincidere con quella
dell'omologo dato presente nell'oggetto RT ("Ricevuta Telematica") o
nell'elemento dataEsitoRevoca della struttura datiSingolaRevoca presente
nell'oggetto ER ("Esito Revoca") di cui alla Sezione II dell'Allegato B
alle Linee guida .

7.2 Standardizzazione del dato identificativoFlusso {#stand-del-dato-identificativoflusso}
===================================================

Al fine di rendere omogenea la modalità di composizione del dato
identificativoFlusso presente nella causale standardizzata del SEPA
Credit Transfer (ref:[cfr. capitolo 6
\<riversamento-agli-enti-creditori\>]{.title-ref}) ed anche nel flusso
di rendicontazione di cui ref:[al capitolo 7
\<flusso-di-rendicontazione\>]{.title-ref} (cfr. Tabella 4 - Flusso per
la rendicontazione -Schema dati), sarà adottata la seguente struttura

**\<data regolamento\> \<istituto mittente\>"-"\<flusso\>**

dove i componenti sopra indicati assumono il seguente significato:

-   **\<data regolamento\>** contiene le stesse informazioni
    dell'elemento dataRegolamento del file XML;

\- **\<istituto mittente\>** contiene il codice del PSP che predispone
il flusso. Si precisa che tale codice deve coincidere con il dato
identificativoPSP indicato dal PSP stesso nel "*Catalogo Dati
Informativi*" di cui [al paragrafo 5.3.7
\<http://pagopa-specifichepagamenti.readthedocs.io/it/latest/
\_docs/Capitolo5.html\#catalogo-dati-informativi\>]() della Sezione II
dell'Allegato B alle Linee guida;

-   **\"-\"** dato fisso;

\- **\<flusso\>** stringa alfanumerica che, insieme alle informazioni
sopra indicate, consente di individuare univocamente il flusso stesso. I
caratteri ammessi all'interno della stringa sono: numeri da 0 a 9,
lettere dell'alfabeto latino maiuscole e minuscole ed seguenti
caratteri.

+-------------------------+---------------+----------+-----------------+
| \+                      | > **ASCII**   | > **S    | > **Nome**      |
|                         |               | imbolo** | >               |
| > -                     | \-\-\-\-\-\-  | >        | > :   -         |
| > -                     | \-\-\-\-\-\-\ | >        |                 |
|                         | -\-\-\-\-\--+ | :   -    | \-\-\-\-\-\-    |
|                         |               |          | \-\-\-\-\-\-\-\ |
|                         | :   **Dec**   | \-       | -\-\-\-\-\-\--+ |
|                         |     \|        | \-\-\-\- |                 |
|                         |     **Hex**   | \-\-\-\- | :   minus       |
|                         |               | \-\-\--+ |     sign -      |
|                         | \-\-\-\-\-    |          |     hyphen      |
|                         | \-\-\--+\-\-\ | :   \-   |                 |
|                         | -\-\-\-\-\--+ |          | \-\-\-\-\-\-    |
|                         |               | \-       | \-\-\-\-\-\-\-\ |
|                         | :   45 \| 2D  | \-\-\-\- | -\-\-\-\-\-\--+ |
|                         |               | \-\-\-\- |                 |
|                         | \-\-\-\-\-    | \-\-\--+ | :   underscore  |
|                         | \-\-\--+\-\-\ |          |                 |
|                         | -\-\-\-\-\--+ | :   \_   |                 |
|                         |               |          |                 |
|                         | :   95 \| 5F  |          |                 |
+-------------------------+---------------+----------+-----------------+

Esempi: **2015-07-15xxxxxxxx-0000000001**

**2015-07-15xxxxxxxx-hh\_mm\_ss\_nnn**
