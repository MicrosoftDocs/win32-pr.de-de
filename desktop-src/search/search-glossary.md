---
description: Glossarseite
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 8e9b45de-c81b-4324-b00b-b11ee6749920
title: Windows Search Glossary
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8efe8bbe07badc7575cc3aba83100814d601bc5c8ebca24961b198950b2e5e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119844650"
---
# <a name="windows-search-glossary"></a>Windows Search Glossary

## <a name=""></a>\#

**OSD-Datei**

OpenSearch Deskriptordatei.

**OSDX-Datei**

Eine OpenSearch XML-Beschreibungsdatei, die verfügbare Serververbindungen und Ergebnisformate für eine bestimmte webbasierte Datenquelle beschreibt. Sie wird für die Interaktion mit der Windows Shell verwendet. Siehe auch: OpenSearch Deskriptor.

## <a name="a"></a>Ein

**Erweiterte Abfragesyntax (AQS)**

Die standardabfragesyntax, die von Windows Search verwendet wird, um den Index abzufragen und Suchparameter zu verfeinern und einzugrenzen. AQS ist in erster Linie für Benutzer zugänglich und kann von Benutzern zum Erstellen von AQS-Abfragen verwendet werden, kann aber auch programmgesteuert verwendet werden. Siehe auch: Natural Query Syntax (NQS).

**Aqs**

Siehe Definition für: Erweiterte Abfragesyntax (Advanced Query Syntax, AQS).

**Verband**

Eine Zuordnung einer Dateinamenerweiterung (z. B. .mp3) oder eines Protokolls (z. B. HTTP) zu einem programmgesteuerten Bezeichner (ProgID). Diese Zuordnung wird in der Registrierung als benutzerspezifische Einstellung mit einem Fallback pro Computer gespeichert. Anwendungen, die am Standardprogrammsystem teilnehmen, legen die Zuordnungszuordnung für die Dateinamenerweiterung oder das Protokoll so fest, dass sie auf die ProgID-Schlüssel verweisen, deren Eigentümer sie sind.

**Zuordnungsarray**

Eine sortierte Liste von Registrierungsspeicherorten, die zum Speichern von Informationen zu einem Elementtyp verwendet werden, einschließlich Handlern, Verben und anderen Attributen wie dem Symbol und dem Anzeigenamen des Typs. Beispielsweise weist eine .jpg-Datei das folgende Zuordnungsarray auf einem Standardsystem Windows auf: "HKCR \\ jpgfile", "HKCR \\ SystemFileAssociations \\.jpg", "HKCR \\ SystemFileAssociations \\ image", "HKCR \\ \* ", "HKCR \\ AllFileSystemObjects".

**Atom**

Ein XML-Schema, das für Webfeeds und die Inhaltsverteilung verwendet wird und als Alternative zu Really Simple Syndication (RSS) entwickelt wurde. Das Atom-Syndication-Format wurde als IETF-vorgeschlagener Standard in RFC 4287 veröffentlicht.

## <a name="b"></a>B

**bind**

Zum Laden oder Zuordnen von Code zu Daten. Beispielsweise kann ein Handler einer Shell-Datenquelle zugeordnet werden.

**Bindung**

Eine Anforderung in einer Suchabfrage für eine Spalte in einem zurückgegebenen Rowset. Die Bindung gibt eine Eigenschaft an, die in die Suchergebnisse aufgenommen werden soll.

**bookmark**

Ein Indikator, der eine Zeile innerhalb einer Gruppe von Zeilen eindeutig identifiziert.

## <a name="c"></a>C

**kanonischer Name**

Der eindeutige Name einer Ressource. Kanonisch bedeutet "gemäß den Regeln". Siehe auch: kanonischer Verbname.

**kanonischer Verbname**

Ein sprachneutraler Name, der programmgesteuert verwendet werden kann, um unabhängig von der lokalisierten Zeichenfolge auf der Benutzeroberfläche auf ein Verb zu verweisen. Siehe auch: kanonischer Name, Verb.

**catalog**

Die höchste Organisationseinheit in Windows Search. Ein Katalog stellt einen Satz indizierter Dokumente dar, die abgefragt werden können. Ein Katalog besteht aus einer Eigenschaftentabelle mit dem Text oder Wert und dem entsprechenden Speicherort, der in Spalten der Tabelle gespeichert ist. Jede Zeile der Tabelle entspricht einem separaten Dokument im Bereich des Katalogs, und jede Spalte der Tabelle entspricht einer -Eigenschaft. Siehe auch: index, Windows Suchdienst.

**category**

Eine hierarchische Gruppierung von Zeilen. Beispielsweise kann ein Abfrageergebnis, das Spalten für Autor und Titel enthält, basierend auf dem Autor kategorisiert werden. In diesem Beispiel stellt jede Gruppe von Zeilen, die den gleichen Wert für author enthält, eine Kategorie dar.

**Kapitel**

Eine Auflistung von Zeilen innerhalb einer Gruppe von Zeilen. Siehe auch: catalog, category.

**column**

Der Container für einen einzelnen Informationstyp in einer Zeile. Spalten werden Eigenschaftennamen zugeordnet und geben an, welche Eigenschaften für die Befehlsstrukturelemente der Suchabfrage verwendet werden. Siehe auch: Kategorie.

**Befehlsstruktur**

Eine Kombination aus Einschränkungen, Kategorien und Sortierreihenfolgen, die für die Suchabfrage angegeben werden. Siehe auch: Kategorie.

**container**

Ein Shellelementtyp, der andere Elemente enthalten kann. Elemente in einem Container werden mithilfe einer Shell-Datenquelle für den Shellnamespace verfügbar gemacht. Beispiele hierfür sind Ordner, Laufwerke, Netzwerkserver und komprimierte Dateien mit einer .zip Dateinamenerweiterung. Siehe auch: Shelldatenquelle, Ordner, Shellelement.

**content**

Text und Eigenschaften, die einem Shellelement oder einer Inhaltsquelle zugeordnet sind, die indiziert werden können.

**Inhaltsquelle**

Ein Element, auf das der Indexer zugreifen kann. Inhaltsquellen können über eine URL adressiert werden und werden dem Indexer von einem Protokollhandler bereitgestellt. Beispiele hierfür sind Dateisystemdateien und -ordner, Microsoft Outlook Elemente und Ordner, Datenbankdatensätze und Gespeicherte Elemente von Microsoft SharePoint. Eine Inhaltsquelle kann als Shellelemente verfügbar gemacht werden, indem eine Shell-Datenquelle implementiert wird. Siehe auch: Inhalt, Shellelement.

**content view (Inhaltsansicht)**

Eine Ansicht im Windows Explorer (angeboten in Windows 7 und höher), die den relevantesten Inhalt für jedes Element in der Liste basierend auf seiner Dateierweiterung oder Kind-Zuordnung anzeigt. Die Inhaltsansicht verwendet eine Größenänderungslogik, die Eigenschaften löscht, wenn die Fenstergröße abnimmt, um sicherzustellen, dass die kritischsten Eigenschaften weiterhin Platz haben, um klar lesbar zu sein. Siehe auch: Layoutmuster, Art, Kind-Zuordnung.

**Inhaltsansichtsmodus**

Siehe Definition für: Inhaltsansicht.

**Kontextmenü**

Dieser Begriff wird manchmal als Kontextmenü verwendet. Siehe Definition für: Kontextmenü.

**Kontextmenühandler**

Dieser Begriff wird manchmal als Kontextmenühandler verwendet. Siehe Definition für: Kontextmenühandler.

**Durchforsten**

Um einen Durchforstungsbereich zu iterieren, identifizieren Sie Inhaltsquellen, die eine Indizierung oder erneute Indizierung erfordern.

**Durchforstungsbereich**

Eine Auflistung von Datenspeichern (durch URL identifizierbar), die Inhalte darstellen, die der Indexer durchforstet und indiziert.

**Cursor**

Im Kontext des lokalen Indexes ist ein Cursor ein Indikator für die Gleichzeitige Arbeit mit einer Zeile oder einem kleinen Zeilenblock in einem Satz von Daten, die in einem Resultset zurückgegeben werden. Nachdem der Cursor in einer Zeile positioniert wurde, können Vorgänge für diese Zeile oder für einen Zeilenblock ausgeführt werden, der an dieser Position beginnt.

## <a name="d"></a>D

**Datenverwaltung, Exploration und Mining**

Siehe Definition für: Database Mining Extensions (DMX).

**Datenobjekthandler**

Ein Handler, der zusätzliche Zwischenablageformate für das Datenobjekt (IDataObject) eines Elements bereitstellt. Datenobjekte werden in Drag & Drop- und Kopier-/Einfügeszenarien verwendet.

**Datenquelle**

Dieser Begriff wird manchmal als Datenspeicher oder Shell-Datenquelle verwendet. Siehe Definition für: Datenspeicher, Shelldatenquelle.

**Datenspeicher**

Ein Repository mit Daten. Ein Datenspeicher kann für das Shell-Programmiermodell als Container mithilfe einer Shell-Datenquelle verfügbar gemacht werden. Die Elemente in einem Datenspeicher können vom Suchsystem mithilfe Windows Protokollhandlers indiziert werden.

**Database Mining Extensions (DMX)**

Eine Abfragesprache, die zum Erstellen und Bearbeiten von Data Mining verwendet wird. Die administrativen Vorlagen für Windows 7, Windows Search und Windows Explorer sind ADMX-Dateien und basieren auf DMX-Technologie. Die folgenden Vorlagen können über die folgenden Gruppenrichtlinie angepasst werden: Search.admx, Explorer.admx und WindowsExplorer.admx.

**Dmx**

Siehe Definition für: Database Mining Extensions.

**document**

Ein Shellelement, das Text enthält und für das die IFilter-Schnittstelle implementiert werden kann.

**Drop-Handler**

Ein Handler, der es einem bestimmten Elementtyp ermöglicht, Drag & Drop- und Kopier-/Einfügeszenarien zu unterstützen.

**Drop-Ziel**

Ein Datenobjekt, das gezogen und in eine Datei gelöscht wird. Siehe auch: Datenhandler, Abbruchhandler.

**Dynamisches Verb**

Ein Verb, das vom Zustand eines Shellelements oder des Systems abhängt; Die Darstellung des Elements ist zustandsbasierte und erfordert, dass der ausgeführte Code bestimmt, ob das Element angezeigt werden soll. Siehe auch: Kontextmenühandler, statisches Verb, Verb.

## <a name="e"></a>E

**Explorer-Befehl**

Ein Objekt, das als Schaltfläche im oberen Bereich des Fensters Windows Explorer angezeigt werden kann, das Funktionen für Elemente und Container in diesem Fenster bietet. Eine Shell-Datenquelle stellt die Windows Explorer-Befehlsobjekte für ein bestimmtes Containerelement. Befehle werden manchmal als Verben verwendet.

## <a name="f"></a>F

**Verbundsuche**

Ein Erweiterbarkeitsmodell, das das Durchsuchen von Datenspeichern und das Darstellen der Ergebnisse als Shellelemente im Windows ermöglicht. Siehe auch: Verbundsuchanbieter, Suchconnector, OpenSearch Deskriptor, OpenSearch Standard.

**Verbundsuchconnector**

Weitere Informationen finden Sie unter Definition for: search connector (Definition für: Suchconnector).

**Verbundsuchanbieter**

Ein von einem Datenspeicher implementierter Webdienst, der die protokolle unterstützt, die von Windows 7 verwendet werden, sodass Windows 7 und höher diesen Datenspeicher remote durchsuchen kann. Siehe auch: OpenSearch Deskriptor, OpenSearch Standard.

**Dateiassoz**

Siehe Definition für: Dateitypassoz.

**Dateiformat**

Ein Format für Daten, die in einer Datei gespeichert sind, die über eine dokumentierte Formatspezifikation verfügt. Beispiele hierfür sind OLE DocFile, OPC, XML, ZIP und andere bekannte Dateiformatspezifikationen. Dateitypersteller verwenden in der Regel ein vorhandenes Dateiformat als Grundlage für einen neuen Dateityp. Ein Dateiformat kann einfach eine Definition sein, die nicht als Dateityp instanziiert wird.

**Dateiformathandler**

Dieser Begriff ist ein Synonym für den Dateityphandler. Siehe Definition für: Dateityphandler.

**Dateinamenerweiterung**

Siehe Definition für: Dateinamenerweiterung.

**Dateinamenerweiterung**

Der primäre Indikator eines Dateityps für Dateisystemelemente ist der Teil des Dateinamens, der auf den letzten Punkt folgt. Die Dateierweiterung darf keine Leerzeichen oder Nicht-ASCII-Zeichen enthalten und gilt nur für Dateien (keine Ordner). Dateinamenerweiterungen werden mithilfe einer Vergleichsfunktion verglichen, bei der die Schreibung oder das Lokale nicht berücksichtigt wird. Siehe auch: Dateiformat, Dateityp.

**Dateityp**

Ein bestimmter Dateinamenerweiterungswert, z. B. ".htm" oder ".jpg", der eine Klasse von Dateien definiert, die denselben Typ haben und einen gemeinsamen Satz von Zuordnungen haben. Siehe auch: Art, Dateitypassoz.

**Dateitypzuordnung**

Für eine bestimmte Dateinamenerweiterung die Zuordnungsarrayelemente, die definieren, wo Handler und andere Attribute registriert werden können. Siehe auch: Zuordnungsarray, Dateityp.

**Anpassung des Dateityps**

Eine Zuordnung, mit der Shell anpassen kann, wie Shell einen Dateityp behandelt. Zu den Dateitypanpassungen gehören: Angeben der Anwendung, die zum Öffnen der Datei beim Doppelklicken verwendet wird, Hinzufügen von Befehlen zum Kontextmenü für einen Dateityp, Angeben eines benutzerdefinierten Symbols, Angeben eines MIME-Inhaltstyps, der einem Dateityp zugeordnet werden soll, Angeben eines wahrgenommenen Typs und Angeben einer oder mehrere Anwendungen, die dem Dateityp mit dem Dialogfeld Öffnen mit zugeordnet sind. Siehe auch: PerceivedType.

**Dateityphandler**

Ein für einen Dateityp registrierter Handler. Siehe auch: Handler.

**filter**

Eine Implementierung der IFilter-Schnittstelle. Sie öffnet Dateien eines bestimmten Dateityps und filtert Eigenschaften und Textbrocken für den Indexer. Filter werden Dateitypen zugeordnet, wie durch Dateierweiterungen, MIME-Typen oder Klassenbezeichner (CLSIDs) angegeben. Obwohl ein Filter mehrere Dateitypen verarbeiten kann, funktioniert jeder Dateityp nur mit einem Filter.

**Ordner**

Weitere Informationen finden Sie unter Definition für: Container.

## <a name="h"></a>H

**handler**

Ein COM-Objekt, das Funktionen für ein Shellelement bietet. Die meisten Shell-Datenquellen bieten ein erweiterbares System zum Binden von Handlern an Elemente. Beispielsweise verwendet der Dateisystemordner das Zuordnungssystem, um die Handler für einen bestimmten Dateityp zu suchen. Siehe auch: Dateiassoz, Dateityp, Dateitypanpassung.

## <a name="i"></a>I

**Symbolhandler**

Ein Handler, der die Informationen enthält, die zum Generieren und Zwischenspeichern eines Symbols für ein Element erforderlich sind. Der Dateisystemdatenspeicher unterstützt das Laden eines Symbolhandlers für ein Element basierend auf dem Dateityp, sodass dieser Handler ein Symbol bereitstellen kann, das für alle Instanzen dieses Dateityps verwendet wird.

**Index**

n. Ein Katalog, der den Inhalt und die Eigenschaften von Shellelementen speichert, um schnelle Suchvorgänge zu ermöglichen. Siehe auch: Katalog, Indexer, Indizierung, invertierter Index. v. Um auf Inhaltsquellen zu zugreifen, filtern Sie die Quellen nach Inhalt und Eigenschaften, und fügen Sie die extrahierten Werte in den Index (für Text) und den Windows Search-Eigenschaftenspeicher (für Eigenschaften) ein. Siehe auch: Inhaltsquelle, Index, Indexer, invertierter Index.

**Indexer**

Eine Anwendung, die die Indizierung übernimmt oder die Indizierung koordiniert. Siehe auch: Index, Indizierung, invertierter Index.

**Infotip-Handler**

Ein Handler, der Popuptext enthält, wenn der Benutzer mit dem Mauszeiger auf ein Benutzeroberflächenobjekt zeigt.

**Invertierter Index**

Eine persistente Struktur, die den Inhalt enthält, der von der Suche aus dateien Windows wird. Der Text ist in einem Index organisiert, der von einem Wort in einer Eigenschaft zu einer Liste der Dokumente und Positionen in einem Dokument, die dieses Wort enthalten, zu ordnet. Daher ist ein invertierter Index die Umkehrung des Prozesses, bei dem der Text und die Eigenschaften aus dem Dokument extrahiert und in den Indexer eingefügt werden. Siehe auch: Index, Indexer, Indizierung.

**item**

Siehe Definition für: Shellelement.

**item-Klasse**

Siehe Definition für: Dateityp.

## <a name="k"></a>K

**Kind**

Eine Eigenschaft, die einen benutzerfreundlichen Kind-Namen bereitstellt und einer Liste von Eigenschaften und einem Layoutmuster zugeordnet werden kann. Kind wurde in Windows Vista eingeführt, um ein benutzerfreundlicheres Konzept des Dateityps auszudrücken, und es wurde als mehrwertige Zeichenfolgeneigenschaft (kanonische Zeichenfolgenwerte) definiert, daher können Sie einen "audio;video"- oder "link;document"-Typwert haben. Einige benutzerfreundliche Kind-Namen sind bereits Eigenschaften und Layoutmustern zugeordnet. Beispielsweise zeigen Elemente, die Kind.Picture zugeordnet sind, und Elemente, die Kind.Document zugeordnet sind, unterschiedliche Eigenschaften an, auch wenn sie sich in derselben Ansicht befinden. Jede Elementart kann einem von vier eindeutigen Layoutmustern zugeordnet werden, die die Anzahl der eigenschaften definieren, die für jedes Element und dessen Layout angezeigt werden. Siehe auch: Artzuordnung, Inhaltsansicht, Layoutmuster.

**Art-Zuordnung**

Eine Eigenschaft im Eigenschaftensystem namens System.Kind, die bestimmt, welche UX-Vorlagen für eine Datei angezeigt werden. Diese Eigenschaft stellt auch einen benutzerfreundlichen Namen für den Typ des Elements bereit und ist mit der Dateinamenerweiterung verknüpft. Siehe auch: Kind.

## <a name="l"></a>L

**Layoutmuster**

Eine von mehreren Anordnungen zum Anzeigen von Eigenschaften. Wenn Sie in Windows 7 und höher einen neuen Dateityp registrieren, können Sie die Inhaltsansicht verwenden, um eine benutzerdefinierte Eigenschaftenliste und ein Layoutmuster für Ihren Dateityp zu registrieren. Sie können aus vier verschiedenen Layoutmustern wählen: Alpha (für Dokumentsuchergebnisse, die Codeausschnitte enthalten), Beta (für E-Mail-Suchergebnisse mit Codeausschnitten), Gamma (ähnlich wie Alpha, aber mit einem zweizeiligen Layout anstelle von vier) und Delta (zum Anzeigen vieler kürzerer Eigenschaften, z. B. mit Musik und Bildern). Siehe auch: Inhaltsansicht, Art, Kind-Zuordnung.

## <a name="m"></a>M

**Metadatenhandler**

Dieser Begriff wird manchmal als Eigenschaftenhandler verwendet. Siehe Definition für: Eigenschaftenhandler.

## <a name="n"></a>N

**Namespaceerweiterung**

Siehe Definition für: Shelldatenquelle.

**Namespace-Exemplarische Schritte**

Ein Hilfsprozess, der den Namespace eines Containers oder einer Gruppe von Containern durchläuft, jedes Element erkennt und möglicherweise etwas mit jedem element macht. Die INamespaceWalk-Schnittstelle kann verwendet werden, um einen beliebigen Teil des Windows Explorer-Namespace zu erkunden oder um die Elemente zu ermitteln, auf die von einem Datenobjekt oder einer Datenansicht verwiesen wird. Containerverben (z.B. "Play" in Containers für Zeichner) gehen durch den Namespace und ermitteln die Elemente.

**Abfrage in natürlicher Sprache**

Siehe Definition für: Natural Query Syntax (NQS).

**Natural Query Syntax (NQS)**

Eine Abfragesyntax, die weniger locker als AQS ist und eher der menschlichen Sprache ähnelt. NQS kann von Windows Search verwendet werden, um den Index abzufragen, wenn NQS anstelle der Standardeinstellung AQS ausgewählt ist. Siehe auch: Erweiterte Abfragesyntax (Advanced Query Syntax, AQS).

**Füllwort**

Ein Wort, das von Windows Search ignoriert wird, wenn es in den für die Suchabfrage angegebenen Einschränkungen vorhanden ist, da es nur einen geringen Wert hat. Beispiele hierfür sind "and" und "the".

**Nqs**

Siehe Definition für: Natural Query Syntax (NQS).

## <a name="o"></a>O

**Object Linking and Embedding-Datenbank (OLE DB)**

Ein Standardsatz von Schnittstellen, der heterogenen Zugriff auf unterschiedliche Informationsquellen an beliebigen Orten ermöglicht, z. B. Dateisysteme, E-Mail-Ordner und Datenbanken.

**OLE DB**

Siehe Definition für: Object Linking and Embedding-Datenbank.

**OpenSearch Deskriptor**

Eine XML-Datei, die verfügbare Serververbindungen und Ergebnisformate für eine bestimmte webbasierte Datenquelle beschreibt. Diese Datei enthält eine oder mehrere URL-Vorlagen und verwendet bei der Interaktion mit der Windows Shell eine OSDX-Dateinamenerweiterung. Eine OpenSearch Beschreibung wird manchmal auch als Suchconnector bezeichnet, obwohl es nur der Beschreibungsteil eines Connectors ist. Siehe auch: Connector suchen.

**OpenSearch Standard**

Eine Sammlung einfacher Formate und Protokolle, die zum Freigeben von Suchergebnissen verwendet werden. Weitere Informationen finden Sie auf der OpenSearch-Website ( https://github.com/dewitt/opensearch) .

## <a name="p"></a>P

**PerceivedType**

Eine breite Kategorie von Dateiformattypen. PerceivedType wurde in Windows XP eingeführt und unterstützt eine begrenzte Anzahl bekannter Dateitypen (z. B. Bild-, Text-, Audio- und komprimierte Dateitypen). Dateitypen, im Allgemeinen öffentliche Dateitypen, können auch einen wahrgenommenen Typ aufweisen. Beispielsweise sind die Bilddateitypen .bmp, .png, .jpg und .gif ebenfalls vom wahrgenommenen Typ Image. Auf der Programmierebene wird PerceivedType als ganze Zahl ausgedrückt. Da es Code gibt, der Kind und PerceivedType verwendet, müssen Besitzer des Dateiformats beides registrieren. Beispielsweise hängt "alles wiedergeben" von PerceivedType ab. Siehe auch: Dateityp.

**Vorschauhandler**

Ein Handler, der schnell eine schreibgeschützte, vereinfachte Ansicht des Shellelements erzeugt, das im Vorschaubereich Windows Explorer angezeigt werden soll.

**Previewer**

Dieser Begriff wird manchmal als Vorschauhandler verwendet. Siehe Definition für: Vorschauhandler.

**Eigenschaftenhandler**

Ein Handler, der in einer Datei gespeicherte Daten in ein strukturiertes Schema übersetzt, das von erkannt wird und auf das Windows Explorer, Windows Search und andere Anwendungen zugreifen können. Diese Systeme können dann mit dem Eigenschaftenhandler interagieren, um Eigenschaften in und aus der Datei zu schreiben und zu lesen. Die übersetzten Daten umfassen Detailansicht, Infotips, Detailbereich, Eigenschaftenseiten usw. Jeder Eigenschaftenhandler ist einem bestimmten Dateityp zugeordnet, der durch die Dateinamenerweiterung identifiziert wird. Siehe auch: Eigenschaftensystem.

**Eigenschaftenblatthandler**

Ein Handler, der verwendet wird, um benutzerdefinierte Eigenschaftenblätter mit Ui-Bildern und -Steuerelementen zu erstellen, die eine benutzerdefinierte Interaktion mit einem Dateityp ermöglichen.

**-Eigenschaftensystem**

Ein erweiterbares Lese-/Schreibsystem von Datendefinitionen, das Eigenschaften verwendet, die als Name-Wert-Paare implementiert sind. Siehe auch: Eigenschaftenhandler, Shellelement.

**-Eigenschaftswert**

Ein Wert, der einem Eigenschaftennamen für ein Shellelement zugeordnet ist. Beispielsweise sind "Author", "Size" und "Date Taken" Eigenschaften. Eigenschaftswerte werden als PROPVARIANT-Struktur ausgedrückt.

**Protokollhandler**

Ein Handler, der auf Inhaltsquellen zugreift und ein IUrlAccessor-Objekt für ein angegebenes Protokoll und eine URL bereitstellt. Protokollhandler erweitern Windows Search-Funktionalität und können Änderungsbenachrichtigungen für Indexer bereitstellen. Unterschiedliche Protokollhandler sind erforderlich, um bestimmte Typen von Datenspeichern zu indizieren. Um eine angemessene Benutzererfahrung zu bieten, müssen Sie zusätzlich zur Implementierung Ihres Protokollhandlers auch eine Shell-Datenquelle für den Datenspeicher bereitstellen. Der Protokollhandler macht die Elemente im Datenspeicher für den Indexer verfügbar, während die Shell-Datenquelle die Elemente im Datenspeicher für die Shell verfügbar macht.

## <a name="r"></a>R

**Einschränkung**

Eine Bedingung, die eine Datei erfüllen muss, um in die Suchergebnisse aufgenommen zu werden, die von Windows Search zurückgegeben werden.

**row**

Die Spalten, die die Eigenschaftswerte enthalten, die ein einzelnes Ergebnis aus dem Satz von -Objekten beschreiben, die den in einer Suchabfrage angegebenen Einschränkungen entsprachen.

**Rowset**

Ein Satz von Zeilen, die in den Suchergebnissen zurückgegeben werden.

## <a name="s"></a>E

**Suchconnector**

Eine XML-Datei, die Informationen zu einem Datenspeicher enthält. Suchconnectors werden für die Verbundsuche bereitgestellt.

**Search-Consumer**

Eine Komponente oder Anwendung, die den Index abfragt.

**Verbund suchen**

Siehe Definition für: Verbundsuchanbieter.

**Suchanbieter**

Eine Komponente oder Anwendung, die Daten für die suche Windows.

**Suchbereich**

Dieser Begriff wird manchmal als Durchforstungsbereich verwendet. Siehe Definition für: Durchforstungsbereich.

**Shelldatenquelle**

Eine Komponente, die verwendet wird, um den Shellnamespace zu erweitern und Elemente in einem Datenspeicher verfügbar zu machen. In der Vergangenheit wurde die Shell-Datenquelle als Shellnamespaceerweiterung bezeichnet. Siehe auch: Container, Handler, Shell-Element.

**Shellerweiterung**

Dieser Begriff wird manchmal als Dateityphandler verwendet. Siehe Definition für: Dateityphandler.

**Shell-Erweiterungshandler**

Dieser Begriff wird manchmal als Dateityphandler verwendet. Siehe Definition für: Dateityphandler.

**Shellhandler**

Dieser Begriff wird manchmal als Dateityphandler verwendet. Siehe Definition für: Dateityphandler.

**Shellelement**

Ein einzelner Inhalt. Einige Shellelemente sind Inhaltsquellen, andere nicht. Ein Ordner ist z. B. eine Inhaltsquelle, eine .jpg jedoch nicht. Dateityphandler machen Shellelemente verfügbar. In einigen Kontexten wird "Item" verwendet, um Container von Nichtcontainern zu unterscheiden. Siehe auch: Container, Inhaltsquelle, Dateityphandler.

**Shellnamespaceerweiterung**

Dieser Begriff wird manchmal als Shell-Datenquelle verwendet. Siehe Definition für: Shell-Datenquelle.

**Kontextmenü**

Eine Benutzeroberfläche, die verwendet wird, um eine Auflistung von Verben zu präsentieren, die einem Benutzeroberflächenelement zugeordnet sind, z. B. eine Datei oder ein Ordner.

**Kontextmenühandler**

Ein Handler, der Verben für ein Element oder Elemente hinzufügt. Diese Verben werden häufig in einem Kontextmenü angezeigt. Siehe auch: Kontextmenü.

**statisches Verb**

Ein Verb, das für ein Shellelement gilt, ohne den aktuellen Zustand eines Elements oder Systems überprüfen zu müssen. Ein statisches Verb basiert auf einer statischen Registrierung der zugeordneten Elemente eines Elements und ändert sich nicht.

## <a name="t"></a>T

**Thumbnail-Handler**

Ein Handler, der ein statisches Bild zur Darstellung eines Shellelements bietet.

**Miniaturansichtsanbieter**

Dieser Begriff wird manchmal als Miniaturbildhandler verwendet. Weitere Informationen finden Sie unter Definition für: Thumbnail Handler.

## <a name="u"></a>U

**URL-Vorlage**

Eine URL-basierte Verbindungszeichenfolge, die zum Abfragen von Suchergebnissen auf einem Webserver verwendet wird. Die Vorlage sieht wie eine URL aus, enthält jedoch mehrere Platzhalterwerte (z. B. {searchTerms}), die der Client durch Daten zu den abzurufenden Ergebnissen ersetzen muss. Die Definition von URL-Vorlagen ist entscheidend für die Implementierung der Verbundsuche und OpenSearch Standards.

**Benutzerfreundlicher Artname**

Siehe Definition für: Kind.

## <a name="v"></a>V

**Verb**

Eine einzelne Aktion, die von einem Shellelement aufgerufen werden kann. Beispiele hierfür sind "öffnen" und "drucken". Verben werden manchmal als Befehle oder Aufgaben bezeichnet. Siehe auch: dynamisches Verb, Kontextmenühandler, statisches Verb.

**Verbhandler**

Dieser Begriff wird manchmal als Kontextmenühandler verwendet. Siehe Definition für: Kontextmenühandler.

## <a name="w"></a>W

**Spaziergang**

Weitere Informationen finden Sie unter Definition for: namespace walk (Exemplarische Vorgehensweise für Namespaces).

**Windows-Suche**

Siehe Definition für: Windows Suchdienst.

**Windows Suchen des Eigenschaftenspeichers**

Der Cache von Eigenschaftswerten, die in der Implementierung des -Windows Suchdienst. Diese Eigenschaftswerte können programmgesteuert mithilfe des Suchanbieters Windows Search OLE DB werden. Der Windows Search-Eigenschaftenspeicher sammelt und speichert Eigenschaften, die von Filterhandlern oder Eigenschaftenhandlern ausgegeben werden, wenn ein Element wie ein Word-Dokument indiziert wird. Dieser Speicher wird verworfen und neu erstellt, wenn der Index neu erstellt wird.

**Windows Suchdienst**

Bezieht sich Windows Search 3.0 und höher. Dieser Dienst analysiert eine Reihe von Dokumenten, extrahiert nützliche Informationen und organisiert dann die extrahierten Informationen, sodass Eigenschaften dieser Dokumente effizient als Reaktion auf Abfragen zurückgegeben werden können. Siehe auch: Katalog.
