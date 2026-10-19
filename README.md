# agile-course-log-iths

## Sprint 4 (v.42)
### Vad jag har gjort
Jag har arbete med 3 backlogg-items. Två indiviuell som är, klicka på produkt kortet som navigerar användaren till produktens egna detaljerad sida och sökning av produkter på produktsidan. Den tredje var att testa att email-service funkar för alla lokalt.

För detaljvyn skapade jag en route på `route.ts` med en id parameter och kopplade filen `productDetailPage.tsx` med en `ErrorBoundary`, en `HydrateFallback` och sin egna loader som tar emot parametern och kallar på metoden `getProductById` och skickar med id och token som argument. Produkt kortet gjordes klickbart med react routers `Link` tag som wrappar hela produkt kortet utan att påverka "Add to cart" knappen och länka till `/products/:{id}`.

För sökning av produkter redigerade jag `productsPage.tsx` med att lägga till en kontrollerad input fält för sökordet som är skiftlägesokänsligt på namn och beskrivning som är kombinerat med kategorifilter. Det klurigaste var filtreringslogiken som redan fanns i filen. Jag försökte utnyttja den med samband av sökningen.

Mejluppgiften gick ut på att verifiera att en order email har skickat lokalt på min dator.

### Eventuella problem och hur jag löste dem
En gruppmedlem upptäckte att `description` kunde vara `null` från backend, vilket orsakade en krash i produkt sökningen. Jag åtgärdade problemet genom att uppdatera modellen i frontend och gjorde en vilkorsats koll `(product.description ?? "")`. Det löste problemet.

Mejltestet fungerade inte i början på grund av ett "ogiltigt" app-lösenord. Jag hade inte fått något mejl från google eller någon typ av meddelande om att mitt lösenord hade gått ut. Jag löste det genom att skapa ett nytt lösenord och det åtgärdade problemet.

Produktuppgiften gav fyra merge konflikter mot main, eftersom en gruppmedlem hade jobbat med en uppdatering av designen på produkt kortet. Jag löste dem konflikterna själv i githubs webbeditor.

### Samarbete och agilt arbete
På måndagens sprintplanering tog vi in åtta uppgifter till sprinten. Jag valde sökning, detljvy, medan mejltestet gjordes individuellt av alla. På onsdagens standup flaggade jag att mina uppgifter inte kunde påbörjas på grund av andras ej påbörjade arbete, istället använde jag tiden till att forska mer av gateway som ska också implementeras. Mejlproblemet lyftes upp under fredagens retro. Där diskuterades en lösning som jag testade direkt och det funkade. Denna vecka funkade bra med att flagga blockeringar till mina gruppmedlemmar och gav mig tid att forks mer om gateway istället för att vänta. Vad som kunde göras bättre är poker planning, just nu pratar vi om poängen för uppgiften och inte anonymt.

## Sprint 5 (v.43)

### Samarbete och agilt arbete
I måndagens sprint planering tog vi in 12 uppgifter till sprinten. Det var uppgifter om gateway som vi hade suttit med varandra och delade upp en stor uppgift till flera små.
