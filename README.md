# ds-core-rilasci

Pacchetti di rilascio di **DS Core**, il plugin WordPress comune ai siti curati da Daniele Smiderle.

Questo repository contiene **solo** i pacchetti pronti (`.zip`), la loro firma digitale e il file con l'ultima
versione disponibile per canale (`test`, `stabile`). Il codice sorgente e la documentazione stanno in un repository
privato. Qui non ci sono e non ci devono mai essere password, chiavi private, token o dati di clienti.

## Come lo usano i siti

1. Il plugin legge il manifest del proprio canale (`manifest-<canale>.json`).
2. Se c'è una versione più nuova, WordPress la mostra come un normale aggiornamento.
3. Prima di installare, il plugin verifica la **firma Ed25519** del pacchetto con la chiave pubblica che ha al suo
   interno. Se la firma non è valida l'aggiornamento si ferma: un pacchetto modificato, anche caricato qui da altri,
   non viene installato.

La chiave privata di firma non è mai stata e non sarà mai in questo repository né su GitHub.

## Struttura (dal primo rilascio)

```
manifest-test.json      ultima versione per il sito di prova
manifest-stabile.json   ultima versione per tutti gli altri siti
pacchetti/              ds-core-<versione>.zip e ds-core-<versione>.zip.sig
```
