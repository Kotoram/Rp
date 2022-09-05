## Základné informácie:    

Tento game design dokument opisuje detaily pre strategickú hru "???".  
Hra je hraná ťahovým systémom, kde sa striedajú ťahy hráča a AI.  
Súboj prebieha taktiež ťahovým systémom v novom okne pri strete hráča s agresívnou jednotkou.  
Hráč si pred začiatkom hry môže vybrať typ rasy za ktorú chce hrať.  
V hre sa nachádzajú 4 rasy.  
Hráč aj AI začína s 1 mestom a s 1 hrdinom.  

## Cieľ hry:  

-Poraziť všetkých protivníkov na vytvorenej mape.  

## Schopnosti používateľa ktorý chce vyhrať hru:  
- Používanie myši  
- Strategické myslenie   
- Spravovanie surovín  

## Podmienky prehry:   
-Strata všetkých miest a hrdinov hráča.  

## Ovládanie:  
- Pohyb hrdinu po mape: Myš   
- Pohyb jednotiek počas súboja: Myš  
- Nákup v meste: Myš  

## Opis hlavných častí hry:   

# 1. Mapa sveta   

Štvorcová sieť na ktorej sa nachádzajú:  
I. Suroviny (opis v časti Suroviny)  
II. Pohyblivé jednotky hráča alebo AI (Hrdinovia)  
III. Neutrálne nepohyblivé jednotky - agresívne voči hráčovi aj AI  
IV. Mestá   
V. Špeciálne budovy (opis v časti Špeciálne budovy)  
VI. Prekážky  

Podklad štvorcovej siete môže mať 4 základné typy: Oheň Voda Zem Vzduch (opis v časti Elementy)  

# 2. Okno súboja 

Štvorcová sieť je závislá na podklade mapy sveta na ktorej sa súboj odohráva.  
V okne súboja sa nachádza:  

I. Jednotky (opis v časti Súboj)  
II. Prekážky  
III. Lišta s frontou pohybu jednotiek.  

# 3. Okno Mesta   

Okno v ktorom hráč môže kliknúť na budovu, ktorú chce postaviť, prípadne kliknúť na postavenú budovu, kde môže vykonávať funkciu danej budovy (napríklad nákup jednotiek).  


## Suroviny:   

V hre sa nachádzajú 3 základné typy surovín: Drevo,Kameň,Zlato.  
Drevo a kameň sú suroviny nevyhnutné na stavanie budov v meste.  
Zlato je surovina nevyhnutná na nákup jednotiek a prípadné stavanie budov v meste.  
Suroviny sa dajú nájsť náhodne na mape sveta, alebo ich hráč môže získať z dolov, ktoré sú vytvorené na mape sveta.  
Zlato je možné získať aj zo súboja s protivníkom.  

##  Elementy:    

Pri vytváraní hry je možné vytvoriť plochu mapy pohybu, vzhľadom na potreby hry.  
Plocha môže mať špeciálny efekt na:  
1. Pohyb hrdinov pre jednotlivé rasy (kratší/dlhší pohyb za kolo).  
2. Štatistiky pre jednotlivé rasy (Poškodenie,Životy,...).  
3. Špeciálne efekty pre jednotlivé rasy.  
- Jednotlivé efekty bude možné zvoliť pri vytváraní rôzneho podkladu.  

**Príklad využitia:  **

# Oheň   
- Neutrálne jednotky sa počas súboja hýbu častejšie (+1 k pohybu)  
- Jednotky Trpaslíkov majú počas súboja + 10% poškodenia  
- Jednotky Elfov majú počas súboja -10%HP   
- Nemŕtve jednotky nemôžu strieľať  

# Voda   
- Neutrálne jednotky sa počas súboja liečia (+10% maxHP po útoku neutrálnej jednotky)  
- Jednotky Trpaslíkov počas súboja nemôžu strieľať  
- Letecké jednotky Elfov majú počas súboja +10% poškodenia  
- Nemŕtve jednotky majú +10% Poškodenia -10% HP  

# Zem   
- Neutrálne jednotky majú + 20%HP  
- Jednotky Trpaslíkov majú + 10% Brnenia  
- Elfovia majú +25%HP  
- Nemŕtve jednotky majú +30%HP, -možnosť oživovať sa (platí pre špecifický typ jednotky)  

# Vzduch   
- Neutrálne jednotky majú +2 dosah pohybu  
- Strelecké jednotky Trpaslíkov majú +33% poškodenie ale iba 50% šancu zásahu  
- Elfovia majú +5% poškodenie  
- Nemŕtve jednotky majú +5% Poškodenie -10% Brnenie  

Časť “Elementy“ bude do budúcna rozšírená/upravená vzhľadom na balancovanie a rozširovanie hry.     


## Rasy: 

Pri vytváraní hry bude možné zvoliť typy rás ktoré sa v hre budú nachádzať.  
Rasy budú obsahovať rôzne bonusy/postihy, ktoré bude možné zvoliť pri vytváraní rás.  
(Základný prefab „rasa“ z ktorého sa môžu vytvárať ostatné rasy)  

# Príklad: 

Každá rasa má vlastné jednotky a budovy (doplnené v dokumente opisujúcom budovy a jednotky)
Rasy majú rôzne bonusy na Elementálnom podklade.  

# Elfovia    
- +2 k dosahu pohybu na všetkých elementoch okrem ohňa  
- -1 k dosahu pohybu na ohni  
- 15% šanca na oživení časti armády na Vzduch+Voda podklade  
- Rasa ktorá pozostáva z Elfov, lesných zvierat,Lesného draka.  

# Trpaslíci    
- +2 suroviny za kolo v každom dole na podklade Zem/Oheň   
- +1 brnenie pre všetky za kolo pokiaľ sa hráč začal aj skončil kolo na políčku oheň (bonus končí po opustení ohnivých políčok)  
- Rasa ktorá pozostáva z Trpaslíkov,vynálezov trpaslíkov(miniatúrny vrtulník, golemovia,etc.)  

# Nemŕtvy    
- Oživenie 25% všetkých jednotiek po súboji na podklade Zem bonus zvýšený na 50%  
- Lacnejšie jednotky  
- Možnosť v meste zmeniť jednotky iných rás na nemŕtve  
- Rasa ktorá pozostáva z Kostier, Zombíkov, Upírov, Nemŕtveho draka  

# Ľudia   
- Nemajú bonusy ani postihy na elementálnom podklade  
- +500g každé kolo  
- Rasa ktorá pozostáva z ľudí  

Časť “Rasy“ bude do budúcna rozšírená/upravená vzhľadom na balancovanie a rozširovanie hry. 

## Hrdinovia: 

V hre sa nachádzajú 2 typy hrdinov pre každú rasu  
Hrdinovia môžu zvyšovať svoj level.  
Hrdinovia majú 4 základné štatistiky:  

# Základ:   

- Útok (+0.1 poškodenia pre všetky jednotky hrdinu)  
- Obrana (+0.1 brnenia pre všetky jednotky hrdinu)  
- Iniciatíva (+0.01 iniciatívy pre všetky jednotky hrdinu)  
- Magická Obrana (+0.05 magického brnenia pre všetky jednotky hrdinu)  

# Možné rozšírenia:   

- Vytvorenie novej vlastnosti, ktorá upraví jednu z základných schopností jednotiek.  

Hrdinovia majú špeciálne schopnosti/bonusy ktoré odovzdávajú svojej armáde.  

Časť “Hrdinovia“ bude do budúcna rozšírená/upravená vzhľadom na balancovanie a rozširovanie hry. 


## Špeciálne budovy na mape:   

1. Surovinové budovy(drevo,kameň,zlato)  
- Drevo,kameň +2/ťah | zlato +250/ťah  
- Zaberajú 4 políčka na štvorcovej sieti.  
- Ďalšie surovinové budovy budú pridané v budúcnosti pri rozširovaní hry.  
2. Budovy na nákup jednotiek  
- Zaberajú 4 políčka na štvorcovej sieti.  
3. Ďalšie budovy ktoré nebudú v základnej verzii  
- Trh (výmena surovín za zlato)  
- Tréner jednotiek (vylepšenie jednotiek na vyššiu úroveň)  
- Tréner hrdinov (vylepšenie schopnosti hrdinu)  

Časť “Špeciálne budovy na mape“ bude do budúcna rozšírená/upravená vzhľadom na balancovanie a rozširovanie hry. 


## Súboj:   

- Ťahový súboj, jednotky sa striedajú podľa iniciatívy.  
- Postava ktorá je na ťahu má nasledujúce možnosti:  
	1. Pohyb/Pohyb+Útok/Útok (kliknutie pravého tlačidla myši na miesto na mape)  
	2. Použitie zvláštnej schopnosti  
	3. Čakanie  

- Viac informácií v súbore “Súboj“.  

## Jednotky(Špeciálne schopnosti):   

- Určitý typ jednotiek môže používať špeciálne schopnosti.  

# Špeciálne schopnosti ktoré môžu byť pridané jednotke pri vytváraní:   

1. “Self-healing“  
2. Lietanie  
3. Použitie kúzla  
4. Zvýšená obrana na X kôl pre seba alebo inú jednotku  
5. Zvýšený útok na X kôl pre seba alebo inú jednotku  
6. Zvýšená rýchlosť pohybu na X kôl pre seba alebo inú jednotku  

Prípadne vytvoriť vlastnú schopnosť ktorá bude pridaná jednotke.  




## AI:  
  
  
1. AI pre súboj  
2. AI pre pohyb po mape, nákup jednotiek/budov ...

# 1. AI pre súboj:
  
Všetky jednotky obsahujú "level ohrozenia" (klasická jednotka - 1, strelecká jednotka - 2).  
Po začatí súboja sa jednotky AI pohybujú smerom k najbližšej jednotke s najvyšším levelom ohrozenia.  
  
# 2. AI pre pohyb po mape, nákup jednotiek...  
  
  
1. Vytvorenie úloh v danom kole vzhľadom na okolnosti. 
2. Zoradenie úloh podľa stupňa dôležitosti.  
3. Priradenie úloh k časti hry ktorá ich vykoná.  

Podrobnejší opis:  

# *Vytvorenie úloh:* 

Príklady:  
Situácia: Hráčová jednotka sa vyskytla blízko jednotky AI.  

Vytvorená úloha:  

1. Útok na hráčovú jednotku, v prípade, že sila armády hráča < q*sila armády AI (q - konstanta)    
2. Útek od jednotky hráča v prípade, že sila armády hráča > p*sila armády AI (p - konstanta)  

Situácia: Začala hra.  

Vytvorená úloha:

1. Zhromaždiť suroviny na stavbu mesta.  
2. Preskúmať mapu.  
3. Nakúpiť jednotky. 


  
# *Priradenie úloh:*  

  
Preskúmanie mapy - Hrdina  
Stavba budov/Nákup jednotiek  - Mesto  
Kontrola mapy - všeobecný systém  


