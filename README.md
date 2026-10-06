# MF@Software · Aggiornamenti

Sito (GitHub Pages) da cui le app di MF@Software leggono l'ultima versione disponibile.

| App | File letto dall'app |
|---|---|
| IP Track | `ip-track/version.json` |
| PasswordVault | `passwordvault/version.json` |
| OPTIMUS | `optimus/version.json` |

Ogni `version.json` ha tre campi: `version` (numero dell'ultima versione), `notes` (novità, facoltativo)
e `download` (pagina o file da cui scaricarla, solo `https`).

## Pubblicare una versione nuova

1. Caricare gli installer in una Release di questo repository (tag es. `ip-track-28`).
2. Aggiornare `version`, `notes` e `download` nel `version.json` dell'app.
3. Commit e push: il sito si aggiorna da solo in un minuto circa.

## Aggiungere un'app

Creare una cartella con il suo `version.json` e aggiungere una riga a `APPS` in `index.html`.
