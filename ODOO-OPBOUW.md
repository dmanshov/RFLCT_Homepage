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

## 7. Hoe verder

1. Open `index.html` in je browser om het ontwerp te beoordelen.
2. Bouw de pagina na in Odoo met de blokken uit de tabel in §2.
3. Stel de themakleuren (§3) in op de echte RFLCT-huisstijl.
4. Koppel het waardebepaling-formulier aan CRM (§4).
5. Vervang voorbeeld-foto, testimonials en contactgegevens door echte content.

---

*Bronnen voor de inhoud: openbare informatie van rflct.be (homepage,
tarievenpagina en blog) over de dienstverlening, het vaste pakket vanaf €2.850
en de besparing tot €10.000 commissie.*
