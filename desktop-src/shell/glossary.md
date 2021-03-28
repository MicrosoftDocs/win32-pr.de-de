---
description: Glossarseite
ROBOTS: NOINDEX, NOFOLLOW
title: Shellglossar
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2F463941-A4BA-4b34-B391-7E599E87BEEA
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e6ec49f808f6c6dea74d3c8c2ac4408bc5d1a26e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345398"
---
# <a name="shell-glossary"></a>Shellglossar

## <a name="a"></a>Ein

<dl> <dt>

**Anwalt**
</dt> <dd>

Eine Zuordnung einer Dateinamenerweiterung (z. b.. MP3) oder eines Protokolls (z. b. http) zu einem programmatischen Bezeichner (ProgID). Diese Zuordnung wird in der Registrierung als benutzerspezifische Einstellung mit einem Fallback pro Computer gespeichert. Anwendungen, die am Standardprogramm System teilnehmen, legen die Zuordnungs Zuordnung für die Dateinamenerweiterung oder das Protokoll fest, um auf die ProgID-Schlüssel zu verweisen, die Sie besitzen.

</dd> <dt>

**Zuordnungs Array**
</dt> <dd>

Eine geordnete Liste der Registrierungs Speicherorte, die zum Speichern von Informationen über einen Elementtyp verwendet werden, einschließlich Handler, Verben und anderen Attributen, wie z. b. Symbol und Anzeige Name des Typs. Beispielsweise verfügt eine JPG-Datei über das folgende Zuordnungs Array auf einem standardmäßigen Windows-System: "HKCR \\ jpgfile", "HKCR \\ systemfileassociations \\ . jpg", "HKCR \\ systemfileassociation \\ Image", "HKCR \\ \* ", "HKCR \\ AllFilesystemObjects".

</dd> </dl>

## <a name="b"></a>B

<dl> <dt>

**bind**
</dt> <dd>

Zum Laden oder Zuordnen von Code mit Daten. Beispielsweise kann ein Handler einer shelldatenquelle zugeordnet werden.

</dd> </dl>

## <a name="c"></a>C

<dl> <dt>

**Kanonischer Name**
</dt> <dd>

Der eindeutige Name einer Ressource. Kanonisch bedeutet "gemäß den Regeln". Siehe auch: kanonischer Verb Name.

</dd> <dt>

**Kanonischer Verb Name**
</dt> <dd>

Ein sprach neutraler Name, der unabhängig von der lokalisierten Zeichenfolge in der Benutzeroberfläche Programm gesteuert verwendet werden kann, um auf ein Verb zu verweisen. Siehe auch: kanonischer Name, Verb.

</dd> <dt>

**container**
</dt> <dd>

Ein Typ von shellelement, das andere Elemente enthalten kann. Elemente in einem Container werden mithilfe einer shelldatenquelle für den Shellnamespace verfügbar gemacht. Beispiele hierfür sind Ordner, Laufwerke, Netzwerkserver und komprimierte Dateien mit der Dateinamenerweiterung ". zip". Siehe auch: Shell-Datenquelle, Ordner, shellelement.

</dd> <dt>

**content**
</dt> <dd>

Text und Eigenschaften, die einem shellelement oder einer Inhaltsquelle zugeordnet sind, das indiziert werden kann.

</dd> <dt>

**Inhaltsquelle**
</dt> <dd>

Ein Element, auf das der Indexer zugreifen kann. Inhalts Quellen sind über eine URL adressierbar und werden von einem Protokollhandler für den Indexer bereitgestellt. Beispiele hierfür sind: Dateisystem Dateien und-Ordner, Microsoft Outlook-Elemente und-Ordner, Datenbankeinträge und gespeicherte Microsoft SharePoint-Elemente. Eine Inhaltsquelle kann als shellelemente verfügbar gemacht werden, indem eine shelldatenquelle implementiert wird. Siehe auch: Inhalt, shellelement.

</dd> <dt>

**content view (Inhaltsansicht)**
</dt> <dd>

Eine Ansicht in Windows-Explorer (in Windows 7 und höher angeboten), die den relevantesten Inhalt für jedes Element in der Liste basierend auf der Dateinamenerweiterung oder der Art der Zuordnung anzeigt. In der Inhaltsansicht wird eine Logik zur Größenänderung verwendet, mit der Eigenschaften gelöscht werden, wenn die Fenstergröße abnimmt, um sicherzustellen, dass die kritischsten Eigenschaften weiterhin Platz aufweisen, um klar lesbar Siehe auch: Layoutmuster, Kind, Kind Association.

</dd> <dt>

**Inhalts Ansichtsmodus**
</dt> <dd>

Siehe Definition für: Inhaltsansicht.

</dd> <dt>

**Kontextmenü**
</dt> <dd>

Dieser Begriff wird manchmal verwendet, um das Kontextmenü zu verwenden. Siehe Definition für: Kontextmenü.

</dd> <dt>

**Kontextmenü Handler**
</dt> <dd>

Dieser Begriff wird manchmal verwendet, um den Kontextmenü Handler zu verwenden. Siehe Definition für: Kontextmenü Handler.

</dd> </dl>

## <a name="d"></a>D

<dl> <dt>

**Datenobjekt Handler**
</dt> <dd>

Ein Handler, der zusätzliche Zwischenablage Formate für das Datenobjekt (IDataObject) eines Elements bereitstellt. Datenobjekte werden in Drag & Drop-und Kopier-/Einfüge Szenarien verwendet.

</dd> <dt>

**Datenquelle**
</dt> <dd>

Dieser Begriff wird manchmal verwendet, um Datenspeicher oder Shell-Datenquelle zu verwenden. Siehe Definition für: Datenspeicher, shelldatenquelle.

</dd> <dt>

**Datenspeicher**
</dt> <dd>

Ein Repository mit Daten. Ein Datenspeicher kann für das shellprogrammierungs Modell als Container mithilfe einer shelldatenquelle verfügbar gemacht werden. Die Elemente in einem Datenspeicher können vom Windows-Suchsystem mithilfe eines Protokoll Handlers indiziert werden.

</dd> <dt>

**Desktop Komposition**
</dt> <dd>

Ein Windows Vista-Feature, das es ermöglicht, dass einzelne Fenster auf Offscreen-Oberflächen im Videospeicher anstatt direkt auf dem primären Anzeigegerät gezeichnet werden können.

</dd> <dt>

**document**
</dt> <dd>

Ein shellelement, das Text enthält und für das die IFilter-Schnittstelle implementiert werden konnte.

</dd> <dt>

**Drop-Handler**
</dt> <dd>

Ein Handler, der einem bestimmten Elementtyp ermöglicht, Drag & Drop-und Kopier-/Einfüge Szenarien zu unterstützen.

</dd> <dt>

**Ablage Ziel**
</dt> <dd>

Ein Datenobjekt, das in eine Datei gezogen und dort abgelegt wird. Siehe auch: Daten Handler, Drop Handler.

</dd> <dt>

**Dynamisches Verb**
</dt> <dd>

Ein Verb, das vom Zustand eines shellelements oder des Systems abhängig ist. das Element ist Zustands basiert und erfordert, dass der ausführende Code bestimmt, ob das Element angezeigt werden soll. Siehe auch: Kontextmenü Handler, statisches Verb, Verb.

</dd> </dl>

## <a name="e"></a>E

<dl> <dt>

**Explorer-Befehl**
</dt> <dd>

Ein Objekt, das als Schaltfläche in der Nähe des oberen Fensters des Windows-Explorer-Fensters angezeigt werden kann, das Funktionen für Elemente und Container in diesem Fenster bereitstellt. Eine shelldatenquelle stellt die Windows-Explorer-Befehls Objekte für ein bestimmtes Containerelement bereit. Befehle werden manchmal als Verben verwendet.

</dd> </dl>

## <a name="f"></a>F

<dl> <dt>

**Datei Zuordnung**
</dt> <dd>

Siehe Definition für: Dateityp Zuordnung.

</dd> <dt>

**Dateiformat**
</dt> <dd>

Ein Format für Daten, die in einer Datei gespeichert sind, die über eine dokumentierte Format Spezifikation verfügt. Beispiele hierfür sind OLE DOCFILE, OPC, XML, zip und andere bekannte Datei Formatspezifikationen. Dateityp-Ersteller verwenden im Allgemeinen ein vorhandenes Dateiformat als Grundlage für einen neuen Dateityp. Ein Dateiformat kann einfach eine Definition sein, die nicht als Dateityp instanziiert wird.

</dd> <dt>

**Dateiformat Handler**
</dt> <dd>

Dieser Begriff ist ein Synonym für den Dateityp Handler. Siehe Definition für: Dateityp Handler.

</dd> <dt>

**Dateinamenerweiterung**
</dt> <dd>

Der primäre Indikator eines Dateityps für Dateisystem Elemente, ist der Teil des Datei namens, der auf den letzten Punkt folgt. Die Dateinamenerweiterung darf keine Leerzeichen oder nicht-ASCII-Zeichen enthalten und gilt nur für Dateien (nicht für Ordner). Dateinamen Erweiterungen werden mithilfe einer Vergleichsfunktion verglichen, bei der es sich nicht um groß-oder Kleinschreibung handelt. Siehe auch: Dateiformat, Dateityp.

</dd> <dt>

**Dateityp**
</dt> <dd>

Ein bestimmter Dateiname-Erweiterungs Wert, wie z. b. ". htm" oder ". jpg", der eine Klasse von Dateien definiert, die denselben Typ aufweisen und über einen gemeinsamen Satz von Zuordnungen verfügen. Siehe auch: Kind, Dateityp Zuordnung.

</dd> <dt>

**Dateitypzuordnung**
</dt> <dd>

Für eine bestimmte Dateinamenerweiterung werden die Zuordnungs Elemente, die angeben, wo Handler und andere Attribute registriert werden können, definiert. Siehe auch: Zuordnungs Array, Dateityp.

</dd> <dt>

**Dateityp Anpassung**
</dt> <dd>

Eine Zuordnung, mit der Shell anpassen kann, wie Shell einen Dateityp behandelt. Dateityp Anpassungen umfassen Folgendes: Angeben der Anwendung, die zum Öffnen der Datei beim Doppelklicken verwendet wurde, Hinzufügen von Befehlen zum Kontextmenü für einen Dateityp, Angeben eines benutzerdefinierten Symbols, Angeben eines MIME-Inhaltstyps, der einem Dateityp zugeordnet werden soll, Angeben eines erkannten Typs und Angeben einer oder mehrerer Anwendungen, die mit dem Dateityp verknüpft sind Siehe auch: wahrnehmvedtype.

</dd> <dt>

**Dateityp Handler**
</dt> <dd>

Ein für einen Dateityp registrierter Handler. Siehe auch: Handler.

</dd> <dt>

**Pfalz**
</dt> <dd>

Siehe Definition für: Container.

</dd> <dt>

**vollständige PIDL**
</dt> <dd>

Eine PIDL, die ein Objekt in Relation zum Desktop Ordner eindeutig beschreibt.

</dd> </dl>

## <a name="h"></a>H

<dl> <dt>

**lers**
</dt> <dd>

Ein COM-Objekt, das Funktionen für ein shellelement bereitstellt. Die meisten shelldatenquellen bieten ein erweiterbares System zum Binden von Handlern an Elemente. Beispielsweise verwendet der Dateisystem Ordner das Zuordnungs System, um die Handler für einen bestimmten Dateityp zu suchen. Siehe auch: Datei Zuordnung, Dateityp, Dateityp Anpassung.

</dd> </dl>

## <a name="i"></a>I

<dl> <dt>

**Symbol Handler**
</dt> <dd>

Ein Handler, der die zum Generieren und Zwischenspeichern eines Symbols für ein Element benötigten Informationen bereitstellt. Der Dateisystem-Datenspeicher unterstützt das Laden eines Symbol Handlers für ein Element auf der Grundlage des Dateityps, sodass dieser Handler ein Symbol bereitstellen kann, das für alle Instanzen dieses Dateityps verwendet wird.

</dd> <dt>

**Infotipp-Handler**
</dt> <dd>

Ein Handler, der Popup Text bereitstellt, wenn der Benutzer mit dem Mauszeiger auf ein Benutzeroberflächen Objekt zeigt.

</dd> <dt>

**item**
</dt> <dd>

Siehe Definition für: shellelement.

</dd> <dt>

**Item-Klasse**
</dt> <dd>

Siehe Definition für: Dateityp.

</dd> <dt>

**Liste der Element Bezeichner**
</dt> <dd>

Sequenz von einer oder mehreren shitemid-Strukturen, die ein Objekt in Relation zu einem Stamm Objekt eindeutig definiert.

</dd> </dl>

## <a name="k"></a>K

<dl> <dt>

**Kind**
</dt> <dd>

Eine Eigenschaft, die einen benutzerfreundlichen Namen bereitstellt und einer Liste von Eigenschaften und einem Layoutmuster zugeordnet werden kann. Art wurde in Windows Vista eingeführt, um einen benutzerfreundlicheren Begriff "Dateityp" zu lesen, und er wurde als mehrwertige Zeichen folgen Eigenschaft (kanonische Zeichen folgen Werte) definiert. Daher können Sie einen "Audiotext"-oder "Link; Dokument"-Wert haben. Einige benutzerfreundliche Arten von Namen sind bereits Eigenschaften und layoutmustern zugeordnet. Beispielsweise werden Elementen, die mit "Kind. Picture" verknüpft sind, und Elementen, die mit Kind.Doc-Ereignis verknüpft sind, andere Eigenschaften angezeigt, auch wenn Sie sich in derselben Ansicht befinden Jede Elementart kann einem von vier eindeutigen layoutmustern zugeordnet werden, die die Anzahl der Eigenschaften definieren, die für die einzelnen Elemente und deren Layout angezeigt werden. Siehe auch: Kind Association, Content View, Layout Pattern.

</dd> </dl>

## <a name="l"></a>L

<dl> <dt>

**Layoutmuster**
</dt> <dd>

Eine von mehreren Anordnungen zum Anzeigen von Eigenschaften. Wenn Sie in Windows 7 und höher einen neuen Dateityp registrieren, können Sie die Inhaltsansicht verwenden, um eine benutzerdefinierte Eigenschaften Liste und ein Layoutmuster für den Dateityp zu registrieren. Sie können aus vier unterschiedlichen layoutmustern wählen: Alpha (für Dokument Suchergebnisse, die Code Ausschnitte enthalten), Beta (für e-Mail-Suchergebnisse mit Code Ausschnitten), Gamma (ähnlich wie Alpha, aber mit einem zweizeiligen Layout anstelle von vier) und Delta (für die Anzeige zahlreicher kürzerer Eigenschaften, z. b. mit Musik und Bildern). Siehe auch: Inhaltsansicht, Kind, Kind Association.

</dd> </dl>

## <a name="m"></a>M

<dl> <dt>

**Metadatenhandler**
</dt> <dd>

Dieser Begriff wird manchmal verwendet, um den Eigenschafts Handler zu verwenden. Siehe Definition für: Eigenschaften Handler.

</dd> </dl>

## <a name="n"></a>N

<dl> <dt>

**Namespace Erweiterung**
</dt> <dd>

Siehe Definition für: shelldatenquelle.

</dd> </dl>

## <a name="o"></a>O

<dl> <dt>

**Objekt Verknüpfungs-und Einbettungs Datenbank (OLE DB)**
</dt> <dd>

Ein Standardsatz von Schnittstellen, der heterogenen Zugriff auf verschiedenartige Informationsquellen bietet, z. b. Dateisysteme, e-Mail-Ordner und Datenbanken.

</dd> <dt>

**OLE DB**
</dt> <dd>

Siehe Definition für: Objekt Verknüpfungs-und Einbettungs Datenbank.

</dd> </dl>

## <a name="p"></a>P

<dl> <dt>

**Wahrnehmungstyp**
</dt> <dd>

Eine breite Kategorie von Dateiformat Typen. "Wahrnehmvedtype" wurde in Windows XP eingeführt und unterstützt eine begrenzte Anzahl bekannter Dateitypen (Beispiele sind Bild-, Text-, Audio-und komprimierte Dateitypen). Dateitypen, in der Regel öffentliche Dateitypen, können auch über einen wahrgenommenen Typ verfügen. Beispielsweise sind die Image Dateitypen. BMP,. png,. jpg und. gif ebenfalls den wahrgenommenen Typ Image. Auf der Programmier Ebene wird "wahrvedtype" als ganze Zahl ausgedrückt. Da es Code gibt, der "Kind" und "wahrnehmvedtype" verwendet, müssen Besitzer von Dateiformaten beide registrieren. Beispielsweise ist "Play All" von "wahrnehmvedtype" abhängig. Siehe auch: Dateityp.

</dd> <dt>

**Vorschau Handler**
</dt> <dd>

Ein Handler, der schnell eine schreibgeschützte, vereinfachte Ansicht des shellelements erstellt, das im Vorschaubereich von Windows-Explorer angezeigt werden soll.

</dd> <dt>

**Eigenschaften Handler**
</dt> <dd>

Ein Handler, der in einer Datei gespeicherte Daten in ein strukturiertes Schema übersetzt, das von erkannt wird und auf das von Windows-Explorer, Windows Search und anderen Anwendungen zugegriffen werden kann. Diese Systeme können dann mit dem Eigenschaften Handler interagieren, um Eigenschaften in die Datei zu schreiben und diese zu lesen. Zu den übersetzten Daten zählen Detailansicht, Infotipps, Detailbereich, Eigenschaften Seiten usw. Jeder Eigenschaften Handler ist einem bestimmten Dateityp zugeordnet, der durch die Dateinamenerweiterung gekennzeichnet ist. Siehe auch: Eigenschaften System.

</dd> <dt>

**Eigenschaften Blatt Handler**
</dt> <dd>

Ein Handler, der zum Erstellen benutzerdefinierter Eigenschaften Blätter mit UI-Bildern und Steuerelementen verwendet wird, die eine benutzerdefinierte Interaktion mit einem Dateityp ermöglichen.

</dd> <dt>

**Eigenschaften System**
</dt> <dd>

Ein erweiterbares Lese-/Schreibsystem von Daten Definitionen, das Eigenschaften verwendet, die als Name-Wert-Paare implementiert werden. Siehe auch: Eigenschaften Handler, shellelement.

</dd> <dt>

**Eigenschafts Wert**
</dt> <dd>

Ein Wert, der einem Eigenschaftsnamen für ein shellelement zugeordnet ist. Beispielsweise sind "Author", "size" und "Date Taken" Eigenschaften. Eigenschaftswerte werden als PROPVARIANT-Struktur ausgedrückt.

</dd> <dt>

**Protokollhandler**
</dt> <dd>

Ein Handler, der auf Inhalts Quellen zugreift und ein iurlaccessor-Objekt für ein angegebenes Protokoll und eine URL bereitstellt. Protokollhandler erweitern die Windows-Suchfunktionen und stellen möglicherweise Änderungs Benachrichtigungen für Indexer bereit. Zum Indizieren bestimmter Typen von Daten speichern sind unterschiedliche Protokollhandler erforderlich. Zum Bereitstellen eines angemessenen Benutzer Erlebnisses müssen Sie zusätzlich zur Implementierung des Protokoll Handlers auch eine Shell-Datenquelle für den Datenspeicher bereitstellen. Der Protokollhandler macht die Elemente im Datenspeicher für den Indexer verfügbar, während die shelldatenquelle die Elemente im Datenspeicher für die Shell verfügbar macht.

</dd> </dl>

## <a name="r"></a>R

<dl> <dt>

**relative PIDL**
</dt> <dd>

Eine PIDL, die relativ zu einem Stamm Objekt im Shell-Namespace ist, das nicht der Desktop Ordner ist. Dies ist in der Regel der übergeordnete Ordner des Elements.

</dd> </dl>

## <a name="s"></a>E

<dl> <dt>

**Shelldatenquelle**
</dt> <dd>

Eine Komponente, die verwendet wird, um den Shellnamespace zu erweitern und Elemente in einem Datenspeicher verfügbar zu machen. In der Vergangenheit wurde die shelldatenquelle als Shell-Namespace Erweiterung bezeichnet. Siehe auch: Container, Handler, shellelement.

</dd> <dt>

**Shellerweiterung**
</dt> <dd>

Dieser Begriff wird manchmal verwendet, um den Dateityp Handler zu verwenden. Siehe Definition für: Dateityp Handler.

</dd> <dt>

**Shellerweiterungs Handler**
</dt> <dd>

Dieser Begriff wird manchmal verwendet, um den Dateityp Handler zu verwenden. Siehe Definition für: Dateityp Handler.

</dd> <dt>

**Shellhandler**
</dt> <dd>

Dieser Begriff wird manchmal verwendet, um den Dateityp Handler zu verwenden. Siehe Definition für: Dateityp Handler.

</dd> <dt>

**Shellelement**
</dt> <dd>

Ein einzelnes Inhalts Element. Einige shellelemente sind Inhalts Quellen, andere hingegen nicht. Ein Ordner ist eine Inhaltsquelle, z. b. eine JPG-Datei. Dateityp Handler machen shellelemente verfügbar. In manchen Kontexten wird "Item" verwendet, um Container von nicht Containern zu unterscheiden. Siehe auch: Container, Inhaltsquelle, Dateityp Handler.

</dd> <dt>

**Shell-Namespace Erweiterung**
</dt> <dd>

Dieser Begriff wird manchmal zum Mean der shelldatenquelle verwendet. Siehe Definition für: shelldatenquelle.

</dd> <dt>

**Kontextmenü**
</dt> <dd>

Eine Benutzeroberfläche, die verwendet wird, um eine Auflistung von Verben darzustellen, die einem Benutzeroberflächen Element zugeordnet sind, z. b. eine Datei oder ein Ordner.

</dd> <dt>

**Kontextmenü Handler**
</dt> <dd>

Ein Handler, der Verben für ein Element oder Elemente hinzufügt. Diese Verben werden in der Regel in einem Kontextmenü angezeigt. Siehe auch: Kontextmenü.

</dd> <dt>

**einfache PIDL**
</dt> <dd>

Eine PIDL, die ohne Datenträger Überprüfung analysiert wird.

</dd> <dt>

**statisches Verb**
</dt> <dd>

Ein Verb, das für ein shellelement gilt, ohne den aktuellen Zustand eines Elements oder Systems überprüfen zu müssen. Ein statisches Verb basiert auf einer statischen Registrierung der zugeordneten Elemente eines Elements und ändert sich nicht.

</dd> </dl>

## <a name="t"></a>T

<dl> <dt>

**Miniatur Ansichts Handler**
</dt> <dd>

Ein Handler, der ein statisches Bild bereitstellt, das ein shellelement darstellen soll.

</dd> <dt>

**Miniatur Ansichts Anbieter**
</dt> <dd>

Dieser Begriff wird manchmal verwendet, um den Miniatur Ansichts Handler zu verwenden. Siehe Definition für: Miniatur Ansichts Handler.

</dd> </dl>

## <a name="u"></a>U

<dl> <dt>

**benutzerfreundlicher Name der Art**
</dt> <dd>

Siehe Definition für: Kind.

</dd> </dl>

## <a name="v"></a>V

<dl> <dt>

**Verb**
</dt> <dd>

Eine einzelne Aktion, die von einem shellelement aufgerufen werden kann. Beispiele hierfür sind Open und Print. Verben werden manchmal als Befehle oder Aufgaben bezeichnet. Siehe auch: Dynamisches Verb, Kontextmenü Handler, statisches Verb.

</dd> <dt>

**Verb Handler**
</dt> <dd>

Dieser Begriff wird manchmal verwendet, um den Kontextmenü Handler zu verwenden. Siehe Definition für: Kontextmenü Handler.

</dd> </dl>

 

 



