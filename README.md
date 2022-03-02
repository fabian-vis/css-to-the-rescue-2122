# Week 1

Ik ben begonnen met het kiezen van een opdracht. Ik heb gekozen voor de vuurwerkshow. Ik denk dat hier genoeg uitdaging ligt aangezien dit mijn eerste keer is dat ik met animaties ga werken. Ik heb na veel proberen eindelijk een css animatie gemaakt die een beetje lijkt op een vuurwerk. Ik heb bij het vuurwerk ook gebruik gemaakt van de ::before selector. *The before selector inserts something before the content of each selected element(s).*

Verder probeerde ik werkend te krijgen dat er een light en dark mode thema in mijn website zit. Dit is nog niet helemaal gelukt omdat ik er niet helemaal uitkwam met de visiblity en het werken met custom properties die trouwens ook helemaal nieuw zijn voor mij

# Week 2

Ik ben verder gegaan met waar ik vorige week met vast zat: De light and dark thema modus. Het is mij uiteindelijk gelukt doormiddel van een checkbox met input:checked dat de background van de website veranderd.
```
input[type="checkbox"]:nth-of-type(2):checked ~ main p {
	animation: laterAarde 1s forwards;
	animation-delay: 5s;
  }
```

Ook is het mij gelukt dat de website zich aanpast aan de thema voorkeur van de gebruiker. Dit is gelukt doormiddel van: media (prefers-color-scheme: light). Hier ben ik persoonlijk heel erg trots op omdat ik dit een gave feature vind.

```
background-color: var(--background-color);
```
```
@media (prefers-color-scheme: light) {
	main {
	  --background-color: #c8cac9;
	}
  
	p:first-of-type {
	  --visibility: visible;
	}
  
	p:last-of-type {
	  --visibility: hidden;
	}
  }
  
  @media (prefers-color-scheme: dark) {
	main {
	  --background-color: #323846;
	}
  
	p:first-of-type {
	  --visibility: hidden;
	}
  
	p:last-of-type {
	  --visibility: visible;
	}
  }
  ```

Ook heb ik een leuke hidden feature toegevoegd. Ik heb een extra checkbox gemaakt en wanneer daar op geklikt wordt komt er een soort atoombom naar beneden en die explodeerd op weergaloze wijze. Hier heb ik gebruik moeten maken van veel verschillende soorten animaties, zoals het aanpassen van de box shadow of het translate en rotaten van een object. Ook heb ik voor het figuur van de atoombom clip-path gebruikt.

