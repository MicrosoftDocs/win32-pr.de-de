---
description: Das Windows Property System ist ein erweiterbares Lese-/Schreibsystem von Datendefinitionen, das eine einheitliche Möglichkeit bietet, Metadaten zu Shellelementen auszudrücken.
ms.assetid: eb2dc2be-fc53-40aa-81f6-f353ab1d3a57
title: Übersicht über das Eigenschaftensystem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 742eebbdb05541a3cfcc1468cd0f93d255f13b67b4bfe777729d1d02d2ed70a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460030"
---
# <a name="property-system-overview"></a>Übersicht über das Eigenschaftensystem

Das Windows Property System ist ein erweiterbares Lese-/Schreibsystem von Datendefinitionen, das eine einheitliche Möglichkeit bietet, Metadaten zu Shellelementen auszudrücken. Mit Windows-Eigenschaftssystem in Windows Vista und höher können Sie Metadaten für Shellelemente speichern und abrufen. Ein Shellelement ist ein beliebiger Inhalt, z. B. eine Datei, ein Ordner, eine E-Mail oder ein Kontakt. Eine Eigenschaft ist ein einzelnes Metadatenelement, das einem Shellelement zugeordnet ist. Eigenschaftswerte werden als [**PROPVARIANT-Struktur**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) ausgedrückt.

Dieses Thema ist wie folgt organisiert:

-   [Introduction (Einführung)](#introduction)
-   [Entwicklungsszenarien](#development-scenarios)
-   [Eigenschaften und Windows Suchen](#properties-and-windows-search)
-   [Hinweis für Implementierer](#note-to-implementers)
-   [Windows Dokumentation zum Eigenschaftensystem](#windows-property-system-documentation)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Eigenschaften werden durch ihren kanonischen Namen (z. B. ) und den Eigenschaftsschlüssel `System.Document.LastAuthor` (z. B. ) eindeutig `PKEY_Document_LastAuthor` identifiziert. Ein Eigenschaftsschlüssel (PKEY) ist der Namensteil eines Name-Wert-Paars, das aus einem PKEY/PROPVARIANT- oder einer Zeichenfolge/PROPVARIANT besteht, wobei die Zeichenfolge der kanonische Name des PKEY ist (z. B. `System.Document.LastAuthor` ). Ein PKEY ist eine Definition, die dem Eigenschaftensystem alles sagt, was es über die Eigenschaft wissen muss, während der Wert eine tatsächliche Instanz der Eigenschaft ist. Ein PKEY enthält intern eine formatID und propID.

Eine einzelne Eigenschaft besteht aus den folgenden drei Teilen:

-   Ein kanonischer Name, z. `System.Music.Artist` B. .
-   Eine Schemabeschreibung, die im PROPDESC-XML-Dateiformat angegeben und programmgesteuert über [**IPropertyDescription ausgedrückt wird.**](/windows/desktop/api/Propsys/nn-propsys-ipropertydescription)
-   Ein -Wert, z. B. der Name eines 30-00-00-00-00-000

Die Schemabeschreibung besteht aus Informationen über die Eigenschaft, z. B. den Eigenschaftennamen, Datentyp, Einschränkungen, Informationen zur Interaktion der Eigenschaft mit Ansichten und dem Suchsystem usw. Der Name und die Schemabeschreibung werden global definiert und sind für alle Elemente und Typen identisch. Ein Wert ist spezifisch für ein einzelnes Element. Das heißt, die Eigenschaft ist immer als mehrwertige Zeichenfolge definiert, kann jedoch für jedes Element einen anderen `System.Music.Artist` Wert (oder gar keinen Wert) haben.

Ein Eigenschaftenhandler übersetzt in einer Datei gespeicherte Daten in ein strukturiertes Schema, das von erkannt wird und von Windows Explorer, Windows Search und anderen Anwendungen aufgerufen werden kann. Diese Systeme können dann mit dem Eigenschaftenhandler interagieren, um Eigenschaften in die Datei zu schreiben und daraus zu lesen. Die übersetzten Daten werden programmgesteuert verfügbar gemacht und dem Benutzer über den Windows-Explorer in einer Vielzahl von Kontexten angezeigt, einschließlich Detailansicht, Infotips, Detailbereich, Eigenschaftenseiten usw. Jeder Eigenschaftenhandler ist einem bestimmten Dateityp zugeordnet, der durch die Dateierweiterung identifiziert wird. Entwickler sollten einen Eigenschaftenhandler implementieren, der das native Format ihres Dateityps erzeugt und nutzt, z. B. .jpg oder .png, oder den In-Memory Property Store verwenden, der das MS-PROPSTORE-Binärformat erzeugt und nutzt.

Das Windows Property System erstellt ein abstraktes Datenmodell, das eine Abstraktionsebene von einzelnen Dateiformaten bietet. Das abstrakte Datenmodell, das vom Windows Property System bereitgestellt wird, ist eine Methode zum Lesen und Schreiben eines erweiterbaren Sets benannter Werte, die einem Shellelement zugeordnet sind. Der Wertausdruck ist flexibel und unterstützt viele Datentypen und ist erweiterbar, sodass beliebige Daten (**VT \_ BLOB**) und Objekte als Wert ausgedrückt werden können.

Aufgrund der Abstraktion können Sie die Attribute oder Metadaten eines beliebigen Elements abfragen. Beispiele für Elemente, die abstrahiert werden können, sind Microsoft Office, ID3-Tags und AutoCAD und andere proprietäre Software von Drittanbietern. Wenn Sie über eine JPEG-Datei verfügen, können Sie die JPEG- und EXIF-Codecs verwenden, um die Bytes der Datei zu lesen und die Abmessungen des Bilds zu finden. Wenn Sie stattdessen über .png verfügen, benötigen Sie dafür einen anderen Codec und anderen Code. Die Verwendung Windows Eigenschaftensystem vermeidet diese Art von Problem. Wenn Sie einen neuen Dateityp implementieren, haben Sie die Möglichkeit, die vom Windows-Eigenschaftensystem angebotene einheitliche Abstraktion zu verwenden und anzugeben, wie Ihre Metadaten verwendet werden können. Aus diesen Gründen ist es immer vorzuziehen, die allgemeine Plattform zu verwenden, die vom Windows Property System bereitgestellt wird.

## <a name="development-scenarios"></a>Entwicklungsszenarien

Eigenschaften werden von Denk- und Consumers ausgedrückt. In diesem Kontext handelt es sich bei den Herstellern um die Eigenschafteneigenschaften im Windows-Eigenschaftensystem, und Die Verbraucher sind Anwendungen (und ihre Entwickler), die Eigenschafteninformationen aus diesem System nutzen. In der folgenden Tabelle sind die Verwendungsmöglichkeiten von Windows -Eigenschaftssystem und der -Teilnehmer aufgeführt.



| Verwendung des Windows-Eigenschaftensystems                                                                                                                                                                                            | Teilnehmer |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|
| Ein Baustein, der eine erweiterbare Registrierung von Eigenschaftenbeschreibungen, eine In-Memory-Eigenschaftenspeicherimplementierung und Dienste zum Binden an Eigenschaftenhandler, Konvertieren von Typen und Serialisieren von Eigenschaftenspeichern bietet. | Consumer    |
| Anwendungen, die Eigenschaften auf abstrakte Weise lesen und schreiben möchten.                                                                                                                                                       | Consumer    |
| Eigenschaftenbearbeiter, die neue Eigenschaften für das Eigenschaftensystem definieren, indem sie benutzerdefinierte Eigenschaftenschemas definieren und eigene Eigenschaftenhandler entwickeln.                                                                          | Producer    |
| Dateiformatbesitzer, die den Zugriff auf die eigenschaften aktivieren möchten, die in ihren benutzerdefinierten Dateiformaten gespeichert sind.                                                                                                                           | Producer    |



 

Consumers nutzen vorhandene Eigenschaften, Schemas und Eigenschaftenhandler. Eigenschaften, die für den Verbrauch verfügbar sind, umfassen Lese-/Schreibeigenschaften von Eigenschaftenhandlern für unterstützte Dateitypen und können auch einige benutzerdefinierte Eigenschaften enthalten. Verfügbare Schemas umfassen mindestens das Systemschema und manchmal auch andere. Ein Consumer kann eine Anwendung erstellen, um Metadaten zu nutzen, und eine Ansicht basierend auf dem Interpreten erstellen, unabhängig davon, in welchen Ordnern die Elemente gespeichert sind. Die Dateiordnerhierarchie ist irrelevant. Sie können z. B. alle Musikelemente nach einem bestimmten 30- oder 10-0-3-3-3-Titel angeben, ohne sich um den Speicherort solcher Elemente sorgen zu müssen. Dieses komplexe End-to-End-Szenario ist nicht auf das Windows-Eigenschaftensystem beschränkt, sondern umfasst mehrere verschiedene Komponenten, z. B. die Indizierungs- und Suchordner.

Eigenschaftenhersteller oder Entwickler von Drittanbietern sind Hersteller im Windows Property System. Überprüfen Sie beim Vorbereiten der Definition einer neuen Eigenschaft zunächst den Satz von Eigenschaften, die Windows definieren. Wenn Sie eine Finden, die Ihren Anforderungen entspricht, des Typs und der Semantik, die ihrer erforderlichen Verwendung entsprechen, verwenden Sie diese Eigenschaft, und erfinden Sie keine neue. Wenn Sie eine neue benutzerdefinierte Eigenschaft definieren, versuchen Sie, eine Vereinbarung mit anderen Entwicklern zu erhalten, die sie möglicherweise verwenden möchten, und veröffentlichen Sie das Ergebnis dieser Vereinbarung, damit sie der Community der Benutzer dieser Eigenschaft beitreten können.

Producers können die Vorteile der Windows Explorer-Funktionalität nutzen. Wenn Sie beispielsweise ein neues Bildformat schreiben und einen Eigenschaftenhandler implementieren, wird das neue Dateiformat im Windows verfügbar. Benutzer können dann ihre Fotos markieren und ihre Sammlung von Fotos basierend auf einer beliebigen Eigenschaft im Windows Property System pivotieren. Tatsächlich kann alles, was Shell mit Eigenschaften macht, von Drittanbietern in ihren eigenen Anwendungen verwendet werden. Dies umfasst das Gruppieren, Sortieren, Abfragen und Anzeigen vollständiger Eigenschaften. Die Benutzeroberfläche, die Windows Explorer bietet, kann größtenteils von Drittanbietern mit öffentlich verfügbaren APIs implementiert werden. Windows Der Explorer kann mithilfe dieser APIs ersetzt oder erweitert werden.

Aus Sicht einer Anwendung, die das Shell-Datenmodell verwendet, gibt es eine Vielzahl von Szenarien, die die Verwendung des Windows beinhalten. Medienverwaltungsanwendungen sind ein prominentes Beispiel. Zu den wichtigsten Eigenschaftensystemszenarien gehören Szenarien wie das Lesen der Schlüsselworteigenschaft eines Fotos oder das Festlegen der datetaken-Eigenschaft. Beispiele für End-to-End-Integrationsszenarien, die das Windows-Eigenschaftensystem ermöglicht, aber für die mehrere andere Komponenten erforderlich sind, umfassen das Anzeigen aller Bilder oder das Suchen eines Dokuments, das ein Schlüsselwort enthält.

## <a name="properties-and-windows-search"></a>Eigenschaften und Windows Suchen

Eigenschaften dienen sowohl für Producers als auch für Consumers, wenn sie eine Schnittstelle Windows Suche und Indizierung verwenden. Windows Die Suche verfügt über einen Cache von Eigenschaftswerten, die in der Implementierung des suchdiensts (Windows Search Service, WSS. Diese Eigenschaftswerte können programmgesteuert mithilfe des Windows Search OLE DB-Anbieters oder über [**ISearchFolderItemFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory)abgefragt werden, das Elemente in Suchergebnissen und abfragebasierten Sichten darstellt. Windows Die Suche erfasst und speichert eigenschaften, die von Filterhandlern oder Eigenschaftenhandlern ausgegeben werden, wenn ein Element wie ein Word-Dokument indiziert wird. Dieser Speicher wird verworfen und neu erstellt, wenn der Index neu erstellt wird.

> [!Note]  
> Denken Sie daran, dass Änderungen an Attributen zuvor definierter Eigenschaften beim erneuten Registrieren eines Schemas vom Indexer möglicherweise nicht beachtet werden. Die Lösung besteht entweder in der Neuerstellung des Indexes oder der Einführung neuer Eigenschaften, die die Änderungen widerspiegeln, anstatt alte zu aktualisieren (nicht empfohlen). Weitere Informationen finden Sie unter [Hinweis für Implementierer](#note-to-implementers) weiter unten in diesem Thema.

 

Beispielsweise möchte ein Entwickler, der eine Medienanwendung erstellt, benutzern der Anwendung alle verfügbaren Musiken eines bestimmten Interpreten zeigen. Die Anwendung würde dem Benutzer eine Liste der verfügbaren Interpreten bereitstellen und dann eine Liste aller verfügbaren Musik vom Interpreten generieren, die der Benutzer auswählt. Oder ein Endbenutzer möchte möglicherweise eine Abfrage für ?interpret:Schrift? ausführen und während der Suche der vollständigen Liste der verfügbaren Eigenschaften zur Verfügung gestellt werden. Dieses Beispiel umfasst die Verwendung des Shell-Namespace, der Eigenschaftenhandler und/oder das Abfragen des Indexes über einen der folgenden:

-   Eine Shell-Datenquelle.
-   Ein OLE DB-Anbieter.
-   Eine Gespeicherte Suchdatei (.search-ms), die zum Initiieren einer Abfrage verwendet wird, indem sie im Windows-Explorer zur Suchdatei navigiert oder programmgesteuert an [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) binden.

> [!Note]  
> Obwohl die -Eigenschaft nicht teil an diesem Medienanwendungsszenario ist, kann sie zum Erstellen einer Abfrage verwendet werden, die alle SEARCH-MS-Dateien in einem bestimmten `System.Kind` Bereich zurückgeben würde.

 

Die bevorzugte Möglichkeit, auf die Such-APIs zu Windows und Suchanwendungen zu erstellen, ist eine Shell-Datenquelle. [**ISearchFolderItemFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) ist eine Komponente, mit der Instanzen der Ordnerdatenquelle Suchen erstellt werden können. Dabei handelt es sich um eine Art "virtuelle" Datenquelle, die von der Shell bereitgestellt wird und Abfragen für andere Datenquellen im Shellnamespace ausführen und Ergebnisse aufzählen kann. Dies kann entweder mithilfe des Indexers oder durch manuelles Aufzählen und Überprüfen von Elementen in den angegebenen Geltungsbereichen erfolgen.

Drittanbieterentwickler können Anwendungen erstellen, die die Daten im Index über programmgesteuerte Abfragen nutzen, und die Daten im Index für benutzerdefinierte Datei- und Elementtypen erweitern, die durch Windows Search indiziert werden sollen. Wenn Sie Abfrageergebnisse in Windows Explorer anzeigen möchten, müssen Sie eine Shell-Datenquelle implementieren, bevor Sie einen Protokollhandler erstellen können, um den Index zu erweitern. Wenn jedoch alle Abfragen programmatisch (z.B. über OLE DB) sind und vom Code der Anwendung anstelle der Shell interpretiert werden, ist ein Shellnamespace weiterhin bevorzugt, aber nicht erforderlich. Für Windows ist ein Protokollhandler erforderlich, um Informationen zu Dateiinhalten abzurufen, z. B. Elemente in Datenbanken oder benutzerdefinierte Dateitypen. Während Windows Search den Namen und die Eigenschaften der Datei indizieren kann, enthält Windows keine Informationen zum Inhalt der Datei. Daher können solche Elemente nicht in der Windows Shell indiziert oder verfügbar gemacht werden. Durch Implementieren eines benutzerdefinierten Protokollhandlers können Sie diese Elemente verfügbar machen. Eine Liste der Handler, die durch das Entwicklerszenario identifiziert werden, das Sie erreichen möchten, finden Sie unter "Übersicht über Handler" in [Windows Search as a Development Platform (Suche als Entwicklungsplattform).](../search/-search-3x-wds-development-ovr.md)

> [!Note]  
> Eine Shell-Datenquelle wird manchmal als Shellnamespaceerweiterung bezeichnet. Ein Handler wird manchmal als Shellerweiterung oder Shellerweiterungshandler bezeichnet.

 

## <a name="note-to-implementers"></a>Hinweis für Implementierer

Aufgrund potenzieller Schwierigkeiten, die der Indexer bei der Nutzung des Schemas des Eigenschaftensystems haben kann, ist es wichtig, attribute sorgfältig und strategisch für die erste Version des Schemas zu definieren. Änderungen an Attributen (Typ, Spaltenbreite, indexierbar) werden nach der Registrierung eines Schemas nicht in der Datenbank widergespiegelt. Die einzige Möglichkeit, diese Änderungen zu erkennen, nachdem das Schema einmal auf einem System registriert wurde, wäre entweder das Neuerstellen des Indexes und das anschließende Registrieren des neuen Schemas oder das Registrieren des Schemas und das anschließende Erstellen einer neuen Eigenschaft für jede nachfolgende Version. z. B. `PKEY_GroupName_PropertyNameV2` `PKEY_GroupName_PropertyNameV3` , usw. Es wird nicht empfohlen, auf diese Weise neue Eigenschaften zu erstellen, da sich mehrere überflüssige Spalten auf die Systemleistung auswirken können.

## <a name="windows-property-system-documentation"></a>Windows Dokumentation zum Eigenschaftensystem

Der Rest dieser Dokumentation enthält die folgenden Abschnitte:

-   [Windows Entwicklerhandbuch für Das Eigenschaftensystem](property-system-developer-s-guide.md)

    Beschreibt ausführlich, wie die wichtigsten Entwicklungsszenarien mit dem Windows Property System implementiert werden.

-   [Referenz zum Eigenschaftensystem](property-system-reference.md)

    Dokumentiert die [Windows Eigenschaften,](props.md) [Eigenschaftenbeschreibungsschema,](property-description-schema.md) [Schnittstellen,](interfaces.md) [Funktionen,](functions.md) [Strukturen](structures.md)und [Konstanten, Enumerationen und Flags](constants--enumerations--and-flags.md) des Windows-Eigenschaftensystems.

-   [Eigenschaftensystem-Codebeispiele](property-system-code-samples.md)

    Beschreibt Beispiele, die die Verwendung des Windows-Eigenschaftensystems veranschaulichen.

## <a name="additional-resources"></a>Weitere Ressourcen

-   Informationen zum wiederverwenden der In-Memory Property Store finden Sie unter [Initialisieren von Eigenschaftenhandlern](building-property-handlers-property-handlers.md) und [**PSCreateMemoryPropertyStore.**](/windows/desktop/api/Propsys/nf-propsys-pscreatememorypropertystore)
-   Eine Spezifikation der Microsoft-Eigenschaft Store Binärdateiformat finden Sie unter [ \[ MS \_ \] PROPSTORE](/openspecs/windows_protocols/ms-propstore/39ea873f-7af5-44dd-92f9-bc1f293852cc).
-   Die Beziehung zwischen Windows Suche und Indizierung sowie die Erweiterung des Indexes werden in den folgenden Themen in Windows Search erläutert:
    -   [Entwickeln von Filterhandlern für die Windows Suche](../search/-search-ifilter-conceptual.md)
    -   [Entwickeln von Protokollhandlern für die Windows Suche](../search/-search-3x-wds-phaddins.md)
    -   [Entwickeln von Eigenschaftenhandlern für die Windows Suche](../search/-search-3x-wds-extidx-propertyhandlers.md)
    -   Informationen zum Download Windows 7 oder aktualisierten Windows Vista SDK finden Sie im [Windows SDK.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Entwicklerhandbuch für Das Eigenschaftensystem](property-system-developer-s-guide.md)
</dt> <dt>

[Referenz zum Eigenschaftensystem](property-system-reference.md)
</dt> <dt>

[Eigenschaftensystem-Codebeispiele](property-system-code-samples.md)
</dt> </dl>

 

 
