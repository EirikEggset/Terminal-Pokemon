# Terminal-Pokemon

Spillet her blir spillt i terminalen ved å skrive 'python main.py'. For å spille må du importere keyboard med komamndoen 'pip install keyboard' på Windows.
Jeg lagde dette som et eget prosjekt som eksamensøving for IN1000 i Desember 2020. Målet var å lære meg objekorientering bedre, ikke grafikk. Men spillet er
lagd slik at man enkelt kan legge til "ordentlig" grafikk. Spillet har flere rom, gjenstander du kan plukke opp, en ryggsekk du kan åpne og lukke, forskjellige pokemons med 
forskjellige angrep og leveler. All data kan enkelt endres i konfig- og csv-filer.

Det brukes ulike unicodekarakterer, dersom terminalen din ikke kan se disse, men viser et spørsmålstegn kan du endre tegnene i filen 'room.py' på linjene 67, 69, 71 og 73.
Nøkkel:
  * '─' = Dør
  * '웃' = Boss (ikke implementert. MERK: dersom du vil bytte denne må strengen være to karakterer lagt, da denne tar to plasser)
  * '◓' = Pokeball (Trykk på 'E' ved siden av en for å få gjenstander/penger)
  * '█' = Brusdispenser (Trykk på 'E' ved siden av en for å kjøpe brus, koster penger)


Rommene er lest inn fra csv-filer. Første linje er 'nøkkelen' og gir informasjon splittet med ';'. Dersom det er flere parameter på noen av dem deles de med ','.
Første del sier posisjonen personen spawner i hvis han ikke kommer fra en dør, neste del sier hvilke rom dørene går til. Neste sier hvilken fil som har innholdet til pokeballen.
Siste sier hvilken dispenser som er i rommet (csv-fil med priser og varer). De to siste er valgfrie, og alt av data leses inn fra csv-filer (items, dispensere, pokemons osv...)

Diagrammet er tegnet med: 
  * bokstaver (hjørestykker)
  * tall (dører, hvilket tall viser indexen til hvilket rom, baser på rekkefølgen i nøkkelen på linje en)
  * - og | (vegger)
  * o (luft/ingenting)
  * \* (firkant, kan tolkes som bord eller stoler)
  * i (items: pokeballer med ting)
  * p (person/boss)
