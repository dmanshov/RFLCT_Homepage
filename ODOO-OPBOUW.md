# RFLCT — Alternatieve homepage: opbouw met Odoo Website building blocks

Dit document beschrijft een **alternatieve homepage** voor [www.rflct.be](https://www.rflct.be)
die bezoekers langer vasthoudt en aanzet tot doorklikken. De begeleidende
mockup staat in **`index.html`** (open dit gewoon in je browser om het ontwerp
te bekijken).

Alle secties zijn ontworpen om **na te bouwen met standaard Odoo Website
"building blocks" (snippets)** — er is geen maatwerk-development nodig.

---

## 1. Het probleem en de strategie

**Symptoom:** veel bezoekers, maar een hoge bounce — men opent de homepage en
vertrekt snel zonder door te klikken.

**Oorzaken die we aanpakken:**

| Oorzaak | Oplossing in dit ontwerp |
|---|---|
| Bezoeker snapt de kernbelofte niet in 5 seconden | Glasheldere hero-titel + concreet cijfer (€10.000 besparing) |
| Geen reden om íéts te doen | **Lead-magnet** "Gratis waardebepaling" — lage drempel, hoge relevantie |
| Geen vertrouwen / bewijs | Cijferbalk, vergelijking, testimonials, FAQ |
| Onduidelijk wat de volgende stap is | Eén dominante CTA-kleur, herhaald op elk schaalpunt |
| Twijfel blijft onbeantwoord | FAQ-accordion neemt bounce-redenen weg |

**Rode draad (de "hook"):** *probleem → oplossing → bewijs → actie*, met de
gratis waardebepaling als terugkerende conversie-anker. Dit is precies wat een
bezoeker nodig heeft om van "even kijken" naar "doorklikken" te gaan.

---

## 2. Sectie-voor-sectie: welk Odoo-blok gebruik je?

In Odoo bouw je de pagina door blokken vanuit het **Edit → Blocks**-paneel naar
de pagina te slepen. Hieronder per sectie het exacte snippet en de instellingen.

| # | Sectie | Odoo building block (categorie › naam) | Belangrijkste instellingen |
|---|---|---|---|
| 0 | Announcement bar | Thema-instelling › **Header › Top Bar** (of snippet **Text**) | Achtergrond = Primary, smalle balk |
| 1 | Navigatie | **Website Header** (thema-template) | Logo links, menu, CTA-knop "Gratis waardebepaling" rechts |
| 2 | Hero | Structure › **Cover** (`s_cover`) | Achtergrondfoto + overlay, 2 knoppen, badge-rij als kleine tekst |
| 3 | Cijferbalk | Content › **Numbers** (`s_numbers`) | 4 kolommen, achtergrond = Primary |
| 4 | Gratis waardebepaling ⭐ | **Call to Action** + **Form** (`s_website_form`) | Form-actie = "Create a Lead/Opportunity" (CRM) of "Send an Email" |
| 5 | Hoe het werkt | Content › **Steps** (`s_process_steps`) | 4 stappen, genummerd |
| 6 | Diensten | Structure › **Columns** / **Features** (`s_three_columns`) | 2 rijen × 3 kolommen, icoon + titel + tekst |
| 7 | Vergelijking | Content › **Comparisons** (`s_comparisons`) | 3 kolommen, middelste gemarkeerd ("Aanbevolen") |
| 8 | Tarief-teaser | Structure › **Text - Image** (`s_text_image`) of **Banner** | Eén CTA naar /tarieven |
| 9 | Testimonials | Content › **Testimonials / Quotes** (`s_quotes_carousel`) | 3 quotes met sterren + naam + gemeente |
| 10 | FAQ | Content › **FAQ** (`s_faq_collapse`) | Accordion, eerste item open |
| 11 | Slot-CTA | Structure › **Call to Action** (`s_call_to_action`) | Achtergrond = Primary, 2 knoppen |
| 12 | Footer | **Website Footer** (thema-template) | 4 kolommen: bedrijf, diensten, links, contact |

> 💡 De snippetnamen (`s_cover`, `s_numbers`, …) komen overeen met de technische
> namen in Odoo. In de editor zie je de Nederlandstalige labels (Cover, Cijfers,
> Stappen, Vergelijkingen, FAQ, …).

---

## 3. Huisstijl instellen in Odoo

In `index.html` zijn de kleuren als CSS-variabelen gekoppeld aan de
Odoo-themakleuren. Stel ze één keer in via **Website → Edit → Theme →
Colors**:

| Variabele | Voorstel (pas aan naar echte RFLCT-stijl) | Gebruik |
|---|---|---|
| `o-color-1` (Primary) | Diep groen/petrol `#14302e` | Vertrouwen, donkere vlakken, titels |
| `o-color-2` (Secondary) | Warm goud `#c8a15a` | Accent + **alle primaire CTA-knoppen** |
| `o-color-3` (Light) | Zacht zand `#f4f1ea` | Afwisselende sectie-achtergronden |
| `o-color-4` | Wit | Basis |
| `o-color-5` | Donkere tekst | Bodytekst |

> Vervang deze door de werkelijke huisstijlkleuren van RFLCT. Door alles aan de
> themakleuren te koppelen, hoef je de waarden maar op één plek aan te passen.

**Lettertype:** een schreefloze, vertrouwenwekkende font (bv. *Inter*,
*Poppins* of *Work Sans*) via **Theme → Fonts**.

---

## 4. De belangrijkste hook: de lead-magnet (sectie 4)

Dit is het zwaartepunt tegen bounce. Bouw het zo:

1. Sleep een **Form**-snippet (`s_website_form`) in een **Call to Action**-blok.
2. Zet de **Action** van het formulier op **"Create a Lead/Opportunity"**
   (vereist de CRM-app) zodat elke inzending automatisch in je pijplijn belandt.
3. Houd het formulier **kort**: alleen *adres* en *e-mail*. Hoe minder velden,
   hoe hoger de conversie.
4. Stel een **automatische bevestigingsmail** in (Marketing/Email Automation) met
   de eerste schatting of een belofte van opvolging binnen 1 werkdag.

Deze ene sectie geeft de bezoeker een concrete, waardevolle reden om te blijven
en iets te doen — in plaats van weg te klikken.

---

## 5. Copy-principes die in het ontwerp zijn toegepast

- **Eén belofte boven de vouw:** *"Verkoop je woning zelf. Maar niet alleen."*
- **Cijfer-ankers** (€10.000, €2.850, 100%) maken de waarde tastbaar.
- **Bezwaren ontkrachten** vóór ze ontstaan (vergelijkingstabel + FAQ).
- **Werkwoorden in CTA's** ("Bereken", "Bezorg mij", "Start vandaag").
- **Eén dominante actie-kleur** (Secondary/goud) zodat het oog altijd weet waar
  te klikken.
- **Regionale relevantie** (Vlaams-Brabant & Limburg) voor herkenbaarheid en
  lokale SEO.

---

## 6. Doorklik-stimulansen (tegen bounce)

Elke sectie eindigt of bevat een logische volgende stap, zodat de bezoeker
nooit "vastloopt":

- Hero → 2 CTA's (waardebepaling + "hoe het werkt")
- Steps → "Start vandaag — gratis"
- Tarief-teaser → "Bekijk alle tarieven" (naar /tarieven)
- Footer → volledige sitemap naar diensten, blog/academy en contact

Interne links naar **/tarieven**, **/aankoopbegeleiding** en **/blog** zorgen
ervoor dat de homepage als verdeelpunt naar de rest van de site werkt — precies
wat nu ontbreekt.

---

## 6b. Hero-variant (`hero-variant.html`)

Een rustiger alternatief voor het eerste blok: lichte achtergrond, tekst links
en één nette foto rechts (zonder donkere overlay). De hook blijft via een
zwevend cijfer-kaartje (€10.000) en de dubbele CTA.

| Onderdeel | Odoo building block | Instellingen |
|---|---|---|
| Hero split-layout | Structure › **Image - Text** (`s_image_text`) | Tekstkolom links, Media (foto) rechts, achtergrond = Light |
| Zwevend besparing-kaartje | **Card** (`s_card`) of Image met tekst-overlay | Absoluut gepositioneerd over de foto; in Odoo: kleine Card onder de foto of overlay-optie |
| Sterren-kaartje | **Card** / **Text** | Klein vertrouwenslabel rechtsboven de foto |

> Kies óf de Cover-hero (`index.html`) óf deze Image-Text-variant — niet beide.

---

## 6c. Detailpagina "Wat je precies krijgt" (`wat-je-krijgt.html`)

Aparte pagina die concreet maakt wat RFLCT aflevert. Tevens de belangrijkste
doorklikbestemming vanaf de homepage (knop in de Diensten-sectie →
`wat-je-krijgt.html`). Maak deze in Odoo aan via **Website → Pages → New Page**
en bouw ze met onderstaande blokken.

| # | Sectie | Odoo building block (categorie › naam) | Belangrijkste instellingen |
|---|---|---|---|
| 1 | Page hero + breadcrumb | Structure › **Banner** (`s_banner`) of smalle **Cover** (`s_cover`) | Achtergrond = Light, breadcrumb als kleine tekst, "tags" als knop-pills |
| 2 | Vier fases met deliverables | Per fase een **Image - Text** (`s_image_text`) óf **Steps** (`s_process_steps`) | Genummerd; de deliverables-lijst eronder als **Card** (`s_card`) of **Text** met opsomming in 2 kolommen |
| 3 | Inbegrepen vs. "goed om te weten" | Content › **Comparisons** (`s_comparisons`, 2 kolommen) of 2× **Text** naast elkaar | Achtergrond = Primary, links checklist, rechts nuanceringen |
| 4 | Resultaat / outcome | Content › **Numbers** (`s_numbers`) | 3 kolommen met grote cijfers |
| 5 | Slot-CTA | Structure › **Call to Action** (`s_call_to_action`) | Achtergrond = Primary, 2 knoppen terug naar de waardebepaling |
| 6 | Footer | **Website Footer** (thema-template) | Beknopte footer |

**Koppeling vanaf de homepage:** in de Diensten-sectie (§2, rij 6) staat onder de
features-grid een **Button**-snippet → link naar `wat-je-krijgt.html`. Dit maakt
van de homepage een verdeelpunt en verlaagt de bounce.

> 💡 Tip voor de fase-deliverables: het kleine, genummerde icoon-vierkant (1–4)
> maak je met de **Steps**-stijl, of met een Image-Text waar je in de
> linkerkolom een gekleurd tekstblok met het cijfer plaatst. De deliverables
> zelf zijn een gewone opsomming binnen een **Card** met achtergrondkleur Light.

---

## 7. Hoe verder

1. Open `index.html`, `hero-variant.html` en `wat-je-krijgt.html` in je browser
   om de ontwerpen te beoordelen.
2. Kies je hero: de Cover-versie (`index.html`) of de rustige Image-Text-variant
   (`hero-variant.html`, §6b).
3. Bouw de homepage na in Odoo met de blokken uit §2 en de detailpagina met §6c.
4. Stel de themakleuren (§3) in op de echte RFLCT-huisstijl.
5. Koppel het waardebepaling-formulier aan CRM (§4).
6. Vervang voorbeeld-foto's, testimonials, deliverables en contactgegevens door
   echte content (stem de deliverables per fase af met RFLCT).

---

*Bronnen voor de inhoud: openbare informatie van rflct.be (homepage,
tarievenpagina en blog) over de dienstverlening, het vaste pakket vanaf €2.850
en de besparing tot €10.000 commissie.*
