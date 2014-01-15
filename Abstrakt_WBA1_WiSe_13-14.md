Abstrakt WBA1 WiSe 13/13


Grundagen
Web-Basics
Html-Basics
Html-Advanced
CSS-Basics
CSS-Advanced
JavaScript

Aufbau
Code
Ajax
JQuery
JS Frameworks
Testing

Css/Design
Css Frameworks
Responsive Design
Responsive Frameworks
Prototyping

Projektmanagement
Agile
Standards
Gesetze / Solmecke
Barrierefreiheit

Content
SocialMedia/OpenGraph
SEO
Medienformate
CMS










+++ Grundlagen

++ Web-Basics

- Web editieren =wichtig wie Web browsen
- Netzstrukturen bevorzugt, Ausnahme = DNS, Regeln zur Domainvergabe

++ www Säulen 
+ URI → Uniform Resource Locator
HTTPS://hans:geheim@example.org:80/demo/example.php?land=de&stadt=koeln#geschichte
Protokoll|Nutzer|Passwort|Domain|	Port|Pfad|			Query 
+ HTTP → Hypertext Transfer Protocol
Client.Request > Server	…..	Server.Response > Client
- Statuscodes > bestimmen Bedeutung der Antwort
100+ Information, 200+ Erfolg, 300+ Umleitung, 400+ Fehler Client, 500+ Fehler Server
- MIME Type > klassifiziert Daten
application/pdf, audio/mp3, image/jpg, text/html, video/mpeg

+ HTML → Hyperteyt Markup Language
non-linear lesen und navigieren
- textbasierte Auszeichungssprache Strukturierung von Inhalten

- Zeichenkodierung > eindeutige Zuordnung v Schriftzeichen
<head>   <meta http-equiv=“content-type“	content=“text/html; charset=ISO-8859-1“ >
<head>	<meta charset=“UTF-8“> 	</head>
-Umlaute/Spezial > Sonderzeichen wie … &auml;


- Protokoll > ein Satz von Regeln nach denen Daten zw Computern/Prozessen ausgetauscht werden
- Dient > Funktion die ein Rechner andere n im Netzwerk bereitstellt
- Format > standardisierte Beschreibung wie Info in einer Datei gespeichert werden

+Vorteile Webbasierter Anwendungen
Aktualisierbarkeit, Zugängl, Kostenstruktur, Plattforumunabhängig, Redundanzfrei, Personalisierbar, , wenig Medienbrüche, Messbarkeit
+ Nachteile Webbasierter Anwendungen
keine Haptik, HW Voraussetzungwen, Sicherheit / Privatsphäre / Datenschutz, Interaktivität/Geschwindigkeit



Html-Basics

+ Grundgerüst:
<html><head></head><body></body></html>

+ Elemente > Komponenten eines HTML Dokuments
+ Attribute > Modifikatoren v Elementen mittels Wert
 <element attribut=“wert“> </element>

+ Einfache Strukturelemente
- Heading: <h1>, <h2>... <h6> → Struktur & Wichtigkeit
- Paragraph: <p>...<br>...</p> → Textformatierung
- Listen:  unordered: <ul><li>..</li><li>...</li></ul> | ordered: <ol><li>..</li><li>...</li></ol>

+ Block > erzeugen neuen Absatz, weitere HTMl Elem beinhalten, <h>, <p>, <div>
+ Inline > erzeugt keinen neuen Absatz, nur Inline Elem beinhalten, <strong>, </span>, </br>



HTML-Advanced

+ List-Typen
<ol list-style-type=“1/A/a/I/i..“>

+ Tabelle
<table>	<thead><th><<<tr><td>>><tfoot>


+ Form
<form id="kontaktformular" name="kontaktformular" action="danke.html">
    <div>
        <label for="absender">Ihre E-Mail-Adresse:</label>
        <input type="text" id="absender" name="absender">
    </div>
    <div>
        <label for="nachricht">Ihre Nachricht:</label>
        <textarea id="nachricht" name="nachricht" cols="22" rows="5"></textarea>
    </div>
    <div>
        <input type="submit" value="Abschicken">
        <input type="reset" value="Loeschen">
    </div>
</form>


+ html5 Strukturen
<!Doctype html>
<section>
</html>



CSS-Basics

+Display → selektor{ display: block/inline; }
- block mit / Inline ohne Zeilenumbruch


CSS-Advanced

+ Positionierung
- position: top/right/bottom/left
- static		>
- relative	>
- absolute	>
- fixed		>

- float: left/right 		> Ausrichtung des Elements im Dom
- clear: left/right/none/both	> Verhalten des Raumes nach dem Element


+ Pseudoklassen → selektor:pseudoklasse
a:link{}, a:hover{}, a:visited{}, a:active{}, a:focus{}

+ Pseudoelemente → selektor::pseudoelement
- Child			p::first-child{}, p::last-child{}, p::nth-child(n){}
- Zeile, Zeichen		div::first-line{}, span::first-letter{}
- Position		p::before{}, p::after{}	
+ Kombinatoren → selektor<Kombinator>selektor
- Nachfahre:		div p {}
- Kind:			div > p {}
- Nachbar:		div + p {}
- Geschwister:		div ~ p {}

+ Attribut-Selektoren → selektor[<Attribut><Attribut-Selektor>“Wert“]
- <a title=...>, <p title=...>	→ a[title]{}, p[title]{}	→ hat Title
- <a title=“red“...		→ a[title=“red“]	→ exakter Title
- <a title=“red riding hood“...	→ a[title~=“red“]	→ in 'Leerzeichen' Liste
- <p class=“hood-red-riding“...	→ p[class|=“red“]	→ in '-' Liste 
- <p class=“reddishRiding“...	→ p[class^⁼“red“]	→ beginnt mit
- <a class=“hoodred“...		→ a[class$=“red“]	→ endet mit
- <a class=“rideredhood“...	→ a[class*=“red“]	→ enthält irgendwo

+ Transitions

+ Spezifität


++ JavaScript Basics

wertet idR. clientseitig Interaktion aus, Inhalte verändert/nachlädt/generiert
Einsatzbereiche: Folie3????

- Zugriff auf Html Elemente und deren Atribute über DOM / DocumentObjectModel, zb:
 → var element = document.getElementById(''IdvonHtmlElement')
 → element.innerHtml = “Neuer Text ins Element“;
- Bsp Formular Folien S4
var form = document.formularName;
var text = form.getElementsByTagName(''text)[0];

+ Datentypen
Object, Number, String, Boolean, Function, undefined

+ Funktionen
function methodenName(Parameter: obj){
	// machwas mit Objekt
	return etwas;
}
+ Events
OnMouseOver, OnMouseDown / OnMouseUp, OnClick, 


+++Aufbau


++Code


++ Ajax

- Asynchronous JavaScript And Xml
- asynchrone Verbindung zw Client & Server zum 'nachladen' einzener Elemente

+ XmlHttpRequest > stellt Verbindungs Methoden bereit
init Objekt:			var request = new XMLHttpRequest();
init Anfrage:			.open(method<GET, POST>, url, [async<true,false>, user, pw])
senden Anfrage		.send()
responseObjekt		string: .responseText, xml: responseXML
Anfrage Status:		.readyState(), 0..4
Http-Status			.status, HttpStatusCodes zb 200 erfolgreich, 404 Res nicht gefunden
Anfrage Status Änderung	.onReadStateChange = function(){....}

+ JSON
Format zum Informationaustausch zw Server & Client
- Variablen:	{ ''Stadt'': ''Köln'',	''PLZ'': 50672	}			
		→ Zugriff .Stadt
- Arrays:	{ ''Stadt'': ''Köln'',	''Bars'': [''B1000'', ''Barracuda'']  }	
		→ Zugriff .Bars[1]
- Obj		{ ''Buergermeister'': { ''Name'': [ ''Tünnes'' , ''Schael''], ''Beruf'': ''Thekenwärmer''	} }
		→ Zugriff .Buergermeister.Name[1]
- Parser	var json = JSON.parse(StringZuParsen);

+ SOP – Same Origin Policy: erlaubt Scripten im Client nur auf Ressource der aktuellen url zuzugreifen
+ CORS - Cross-Origin Resource Sharing: explizite Einstellung des Script-Ressourcen Zugriffs	
		→ Access-Control-Allow-Origin: <*, null,  url > <Alle, Keine, Spezifisch>
+ Nachteile:	Lesez, Vor/Zurück Funktion im Browser, SEO, Ladezeit ndikator nur mit zT aufwändiger 		expliziter Implementierng möglich
+ Vorteile:	geringeres Datenvolumen, gute Usbaillity → dynamischere UX, plattformunabhängig
		


++ Jquery
freie js Lib zur DOM Manipulation
- Syntax	jquery.(Element).methode()
		$.(css-selektor).methode()


++ JS Frameworks
- Codestrukturen zur Erstellung von Anwendungen in Form von Bibliotheken mit abstrakten und     	konkreten Klassen
- einfache Methoden und Objekte als eine Abstraktionsebene über JavaScript

- Ereignisgesteuert < > Aktionsgesteuert ????

- spezielle Varianten für Mobile Entwicklung da unterschiedliche Funktionen für mobile HW

Vorteile: 
reduziert oft eigene Schreibarbeit, vereinfachen JS, Helferfunktioenn, idR kostenlos/OpenSource, 
Nachteile:
'Wildwuchs' von Dokumentation/ANleitungen/BestPractice, inkompatibel bei Nutzung mehrerer Frameworks



Jquery
Moo
Dojo
Yui
ExtJS

DRAG AND DROP
YES
YES
YES
YES
YES
DOM WRAPPED
YES
NO
YES
YES
YES
FEATURE DETECTION
YES
YES
YES
YES
NO
OFFLINE STORAGE
YES
YES
NO
YES
YES
MOBILE/TABLET SUPPORT (TOUCH EVENTS)
with plugins
YES
YES
YES
YES



++ Testing

Warum?	Fehlerarme, stabile Software
		Fehlerwahrscheinlichkeit steigt mit Komplexität der Software

Was?		Quellcode, Funktion, Laufzeitverhalten, Sicherheit, Bedienbarkeit

Wie?

White-Box
Tester Kenntnissen der inneren Programmstruktur, Testfälle auf innere Programmstruktur, Ziel Quellcode muss Kriterien erfüllen

Black-Box
Tester keine Kenntnisse der inneren Programmstruktur, Testfälle Interaktionsszenarien testen SW Verhalten, Ziel Übereinstimmung des SW Verh mit Specs

Unittest: einzelne Module – Ausgangszustand init, testoperationen durchführen, Vergleich Ist =/!=Soll-Zustand

Validierung: idR automatisiert prüfen des Quellcodes (html, ja, css) auf erfüllen von Standards

Performance Test: Ziel optimierung von Quellcode, Ladezeit, Performance

Usability: Tester: möglichst unerfahrene/naive aus Zielgruppe, Nutzer/Interaktionsfreundlichkeit,
Asynchron: Nutzer- tagebücher, -verhalten digital aufzeichnen, Synchron: Nutzer beobachten, laut denken

Nutzer-Befragung, Logfiles > Zugriffe, Herkunft der User




++ Design/Css


++ css Frameworks

- Fundament für Entwicklung der Gestltung einer Web
- standard CSS Klassen als Entwicklungsbasis
- einheitliche Konvention von Codestruktur
- Css Layout-Grid-Systeme 

++ SASS/SCSS
- Variablen
$varName: Wert;
selektor {	attribut: $varName;	}
- Funktionen
@function golden($size){	@return ceil($size * 0.618);	}
selektor{
	width: golden($div_size);
}


- MIXIN Types → style def mit parameter & include 
@mixin box($size:40px) {
	width: $size;
	height: $size;
}
.box {
	@include box(100px);
	background: #fc0;
}

- Nesting → verschachtelung von styles
nav {
	color: #000;	
	nav ul {
	color:#333;
	}
}

++ Responsive Design

'respondere' → lateinisch: antworten, melden

flexible raster die sihc an Breakpoints orientieren an denen das layout an die HW angepasst wird

'Mobile first': mit kleinestem Gerät beginnen, aufs wesentliche reduzieren
Vorteile: formatvielfalt steigt., mobile wächst, nur eine Website Verison
Nachteile: gestiegener Aufwand, erzwungene Darstellungsweisen

- Media Queries
Css implementierte Abfrage des aktuellen Medientyps zur Anpassung an Bildschirmgröße
	→ Auflösung, Orietierung (Hoch- , Querformat), Eingabemögl  
@media screen and (height:600px){
	//css definitionen überschreiben
}
@media screen and (orientation: landscape) { // css Definitionen }
@media screen and (max-width: 500px){
	//zb Bildgröesse ändern
	img{	width: 80%;	}
}

++ Responsive WebDesign Frameworks / Bootstrap

- sollen Darstellungsanforderungen möglichst aller Endgeräten bedienen
- spaltenbasiertes Layout-Grid
- bedient zuerst mobile Endgeräte
- bietet vorgefertigte dynamische Gestaltungselemente
	→ resp Grafiken/Typo/links, Forms/Eingabe, Navigation, Tabellen

+ Bootstrap Implementierung BSP:
- basiert auf 12 spalten, Spaltendefinition .<div class=“col-md-*“>....
<div class=“row“>
	<div class=“col-md-6>...</div>
	<div class=“col-md-4>...</div>
	<div class=“col-md-2>...</div>
</div>
- responsive Grafiken <img src=“...“ class=“img-responsive“>...
- Grafikoptionen <img class=“<img-rounded, img-circle, img-thumbnail>“...
- Eingabe
<form><input type=“...“ class=“form-control“...
- Schaltflächen Klassen <default, primary, sucess, info, warning, danger, link> zb:
	<button type=“...“ class=“btn btn-default>
- Glyphicons > skalierbare Grafiken, zb: <span class=“glyphiocn glaphicon-star“
- Navigation, zb Tabs
<ul class=“nav nav-tabs“><li><a href=“...“...</li><li a href=“...“>...</ul>



++Prototyping

Prototyp: 
Modell → einfach zu ändern, erweiterbar, ausführbar, weist grundegende Merkmale des Produkts

Nutzen: relevante Specs & Entwicklunsprob untersuchen, Diskussionsbasis, Entscheidungshilfe

+ Arten
explorativ: Anforderungen an UI klären, schnelle Ergebnisse, klare Design Vorstellung
eperimentell: Proof of Cncept, technische Realisierung klären
evolutionär: kontinuierlich, inkrementell Erweitern/Verbessern, Ptyp lauffähig & wird zum Produkt weiterentwickelt

horizontales: testen kompletter Features, wenig genau, Usabillity: Navigation, Platzierung, allg Layout/Design
vertikales: einzelnes Feature, sehr genau, Fet. Vverbessern & an Nutzerbedürfnse anpassen

Vorteile: Anforderungen laufend präzisieren, Senung Risiko Fehlentwicklungen
Nachteile: zusätzl Aufwand/Kosten, verleietet zu ungenauen Specs & Dokumentation

Demonstrationsprototyp: frühe Projektphase, grobe Entwicklungsrichtung
Pilotsysteme: nah an finaler Version, Anwedner sind eingebunden/testen

Paper-Prototyping: frühe Utersuchung v. Usability, schneller Design Iterationen, spart Zeit&Geld
Darstellung: Papier, Storyboard, Wireframes




++ Management


++ Agiles Projektmanagement

Projektplanung gibt es seit Menschen größere Vorhaben gemeinschaftlich umsetzen.
Projekt: zielgerichtetes einmaliges Vorhaben, mit abgestimmten, gelenkten Tätigkeiten mit Anfangs und Endtermin, Berücksichtigung Zeit, Resource, Produktions/Arbeitsbedingungen, Personal, Qualität

- Kontrolle von Termine&Abläufe, Kosten, Ergebnisse 
- nach SMART Regeln: spezifisch, messbar, akzeptiert, realistisch, terminiert	
- Durchführung mit PMS: 

+ agile → flexibel, beweglich
1. Menschen & Iteraktion > Prozesse & Werkzeuge
2. funktionierende SW > umfassende Dokumentation
3. Zusammenarbeit Kunden > ursprünglich Specs
4. eingehen auf Veränderungen > Festhalten an Plan

agile Methoden
- Scrum
+> Product Backlog (n Produkt Verbesserungen) → 1 Sprint Backlog → 24h/30Tage Sprint → inkrementell verbesserte Software
- RapidApplicationDevelopment / RAD
erste Iterationen direkt in Code, inkrementelle Weiterentwicklung, für wenig komplexe Projekte
- Paired Programming
zu Zweit gecodet, Austausch der Rollen/Partner, Ziel: hohe Qualität „2 Augen sehen mehr als 2“


++ Standards	

Standard: Art&Weise einer Durchführung die sich ggüber anderen durchgesetzt hat

Norm: rechtlich anerkannte & durch Normverfahren beschlossene, veröffentlixchte Regel zur Lösung eines Sachverhalts
Normungsstufen: Auswahlnorm, Vornorm, Normentwurf

Konvention: verhalten/Regel wird von einer Gruppe v Menschen durch Konsens eingehalten

WebStandards: W3C, STD, IETF, RFC
- Code vereinfachen, Prod. Kosten senken, größtmögl Lebensdauer eines Web-Dokuments


++ Gesetze

+ Wann Impressum? → kommerzielle Inhalte (Werbung), Umsatz ergal, journalistische Inhalte (oft auch Blogs)
+ Domains (Tippfehler) → Wettbewerbsbehinderung, Verstoß gg ames- Wettberwerbsrecht




++ Barrierefreiheit

Nutzung von (Web) Angeboten / Medien unabhängig von körperlichen Einschränkungen
Klassifizierung: visuell, motorisch, kognitiv, auditiv

visuell:
navigation über tastatur, beschreibende Metadaten, Schriftgrößen skalierbar, erhöhung des kontrasts,      HG & Schriftfarbe umkehren
motorisch:
klare Struktur → nur mit Tastatur/MAus bedienbar, großflächiges Layout 
kognitiv:
leicht versändliche Texte, Nav mit deutliche Symbole, keine Ablenkung

techn Umsetzung:
- tabcodes <a tabindex=“x“...   a:focus { color: klar & deutlich; }
- <img alt=“gute beschreibende texte“ title=“und titel“


++ Content



++  SocialMedia

Medien über die Kommunikation stattfindet, idR inkl Profile, Many-to-Many Kommunikation
Werbung: Anzeige: Text/Bild, Apps,, CPC CostperClick, CPM/TKP CostPerMille TausendKontaktPreis
PemiumMitgliedschaften: Xing

+ Oauth
- Authorisierung mit externem Server



+ APIs
- Access-Api: Zugriff/Authorisierung
- Plugin-Api: Erstellung von Inhalten


+ SocialGraph
ORM Modell v Nutzern, deren Interaktion, Vorlieben


+ 


++ SEO

- inhaltliche & technische Optimierung
Ziele: höhere Positionierung in Suchergebnissen / Reichweite / Umsatz, ggf bessere UX

Suchmaschine: crawlt durchs Web, folgt Links, indexiert/Analysiert Inhalte
Nutzererwartung: für ihn(Zielgruppe) relevanteste Seiten werden agezeigt

klare Seitenstruktur, aussagekräftige Sprache, Content mit Mehrwert/Relevanz
OnPage: optimierung durch Betreiber, in Content/Formatierung... , im Html
OffPage: qulitative Backlings (tauschen/Kataloge/SocialBookmarking)
	Qualifizierung durch: Relevanz, Autorität(PageRank), Vertrauenswürdigkeit



++ Medienformate
<(audio/video) controls autoplay loop>
	<source src=“pfad/datei.format“  type“(audio|video)/Format“>
</(audio|video)>

++ CMS

Benutzerfreundliche Verwaltung von Inhalten
Frontend: template basierte Darstellung von Inhalten, 'Leser/Nutzer'-Interaktion
Backend: Verwaltung Inhalte / Funktionen (Extensions)
Authentifizierung: hierarchisches Berechtigungskonzept / Nutzerrollen

Vorteile: einfache Bearbeitung Inhalte, Erw. Funktionen, MVC
Nachteile: für wenige Inhalte → hoher Aufwand


