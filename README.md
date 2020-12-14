# kodeklubb-unreal
En slags intro til programmering som bruker Unreal Engine
Det er veldig uklart hva jeg skal gjøre med dette, eller hvor langt jeg skal gå, eller hva dette gir som ikke
man får bedre gjennom [Blueprint tutorials](https://www.youtube.com/watch?v=EFXMW_UEDco
). Det er ikke engang sikkert det er så veldig riktig, for jeg har jobbet lite med Unreal.

Det som er kult med Unreal er at det er litt som i Incredible Machine jeg spilte da jeg var liten
![inc machine](https://user-images.githubusercontent.com/1174441/102125050-571d3a00-3e49-11eb-8a18-0aa65892ed44.png)
i at man har en fysikkmotor og den slags. Her kan man også programmere, så man kan på en måte gjøre litt av begge deler, programmere med programmeringsspråk og stable ting som interagerer fysisk. Det kan fort bli meta.

For å gjøre dette må man laste ned og installere [Unreal Engine](https://www.unrealengine.com/) 

# Oppgave 1 - lage litt lysstyring
Det er kanskje ikke så mye en oppgave som bare at vi lager noe greier.
Det er på ingen måte ment å være "riktig" måte å styre lys på, det antar jeg man gjøre med DMX eller no hvis man skal gjøre noe tøft. 
Hensikten er bare å ha noe å styre. Men det kan jo fort være riktig også. Hvem vet. Spørs hva du skal.

Det første vi gjør er å lage et nytt prosjekt. Jeg bruker Unreal 4.25.4 (sliter litt nå med unreal, det bør gå i  4.26 og) nå men det bør gå i mange andre versjoner, vi skal ikke bruke så avanserte ting.
Velg nytt "Film, Televisino, and Live Events".

![nytt prosjekt](https://user-images.githubusercontent.com/1174441/102125734-6b156b80-3e4a-11eb-806e-05df0fdc23f2.png)

![blank template](https://user-images.githubusercontent.com/1174441/102125690-5afd8c00-3e4a-11eb-99a7-1ad1517501e5.png)

![ta med starter content](https://user-images.githubusercontent.com/1174441/102125793-79fc1e00-3e4a-11eb-83a3-66a1de75b52f.png)

Det kan ta litt tid.

Jeg drar inn et *Point light* og så flytter jeg spilleren til kanten av brettet.
![Point light](https://user-images.githubusercontent.com/1174441/102131530-a0be5280-3e52-11eb-9301-4fb4692cbccf.png)

Når man da trykker play eller <kbd>alt</kbd><kbd>p</kbd> så burde man se et lite lys.
Hvis man har god tid så kan man bygge litt ting rundt lyset sitt så man får litt mer skygge. Strengt tatt ikke nøye. Eller slette sola. Alt etter hva man føler for. kan skru opp lyset til 20 candela. Sånne ting.

Trykk på Blueprints og Level Blueprints.

![litt kode](https://user-images.githubusercontent.com/1174441/102133671-bed98200-3e55-11eb-918c-dbe9ffbc9723.png)

Da kan vi lage den her
![skru av](https://user-images.githubusercontent.com/1174441/102133791-f3e5d480-3e55-11eb-852c-ab36f2535575.png)

Så hva skjer når vi spiller? Nå kan vi diskutere om vi ikke er tilbake til start igjen...

Da skal vi lære å debugge. Da må vi først legge til et breakpoint.
![breakpoint](https://user-images.githubusercontent.com/1174441/102133982-3d362400-3e56-11eb-98fb-8271653a9c26.png)
Ikke så mye ennå, men kan bli nyttig..

La oss lage en box trigger. Sett den mellom spilleren og lyset og lag den litt stor.
![box trigger](https://user-images.githubusercontent.com/1174441/102134441-cc433c00-3e56-11eb-86eb-1967b4d66e65.png)

Triggerboxen må være valgt, da får man context sensitive meny.
koble til
![overlap](https://user-images.githubusercontent.com/1174441/102135152-d74a9c00-3e57-11eb-92a2-42737ed3993f.png)

Husk simualte physics
![overlap](https://user-images.githubusercontent.com/1174441/102136749-1a0d7380-3e5a-11eb-8c04-e7784a9f17aa.png)

Copy-paste set visibility.
![foo](https://user-images.githubusercontent.com/1174441/102135291-0bbe5800-3e58-11eb-978d-e6377a5371e5.png)

Nå kan du sette breakpoints på (eller ta dem av) og gå inn og ut av den boksen og se at lyset går på... Men aldri av?
https://user-images.githubusercontent.com/1174441/102136399-9fdcef00-3e59-11eb-84d0-b2b82fcb0855.png
