# fakturuj-sharp
![Promo](https://i.imgur.com/ALQ8lgO.png)
Fakturuj# je jednoduchý program pro tvorbu faktur. Program neobsahuje žádná omezení a je zcela zdarma. **Program ukládá data pouze na počítač uživatele** ukládány jsou účetní jednotky zadané uživatelem a klienti které je možné odebrat pravým klikem po najetí na nabízenou položku. Uložená data je možné kdykoliv smazat v nastavení, nebo smazáním souboru ```data``` ve složce programu. Jedinou funkcionalitou vyžadující připojení je vyhledávání v registru podnikatelů podle IČO.

## Tvorba vlastní šablony
Pro fakturu je možné si vytvořit vlastní HTML šablonu. Pro každou informaci ve faktuře existuje klíč v čabloně který bude nahrazen příslušnou hodnotou. Každý klíč je obalen dvěmi složenými závorkami např. {{UCETNI_JEDNOTKA_NAZEV}} 
Jako příklad je možné si v nastavení vyexportovat zabudovanou šablonu.

### Seznam klíčů pro hodnoty
| Proměnná                                | Význam                                                                                           |
|-----------------------------------------|--------------------------------------------------------------------------------------------------|
| UCETNI_JEDNOTKA_NAZEV                   |                                                                                                  |
| UCETNI_JEDNOTKA_ULICE                   |                                                                                                  |
| UCETNI_JEDNOTKA_PSC                     |                                                                                                  |
| UCETNI_JEDNOTKA_MESTO                   |                                                                                                  |
| UCETNI_JEDNOTKA_ZEME                    |                                                                                                  |
| ODBERATEL_NAZEV                         |                                                                                                  |
| ODBERATEL_ULICE                         |                                                                                                  |
| ODBERATEL_PSC                           |                                                                                                  |
| ODBERATEL_MESTO                         |                                                                                                  |
| ODBERATEL_ZEME                          |                                                                                                  |
| CISLO_FAKTURY                           |                                                                                                  |
| DATUM_VYSTAVENI                         |                                                                                                  |
| DATUM_SPLATNOSTI                        |                                                                                                  |
| ZPUSOB_PLATBY                           |                                                                                                  |
| ZAPLACENO                               | Ano/Ne                                                                                           |
| POZNAMKA                                |                                                                                                  |
| CISLO_UCTU                              |                                                                                                  |
| QR_SPAYD                                | data-url qr kódu ```<image src="{{QR_SPAYD}}"/>```                                               |
| IBAN                                    |                                                                                                  |
| SWIFT                                   |                                                                                                  |
| BANKA                                   | Název banky                                                                                      |
| KOD_BANKY                               |                                                                                                  |
| {{POLOZKA_SABLONA}}{{/POLOZKA_SABLONA}} | Označení šablony položky HTML obsah mezi těmito dvěmi značkami  bude opakován pro každou položku |
| POLOZKA_PORADI                          | Dostupné pouze mezi značkami pro  šablonu položky                                                |
| POLOZKA_NAZEV                           | Dostupné pouze mezi značkami pro  šablonu položky                                                |
| POLOZKA_POCET                           | Dostupné pouze mezi značkami pro  šablonu položky                                                |
| POLOZKA_CENA                            | Dostupné pouze mezi značkami pro  šablonu položky                                                |
| POLOZKA_CELKEM                          | Dostupné pouze mezi značkami pro  šablonu položky                                                |
