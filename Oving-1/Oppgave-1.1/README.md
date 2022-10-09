# Oppgave 1.1 - Lag spillet i kode!

Vi skal nå "modellere" spillet i kode. Utfør ett punkt av gangen og sørg for at ting fungerer (koden kompilerer) etter hvert punkt. IKKE gå videre til neste punkt før alt er OK i forrige punkt.

## Oppgave 1.1 a)
* **Lag en klasse og gi den navnet "Spill"**
* **Lag en array som medlemsvariabel i Spill-klassen.**
  * Denne skal representere eskene i spillet så du kan kalle den "esker". 
  * Arrayen kan være av type boolean[]. Da kan vi senere benytte verdiene true eller false for å angi om hunden har gjemt seg i en eske eller ei.
* **Lag en konstruktør/constructor til Spill-klassen som tar antall esker vi skal benytte i spillet som parameter/argument**
  * I konstruktøren kan du instansiere esker-arrayen. Lengden settes til verdien som sendes inn i kontstruktøren.
  * Plasser hunden i en tilfeldig eske 
    * Bruk Random-klassen i Java og dens nextInt() metode/funksjon for å finne ett tall mellom 0 og (antall esker - 1)
    * Bruk dette tilfeldige tallet til å sette tilsvarende "eske" i esker-arrayen til verdien true
* **Lag en "nesteRunde" metode/funksjon i Spill-klassen som flytter hunden en eske til høyre eller til venstre for der den befinner seg.**
  * Benytt Random-klassen for å velge høyre eller venstre. Benytt nextInt-funksjonen og finn et tall mellom 0 og 1. Verdien 0 kan representere venstre, mens verdien 1 kan representere høyre.
  * NB! Husk reglene som gjelder dersom hunden befinner seg i esken lengst til venstre eller lengst til høyre
* **Lag en "gjett" metode/funksjon i Spill-klassen for å kunne gjette hvilken eske hunden befinenr seg i.**
  * Metoden må ta en tall som paramteter/argument, som representerer hvilken eske man gjetter at hunden befinner seg i
  * Metoden returnerer verdien fra esken i esker-arrayen som angis som parameter
  * Før metoden returnerer må du gjøre et kall mot "nesteRunde"-metoden som flytter hunden.

## Oppgave 1.1 b) - Lag en enkel testklient
* **Opprett en klasse og gi den navnet "Testklient"**
* **Opprett metoden/funksjonen main i Testklient-klassen**
  * Opprett en ny instans av Spill-klassen med 5 esker.
  * Lag en loop som går helt til hunden er funnet
    * For hver runde i loopen skal du hente inn et tall fra brukeren og kalle gjett-metoden på Spill-instansen. Brukers input benytter som argument til gjett-metoden.
    * Hvis gjett-metoden returnerer true har brukeren funnet hunden og spillet avsluttes
    * Hvis gjett-metoden returnerer false har IKKE brukeren funnet hunden og spillet/loopen fortsetter.
