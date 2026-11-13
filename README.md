# Njuškalo Clean

Lista filtera za blokatore oglasa (AdGuard, uBlock Origin, Brave Shields) koja na njuskalo.hr sklanja prozor o kolačićima (Didomi) i obavijesti o privatnosti, a stranici vraća pomicanje (scroll) koje taj prozor zaključava.

Lista se sama provjerava za nove verzije svaki dan.

## Instalacija jednim klikom

Za AdGuard i uBlock Origin u pregledniku:

[Dodaj Njuškalo Clean](https://subscribe.adblockplus.org/?location=https://raw.githubusercontent.com/sanjinplesa/njuskalo_block/main/njuskalo-clean.txt&title=Njuskalo%20Clean)

Ako klik ne otvori prozor za potvrdu pretplate (Brave to često ne radi), dodaj listu ručno prema uputama niže.

## Ručno dodavanje

Adresa liste:

```
https://raw.githubusercontent.com/sanjinplesa/njuskalo_block/main/njuskalo-clean.txt
```

### AdGuard

1. Otvori postavke AdGuarda i idi na Filteri (u aplikaciji za računalo: Postavke, Blokiranje oglasa, Filteri).
2. Odaberi Prilagođeni filteri, pa Dodaj prilagođeni filter.
3. Zalijepi adresu liste i potvrdi.

### uBlock Origin

1. Klikni ikonu uBlock Origina i zatim ikonu zupčanika (Otvori nadzornu ploču).
2. Otvori karticu Filter lists.
3. Na dnu u odjeljku Import označi "Import..." i zalijepi adresu liste.
4. Klikni Apply changes.

### Brave Shields

1. U adresnu traku upiši `brave://settings/shields/filters`.
2. Uključi "Developer mode" ako ga stranica traži.
3. Pod Custom filters klikni "Add new filter list", zalijepi adresu liste i spremi.
4. Osvježi stranicu njuskalo.hr.

## Što lista blokira

| Pravilo | Učinak |
| --- | --- |
| `sdk.privacy-center.org` | Ne učitava Didomi skriptu na njuskalo.hr |
| `#didomi-host`, `.didomi-popup-backdrop` | Sklanja Didomi prozor i tamnu pozadinu |
| `.PrivacyPolicyModal`, `[class*="PrivacyPolicy"]` | Sklanja prozore s obavijesti o privatnosti |
| `.Modal-backdrop` | Sklanja tamnu pozadinu iza prozora |
| `html, body:style(...)` | Vraća pomicanje stranice |

## Napomena

Pravilo `[class*="PrivacyPolicy"]` sklanja svaki element čija klasa sadrži taj tekst, pa može sakriti i legitiman dio stranice. Ako Njuškalo promijeni nazive klasa, neka pravila prestaju raditi. Prijavi to kroz Issues na ovom repozitoriju.
