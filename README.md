# MunnezzAssistant


---

![Versione](https://img.shields.io/badge/version-1.0.0-blue)
![Compatibile](https://img.shields.io/badge/compatible-Home_Assistant_2024.12.0+-green)
![Licenza](https://img.shields.io/badge/licenza-Open_Limited_Use-brightgreen)

[![Download](https://img.shields.io/badge/Download-⬇️-blue?style=for-the-badge&logo=homeassistant)](https://github.com/VesuvioCode/MunnezzAssistant/releases/latest)
![Gratuito](https://img.shields.io/badge/Gratuito-Sì-green?style=for-the-badge)
[![Supporta](https://img.shields.io/badge/Supporta-Gumroad-orange?style=for-the-badge&logo=gumroad)](https://vesuviocode.gumroad.com/l/pelkif)

---

---

> **MunnezzAssistant è gratuito!**  
> Se lo trovi utile, puoi supportare lo sviluppo con una donazione libera su Gumroad.

---

**MunnezzAssistant** è l'integrazione intelligente per Home Assistant che ti aiuta a gestire la raccolta differenziata in modo semplice, automatico e personalizzabile.

Ideato da **Ivan Aragione**, MunnezzAssistant semplifica la vita domestica grazie a:
- Notifiche dinamiche sulla raccolta dei rifiuti
- Conferma dei conferimenti
- Gestione completamente integrata con Home Assistant
- Configurazione grafica facile, accessibile a tutti

Compatibile con Home Assistant **versione 2024.12.0** e successive.

---

## Licenza

MunnezzAssistant è distribuito con **Licenza Open Limitata**.  
Con l'acquisto o il download gratuito è consentito:
- Utilizzo personale e commerciale illimitato
- Installazione presso clienti finali da parte di aziende o installatori

**È vietato:**
- Rivendere il codice sorgente
- Ridistribuire pubblicamente il progetto senza autorizzazione
- Modificare il codice per rimuovere la paternità dell'autore Ivan Aragione

---

## 🖥️ Dashboard Lovelace integrata

MunnezzAssistant include una dashboard visiva già pronta all’uso, progettata per offrire un'esperienza chiara, ordinata e in stile premium.

### 📁 Cartella `lovelace/`

| File                            | Descrizione                                                                 |
|---------------------------------|-----------------------------------------------------------------------------|
| `munnezzassistant_dashboard.yaml` | Layout completo con card interattive e notifiche integrate                |
| `munnezzassistant_light_theme.yaml` | Tema chiaro in stile MunnezzAssistant, con colori armonizzati             |
| `README_lovelace.md`            | Istruzioni dettagliate per importare la dashboard e attivare il tema      |

### 🛠️ Come importare la dashboard

1. Vai su **Impostazioni > Dashboard > 3 puntini in alto a destra > Importa da YAML**
2. Scegli il file `munnezzassistant_dashboard.yaml`
3. Salva e visualizza la dashboard

### 🎨 Come attivare il tema

1. Copia `munnezzassistant_light_theme.yaml` in `/config/themes/`
2. In `configuration.yaml`, assicurati di avere:

```yaml
frontend:
  themes: !include_dir_merge_named themes
```

3. Riavvia Home Assistant
4. Vai su **Impostazioni > Aspetto > Tema > munnezzassistant_light**

### ⚙️ Sensori richiesti

Per il corretto funzionamento della dashboard, assicurati di avere integrato questi sensori:

- `sensor.rifiuto_oggi` – tipo di rifiuto da conferire oggi
- `sensor.rifiuto_domani` – tipo di rifiuto per domani (facoltativo)
- `input_boolean.rifiuto_confermato` – conferma manuale dell’utente
- `input_select.utente_rifiuto` – (opzionale) selezione utente responsabile
- `automation.notifica_raccolta` – notifica vocale o mobile programmata

💡 *La dashboard si adatta automaticamente al tipo di raccolta prevista e semplifica la gestione da parte di tutti i membri della famiglia.*