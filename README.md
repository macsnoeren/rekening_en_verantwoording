# Rekening en Verantwoording

Een browser-gebaseerde webapplicatie voor het verwerken en categoriseren van banktransacties, bedoeld om rekening en verantwoording eenvoudiger te maken.

## Wat doet het?

Upload één of meerdere CSV-exports van uw bank en categoriseer elke transactie met een type (inkomsten, uitgaven, intern) en een categorie. De applicatie berekent automatisch samenvattingen per rekening, toont interne overboekingen overzichtelijk en geeft een totaaloverzicht van alle inkomsten en uitgaven over de geselecteerde periode.

## Functionaliteiten

- **CSV import** — importeer bankafschriften als CSV-bestand; de kolommen worden automatisch herkend (datum, bedrag, omschrijving, eigen rekening, saldo, tegenrekening)
- **Automatische typering** — negatieve bedragen worden automatisch ingesteld als uitgaven, positieve als inkomsten
- **Categorisering** — wijs per transactie een categorie toe uit een voorgedefinieerde lijst; interne overboekingen verwijzen naar uw eigen rekeningen
- **Bulk-toepassen** — één categorie toepassen op alle transacties met dezelfde tegenrekening binnen dezelfde rekening
- **Overzicht per rekening** — schakel rekeningen aan of uit om het overzicht te filteren; het saldo-overzicht toont altijd alle rekeningen
- **Saldo-controle** — begin- en eindsaldo per rekening worden berekend vanuit de CSV-data; een afwijkingsregel laat zien of inkomsten/uitgaven aansluiten op de saldowijziging
- **Interne overboekingen** — aparte tabel met van/naar rekening per overboeking
- **Overige uitgaven** — detailtabel met alle transacties die als "Overige uitgaven" zijn gecategoriseerd, inclusief tegenrekening en detailweergave
- **Detailweergave** — via het ⓘ-knopje per transactie alle ruwe CSV-velden inzien
- **Persistentie** — alle labels en instellingen worden opgeslagen in localStorage; na het sluiten van de browser blijft alles bewaard
- **Geheugenindicator** — de header toont hoeveel localStorage-ruimte in gebruik is

## Privacy & beveiliging

**Alle data blijft op uw eigen computer.** Er wordt geen informatie naar een server gestuurd. De applicatie werkt volledig in de browser zonder externe verbindingen. CSV-bestanden worden alleen lokaal verwerkt en nooit geüpload.

## Gebruik

1. Open `index.html` in een moderne browser (Chrome, Firefox, Edge, Safari)
2. Sleep een CSV-bestand naar het uploadgebied of klik om een bestand te kiezen
3. Wijs de juiste kolommen toe in de kolomkoppeling
4. Categoriseer de transacties in de tabel
5. Klik op **Overzicht** voor het totaaloverzicht

## Techniek

- Pure HTML, CSS en JavaScript — geen frameworks, geen afhankelijkheden
- Geen installatie nodig, werkt direct vanuit het bestand
- Opslag via de Web Storage API (`localStorage`, max. ~5 MB)
- CSV-parsing ondersteunt puntkomma- en komma-scheiding, aanhalingstekens en BOM

## Bestandsstructuur

```
index.html   — de volledige applicatie (één bestand)
README.md    — deze documentatie
```
