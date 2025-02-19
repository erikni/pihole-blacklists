# PI-HOLE BLACKLISTS pro CZ a SK zdroje

Tento repozitář obsahuje seznam [Pi-hole](https://pi-hole.net/) blacklistů zaměřených na ochranu před nevhodným obsahem pro uživatele v České republice a na Slovensku. Seznam se zaměřuje na:

- **[Hazardní weby a online casina](/erikni/pihole-block-betting-cz/)** – podle seznamu vydaného Ministerstvem financí ČR (MFČR), který je udržován ručně.
- **[Rizikové e-shopy](/erikni/pihole-block-risky-eshops-cz/)** – dle seznamu České obchodní inspekce. (automatická denní aktualizace)
- **[Dezinformační weby](/erikni/pihole-block-disinformation-webs/)** – dle seznamu Nadačního fondu nezávislé žurnalistiky a Konspiratori.sk (automatická denní aktualizace)

## Jak používat

1. **Stažení blacklistu:**
   - Stáhněte si aktuální verzi seznamu
```
https://raw.githubusercontent.com/erikni/pihole-block-risky-eshops-cz/refs/heads/main/risky-eshops-cz.txt
https://raw.githubusercontent.com/erikni/pihole-block-betting-cz/refs/heads/main/betting-cz.txt
https://raw.githubusercontent.com/erikni/pihole-block-disinformation-webs/refs/heads/main/disinformation-webs.txt
```

2. **Import do Pi-hole:**
   - Přihlaste se do administračního rozhraní Pi-hole.
   - Přejděte do sekce *Group Management* → *Adlists*.
   - Vložte URL adresu ke staženému souboru nebo přidejte jednotlivé zdroje ručně.
   - Aktualizujte blacklist spuštěním příkazu `pihole -g` na vašem serveru.

3. **Automatická aktualizace:**
   - Pro zajištění aktuálnosti doporučujeme nastavit cron job, například:
     ```bash
     0 3 * * * /usr/local/bin/pihole -g
     ```

## Přispívání

Pokud máte návrhy na zlepšení nebo jste identifikovali nové zdroje, neváhejte vytvořit *pull request* nebo otevřít *issue*. Při přidávání nových položek prosím dbejte na:

- Funkčnost URL.
- Relevanci zdroje pro CZ/SK uživatele.
- Pravidelnou aktualizaci a údržbu seznamu.

## Kontakty

Máte-li jakékoliv dotazy nebo připomínky, kontaktujte mě prostřednictvím GitHub Issues

---

*Projekt je stále ve vývoji a vítáme každou zpětnou vazbu či přínos od komunity!*
