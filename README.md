Wat
---
Vastgoedtool maken voor belgie cfr. https://vastgoedtool.com/ die enkel voor Nederland beschikbaar is.
Moet toelaten om bulk van panden te filteren bij zoeken naar interessant pand door
1. aggregeren van panden op verschillende websites (soort mashup)
2. custom metrics die interessant zijn voor investeerders bij te houden of toe te laten om te berekenen.


Bron:
-----
https://www.facebook.com/groups/552381698185474/permalink/1441987712558197/


Initiel scope:
--------------
1. vastgoed info verzamelen via immoweb (kan later uitbreiden met oneindig veel inputkanalen)
1.1 Lijst van alle gemeenten zoeken in belgie
1.2 per gemeente alle panden te huur zoeken.  (appartementen en huizen)
--> voor schatten wat je kan vragen qua huur
1.3 per gemeente alle panden te koop zoeken (appartementen en huizen)
--> voor te schatten welke prijs je mag verwachten te betalen.

Indexeren op
- type: appartement/huis
- prijs (range index ofzo): 100-200, 200-300, 300-400, 400-500, 500-600, ...
- aantal m2 bewoonbaar(range): 0-20, 30-40, 40-60, 60-80, 80 - 100, ...
- aantal m2 enkel voor huizen (range): 0-20, 30-40, 40-60, 60-80, 80 - 100, ...
- EPC (range): 0-100, 100-200, 200-300,400-500,500-600,600-700,700-800,800-900,900-1000,...
- gemeente --> beginnen per gemeente mss later via geolocatie panden in de buurt van etc.. zoekn.
 Of beet zoals zimmo...
- aantal kamers


appendix:
---------
Andere interessante metrics . bvb specific op basis van cursus.

1. Alle panden ophalen die voldoen aan de verschillende rendementsberekeningen op basis
van vraagprijs en gemiddelde huurprijs voor vergelijkbare panden.

2. Regio's zoeken waar verhouding huurprijs/aankoopprijs in interessant is (beetje gelinkt aan 1)

3. De panden ophalen met foto's die waarmee rekening word gehouden voor de vergelijkingen/berekeningen
Zodat je via de foto's enzo kan zien of er eventueel grote verschillen zijn ... 
bvb heel oud en versleten vs helemaal gerenoveerd etc... maar wel zelfde bouwjaar.
EPC opnemen als variabele in vergelijking zou dit wss grotendeels oplossen maar toch ... manueel verifieren
eenvoudig toelaten vind ik heel belangrijk...
De tool moet het grote werk wegnemen maar kan geen beslissing nemen omdat die bvb. geen foto's kan interpreteren ...

4. Eenvoudig toelaten om gebruiker zelf formules te laten maken en op te slaan etc...
En daarop dan alarmen te zetten... .

5. Linken gemeenten en hun deelgemeenten ...




Extra data koppelen ook cursusspecifiek.

1. Excel files met demografische info inlezen en deze ook gebruiken om interessante regio's te zoeken.

2. Eventueel per gemeente de demografische rapporten ophalen en ook zo beschikbaar maken via de tool.




Technologie:
------------
* Voor immoweb te queryen.
Checken of dit eenvoudig gaat via webdriver (wss met timeout - configureerbaar. teveel requests zal server wss niet toelaten ...)
alternatief is immoweb-api. maar lijkt me niet zo heel goed te werken. Te bekijken 

* spring boot voor backend

* opslaan + indexeren
beginnen met mongodb

* swagger voor documenteren endpoints

* angular2 voor frontend?
Mss voor heel snel prototype gewoon iets met bootstrat gebaseerd op enkele rest calls
En dan later. Zal afhangen van hoe vlot het gaat...
