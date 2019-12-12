---
---
Laddningstid för synttillverkare
=========================

I den här rapporten tänker jag undersöka laddningstid, resursanvändning och storleken hos tre av de största synt-och keyboardtillverkarnas webbplatser. Jag tänker även föreslå förbättringar för sänka laddningstiden och öka deras mätresultat i [Google PageSpeed](https://developers.google.com/speed/pagespeed/insights/?hl=sv). Jag tänker att min gräns för vad som är en acceptabel laddningstid för en sida ligger runt 4-5 sekunder, men ser helst att den ligger på max 2 sekunder.

Urval
-----------------------

Det finns många tillverkare av keyboards och syntar och jag har valt tre av de allra största och mest respekterade företagen i branschen, [KORG](https://www.korg.com/us/), [Roland](https://www.roland.com/global/) och [Moog](https://www.moogmusic.com/). Deras webbplatser skiljer sig någorlunda men har alla gemensamt att de använder många bilder och liknande sidupplägg. Jag har utifrån dessa webbplatser valt tre sidor som liknar varandra, nämligen startsidan, en produktsida och en supportsida. Hade jag gjort en mer omfattande studie hade jag även inkluderat företag som Yamaha, Sequential Circuits och Elektron.

Metod
-----------------------
I den här undersökningen använder jag Google Chrome som webbläsare och deras verktyg [PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights/?hl=sv) för att mäta labbdata och möjligheter till förbättringar. Jag använder även devtools inbyggt i Chrome för att analysera sidornas resurshantering, laddningstid och storlek.

Rsultat av undersökning finns att hitta [här](https://docs.google.com/spreadsheets/d/e/2PACX-1vTaJWLUTvbwsldnpnuaaUpBcoiXvKF6zqJuyXQt_3ANW4abmudo_AQj8BZQo1U-dGyv4JGZSMdsd2Lw/pubhtml?gid=0&single=true). Notera att undersökningen är gjord med cache avstängd. Detta påverkar laddningstiden nämnvärt på vissa sidor som använder många resurser i form av bilder.

Resultat
-----------------------
### KORG
[FIGURE src="img/korg_front.png " class="rapport-image" caption="Korg Startsida"]

I desktopvy får KORGs startsida ett lågt betyg på 37 av PageSpeed, medans deras produkt-och supportsidor får ett ganska högt betyg, 76 respektive 86. I mobilvy får de ännu lägre betyg, 15 och 16, på sin startsida och produktsida medans deras supportsida får 57 i betyg.

Laddningstiderna är långa. På mobilen tar det mellan 9.5 till nästan 13 sekunder att ladda en sida, medans desktopversionerna ligger mellan 2.5 och 5.8 sekunder.

Startsidan är den som tar allra längst tid vilket nog speglas av antalet resurser och storleken på sidan. 18 MB och 163 resurser på desktop samt 14.8 MB och 181 resurser på mobil. Det mesta av sidan tas upp av högupplösta bilder, jag räknar det till 88 stycken, där många är mellan 200 - 400 KB stora. I datan kan man läsa att deras mobilsida laddar mellan 20-30 fler resurser än desktopsidan.

Enligt Pagespeed kan inläsningen av sidan bli 9.72 sekunder snabbar genom att använda bildformaten JPEG 2000 eller WebP istället för PNG och JPG på grund av deras bättre komprimering. Oklart hur det påverkar kvalitén på bilderna dock. De säger även att det skulle gå att spara 7.6 sekunder på inläsning genom att koda bilderna effektivare.

Deras mobilvy skulle enligt Pagespeed kunna spara upp till 45 respektive 34 sekunder av samma åtgärder.

### Roland

[FIGURE src="img/roland_front.png " class="rapport-image" caption="Roland Startsida"]

I desktopvy får Roland högt betyg på alla sidor, 82, 88 och 85. I mobil får de däremot låga betyg, 28, 31 och 32.

Laddningstider för samtliga sidor i båda vyerna ligger mellan 1.5 sekunder till 2.5 sekunder. Storleken på sidorna och antalet laddade resurser för desktop och för mobil är i stort sett samma.

Deras startsida använder en hel del vitt utrymme och bara 28 bilder, vilket bidrar till att sidan laddas snabbare än KORGS startsida.

Även på denna sida säger Pagespeed att vi kan spara inläsningstid, 2.09 sekunder, på att använda modernare bildformat och 0.92 sekunder genom effektivare kodning. Deras mobilvyer skulle kunna spara mycket tid, upp till 18 sekunder, på att skjuta upp inläsningen av bilder som inte visas på skärmen.


### Moog

[FIGURE src="img/moog_front.png " class="rapport-image" caption="Moog Startsida"]

I desktopvy får Moogs supportsida högst betyg av alla undersökta sidor, 91 av 100. Deras start-och produktsidor får däremot 65 respektive 63 i betyg. Mobilvyn får däremot låga betyg. Start-och produktsidorna får 18 medans supportsidan ligger på 44.

Deras laddningstider är låga, supportsidan i desktopvy ligger på 1.4 sekunder och alla de övriga ligger mellan 1.8 och 2.5 sekunder.

Deras start-och produktsidor använder runt 80 resurser i båda vyerna men mobilvyn är ungefär 1 MB större än desktopvyn. Deras supportsida använder bara 46 och 47 resurser i sina vyer och har runt 1 MB i storlek.

Deras mobilvyer som får låga betyg skulle enligt Pagespeed kunna spara nästan 4 sekunder genom att använda bilder med rätt storlek.

Analys
-----------------------

När jag analyserar resultatet av studien framgår det att den webbplats som genomgående har längst laddningstid är KORG, vilket också speglas av ett lågt betyg i PageSpeed. Deras startsida i desktopvy är drygt 12 gånger större än och laddar dubbelt så många resurser som Moogs startsida. KORG har längst laddningstider i alla kategorier, där deras mobilvyer av start-och produktsidorna tar mellan 12 och 13 sekunder att ladda. De har även den största differensen i storlek och laddningstid mellan mobil och desktop.

Rolands start-och produktsidor får högst betyg av Pagespeed i båda vyerna, trots lågt betyg i mobilvy, men laddar samtidigt flest resurser och är störst i jämförelse med sina konkurrenter.

Moog vinner laddningstidspriset i den här undersökningen, men de som mest ett hundratal millisekunder snabbare än Roland. De använder även i de flesta fall lägst i antal resurser och storlek på sidan. Deras mobilbetyg på Pagespeed är aldrig högst eller längst i klassen men överlag väldigt lågt.

Den största förbättringsåtgärden hos alla tre sidor gäller bildernas filformat, storlek och kodning.

Min rangordning av hemsidorna är följande:

1. Roland (bäst mätbetyg i Pagespeed och låg laddningstid)
2. Moog (kortast laddningstid men färre resurser och lägre betyg i Pagespeed)
3. KORG (längst laddningstider och lägst betyg i Pagespeed)

Roland vinner på grund av överlag högt betyg i Pagespeed i desktop samt laddningstider som inte är så mycket längre än Moog. Det var däremot ingen sida som fick högt betyg i mobilvy.


Författare
-----------------------
Studie utförd och skriven av Nils Hollmer.
