# Opslags bog til scriptcraft.

## Indhold:
* [Introduktion](#introduktion)

* [Javascript](#javascript)
  * [Variable](#variable)
  * [If Statements](#if-statements)
  * [Loops](#loops)

* [Scriptcraft Funktioner](#scriptcraft-funktioner )
  * [echo](#echo)
  
  * [Drone](#drone)
     * [Drone Funktioner](#drone-funktioner)

  * [Minecraft Blocks](#minecraft-blocks)


## Introduktion
Denne side bliver opdateret løbende med de ting vi lærer. Hvis man vil læse foran kan man altid gå ind på scriptcrafthjemmeside!
Link til den engelske hjemmeside: https://scriptcraftjs.org/
Herinde kan man også finde en instalations guide til scriptcraft.


Hust at når man skriver javascript kode i minecraft, så skal man skrive /js foran. Ex: 

`/js var placering = 10;`

Hvis man skriver kode i filer er dette ikke nødvendigt, her kan man nøjes med:

`var placering = 10;`


## Javascript
Dette afsnit beskriver javascript generelt. Hvis i er i tvivl om noget generelt java script kode så findes det her.
### Variable
En variabel er et navn på noget man har gemt i computerens hukommelse. Man kan forestille sig det lidt som en kasse hvor man har skrevet et navn på, og så kan man ligge ting ned i kassen. 

I javascript kan man oprette variable ved at skrive 'var'. Man skriver fx:

`var spillerNavn;`

Nu har vi oprettet en variabel der hedder spillerNavn. Vi kan nu sætte spiller navn til at være lig et navn. Dette kan vi gøre således:

`spillerNavn = 'Anders And';`

Nu har vi sat spillerNavn til at være lig 'Anders And'. Hver gang vi bruger spillerNavn fra nu af så vil den være ligmed 'Anders And'. Vi kunne fx bruge **echo** funktionen i scriptcraft til at vise navnet.

`echo(spillerNavn);`

Dette vil printe 'Anders And' ud på skærmen.
Man kan altid ændre en variabel igen, vi kan fx ændre spillerNavn til 'Mickey Mouse'. Så har vi ændret indeholdet i variablen, så den nu indeholder 'Mickey Mouse'.

`spillerNavn = 'Mickey Mouse';`

Man kan også sætte en variabel i samme linje som man laver den, her er et eksempel:

`var spiller2Navn = 'Fedtmule';`


### If Statements

#### Sandt/Falsk

I kender begreberne sandt og falsk. Disse begreber findes også i javascript. Vi kalder dem 'true' for sandt og 'false' for falsk. Et simpelt eksempel kunne være. Er jorden rund? Hvilket er sandt. Tilsvarende: Er jorden firkantet? Hvilket er falsk.

Disse eksempler kan vi ikke bruge i javascript. Computeren forstår ikke abstrakte begreber, men det forstår simple matematiske spørgsmål. Vi kan fx spørge computeren om: Er 5 lig med 7? Er 3 mindre end 4? 

Det giver ikke så meget mening at skrive, men hvis vi bruger variable giver det pludselig mere mening. Så lad os sige vi har en variabel kaldet antalElever. Denne variable indeholder antallet af elever i en eller anden klasse. Nu kan vi stille spørgsmål ligesom før: Er antalElever lig med 7? Er antalElever mindre end 4?

I javascript skriver man selvføgelig ikke tekst på den måde. Man skriver i stedet forskellige tegn. Fx:  Er antalElever lig med 7? er det samme som antalElever==7.

* x\<y,   Er x mindre end y
* x\>y,   Er x større end y
* x==y,   Er x lig med y
* x<=y,   Er x mindre end eller lig med y
* x>=y,   Er x større end eller lig med y
* x!=y,   Er x ikke lig med y. Altså er x forskellige fra y.

Her er et par eksempler hvor **antalElever er lig 7**:

* antalElever\<10 :   true
* antalElever > 10 :  false
* antalELever == 7 :  true
* antalElever <= 6 :  false
* antalElever >= 7 :  true
* antalElever != 7 :  false

#### if/else

If er en indbygget funktion i de fleste programmerings sprog. If tjekker om noget er sandt og hvis det er sandt, så udføres koden der står inde if statementen oprationer. Koden kan fx se sådan ud: 

```javascript
if(antalElever<7){
/*Denne kode udføres hvis statementen er sand.*/
}
/*Denne kode udføres altid*/
```

Vi kan nu se at vi har en if statement, som tager et input. Vores input er (antalElever\<7). Så vi tjekker om antallet af elever er mindre end 7. Hvis  det er sandt, så køre vi koden der står imellem {}. Hvis det ikke er sandt, så springer vi alt koden over der står mellem {}. Her er et par eksempler:

```javascript
antalElever= 8
if(antalElever<9){
 /*Denne kode udføres. Fordi antallet af elever er mindre end 9*/
}

if(antalElever>7){
 /*Denne kode udføres. Fordi at antalElever er større end 7*/
}

if(antalElever!=8){
 /*Denne kode udføres ikke. Fordi at antal elever er lig med 8.*/
}
else{
  /*Denne kode udføres, fordi if'en der står ovenover ikke var sand.*/
}
```

Vi kan se at det første og andet if statement bliver kørt, men det tredje if statement er ikke sandt. Så kommer der en ny funktion som kaldes else. Else betyder at hvis den if statement der står ovenover er falsk, så udføre den det som står i else. Fx kan vi se på koden her:

```javascript

if(antalElever<8){
 /*Denne kode udføres, hvis antallet af elever er mindre end 8*/
}
else{
  /*Denne kode udføres, hvis antallet af elever er større end eller lig med 8.*/
}
if(antalElever!=8){
 /*Denne kode udføres, hvis antallet af elever er forskellige fra 8*/
}
else{
  /*Denne kode udføres, hvis antallet af elever er lig 8*/
}
```

Der findes også en funktion der hedder else if. else if virker ligesom else. Hvis den statement der står ovenover er falst, så kaldes else if. Modsat else, så tjekker else if også om et eller andet er sandt. Her er et eksempel:

```javascript

if(antalElever==8){
 /*Denne kode udføres, hvis antallet af elever er lig 8*/
}
else if(antalElever==7){
 /*Denne kode udføres, hvis antallet af elever er lig 7 og den forrige if statement ikke var sand.*/
}
else if(antalElever<10){
  /*Denne kode udføres, hvis antallet af elever er mindre end 10 og alle de forrige if statements er falske*/
}
else{
 /*Denne kode udføres hvis ingen af de andre if statements var sande.*/
}
```

Hver gang man skriver `if(variabel){}`, så starter man en ny sekvens. Man kan altså have flere if statements, der ikke afhænger af hinanden. fx:

```javascript
if(antalElever>10){
 /*Denne kode udføres, hvis antallet af elever er større end 10*/
}

if(antalElever==8){
 /*Denne kode udføres, hvis antallet af elever er lig 8. Uanset hvad der skete i den forrige if statements. */
}
else if(antalElever==7){
 /*Denne kode udføres, hvis antallet af elever er lig 7 og den forrige if statement ikke var sand.*/
}
else{
 /*Denne kode udføres hvis ingen af de andre (if/else if) statements var sande.*/
}
```


### Loops

Loops er en en funktion i javascript der får kode til at gentage sig selv. Vi kunne fx sige:

```javascript
 while(true){
   this.box(5,1,1,1);
   this.right(1);
 }
```

Som i kan se brug vi ordet while. While kan oversættes til 'så længe at'. Så når vi skriver while(true), så skriver vi at så længe dette er sandt, gør noget. Vi gentager altså koden uendeligt. Vi kan derfor ændre lidt på inputtet:

```javascript
var antalKasser=0
while(antalKasser<10){
   this.box(5,1,1,1);
   this.right(1);
   antalKasser++;
 }
```

Nu har vi modificeret koden, og koden gør derfor følgende: Vi starter med 0 kasser. Så går vi ind i while loopen og køren koden så længe antallet af kasser er mindre end 10. Inde i loopet laver vi en kasse, så rykker vi dronen en til højre og til sidst tæller vi antallet af kasser 1 gang op.
På den måde har vi nu gentaget noget kode vi bruger flere gange, uden at kopier der. Hvis vi ikke brugte loops, kunne koden komme til at set sådan her ud:


```javascript

   this.box(5,1,1,1);
   this.right(1);
   this.box(5,1,1,1);
   this.right(1);
   this.box(5,1,1,1);
   this.right(1);
   this.box(5,1,1,1);
   this.right(1);
   this.box(5,1,1,1);
   this.right(1);
   this.box(5,1,1,1);
   this.right(1);
   this.box(5,1,1,1);
   this.right(1);
   this.box(5,1,1,1);
   this.right(1);
   this.box(5,1,1,1);
   this.right(1);
   this.box(5,1,1,1);
   this.right(1);
```

Her kan man se at der er meget svære at læse hvad der står, og while loopet gør det markant nemmere at læse og forstå hvad koden gør.
Der findes et loop mere som kaldes for et for loop. Et for loops bruges oftest når man har et start punkt og man skal køre koden et antal gange. Vi kan fx omskrive den forrige while loop til et foor loop således:

```javascript
 for(antalKasser=0;antalKasser<10;antalKasser++){
   this.box(5,1,1,1);
   this.right(1);
 }
```

Det kan ses at koden er blevet en lille smule kortere, og det kan nogle gange gør det nemmere at læse koden.


## Scriptcraft Funktioner 

### echo
**echo** er en funktion i scriptcraft der printer ting på skærmen i minecraft. **echo** har to input. Hvem den skal skrive beskeden til og hvad den skal skrive. 

```javascript
echo(self, 'Denne besked printes på skærmen.');
```
Her er self den spiller som kalder funktionen echo.

### Drone

Drone er et objekt i scriptcraft. Den bruges til at bygge ting i minecraft. Det mest simple metode til at bygge ting er **box**. Med box der laver man en kasse. Hvilket jo er praktisk når minecraft består af kasser. Den mest simple udgave af box kan se således ud:

```javascript
box(blocks.oak);
```
Dette laver en 'oak' block i stedet for den block spilleren pejer på. Hvis spilleren ikke peger på en block laver den en oak block to klodser foran ham.

Man kan også lave en kasse med en variabel størrelse. fx:

```javascript
var bredde = 10;
var hoejde = 3;
var dybde = 6;
var d=box(blocks.oak, bredde, hoejde, dybde);
```
Dette laver en kasse af oak som er 10 bred, 3 høj og 6 dyb. Det kan være en rigtig god ide at prøve sig frem hvis man er i tvivl om hvad de forskellige ting betyder.

Der er selvfølgelig muligt at lave ting af mange forskellige blocks. Det er to måder at gøre det på.  Den første måde er at bruge blocks objektet. Vi har allerede set blocks.oak. Men der findes tilsvarende navne på alle de andre blocks. fx blocks.air.

Den anden måde er at skrive tal værdien for blocken man skal bruge. Man skriver her i stedet talværdien for blokken. For oak er det fx: 

```javascript
box('5', bredde, hoejde, dybde);
```
Nogle blocks findes der flere forskellige udgaver af. Fx findes der mange forskellige typer af planker. Vi har set oak allerede. Men der findes tre andre slags træer. I denne situation skriver man et tal bagved ':'. Vi kan tage blocks.birch. Den kan laved ved: 

```javascript
box('5:2', bredde, hoejde, dybde);
```
Der findes en liste over alle block numre i afsnittet [Minecraft Blocks](#minecraft-blocks).

Man kan også bevæge dronen rundt. Dette gør man ved at bruge følgende funktioner:
 * up()
 * down()
 * left()
 * right()
 * fwd()
 * back()
 * turn()
 
De første seks funktioner bevæger dronen i en retning i forhold til hvilken vej den pejer. Dronen pejer altid frem i den retning som spilleren først lavede dronen. Fx vil medtoden up() rykke dronen en klods op. Man kan også give up et input og så rykker den det antal klodser. Fx up(4) rykker dronnen 4 klodser op. Man kan gøre det samme for de andre metoder.

Den sidste metode turn, den rykker ikke dronen. Den rotere i stedet dronen. Så hvis man skriver turn() så roterer dronen 90 grader i urets retning. Man kan også give et tal input, så roterer dronen 90 grader med uret det antal gange man skriver.

Drone kan rigtig mange ting, derfor anbefaler vi at man kigger på den engelske guide, så man kan se alle de forskellige funktioner! 
Link: https://github.com/walterhiggins/ScriptCraft/blob/master/docs/API-Reference.md#drone-plugin

#### Drone Funktioner

Det er muligt at implementere droner i en javascript funktion i en seperat fil. Det kunne fx være jeg ville lave en funktion der bygger et minecraft begynder hus. Jamen så kunne jeg lave en funktion der hed 'begynderhus'. Inde i minecraft kan man så kalde `/js begynderhus()`. Så udføre den det som er beskrevet i funktionen.

Der ligger en skabelon til hvordan man skriver en drone funktion her:
https://github.com/ArvidLangsoe/MineCraft-WorkShop-CP/blob/master/Drone%20Eksempler/skabelon.js

Det er vigtigt at navnet på ens funktion står i toppen og i bunden. I skabelonen står der fx: `function skabelon()`. Her skal `skabelon` erstates med funktionens navn. Hvis jeg bruger begynderhus eksemplet, så ville jeg skrive: `function begynderhus()`. I nederste linje skal jeg også erstate 'skabelon' med 'begynderhus'. Der må **IKKE** være mellemrum i en funktions navn.

Når man arbejder med droner, så skal man inde i sin funktion bruge ordet `this`. `this` refferere til den drone man starter når man kalder funktionen. Derfor kan man fx skrive `this.box('5')`. Dette vil lave en block af typen oak. Tilsvarende kan man bruge alle de andre drone operationer, som beskrevet i det tidligere afsnit.

Der ligger et eksempel på hvordan man bruger dronen i funktioner her:
https://github.com/ArvidLangsoe/MineCraft-WorkShop-CP/blob/master/Drone%20Eksempler/mystarterhouse.js

Når man har lavet sin funktion skal man gemme den på serveren. Det gør man ved at gemme sin funktion som en javascript der hedder det samme som ens funktion. Min fil hedder altså begynderhus.js. Jeg skal så gemme den fil på serveren, så jeg ligge den i følgende mappe: ./MinecraftServer/Scriptcraft/plugins/*MitMinecraftNavn*/begynderhus.js
Her skal *MitMinecraftNavn* erstattes med dit minecraft navn.

Nu kan man i minecraft på serveren skrive: `/js refresh()` Så er serveren opdateret med de nyeste funktioner.
Nu kan man skrive `/js begynderhus()` for at kalde den funktion. Hvis du har kaldt din funktion noget andet skal du selvfølgelig bruge det navn i stedet.

### Minecraft Blocks
Dette er en liste over minecraft blocks. Det bruges blandt andet af drone.

![Minecraft Data Values][img_dv]
[img_dv]: https://github.com/ArvidLangsoe/MineCraft-WorkShop-CP/blob/master/source/ypgpm_datavalues.png "All minecraft blocks."

