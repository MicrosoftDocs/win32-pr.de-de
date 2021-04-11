---
description: Glossarseite
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 8e9b45de-c81b-4324-b00b-b11ee6749920
title: Glossar für Windows-Suche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ac0620f4c85c43aac6d41300e16e3e5a8dd037f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128500"
---
# <a name="windows-search-glossary"></a>Glossar für Windows-Suche

## <a name=""></a>\#

**OSD-Datei**

OpenSearch-Deskriptordatei.

**OSDX-Datei**

Eine OpenSearch-Beschreibungs-XML-Datei, die die verfügbaren Serververbindungen und Ergebnis Formate für eine bestimmte webbasierte Datenquelle beschreibt. Sie wird für die Interaktion mit der Windows-Shell verwendet. Siehe auch: OpenSearch-Deskriptor.

## <a name="a"></a>A

**Erweiterte Abfrage Syntax (AQS)**

Die Standard Abfrage Syntax, die von Windows Search verwendet wird, um den Index abzufragen und Suchparameter zu verfeinern und einzuschränken. AQS ist hauptsächlich für Benutzer sichtbar und kann von Benutzern verwendet werden, um AQS-Abfragen zu erstellen. Sie können aber auch Programm gesteuert verwendet werden. Siehe auch: natürliche Abfrage Syntax (NQS).

**AQS**

Siehe Definition für: Erweiterte Abfrage Syntax (AQS).

**Anwalt**

Eine Zuordnung einer Dateinamenerweiterung (z. b.. MP3) oder eines Protokolls (z. b. http) zu einem programmatischen Bezeichner (ProgID). Diese Zuordnung wird in der Registrierung als benutzerspezifische Einstellung mit einem Fallback pro Computer gespeichert. Anwendungen, die am Standardprogramm System teilnehmen, legen die Zuordnungs Zuordnung für die Dateinamenerweiterung oder das Protokoll fest, um auf die ProgID-Schlüssel zu verweisen, die Sie besitzen.

**Zuordnungs Array**

Eine geordnete Liste der Registrierungs Speicherorte, die zum Speichern von Informationen über einen Elementtyp verwendet werden, einschließlich Handler, Verben und anderen Attributen, wie z. b. Symbol und Anzeige Name des Typs. Beispielsweise verfügt eine JPG-Datei über das folgende Zuordnungs Array auf einem standardmäßigen Windows-System: "HKCR \\ jpgfile", "HKCR \\ systemfileassociations \\ . jpg", "HKCR \\ systemfileassociation \\ Image", "HKCR \\ \* ", "HKCR \\ AllFilesystemObjects".

**Atom**

Ein XML-Schema, das für Webfeeds und Inhalts Verteilung verwendet wird und als Alternative zu "Really Simple Syndikation (RSS)" entwickelt wurde. Das Atom-Syndizierungs Format wurde als von IETF vorgeschlagene Standard in RFC 4287 veröffentlicht.

## <a name="b"></a>B

**bind**

Zum Laden oder Zuordnen von Code mit Daten. Beispielsweise kann ein Handler einer shelldatenquelle zugeordnet werden.

**lichere**

Eine Anforderung in einer Suchabfrage für eine Spalte in einem zurückgegebenen Rowset. Die Bindung gibt eine Eigenschaft an, die in den Suchergebnissen enthalten sein soll.

**bookmark**

Ein Indikator, der eine Zeile innerhalb einer Gruppe von Zeilen eindeutig identifiziert.

## <a name="c"></a>C

**Kanonischer Name**

Der eindeutige Name einer Ressource. Kanonisch bedeutet "gemäß den Regeln". Siehe auch: kanonischer Verb Name.

**Kanonischer Verb Name**

Ein sprach neutraler Name, der unabhängig von der lokalisierten Zeichenfolge in der Benutzeroberfläche Programm gesteuert verwendet werden kann, um auf ein Verb zu verweisen. Siehe auch: kanonischer Name, Verb.

**catalog**

Die Organisationseinheit der obersten Ebene in Windows Search. Ein Katalog stellt einen Satz indizierter Dokumente dar, die abgefragt werden können. Ein Katalog besteht aus einer Eigenschaften Tabelle mit dem Text oder Wert und dem entsprechenden Speicherort, der in Spalten der Tabelle gespeichert ist. Jede Zeile der Tabelle entspricht einem separaten Dokument im Geltungsbereich des Katalogs, und jede Spalte der Tabelle entspricht einer Eigenschaft. Siehe auch: Index, Windows Search-Dienst.

**category**

Eine hierarchische Gruppierung von Zeilen. Beispielsweise kann ein Abfrageergebnis, das Autoren-und Titel Spalten enthält, basierend auf dem Autor kategorisiert werden. In diesem Beispiel stellt jede Gruppe von Zeilen, die den gleichen Wert für Author enthält, eine Kategorie dar.

**geschlagen**

Eine Auflistung von Zeilen innerhalb einer Reihe von Zeilen. Siehe auch: Catalog, Category.

**column**

Der Container für einen einzelnen Typ von Informationen in einer Zeile. Spalten werden Eigenschaftsnamen zugeordnet und geben an, welche Eigenschaften für die Befehlsstruktur Elemente der Suchabfrage verwendet werden. Siehe auch: Kategorie.

**Befehlsstruktur**

Eine Kombination aus Einschränkungen, Kategorien und Sortier Reihenfolgen, die für die Suchabfrage angegeben werden. Siehe auch: Kategorie.

**container**

Ein Typ von shellelement, das andere Elemente enthalten kann. Elemente in einem Container werden mithilfe einer shelldatenquelle für den Shellnamespace verfügbar gemacht. Beispiele hierfür sind Ordner, Laufwerke, Netzwerkserver und komprimierte Dateien mit der Dateinamenerweiterung ". zip". Siehe auch: Shell-Datenquelle, Ordner, shellelement.

**content**

Text und Eigenschaften, die einem shellelement oder einer Inhaltsquelle zugeordnet sind, das indiziert werden kann.

**Inhaltsquelle**

Ein Element, auf das der Indexer zugreifen kann. Inhalts Quellen sind über eine URL adressierbar und werden von einem Protokollhandler für den Indexer bereitgestellt. Beispiele hierfür sind: Dateisystem Dateien und-Ordner, Microsoft Outlook-Elemente und-Ordner, Datenbankeinträge und gespeicherte Microsoft SharePoint-Elemente. Eine Inhaltsquelle kann als shellelemente verfügbar gemacht werden, indem eine shelldatenquelle implementiert wird. Siehe auch: Inhalt, shellelement.

**content view (Inhaltsansicht)**

Eine Ansicht in Windows-Explorer (in Windows 7 und höher angeboten), die den relevantesten Inhalt für jedes Element in der Liste basierend auf der Dateinamenerweiterung oder der Art der Zuordnung anzeigt. In der Inhaltsansicht wird eine Logik zur Größenänderung verwendet, mit der Eigenschaften gelöscht werden, wenn die Fenstergröße abnimmt, um sicherzustellen, dass die kritischsten Eigenschaften weiterhin Platz aufweisen, um klar lesbar Siehe auch: Layoutmuster, Kind, Kind Association.

**Inhalts Ansichtsmodus**

Siehe Definition für: Inhaltsansicht.

**Kontextmenü**

Dieser Begriff wird manchmal verwendet, um das Kontextmenü zu verwenden. Siehe Definition für: Kontextmenü.

**Kontextmenü Handler**

Dieser Begriff wird manchmal verwendet, um den Kontextmenü Handler zu verwenden. Siehe Definition für: Kontextmenü Handler.

**Durchforsten**

Zum Durchlaufen eines Durchforstungs Bereichs, der Inhalts Quellen identifiziert, die Indizierung oder Neuindizierung erfordern.

**Crawl Bereich**

Eine Auflistung von Daten speichern (nach URL identifizierbar), die Inhalt darstellt, den der Indexer durch forken und indiziert.

**Cursor**

Im Kontext des lokalen Indexes ist ein Cursor ein Indikator für das Arbeiten mit einer Zeile oder einem kleinen Zeilen Block zu einem Zeitpunkt in einem Satz von Daten, der in einem Resultset zurückgegeben wird. Nachdem der Cursor auf einer Zeile positioniert wurde, können Vorgänge für diese Zeile oder einen Zeilen Block gestartet werden, beginnend an dieser Position.

## <a name="d"></a>D

**Datenverwaltung, durchsuchen und Mining**

Siehe Definition für: Database Mining Extensions (DMX).

**Datenobjekt Handler**

Ein Handler, der zusätzliche Zwischenablage Formate für das Datenobjekt (IDataObject) eines Elements bereitstellt. Datenobjekte werden in Drag & Drop-und Kopier-/Einfüge Szenarien verwendet.

**Datenquelle**

Dieser Begriff wird manchmal verwendet, um Datenspeicher oder Shell-Datenquelle zu verwenden. Siehe Definition für: Datenspeicher, shelldatenquelle.

**Datenspeicher**

Ein Repository mit Daten. Ein Datenspeicher kann für das shellprogrammierungs Modell als Container mithilfe einer shelldatenquelle verfügbar gemacht werden. Die Elemente in einem Datenspeicher können vom Windows-Suchsystem mithilfe eines Protokoll Handlers indiziert werden.

**Daten Bank Mining-Erweiterungen (DMX)**

Eine Abfragesprache, die zum Erstellen und Bearbeiten von Data Mining verwendet wird. Bei den administrativen Vorlagen für Windows 7, Windows Search und Windows Explorer handelt es sich um ADMX-Dateien, die auf der DMX-Technologie basieren. Die folgenden Vorlagen können über Gruppenrichtlinie angepasst werden: Search. ADMX, Explorer. ADMX und WindowsExplorer. ADMX.

**DMX**

Siehe Definition für: Daten Bank Mining Erweiterungen.

**document**

Ein shellelement, das Text enthält und für das die IFilter-Schnittstelle implementiert werden konnte.

**Drop-Handler**

Ein Handler, der einem bestimmten Elementtyp ermöglicht, Drag & Drop-und Kopier-/Einfüge Szenarien zu unterstützen.

**Ablage Ziel**

Ein Datenobjekt, das in eine Datei gezogen und dort abgelegt wird. Siehe auch: Daten Handler, Drop Handler.

**Dynamisches Verb**

Ein Verb, das vom Zustand eines shellelements oder des Systems abhängig ist. das Element ist Zustands basiert und erfordert, dass der ausführende Code bestimmt, ob das Element angezeigt werden soll. Siehe auch: Kontextmenü Handler, statisches Verb, Verb.

## <a name="e"></a>E

**Explorer-Befehl**

Ein Objekt, das als Schaltfläche in der Nähe des oberen Fensters des Windows-Explorer-Fensters angezeigt werden kann, das Funktionen für Elemente und Container in diesem Fenster bereitstellt. Eine shelldatenquelle stellt die Windows-Explorer-Befehls Objekte für ein bestimmtes Containerelement bereit. Befehle werden manchmal als Verben verwendet.

## <a name="f"></a>F

**Verbund Suche**

Ein Erweiterbarkeits Modell, das das Durchsuchen von Daten speichern und das darstellen der Ergebnisse als shellelemente in Windows-Explorer ermöglicht. Siehe auch: Anbieter für Verbund Suche, Suchconnector, OpenSearch-Deskriptor, OpenSearch-Standard.

**Connector für Verbund Suche**

Siehe Definition für: Suchconnector.

**Anbieter für Verbund Suche**

Ein von einem Datenspeicher implementierter Webdienst, der die von Windows 7 verwendeten Protokolle unterstützt, sodass Windows 7 und spätere Versionen diesen Datenspeicher Remote durchsuchen können. Siehe auch: OpenSearch-Deskriptor, OpenSearch-Standard.

**Datei Zuordnung**

Siehe Definition für: Dateityp Zuordnung.

**Dateiformat**

Ein Format für Daten, die in einer Datei gespeichert sind, die über eine dokumentierte Format Spezifikation verfügt. Beispiele hierfür sind OLE DOCFILE, OPC, XML, zip und andere bekannte Datei Formatspezifikationen. Dateityp-Ersteller verwenden im Allgemeinen ein vorhandenes Dateiformat als Grundlage für einen neuen Dateityp. Ein Dateiformat kann einfach eine Definition sein, die nicht als Dateityp instanziiert wird.

**Dateiformat Handler**

Dieser Begriff ist ein Synonym für den Dateityp Handler. Siehe Definition für: Dateityp Handler.

**Dateinamenerweiterung**

Siehe Definition für: Dateinamenerweiterung.

**Dateinamenerweiterung**

Der primäre Indikator eines Dateityps für Dateisystem Elemente, ist der Teil des Datei namens, der auf den letzten Punkt folgt. Die Dateinamenerweiterung darf keine Leerzeichen oder nicht-ASCII-Zeichen enthalten und gilt nur für Dateien (nicht für Ordner). Dateinamen Erweiterungen werden mithilfe einer Vergleichsfunktion verglichen, bei der es sich nicht um groß-oder Kleinschreibung handelt. Siehe auch: Dateiformat, Dateityp.

**Dateityp**

Ein bestimmter Dateiname-Erweiterungs Wert, wie z. b. ". htm" oder ". jpg", der eine Klasse von Dateien definiert, die denselben Typ aufweisen und über einen gemeinsamen Satz von Zuordnungen verfügen. Siehe auch: Kind, Dateityp Zuordnung.

**Dateitypzuordnung**

Für eine bestimmte Dateinamenerweiterung werden die Zuordnungs Elemente, die angeben, wo Handler und andere Attribute registriert werden können, definiert. Siehe auch: Zuordnungs Array, Dateityp.

**Dateityp Anpassung**

Eine Zuordnung, mit der Shell anpassen kann, wie Shell einen Dateityp behandelt. Dateityp Anpassungen umfassen Folgendes: Angeben der Anwendung, die zum Öffnen der Datei beim Doppelklicken verwendet wurde, Hinzufügen von Befehlen zum Kontextmenü für einen Dateityp, Angeben eines benutzerdefinierten Symbols, Angeben eines MIME-Inhaltstyps, der einem Dateityp zugeordnet werden soll, Angeben eines erkannten Typs und Angeben einer oder mehrerer Anwendungen, die mit dem Dateityp verknüpft sind Siehe auch: wahrnehmvedtype.

**Dateityp Handler**

Ein für einen Dateityp registrierter Handler. Siehe auch: Handler.

**filter**

Eine Implementierung der IFilter-Schnittstelle. Er öffnet Dateien eines bestimmten Dateityps und filtert Eigenschaften und Textabschnitte für den Indexer. Filter sind Dateitypen zugeordnet, die durch Dateinamen Erweiterungen, MIME-Typen oder Klassen Bezeichner (CLSIDs) bezeichnet werden. Obwohl ein Filter mehrere Dateitypen verarbeiten kann, kann jeder Dateityp nur mit einem einzigen Filter verwendet werden.

**Pfalz**

Siehe Definition für: Container.

## <a name="h"></a>H

**lers**

Ein COM-Objekt, das Funktionen für ein shellelement bereitstellt. Die meisten shelldatenquellen bieten ein erweiterbares System zum Binden von Handlern an Elemente. Beispielsweise verwendet der Dateisystem Ordner das Zuordnungs System, um die Handler für einen bestimmten Dateityp zu suchen. Siehe auch: Datei Zuordnung, Dateityp, Dateityp Anpassung.

## <a name="i"></a>I

**Symbol Handler**

Ein Handler, der die zum Generieren und Zwischenspeichern eines Symbols für ein Element benötigten Informationen bereitstellt. Der Dateisystem-Datenspeicher unterstützt das Laden eines Symbol Handlers für ein Element auf der Grundlage des Dateityps, sodass dieser Handler ein Symbol bereitstellen kann, das für alle Instanzen dieses Dateityps verwendet wird.

**Index**

n. Ein Katalog, in dem der Inhalt und die Eigenschaften von shellelementen gespeichert werden, um schnelle Suchvorgänge zu ermöglichen. Siehe auch: Catalog, Indexer, Indizierung, invertierter Index. v. Um auf Inhalts Quellen zuzugreifen, Filtern Sie die Quellen nach Inhalt und Eigenschaften, und fügen Sie die extrahierten Werte in den Index (für Text) und den Windows Search-Eigenschaften Speicher (für Eigenschaften) ein. Siehe auch: Inhaltsquelle, Index, Indexer, invertierter Index.

**Indexer**

Eine Anwendung, die die Indizierung indiziert oder koordiniert. Siehe auch: Index, Indizierung, invertierter Index.

**Infotipp-Handler**

Ein Handler, der Popup Text bereitstellt, wenn der Benutzer mit dem Mauszeiger auf ein Benutzeroberflächen Objekt zeigt.

**umgekehrter Index**

Eine persistente Struktur, die den Inhalt enthält, der von der Windows-Suche aus Dateien entnommen wurde. Der Text wird in einen Index organisiert, der aus einem Wort in einer Eigenschaft einer Liste der Dokumente und Speicherorte innerhalb eines Dokuments zugeordnet ist, die dieses Wort enthalten. Daher ist ein invertierter Index der umgekehrte Vorgang des Extrahierens von Text und Eigenschaften aus dem Dokument und dem Einfügen in den Indexer. Siehe auch: Index, Indexer, Indizierung.

**item**

Siehe Definition für: shellelement.

**Item-Klasse**

Siehe Definition für: Dateityp.

## <a name="k"></a>K

**Kind**

Eine Eigenschaft, die einen benutzerfreundlichen Namen bereitstellt und einer Liste von Eigenschaften und einem Layoutmuster zugeordnet werden kann. Art wurde in Windows Vista eingeführt, um einen benutzerfreundlicheren Begriff "Dateityp" zu lesen, und er wurde als mehrwertige Zeichen folgen Eigenschaft (kanonische Zeichen folgen Werte) definiert. Daher können Sie einen "Audiotext"-oder "Link; Dokument"-Wert haben. Einige benutzerfreundliche Arten von Namen sind bereits Eigenschaften und layoutmustern zugeordnet. Beispielsweise werden Elementen, die mit "Kind. Picture" verknüpft sind, und Elementen, die mit Kind.Doc-Ereignis verknüpft sind, andere Eigenschaften angezeigt, auch wenn Sie sich in derselben Ansicht befinden Jede Elementart kann einem von vier eindeutigen layoutmustern zugeordnet werden, die die Anzahl der Eigenschaften definieren, die für die einzelnen Elemente und deren Layout angezeigt werden. Siehe auch: Kind Association, Content View, Layout Pattern.

**Kind-Zuordnung**

Eine Eigenschaft im Eigenschaften System namens System. Kind, die bestimmt, welche UX-Vorlagen für eine Datei angezeigt werden. Diese Eigenschaft stellt auch einen benutzerfreundlichen Namen für den Typ des Elements bereit und ist mit der Dateinamenerweiterung verknüpft. Siehe auch: Kind.

## <a name="l"></a>L

**Layoutmuster**

Eine von mehreren Anordnungen zum Anzeigen von Eigenschaften. Wenn Sie in Windows 7 und höher einen neuen Dateityp registrieren, können Sie die Inhaltsansicht verwenden, um eine benutzerdefinierte Eigenschaften Liste und ein Layoutmuster für den Dateityp zu registrieren. Sie können aus vier unterschiedlichen layoutmustern wählen: Alpha (für Dokument Suchergebnisse, die Code Ausschnitte enthalten), Beta (für e-Mail-Suchergebnisse mit Code Ausschnitten), Gamma (ähnlich wie Alpha, aber mit einem zweizeiligen Layout anstelle von vier) und Delta (für die Anzeige zahlreicher kürzerer Eigenschaften, z. b. mit Musik und Bildern). Siehe auch: Inhaltsansicht, Kind, Kind Association.

## <a name="m"></a>M

**Metadatenhandler**

Dieser Begriff wird manchmal verwendet, um den Eigenschafts Handler zu verwenden. Siehe Definition für: Eigenschaften Handler.

## <a name="n"></a>N

**Namespace Erweiterung**

Siehe Definition für: shelldatenquelle.

**Namespace-Walk**

Ein Hilfsprozess, der den Namespace eines Containers oder einer Gruppe von Containern durchläuft, wobei jedes Element ermittelt und ggf. eine beliebige Aufgabe durchgeführt wird. Die inamespacewalk-Schnittstelle kann zum Durchlaufen eines beliebigen Teils des Windows Explorer-Namespace oder zum Ermitteln der Elemente verwendet werden, auf die von einem Datenobjekt oder einer Sicht verwiesen wird. Container Verben (z. b. "Play" in Artists-Containern) durchlaufen den Namespace und ermitteln die Elemente.

**Abfrage in natürlicher Sprache**

Siehe Definition für: natürliche Abfrage Syntax (NQS).

**Natürliche Abfrage Syntax (NQS)**

Eine Abfrage Syntax, die einfacher als AQS ist und mehr wie die menschliche Sprache aussieht. NQS kann von Windows Search verwendet werden, um den Index abzufragen, wenn NQS anstelle der standardmäßigen AQS ausgewählt wird. Siehe auch: Erweiterte Abfrage Syntax (AQS).

**Füll Wort**

Ein Wort, das von Windows Search ignoriert wird, wenn es in den für die Suchabfrage angegebenen Einschränkungen vorhanden ist, da es wenig diskriminierenden Wert hat. Beispiele hierfür sind "and" und "The".

**NQS**

Siehe Definition für: natürliche Abfrage Syntax (NQS).

## <a name="o"></a>O

**Objekt Verknüpfungs-und Einbettungs Datenbank (OLE DB)**

Ein Standardsatz von Schnittstellen, der heterogenen Zugriff auf verschiedenartige Informationsquellen bietet, z. b. Dateisysteme, e-Mail-Ordner und Datenbanken.

**OLE DB**

Siehe Definition für: Objekt Verknüpfungs-und Einbettungs Datenbank.

**OpenSearch-Deskriptor**

Eine XML-Datei, die die verfügbaren Serververbindungen und Ergebnis Formate für eine bestimmte webbasierte Datenquelle beschreibt. Diese Datei enthält eine oder mehrere URL-Vorlagen und verwendet bei der Interaktion mit der Windows-Shell die Dateinamenerweiterung. OSDX. Eine OpenSearch-Beschreibung wird manchmal auch als Suchconnector bezeichnet, obwohl Sie nur der Beschreibungs Teil eines Verbindungs-Connector ist. Siehe auch: Suchconnector.

**OpenSearch-Standard**

Eine Auflistung von einfachen Formaten und Protokollen, die für die Freigabe von Suchergebnissen verwendet werden. Weitere Informationen finden Sie auf der OpenSearch-Website ( https://github.com/dewitt/opensearch) .

## <a name="p"></a>P

**Wahrnehmungstyp**

Eine breite Kategorie von Dateiformat Typen. "Wahrnehmvedtype" wurde in Windows XP eingeführt und unterstützt eine begrenzte Anzahl bekannter Dateitypen (Beispiele sind Bild-, Text-, Audio-und komprimierte Dateitypen). Dateitypen, in der Regel öffentliche Dateitypen, können auch über einen wahrgenommenen Typ verfügen. Beispielsweise sind die Image Dateitypen. BMP,. png,. jpg und. gif ebenfalls den wahrgenommenen Typ Image. Auf der Programmier Ebene wird "wahrvedtype" als ganze Zahl ausgedrückt. Da es Code gibt, der "Kind" und "wahrnehmvedtype" verwendet, müssen Besitzer von Dateiformaten beide registrieren. Beispielsweise ist "Play All" von "wahrnehmvedtype" abhängig. Siehe auch: Dateityp.

**Vorschau Handler**

Ein Handler, der schnell eine schreibgeschützte, vereinfachte Ansicht des shellelements erstellt, das im Vorschaubereich von Windows-Explorer angezeigt werden soll.

**Vorschau**

Dieser Begriff wird manchmal verwendet, um einen Vorschau Handler zu verwenden. Siehe Definition für: Vorschau Handler.

**Eigenschaften Handler**

Ein Handler, der in einer Datei gespeicherte Daten in ein strukturiertes Schema übersetzt, das von erkannt wird und auf das von Windows-Explorer, Windows Search und anderen Anwendungen zugegriffen werden kann. Diese Systeme können dann mit dem Eigenschaften Handler interagieren, um Eigenschaften in die Datei zu schreiben und diese zu lesen. Zu den übersetzten Daten zählen Detailansicht, Infotipps, Detailbereich, Eigenschaften Seiten usw. Jeder Eigenschaften Handler ist einem bestimmten Dateityp zugeordnet, der durch die Dateinamenerweiterung gekennzeichnet ist. Siehe auch: Eigenschaften System.

**Eigenschaften Blatt Handler**

Ein Handler, der zum Erstellen benutzerdefinierter Eigenschaften Blätter mit UI-Bildern und Steuerelementen verwendet wird, die eine benutzerdefinierte Interaktion mit einem Dateityp ermöglichen.

**Eigenschaften System**

Ein erweiterbares Lese-/Schreibsystem von Daten Definitionen, das Eigenschaften verwendet, die als Name-Wert-Paare implementiert werden. Siehe auch: Eigenschaften Handler, shellelement.

**Eigenschafts Wert**

Ein Wert, der einem Eigenschaftsnamen für ein shellelement zugeordnet ist. Beispielsweise sind "Author", "size" und "Date Taken" Eigenschaften. Eigenschaftswerte werden als PROPVARIANT-Struktur ausgedrückt.

**Protokollhandler**

Ein Handler, der auf Inhalts Quellen zugreift und ein iurlaccessor-Objekt für ein angegebenes Protokoll und eine URL bereitstellt. Protokollhandler erweitern die Windows-Suchfunktionen und stellen möglicherweise Änderungs Benachrichtigungen für Indexer bereit. Zum Indizieren bestimmter Typen von Daten speichern sind unterschiedliche Protokollhandler erforderlich. Zum Bereitstellen eines angemessenen Benutzer Erlebnisses müssen Sie zusätzlich zur Implementierung des Protokoll Handlers auch eine Shell-Datenquelle für den Datenspeicher bereitstellen. Der Protokollhandler macht die Elemente im Datenspeicher für den Indexer verfügbar, während die shelldatenquelle die Elemente im Datenspeicher für die Shell verfügbar macht.

## <a name="r"></a>R

**Geschwin**

Eine Bedingung, die eine Datei erfüllen muss, um in die von Windows Search zurückgegebenen Suchergebnisse aufgenommen zu werden.

**row**

Die Spalten, die die Eigenschaftswerte enthalten, die ein einzelnes Ergebnis aus dem Satz von-Objekten beschreiben, der den in einer Suchabfrage angegebenen Einschränkungen entspricht.

**Rowset**

Eine Reihe von Zeilen, die in den Suchergebnissen zurückgegeben werden.

## <a name="s"></a>E

**Connector suchen**

Eine XML-Datei, die Informationen zu einem Datenspeicher enthält. Suchconnectors werden für die Verbund Suche bereitgestellt.

**Consumer durchsuchen**

Eine Komponente oder Anwendung, die den Index abfragt.

**Verbund suchen**

Siehe Definition für: Verbund-Suchanbieter.

**Suchanbieter**

Eine Komponente oder Anwendung, die Daten für die Windows-Suche bereitstellt.

**Suchbereich**

Dieser Begriff wird manchmal verwendet, um den Crawl Bereich zu Mean. Siehe Definition für: Crawl Bereich.

**Shelldatenquelle**

Eine Komponente, die verwendet wird, um den Shellnamespace zu erweitern und Elemente in einem Datenspeicher verfügbar zu machen. In der Vergangenheit wurde die shelldatenquelle als Shell-Namespace Erweiterung bezeichnet. Siehe auch: Container, Handler, shellelement.

**Shellerweiterung**

Dieser Begriff wird manchmal verwendet, um den Dateityp Handler zu verwenden. Siehe Definition für: Dateityp Handler.

**Shellerweiterungs Handler**

Dieser Begriff wird manchmal verwendet, um den Dateityp Handler zu verwenden. Siehe Definition für: Dateityp Handler.

**Shellhandler**

Dieser Begriff wird manchmal verwendet, um den Dateityp Handler zu verwenden. Siehe Definition für: Dateityp Handler.

**Shellelement**

Ein einzelnes Inhalts Element. Einige shellelemente sind Inhalts Quellen, andere hingegen nicht. Ein Ordner ist eine Inhaltsquelle, z. b. eine JPG-Datei. Dateityp Handler machen shellelemente verfügbar. In manchen Kontexten wird "Item" verwendet, um Container von nicht Containern zu unterscheiden. Siehe auch: Container, Inhaltsquelle, Dateityp Handler.

**Shell-Namespace Erweiterung**

Dieser Begriff wird manchmal zum Mean der shelldatenquelle verwendet. Siehe Definition für: shelldatenquelle.

**Kontextmenü**

Eine Benutzeroberfläche, die verwendet wird, um eine Auflistung von Verben darzustellen, die einem Benutzeroberflächen Element zugeordnet sind, z. b. eine Datei oder ein Ordner.

**Kontextmenü Handler**

Ein Handler, der Verben für ein Element oder Elemente hinzufügt. Diese Verben werden in der Regel in einem Kontextmenü angezeigt. Siehe auch: Kontextmenü.

**statisches Verb**

Ein Verb, das für ein shellelement gilt, ohne den aktuellen Zustand eines Elements oder Systems überprüfen zu müssen. Ein statisches Verb basiert auf einer statischen Registrierung der zugeordneten Elemente eines Elements und ändert sich nicht.

## <a name="t"></a>T

**Miniatur Ansichts Handler**

Ein Handler, der ein statisches Bild bereitstellt, das ein shellelement darstellen soll.

**Miniatur Ansichts Anbieter**

Dieser Begriff wird manchmal verwendet, um den Miniatur Ansichts Handler zu verwenden. Siehe Definition für: Miniatur Ansichts Handler.

## <a name="u"></a>U

**URL-Vorlage**

Eine URL-basierte Verbindungs Zeichenfolge, die zum Abfragen eines Webservers für Suchergebnisse verwendet wird. Die Vorlage sieht wie eine URL aus, enthält jedoch mehrere Platzhalter Werte (z. b. {searchTerms}), die der Client durch Daten zu den Ergebnissen ersetzen muss, die er abrufen möchte. Die Definition von URL-Vorlagen ist entscheidend für die Implementierung der Verbund Suche und der OpenSearch-Standards.

**benutzerfreundlicher Name der Art**

Siehe Definition für: Kind.

## <a name="v"></a>V

**Verb**

Eine einzelne Aktion, die von einem shellelement aufgerufen werden kann. Beispiele hierfür sind Open und Print. Verben werden manchmal als Befehle oder Aufgaben bezeichnet. Siehe auch: Dynamisches Verb, Kontextmenü Handler, statisches Verb.

**Verb Handler**

Dieser Begriff wird manchmal verwendet, um den Kontextmenü Handler zu verwenden. Siehe Definition für: Kontextmenü Handler.

## <a name="w"></a>W

**Promenade**

Siehe Definition für: Namespace-Exemplarische Vorgehensweise.

**Windows-Suche**

Siehe Definition für: Windows Search-Dienst.

**Eigenschaften Speicher für Windows-Suche**

Der Cache der Eigenschaftswerte, die in der Implementierung des Windows Search-Dienstanbieter verwendet werden. Diese Eigenschaftswerte können mithilfe des Windows Search-OLE DB Anbieters Programm gesteuert abgefragt werden. Der Windows Search-Eigenschaften Speicher sammelt und speichert Eigenschaften, die von Filter Handlern oder Eigenschaften Handlern ausgegeben werden, wenn ein Element wie ein Word-Dokument indiziert wird. Dieser Speicher wird verworfen und neu erstellt, wenn der Index neu erstellt wird.

**Windows Search-Dienst**

Bezieht sich auf Windows Search 3,0 und höher. Dieser Dienst analysiert eine Reihe von Dokumenten, extrahiert nützliche Informationen und organisiert dann die extrahierten Informationen, sodass die Eigenschaften dieser Dokumente als Reaktion auf Abfragen effizient zurückgegeben werden können. Siehe auch: catalog.
