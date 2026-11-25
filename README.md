# PC-wijzer

Gsm-app met de lonen en toeslagen per paritair comité, voor studentplanners, projectleiders en fields van Silver Tie P&H.

**App:** https://franflamen.github.io/pc-wijzer/

## Waar staan de gegevens?

De app leest drie bestanden. Pas je er één aan, dan ziet iedereen de wijziging binnen 1 à 2 minuten (eventueel de app even vernieuwen).

| Bestand | Wat staat erin | Kolommen |
|---|---|---|
| `pcs.csv` | één regel per PC | pc; naam; statuut; barema_lonen (ja/nee); flexiloon; studentloon |
| `lonen.csv` | één regel per categorie | pc; categorie; uurloon; aantal_functies; jongerenloon |
| `toeslagen.csv` | één regel per toeslag | pc; soort; toeslag; bedrag; voorwaarden; geldt_voor |

## Iets aanpassen

1. Klik hierboven op het bestand (bv. `toeslagen.csv`).
2. Klik rechtsboven op het **potloodje** (Edit this file).
3. Pas de tekst aan. Kolommen worden gescheiden door `;`.
4. Klik op **Commit changes…** en bevestig.

**Regels:**
- Het PC-nummer (`pc`) moet in de drie bestanden exact hetzelfde geschreven zijn (bv. `130.00`, niet `130`).
- Bedragen in `pcs.csv` en `lonen.csv`: komma als decimaal, zonder €-teken (bv. `15,2097`).
- `jongerenloon`: leeftijd=percentage, gescheiden door `;` en tussen aanhalingstekens, bv. `"16=80; 17=90"`.
- In `toeslagen.csv` is `bedrag` vrije tekst zoals je het in de app wil zien (bv. `€ 2,00 /uur` of `100 %`).
- `soort` groepeert de toeslagen in de app: Ecocheques, Flexi-vakantiegeld, Overuren, Feestdag, Zondag, Zaterdag / 6de-7de dag, Avond / namiddag, Nacht, Koude, Kledij, Overige vergoedingen.
- Een nieuwe PC toevoegen: een regel in `pcs.csv` + de categorieën in `lonen.csv` + de toeslagen in `toeslagen.csv`.
- Een regel verwijderen = de regel wissen.

Openen in Excel kan, maar Excel maakt van `130.00` soms `13000`. Bewerk daarom liefst rechtstreeks in GitHub.

Let op: deze repository is openbaar. Zet hier geen interne gegevens (factoren, marges, klantgegevens) in.
