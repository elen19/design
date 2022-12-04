---
Title: Colors
Description: Page about colors
---


Titel på rapporten
=======================
Syftet med rapporten är att undersöka hur snabbt hemsidor laddar samt om det går att förändra något särskillt innehåll för att förbättra laddningstiden.

Urval
-----------------------

De tre sidorna som undersöks är blocket.se, svt.se samt bth.se. Blocket och SVT valdes för de är två vanliga hemsidor som många svenskar besöker varje dag. 
BTH:s hemsida valdes främst för att skolan lär ut om hur hemsidor ska skapas och hålla en viss prestanda.


Metod
-----------------------

För varje webbplats mättes tre olika hemsidor. Hemsidan pagespeed, skapad av Google, användes för att mäta prestanda. Devtools network användes för att få ut laddningstid och resurser. Alla mätningar gjordes tre gånger och sedan togs ett genomsnitt för varje hemsida.

Resultat
-----------------------
### Alla mätvärden
<iframe src="https://docs.google.com/spreadsheets/d/e/2PACX-1vTo4pSz24wQmlEF7GCdM8P-q2L5kzcvqVHuN7DA3E6DN4voHaDyWcyy1gQTp1DlK1BwM5G_4Slk16om/pubhtml?widget=true&amp;headers=false" width="70%" height="300px"></iframe>

### BTH
![BTH](../image/bth-load.png?save-as=jpg){.analyze.pic}

BTH:s största problem på mobil är baserad på JavaScript och CSS. Det finns onödig JavaScript som inte används optimalt vilket saktar ner laddningstiden. På datorn är det liknande prolbem, dock är servers första svarstid de som saktar ner mest. Det beror oftast på tema, pluginmoduler eller serverns prestanda.[^1]

[^1]: https://developer.chrome.com/docs/lighthouse/performance/time-to-first-byte/

### SVT
![SVT](../image/svt-load.png?save-as=jpg){.analyze.pic}

Problemet på SVT:s sida både mobilt och på datorn är att den laddar in onödig JavaScript. Ett sätt att lösa det på är att reducera JavaScript kod som inte används äverhuvudtaget eller vänta med att läsa in scripts tills när de är relevanta.

### Blocket
![Blocket](../image/blocket.png?save-as=jpg){.analyze.pic}

Blocket fallar under samma problem som överstående. Det finns onödig JavaScript som körs och tar upp laddningstid.

Analys
-----------------------

Alla hemsidor har ett gemensamt problem med onödig JavaScript. Det går att lösa genom att förminska vilken kod som ska läsas in eller läsa in script endast när de behövs istället för direkt när hemsidan laddas in.

Det går att rangordna hemsidorna enligt följande efter alla mätningar, svt.se, blocket.se och sist bth.se. SVT och Blocket hade relativt bra prestandaoptimering där SVT låg lite före. Om man tar i hänsyn till att SVT laddar in nya nyheter hela tiden och Blocket tar nya artiklar varje sekund så är laddningstiderna väldigt bra. BTH gör någon uppdatering i veckan men ligger ändå en bra bit efter i både prestanda och laddningstid jämfört med de två andra webbplatserna.

Vi upplever att sida räknas som långsam och det tar över fyra sekunder att laddas in. Det vi menar med laddas in är dock inte hela sidan utan fram tills man börja se något på webbplatsen. När vi mätte BTH till exempel så fick vi att de skulle ta cirka sex sekunder. Den laddningstiden är för att hela sidan ska laddas in med alla länkar, bilder och så vidare. Det går att börja se sidan efter en till två sekunder vilket är godkänt. 

Vi tycker att BTH, SVT och Blocket har bra laddningstider från de perspektiv vi nyss nämnde. Hemsidorna laddar snabbt och det går snabbt att börja läsa på förstasidan. En sidnot som går att nämna är att alla tester har körts via en virituell maskin. Den har inte tillgång till 100% av datorns kraft vilket kan göra att testerna blir långsamare än vad de faktiskt är.

Övrigt
-----------------------

Skriven av Elis Engström (elen19) och Elias Andersson (elan19).
