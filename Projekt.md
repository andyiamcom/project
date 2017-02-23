**kasutajad:**

isik - projektilooja, soundeng - kas algataja rollis või collaboratori rollis (vähemate õigustega)

grupp/juriidiline keha - selleks võib olla bänd või projektijuhi, soundengineeri firma - sisuliselt samade õigustega nagu isikud

**projektide roll ver1’s:**

projektide loomine, nendesse eventide loomine ja omakorda bändidega sidumine. Kasutajate haldus projektis ja eventides, kasutajatele õiguste määramine (erinevatel kasutajatel on erinevaid huvid ja vaated). 

**olemid**

Projekt - Pealkiri, tahtaeg, asukoht, starred, asukoht, arhiveeritud, autor, 

projekti_kasutajad

projekti_kasutajate_õigused

projekti_eventid - iga projekt on 1 või mitme evendiga seotud.

klassifikaatorid

**olemi seosed**

Bandid - bandid on seotud eventidega, event omakorda projektiga. Ühel evendil on 0...n bandi.

Raider - raider on seotud 0...n eventiga, event omakorda raideriga.

**põhilised sündmused**

Projekti lähenemine - nt. nädal enne projekti algust antakse kasutajale teada, et projekt läheneb 

Projekti algusaeg - nt. projekt omandab uue staatuse "ongoing"

Projekti lõpp - staatus muutub "lõpp". 

**kasutusjuhud (nimi, kasutajad, eesmärgid, ****infovajadused/vaated****, uml+mockupid)**

Projektide otsing, nimekiri

	kõik kasutajad

		Kasutajad saavad näha, mis projektid on temaga endaga seotud. Olgu looja rollis või collaboratori rollis. Võimalus näha eri tüüpi projekte - tähtaja ületanud, tulemas, starred jne. 			

Infovaade: saab projekte näha library view’s. 			Sidebarilt kui projekte filtreerida.

Näide:

1. Kasutaja logib

2. Avab sidebar’i

3. Soovib projekte, mis on temaga seotud ja tulemas ja tähistatud.

4. Sidebar kuvab soovitud projektid

IDEE - võimalus avada sidebarilt tehtud otsingud library view’s. Suurem vaade.

------------------

Projektide arhiveerimine

	Kõik kasutajad

		Kasutajad saavad arhiveerida nendega seotud projekte. See tähendab, et projektid saavad uue oleku - arhiveeritud. Küll aga on arhiveeritud olek igal kasutajal unikaalne - st ühe projekti atribuudid ja nende olek on igal projektiga seotud kasutajal sõltumatud.

			Infovaade: Projekte saab arhiveerida projekti detailvaates. Library vaates, sidebarilt (selekteerides üks või mitu projekti. Hiirega avades kontekstmenüü, andes seal oleku "arhiveeritud" või peale selekteerimist avaneb kasutajaliideses valik “Soovid arhiveerida?”.

IDEE: Kasutajal võiks olla seade profiili all, mis võimaldaks ajaliselt möödunud projekte automaatselt arhiveerida.

Näide:

1. Kasutaja logib

2. Otsib sidebarilt ülesse tähtaja ületanud projektid.

3. Selekteerib projektid

4. Rakendus kuvab "Soovid selekteeritd projektid arhiveerida?" (Seda juhul, kui kõik selekteeritud projektid on tähtaja ületanud. Kui kasvõi üks neist ei ole möödunud, siis rakendus sellist võimalust ei paku. Küll aga saab manuaaselt arhiveerida alati (st. avades kontekstmenüü hiirega).

 

-------------

Projektide tähistamine

kõik kasutajad - projektilooja, soundeng, band

		Iga kasutaja saab temaga seostatud projekti (kas looja või osaline projektis)

 ära märgistada oluliseks (starred). Jällegi, see atribuut on igal kasutajal sõltumatu.

		Infovaated: saab teostada projektide nimekirjas (läbi otsingu), library vaates või projekti detailvaates

Näide:

1. Kasutaja logib

2. Teostab sidebaril otsingu nt nime järgi

3. Otsingutulemusest selekteerib ühe või mitu projekti.

4. Kasutaja klikkab "tähistamise" ikoonil

 

-------------------

IDEE - avalike projektide otsing, nimekiri, vaatamine

kõik kasutajad - projektilooja, soundeng, band

Võimalus otsida avalikke teiste kasutajate evente. Vajalik näiteks, et band (või miks mitte sound engineer) saaks otsida projekti, millega liituda ja olla üks artist (seda ver1’s kindlasti veel ei oleks). Või sound engineer, kes otsib endale tööd mingil eventil. (põhimõtteliselt, aga jällegi, otseselt sound engineer ise liituda projektiga ei saaks). Mõte pigem, et on olemas "public" atribuut projektidel, mis võimaldab otsida eraldi vaates avalikke projekte nt kuupäeva, asukoha, esinevate bändide järgi.

Avades projekti, siis detailvaade sisaldab üldist infot - kes millal esineb, kus kohas, mis järjekorras jne

Infovaade: see toimub eraldi vaates "avalike projektide otsing". Sidebarilt ja library vaates on kasutaja enda projektid, mis võivad aga ei pruugi olla avalikud

Näide:

1. Kasutaja logib

2. Avab vaate "avalike projektide otsing"

3. Sisestab kuupäeva ja asukoha.

4. Otsingutulemusest valib projekti ja avab selle

5. Näeb projekti detailvaadet

--------------

Projekti loomine

	Iga süsteemi kasutaja

		Kõik kasutajad saavad luua süsteemis projekte. Igal projektil on atribuudid nagu loomise kuupäev, autor, staatus, mis omandavad loomise hetkel uued väärtused. Automaalselt ühe projektiga seotakse üks event. Iga kasutaja saab luua lõppematu arvu projekte.

			Infovaade: projekte luuakse library view’s, lisaks sidebaril saab luua

Näide:

1. Kasutaja logib sisse

2. Library vaates loob uue projekti

3. Avaneb dialoogiaken uue projekti detailide kohta

4. Kasutaja sisestab nime.

5. Süsteemipoolt täidetakse ära loomisekuupäev, autor.

6. Avatakse uue projekti detailvaade

----------------

Projekti muutmine

	kõik kasutajad

		Kõige suuremad võimalused projektiloojal, kellel admin õigused. Rollidel nagu sound engineer, band on piiratumad õigused (vaikmisi, aga admin õigustega kasutaja nt projektijuht saab muuta õiguseid). Admin õigustega kasutaja saab teha kõiki projektiga seotud toiminguid - lisada kasutajaid, muuta õiguseid, lisada raidereid, muuta raidereid jne.

Admin õigustega kasutajale ei kehti ajalised sündmused - nt projekt on alanud. See tähendab, et ta saab muuta projekti iga kell. Teistele kasutajatele kehtivad ajalised piirangud muudatuste osas. Samuti kui mitteadmin kasutaja sooritab muudatusi, siis muudatused, mis puudutavad teisi kasutajaid, saadetakse välja teavitus teistele kasutajatele.

			Infovaade: kõik muudatusi teostatakse detailvaates. Üldiseid muudatusi nagu nimi ja kuupäev saab teostada libraryis ja sidebaril.

Näiteks:

1. Kasutaja logib (mitteadmin õigustega)

2. Library view’s selekteerib ühe projekti (mis pole veel alanud)

3. Avanenud projektivaates (ja selles osas, millele on tal ligipääs) teostab vajalikud muudatused

4. Kui muudatus puudutab teisi kasutajaid (nt. raideri muutus), saadetakse teade teistele collaboratoritele.

5. Collaborator logib süsteemi

6. Kuvatakse teavitused tehtud muudatustest temaga seotud projektides

----------------

Projekti kustutamine

admin õigustega projektilooja

	Projekti saab kustutada admin õigustega projektilooja. Teised kasutajad projekti kustutada ei saa. 

		Infovaade: projekti detailvaates, library views

Näiteks:

1. Kasutaja logib

2. Selekteerib libraryis projekti

3. Avanenud detailvaates kustutab projekti

4. Süsteem küsib kinnitust.

5. Teistele collaboratitele saadetakse teade projekti kustutamisest.

-------

Projekti eventide loomine

admin õigustega kasutaja

	Saab luua evente projekti sees.

		Infovaade: projekti detailvaates

Näiteks:

1. Kasutaja logib

2. Selekteerib projekti library’s

3. Avanenud detailvaates lisab eventid ja nende arvu projekti

-----------------------

Projekti analüüs 

süsteemipoolne		

Süsteem analüüsib, mis on projekti puhul puudu, olemas. Siia hulka ka agregeerivad funktsioonid - eventide arv,  kas on olemas kõikidel eventidel soundengineer, kas kõikidel eventidel on olemas raider jne

			Infovaade: projekti detailvaates selleks eraldi tab, kus kujutatud summaarsed andmed projekti kohta.

-------------------------

Projektile kasutajate määramine

projektilooja algselt, admin õigustega kasutaja

Algselt, kui projekt luuakse, on admin õigused algselt projektiloojal. Projektilooja saab admin õiguseid anda teistele kasutajatele. Admin õigustega kasutaja (algselt projektilooja) saab kutsuda juurde teise kasutajaid.Kasutajate lisamine toimub autocomplete põhjal. Õiguseid saab anda nii projekti kui eventide suhtes üksikult. Õigused puudutavad raiderit, projekti, eventi muuta, kustutada, lugeda. Vastavalt kasutajatüübile (soundengineer, band) määratakse ära ka õigused, mida kasutaja antud projektis teha saab. Kasutajad, kes projektiga seotakse saavad invide’i projektiga ühineda.

Infovaade: projekti detailvaates õiguste tab

Näiteks:

1. Kasutaja logib

2. Selekteerib projekti

3. Avab projekti detailvaate

4. Olles admin õigustega, saab autocomplete põhjal selekteerida kasutajaid. Nt. sisestades "john4@gma" pakub süsteem “[john4@gmail.com](mailto:john4@gmail.com)” kasutajat.

5. Kasutaja selekteerib antud kasutaja ja valib talle rolli. Nt soundengineer. Määrab ära eventide puhul, mis eventidega on seotud.

6. Kasutajale john4 saadetakse emailpõhine invite ühineda projektiga 

7. Kasutaja john4 aktsepteerib invite’i.

8. Esmakordsel kasutamisel registeerib john4 end süsteemis kasutajaks 

9. Projekt on nüüdsest john4’le kättesaadav

Projekti share’imine

Kõik kasutajad

	Võimalus eksportida süsteemist välja projekt (pdf kujul - ver1’s). Sõltuvalt kasutaja õigustest projekis, saab ta eksportida välja seda, mida ta näeb. Nt. projektijuht, kellel on suuremad õigused projekti suhtes, saab eksportida rohkem vs. soundengineer, kel on õigused oma sound engineers vaate suhtes.

		infovaade: projekti detailvaates saab

Näiteks:

1. Kasutaja sisse loginud

2. Avab projekti detailvaate

3. Soovib projekti jagada

4. Selekteerib, mida share’tud projektis on - kas stageplan, kas sound eng view, kas eventid ja nende alam vaated, kas kasutajad ja nende kontaktid

Venue parameetrite määramine

projektilooja või kasutaja, kellel on projekti suhtes admin õigused.

	Saab määrata projektile venue parameetrid. See oleks aluseks raideri vaates stageplani koostamisele.

		Infovaade: projekti detailvaade

------------

**Kas sound-engineer lisatakse juurde nüüd bändipoolt (st. raideri looja poolt)? Või lisatakse juurde projektijuhi poolt?**

**Kui projektijuhil ja raideri loojal on kindlad kasutuslood ala projekti ja raideri loomine, muutmine jne, siis kuidas liidestub sound-engineer?**

Saan aru nii: kasutaja loob konto. Ta isegi ei määra oma rolli. Põhjus - sõltuvalt projektist võib kasutaja roll muutuda. Ta võib olla ühel hetkel nii raideri koostaja kui ka projekti koostaja või miks mitte, ka sound engineer. 

Küll aga projektijuht või raiderikoostaja saab määratleda, kes rakenduse kasutajast on sound-engineer.

---------------

Teiste kasutajate andmete nägemine:

Kui kasutaja loob konto ja täidab ära väljad ala telefon, email jne, siis kasutaja saab valida, kas ta share'b neid teiste kasutajatega või mitte. 

Süsteemi kasutajad (kõik) näevad teiste kasutajate avalikke andmeid. Kui on loodud projekt, siis projekti puhul võiksid kasutajad saada määratleda enda kohta käivaid lisaandmeid (lisatelefon, lisaemail jne), mida näevad ainult selle projekti kasutajad (või projektijuht, kui määratleme projektiloojat kui projektijuhti)Ehk siis kui me jagame mingile kasutajale enda projekti siis peaks nägema kõiki selle kasutaja andmeid. juhul kui talle ei ole midagi kunagi jagatud, siis me ei pea ta profiili andmeid nägema, sest me ei tee temaga koostööd või ei ole seda teinud.

----------

Kasutaja roll sõltub projektist. Regamisel rolli ei määrata. Kasutajad näevad enda primary andmeid. Kasutajad saavad ennast registeerida. Kasutajavad saavad sisselogida. Projektikasutajad näevad teiste kasutajate andmeid. Projektikasutajad saavad määratleda, mis andmeid teised projektikasutajad näevad. By default, teised projektikasutajad näevad teiste andmeid. Andmete nägemist saab piirata. Projektiloojal on projektilooja õigused, raideriloojal raideri kohta olevad õigused. Kasutajate õiguseid saab määratleda. Projektil on kõik õigused projektijuhil. Projektijuht saab määratleda projektikasutajaid ja nende õiguseid. Raideri looja saab määratleda, kes ja kas seda raiderit veel saab muuta/lugeda jne.

Kasutajad saavad määratleda enda andmeid

Kasutajad saavad näha teiste andmeid

Kasutajad saavad kontakteeruda teiste kasutajatega

Kasutajad saavad saata üksteisele sõnumeid?

*Kasutaja saab ennast süsteemist kustudada.*

*Teiste kasutajate otsimine*

*Avalike andmete määramine*

*Süsteemist automaatne väljalogimine/selle seadistus*

*---------------*

Kasutaja on isik.

Kasutajal on roll.

Roll sõltub projektist.

Kasutaja määrab enda kohta käivad isikuandmed. 

Administraator saab kasutajaid…?

Kasutaja saab salasõna muuta

Kasutaja saab määratleda endale keele

kASutaja saab määratleda 2-tasemeline sisselogimise? hiljem

*-----------------*

--------------

**UPDATE:**

**Kui mainrole = "band", siis useril on lisaobjekt “band”, mis on seotud useriga.  “Band” sisaldab helirezissööre, teiste bändiliikmete kirjeldusi, mida nad kasutavad.**

**--------------**

**Kasutajate moodulist: üks asi jäi märkimata. Kui kasutaja teeb endale konto ja valib enda mainrole’iks ‘bänd’, siis selle kasutaja tüübiga tekib uus seotud objekt ‘band’, mis kirjeldab bandiliikmeid jne**

**[1:15]  **

**edasine on see, kas tahame, et bandliige oleks ise eraldi kasutajatüüb (nagu on süsteemis projektilooja, band, soundeng).**

**[1:16]  **

**Ehk - kas bandiliige ise on huvitatud, et ta saab ennast süsteemis registeerida eraldi liikmena. Hetkel arvan, et see pole oluline. Seega kasutajatüübi vajadus puudub hetkel.**

