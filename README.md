# MFSOFT · Aggiornamenti

Sito (GitHub Pages) da cui le app di MFSOFT leggono l'ultima versione disponibile.

| App | File letto dall'app |
|---|---|
| IP Track | `ip-track/version.json` |
| PasswordVault | `passwordvault/version.json` |
| OPTIMUS | `optimus/version.json` |
| CriptoTransfer | `criptotransfer/version.json` |

Ogni `version.json` ha tre campi: `version` (numero dell'ultima versione), `notes` (novità, facoltativo)
e `download` (pagina o file da cui scaricarla, solo `https`).

## Pubblicare una versione nuova

1. Caricare gli installer in una Release di questo repository (tag es. `ip-track-28`).
2. Aggiornare `version`, `notes` e `download` nel `version.json` dell'app.
3. Commit e push: il sito si aggiorna da solo in un minuto circa.

CriptoTransfer legge anche `app_url` (il file `CriptoTransfer.exe` nella Release, solo da
`https://github.com/F4310M/`) e `app_sha256` (la sua impronta): con entrambi l'app offre "Aggiorna ora",
scarica il file, ne controlla l'impronta e si riavvia. Senza, mostra solo la pagina di download.

## Aggiungere un'app

Creare una cartella con il suo `version.json` e aggiungere una riga a `APPS` in `index.html`.
