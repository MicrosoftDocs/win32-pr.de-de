---
description: Um den Inhalt und die Eigenschaften neuer Dateiformate und Datenspeicher zu indizieren, muss Microsoft Windows Search mit Add-Ins erweitert werden.
ms.assetid: 04ddcd97-c358-44d2-9092-a035436c50c9
title: Windows Search als Entwicklungsplattform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19041ac23c90006cc2f1b2f6146cb20a6b972fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750441"
---
# <a name="windows-search-as-a-development-platform"></a>Windows Search als Entwicklungsplattform

Um den Inhalt und die Eigenschaften neuer Dateiformate und Datenspeicher zu indizieren, muss Microsoft Windows Search mit Add-Ins erweitert werden.

Bevor Entwickler neuer Dateiformate und Datenspeicher von Drittanbietern diese Formate und Speicher in den Abfrage Ergebnissen in Windows-Explorer anzeigen können, muss der Entwickler die folgenden drei Schritte ausführen:

-   Implementieren Sie eine shelldatenquelle, um den Shellnamespace zu erweitern.
-   Machen Sie Elemente in einem Datenspeicher verfügbar (wenn Sie einen neuen Datenspeicher hinzufügen, da Sie indiziert werden müssen).
-   Entwickeln Sie einen Protokollhandler, damit Windows Search für die Indizierung auf die Daten zugreifen kann.

Dieses Thema ist wie folgt organisiert:

-   [Erste Schritte](#getting-started)
-   [Übersicht über Such Entwicklungsszenarien](#overview-of-search-development-scenarios)
    -   [Hinzufügen eines neuen Datenspeicher](#adding-a-new-data-store)
    -   [Hinzufügen eines neuen Datei Formats](#adding-a-new-file-format)
    -   [Verwenden von Windows-Suchergebnissen](#consuming-windows-search-results)
-   [Übersicht über Handler](#overview-of-handlers)
-   [Richtlinien für Add-in-Installer](#add-in-installer-guidelines)
-   [Hinweis für Implementierer](#note-to-implementers)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="getting-started"></a>Erste Schritte

Bevor Sie mit dem Erstellen einer Windows-Suchanwendung beginnen, sollten Sie daran denken, dass es sich um eine Shell-Datenquelle handelt. Eine shelldatenquelle erweitert den Shellnamespace und macht die Elemente in einem Datenspeicher verfügbar. Die Elemente im Datenspeicher können dann mithilfe eines Protokoll Handlers vom Windows-Suchsystem indiziert werden. Diese indirekte Methode für den Zugriff auf Windows Search durch Implementieren einer shelldatenquelle wird bevorzugt, da Sie Zugriff auf die vollständige Shellfunktionalität bietet. Auf diese Weise wird eine angemessene Benutzer Leistung sichergestellt.

Wenn Sie möchten, dass die Abfrageergebnisse in Windows-Explorer angezeigt werden, müssen Sie eine Shell-Datenquelle implementieren, bevor Sie einen Protokollhandler zum Erweitern des Indexes erstellen können. Wenn allerdings alle Abfragen Programm gesteuert werden (z. b. über OLE DB) und vom Code der Anwendung anstelle der Shell interpretiert werden, wird ein Shellnamespace weiterhin bevorzugt, ist aber nicht erforderlich.

Ein Protokollhandler ist erforderlich, damit Windows Informationen zum Inhalt der Datei, z. b. Elemente in Datenbanken oder benutzerdefinierten Dateitypen, abrufen kann. Obwohl der Name und die Eigenschaften der Datei in Windows Search indiziert werden können, hat Windows keine Kenntnis über den Inhalt der Datei. Folglich können solche Elemente in der Windows-Shell nicht indiziert oder verfügbar gemacht werden. Durch Implementieren eines benutzerdefinierten Protokoll Handlers können Sie diese Elemente verfügbar machen. Eine Liste mit Handlern, die durch das Entwickler Szenario identifiziert werden, das Sie zu erreichen versuchen, finden Sie unter [Übersicht über Handler](#overview-of-handlers).

## <a name="overview-of-search-development-scenarios"></a>Übersicht über Such Entwicklungsszenarien

Die häufigsten Entwicklungsszenarien in Windows Search lauten wie folgt:

-   [Hinzufügen eines neuen Datenspeicher](#adding-a-new-data-store)
-   [Hinzufügen eines neuen Datei Formats](#adding-a-new-file-format)
-   [Verwenden von Windows-Suchergebnissen](#consuming-windows-search-results)

### <a name="adding-a-new-data-store"></a>Hinzufügen eines neuen Datenspeicher

Sie benötigen nur dann einen shelldatenspeicher für Windows Search, wenn Sie einen neuen Datenspeicher hinzufügen, der indiziert werden soll. Ein Datenspeicher ist ein Repository von Daten, die für das shellprogrammierungs Modell als Container mithilfe einer shelldatenquelle verfügbar gemacht werden können. Die Elemente in einem Datenspeicher können dann vom Windows-Suchsystem mithilfe eines Protokoll Handlers indiziert werden. Der Protokollhandler implementiert das Protokoll für den Zugriff auf eine Inhaltsquelle im systemeigenen Format. Die [**isearchprotocol**](/windows/win32/api/Searchapi/nn-searchapi-isearchprotocol) -und [**ISearchProtocol2**](/windows/win32/api/Searchapi/nn-searchapi-isearchprotocol2) -Schnittstellen werden verwendet, um einen benutzerdefinierten Protokollhandler zu implementieren, um die Datenquellen zu erweitern, die indiziert werden können. Weitere Informationen zum Erstellen einer shelldatenquelle finden Sie unter [Implementieren der grundlegenden Ordner Objekt Schnittstellen](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

### <a name="adding-a-new-file-format"></a>Hinzufügen eines neuen Datei Formats

Wenn Sie ein neues benutzerdefiniertes Dateiformat hinzufügen, müssen Sie entweder einen Filter Handler oder einen Eigenschafts Handler entwickeln, aber nicht beides. Ein Filter ist eine Implementierung der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle. Er öffnet Dateien eines bestimmten Dateityps und filtert Eigenschaften und Textabschnitte für den Indexer. Filter sind Dateitypen zugeordnet, die durch Dateinamen Erweiterungen, MIME-Typen oder Klassen Bezeichner (CLSIDs) bezeichnet werden. Obwohl ein Filter mehrere Dateitypen verarbeiten kann, kann jeder Dateityp nur mit einem einzigen Filter verwendet werden.

Ein Eigenschafts Handler übersetzt in einer Datei gespeicherte Daten in ein strukturiertes Schema, das von erkannt wird und auf das Windows-Explorer, Windows Search und andere Anwendungen zugreifen können. Diese Systeme können dann mit dem Eigenschaften Handler interagieren, um Eigenschaften in eine und aus einer Datei zu schreiben und zu lesen. Zu den übersetzten Daten zählen Detailansicht, Infotipps, Detailbereich, Eigenschaften Seiten usw. Jeder Eigenschaften Handler ist einem bestimmten Dateityp zugeordnet, der durch die Dateinamenerweiterung gekennzeichnet ist. Sie benötigen einen Eigenschaften Handler, um Folgendes zu tun:

-   Eigenschaften nicht indizierter Elemente in der Benutzeroberfläche anzeigen.
-   Unterstützung für das Schreiben von Eigenschaften

### <a name="consuming-windows-search-results"></a>Verwenden von Windows-Suchergebnissen

In den folgenden Abschnitten werden verschiedene Möglichkeiten zur Nutzung der Windows-Suchergebnisse beschrieben:

-   [Abfragen von Daten](#querying-data)
-   [Abfragen von Remote Daten speichern (Verbund Suche)](#querying-remote-data-stores-federated-search)
-   [Indizieren von Dateien und Elementen](#indexing-files-and-items)
-   [Indizieren eines Datenspeicher](#indexing-a-data-store)
-   [Verwalten des Indizierungs Prozesses](#managing-the-indexing-process)
-   [Integrieren des Windows-Eigenschaften Systems in Windows Search-Anwendungen](#integrating-the-windows-property-system-with-windows-search-applications)

### <a name="querying-data"></a>Abfrage von Daten

Entwickler, die Anwendungen auf der Grundlage des kombinierten Windows Search-und Windows-Eigenschaften Systems schreiben, können unabhängig von der Anwendung oder dem Dateityp auf Dateien und Elemente zugreifen. Es gibt zwei Möglichkeiten für Anwendungen, auf die Indexer-Daten zuzugreifen:

-   Anwendungen kommunizieren direkt mit OLE DB, indem Sie Windows Search-Structured Query Language (SQL)-Abfragen an den Windows Search-OLE DB Anbieter senden, um Ergebnisse abzurufen. Abfragen können manuell oder mithilfe der [**isearchqueryhelper**](/windows/win32/api/Searchapi/nn-searchapi-isearchqueryhelper) -Schnittstelle erstellt werden, um die SQL-Such Schlüsselwörter und die Erweiterte Abfrage Syntax (AQS) zu generieren.
-   Anwendungen arbeiten über die shellschicht. Der Vorteil der shellschicht besteht darin, dass Sie auch andere Quellen wie grep unterstützt. Der Nachteil ist jedoch, dass nicht alle Indexer-Features verfügbar sind.

Eine andere Möglichkeit ist die Verwendung der Protokolle Search-MS://und Search://, die URL-basierte Suchvorgänge ausführen, die über Windows Explorer gerendert werden. Diese Option ermöglicht die Entwicklung mit leichtesten Gewichtungen, gibt jedoch keine Ergebnisse oder Benutzer Auswahl aus der Ergebnis Ansicht an die aufrufenden Anwendung zurück. Ebenso wie andere Protokolle können Suchanwendungen von Drittanbietern die Protokolle Search-MS://und Search://übernehmen, wenn die Anwendungen den erforderlichen Featuresatz entsprechen. Weitere Informationen zum Abfragen finden Sie unter [Querying Process in Windows Search](querying-process--windows-search-.md) (Programm gesteuertes Abfragen [des Indexes](-search-3x-wds-qryidx-overview.md)).

### <a name="querying-remote-data-stores-federated-search"></a>Abfragen von Remote Daten speichern (Verbund Suche)

In Windows 7 und höher bietet die Verbund Suche einen neuen Suchanbieter, der Remote Datenspeicher über Webserver über das [OpenSearch](https://github.com/dewitt/opensearch) -Protokoll abfragt und die Ergebnisse als RSS-oder Atom-XML-Feeds auflistet. Suchconnectors sind Namespace-Verbindungen, die das Ordner Verhalten mithilfe eines Such Anbieters simulieren. Weitere Informationen zum Durchsuchen von Verbund-zu-Remote-Daten speichern in Windows 7 finden Sie unter [Federated Search in Windows](-search-federated-search-overview.md).

### <a name="indexing-files-and-items"></a>Indizieren von Dateien und Elementen

Der indizierte Inhalt basiert auf den Datei-und Datentypen, die durch in Windows Search enthaltene Add-Ins und die standardmäßigen Einschluss-und Ausschluss Regeln für Ordner im Dateisystem unterstützt werden. Beispielsweise unterstützen die in der Fenster Suche enthaltenen Filter über 200 allgemeine Datentypen, einschließlich Microsoft Office Dokumenten, Microsoft Outlook-e-Mail (in Verbindung mit dem MAPI-Protokollhandler), nur-Text-Dateien, HTML und viele mehr. Eine vollständige Liste der Dateitypen, die nativ unterstützt werden, finden Sie unter [Was ist im Index enthalten](-search-3x-wds-included-in-index.md).

Der Index kann mit Eigenschaften Handlern und Filtern erweitert werden, um den Inhalt und die Eigenschaften neuer Dateiformate für den Index und Windows Explorer verfügbar zu machen. Filter sind eine Implementierung der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle. Es gibt zwei Arten von Filtern: einen, der mit einzelnen Elementen interagiert, z. b. Dateien und einen, der mit Containern interagiert, wie z. b. Ordnern. Filter sind mehr zweckmäßig, da Sie Segmentieren von Daten, Text Inhalt, einige Eigenschaften und mehrere Sprachen unterstützen.

Im Gegensatz dazu haben Eigenschafts Handler einen spezifischeren Zweck:, um die Eigenschaften bestimmter Dateitypen verfügbar zu machen, die durch Dateinamen Erweiterungen identifiziert werden. Ein Eigenschafts Handler für einen Dateityp kann Get-und Set-Eigenschaften aktivieren und die diesem Dateityp zugeordneten Eigenschaften auflisten. Im Gegensatz zu Filtern unterstützen Eigenschaften Handler keine Daten oder Textinhalte, und Eigenschaften Handler können nicht angeben, in welcher Sprache eine Text Eigenschaft enthalten ist, es sei denn, Sie unterstützen das Schreiben von Eigenschaften.

### <a name="indexing-a-data-store"></a>Indizieren eines Datenspeicher

Der Index kann mit Protokoll Handlern erweitert werden, um den Zugriff auf proprietäre Datenspeicher bereitzustellen. Beispielsweise erfordern Dateien und Elemente, die in nicht-Dateisystem-Daten speichern (z. b. Datenbanken und e-Mail-Speicher) enthalten sind, einen Protokollhandler, der von einer URL zu einem Stream zugeordnet werden kann Protokollhandler können optional auch die richtigen Filter bestimmen, die zum Extrahieren von Informationen aus einem Stream verwendet werden sollen. Filter listet die Datenspeicher-URLs auf. Die Elemente werden dann einzeln mithilfe des richtigen Filter-und/oder Eigenschaften Handlers indiziert. Weitere Informationen finden Sie unter [Erweitern des Indexes](-search-3x-wds-extidx-overview.md).

### <a name="managing-the-indexing-process"></a>Verwalten des Indizierungs Prozesses

Anwendungsentwickler können den Umfang und die Häufigkeit der Windows Search-Indizierung mithilfe verschiedener Verwaltungs Schnittstellen steuern. Diese Schnittstellen enthalten Funktionen zum Hinzufügen und Entfernen der Verzeichnisse, die der Indexer auf Änderungen überprüft, den Index von Änderungen an Daten manuell benachrichtigen, den Status des Indexers überprüfen und die erneute Indizierung einiger oder aller Daten erzwingen. Weitere Informationen finden Sie unter [Managing the index](-search-3x-wds-mngidx-overview.md).

### <a name="integrating-the-windows-property-system-with-windows-search-applications"></a>Integrieren des Windows-Eigenschaften Systems in Windows Search-Anwendungen

Das Windows-Eigenschaften System ist ein erweiterbares Lese-/Schreibsystem mit Daten Definitionen, das eine einheitliche Methode zum Ausdrücken von Metadaten über shellelemente bietet. Mit dem Windows-Eigenschaften System in Windows Vista und höher können Sie Metadaten für shellelemente speichern und abrufen. Ein shellelement ist ein beliebiges einzelnes Element, z. b. eine Datei, ein Ordner, eine e-Mail oder ein Kontakt. Eine Eigenschaft ist ein einzelner Metadatenelement, das einem shellelement zugeordnet ist. Eigenschaftswerte werden als [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Struktur ausgedrückt.

Eine umfassende Liste allgemeiner Eigenschaften ist für eine Reihe von allgemeinen Elementtypen enthalten, z. b. Fotos, Musik, Dokumente, Nachrichten, Kontakte und Dateien. Entwickler können auch Ihre eigenen Eigenschaften für die Plattform einführen, wenn keine vorhandene Eigenschaft Ihren Anforderungen entspricht. Weitere Informationen zum Integrieren von Anwendungen in das Windows-Eigenschaften System finden Sie unter [entwickeln von Eigenschaften Handlern](-search-3x-wds-extidx-propertyhandlers.md).

## <a name="overview-of-handlers"></a>Übersicht über Handler

Ein Handler ist ein Component Object Model (com)-Objekt, das Funktionen für ein shellelement bereitstellt. Die meisten shelldatenquellen bieten ein erweiterbares System zum Binden von Handlern an Elemente. Beispielsweise verwendet der Dateisystem Ordner das Zuordnungs System, um die Handler für einen bestimmten Dateityp zu suchen. Für jeden Dateityp ist ein bestimmter Handler erforderlich. Ein Filter Handler ist für den Adobe Acrobat. PDF-Dateityp erforderlich, z. b., wenn ein anderer Filter Handler für das doc-Dateiformat erforderlich ist usw.

Verschiedene Handler haben eine gewisse Gemeinsamkeit. In Windows Vista und höher müssen alle Handler eine der folgenden Schnittstellen verwenden, um den Handler zu initialisieren: [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)oder [**iitinitializewithfile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile).

In der folgenden Tabelle sind allgemeine Entwickler Aufgaben, der Typ des Handlers, der für die einzelnen Aufgaben erforderlich ist, sowie ein Link zu konzeptionellen Informationen zum Ausführen der einzelnen Aufgaben aufgeführt.



| Aufgabe                                                                                                                                                            | Handler                          | Konzeptionelle Informationen                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Zugreifen auf die Eigenschaften einer Datei zur Indizierung                                                                                                                 | Eigenschaften Handler                 | [Entwickeln von Eigenschaften Handlern](-search-3x-wds-extidx-propertyhandlers.md)<br/> [System definierte Eigenschaften für benutzerdefinierte Dateiformate](-shell-systemdefinedpropertiesforfileformats.md)<br/> |
| Das Hinzufügen von Zwischenablage Formaten für das Datenobjekt ([**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)) eines Elements (Datenobjekte werden in Drag & Drop-und Kopier-/einfügeszenarien verwendet.) | Datenobjekthandler              | [Erstellen von Daten Handlern](/previous-versions/windows/desktop/legacy/cc144163(v=vs.85))                                                                                                                                                          |
| Hinzufügen von Verben für ein Element, die häufig in einem Kontextmenü angezeigt werden                                                                                         | Kontextmenü Handler            | [Erstellen von Kontextmenü Handlern](../shell/context-menu-handlers.md)<br/> [Anpassen eines Kontextmenüs mithilfe dynamischer Verben](../shell/shortcut-menu-using-dynamic-verbs.md)<br/>                         |
| Zuordnen eines Dateityps zu einem bestimmten Symbol                                                                                                                    | Symbol Handler                     | [Erstellen von Symbol Handlern](../shell/how-to-create-icon-handlers.md)                                                                                                                                                          |
| Erstellen von Eigenschaften Blättern mit UI-Bildern und Steuerelementen, die eine benutzerdefinierte Interaktion mit einem Dateityp zulassen                                                          | Eigenschaftenblatthandler           | [Eigenschaften Blatt Handler](/previous-versions/windows/desktop/legacy/cc144106(v=vs.85))                                                                                                                                                    |
| Aktivieren eines Elementtyps zur Unterstützung von Drag & Drop-und Kopier-/Einfüge Szenarien                                                                                         | Drop-Handler                     | [Übertragen von shellobjekten mit Drag & Drop und der Zwischenablage](/previous-versions/windows/desktop/legacy/bb776905(v=vs.85))                                                                                                                      |
| Extrahieren von Text-und Dokumenteigenschaften für die Indizierung                                                                                                  | Filter Handler                   | [Entwickeln von Filter Handlern](-search-ifilter-conceptual.md)                                                                                                                                           |
| Indizieren eines neuen Dateityps                                                                                                                                        | Filter Handler, Eigenschaften Handler | [Entwickeln von Filter Handlern](-search-ifilter-conceptual.md)<br/> [Entwickeln von Eigenschaften Handlern](-search-3x-wds-extidx-propertyhandlers.md)<br/>                                          |
| Indizieren des Inhalts eines Datenspeicher                                                                                                                           | Protokollhandler                 | [Entwickeln von Protokoll Handlern](-search-3x-wds-phaddins.md)                                                                                                                                            |
| Anzeigen einer vereinfachten Ansicht des shellelements im Vorschaubereich von Windows-Explorer                                                                             | Vorschau Handler                  | [Vorschau Handler](../shell/preview-handlers.md)                                                                                                                                                             |
| Bereitstellen von Popup Text, wenn ein Mauszeiger über ein UI-Objekt bewegt wird                                                                                                      | QuickInfo-Handler                  | [Erstellen von Shellerweiterungs Handlern](../shell/handlers.md) (infotip-Anpassung)                                                                                                                            |
| Bereitstellen eines statischen Bilds zur Darstellung eines shellelements                                                                                                              | Miniatur Ansichts Handler                | [Miniatur Ansichts Handler](/previous-versions/windows/desktop/legacy/cc144118(v=vs.85))                                                                                                                                                        |



 

In der folgenden Tabelle sind Handler und Schnittstellen zum Implementieren der einzelnen Handlertypen aufgeführt.



| Handler                | Schnittstellen                                                                                                                                                                                                                                                                                                                                                                |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Drop-Handler           | [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget), [**idroptargethelper**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idroptargethelper), [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile), [**ishellextinit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)                                                                                                                                                                                                      |
| Datenobjekthandler    | [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject), [ **IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)                                                                                                                                                                                                                                                                                                  |
| Filter Handler         | [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)<br/>                                                                                                                                                                                                                                                                                                                             |
| Symbol Handler           | [**Iextracticon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona)<br/> Optional: [**ipersistent**](/windows/win32/api/objidl/nn-objidl-ipersist), [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)<br/>                                                                                                                                                                                                                                 |
| QuickInfo-Handler        | [**Iqueryinfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo)                                                                                                                                                                                                                                                                                                                                        |
| Vorschau Handler        | [**IPreviewHandler**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler)                                                                                                                                                                                                                                                                                                                              |
| Eigenschaften Handler       | [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)                                                                                                                                                                                                                                                                                                                           |
| Protokollhandler       | [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), [**isearchprotocol**](/windows/win32/api/Searchapi/nn-searchapi-isearchprotocol), [**iurlaccessor**](/windows/win32/api/Searchapi/nn-searchapi-iurlaccessor)<br/> Optional: [**ISearchProtocol2**](/windows/win32/api/Searchapi/nn-searchapi-isearchprotocol2), [**IUrlAccessor2**](/windows/win32/api/Searchapi/nn-searchapi-iurlaccessor2), [**IUrlAccessor3**](/windows/win32/api/Searchapi/nn-searchapi-iurlaccessor3), [**IUrlAccessor4**](/windows/win32/api/Searchapi/nn-searchapi-iurlaccessor4)<br/> |
| Eigenschaftenblatthandler | [**Ishellextinit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit), [ **ishellpropsheetext**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)                                                                                                                                                                                                                                                                              |
| Kontextmenü Handler  | [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu), [**IExplorerCommand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iexplorercommand), [**ishellextinit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)                                                                                                                                                                                                                                          |
| Miniatur Ansichts Handler      | [**IThumbnailProvider**](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider)                                                                                                                                                                                                                                                                                                                        |



 

> [!Note]  
> Ein Eigenschaften Handler wird manchmal als Metadatenhandler kown. Eine shelldatenquelle wird manchmal als Shellnamespace Erweiterung bezeichnet. Ein Dateityp Handler wird manchmal als Shellerweiterungs Handler oder Shellerweiterung bezeichnet.

 

Weitere Informationen zum Erstellen von Handlern finden Sie unter [Erstellen von Shellerweiterungs Handlern](../shell/handlers.md). Weitere Informationen zu Eigenschaften finden Sie unter [Windows](../properties/windows-properties-system.md)-Eigenschaften System.

## <a name="add-in-installer-guidelines"></a>Richtlinien für Add-in-Installer

Beachten Sie beim Erstellen eines Add-in-Installers die folgenden Richtlinien:

-   Das Installationsprogramm muss entweder das exe-oder das MSI-Installationsprogramm verwenden.
-   Anmerkungen zu dieser Version müssen bereitgestellt werden.
-   Ein Eintrag zum **Hinzufügen/Entfernen von Programmen** muss für jedes installierte Add-in erstellt werden.
-   Das Installationsprogramm muss alle Registrierungs Einstellungen für einen bestimmten Dateityp oder-Speicher übernehmen, den das aktuelle Add-in versteht.
-   Wenn ein vorheriges Add-in überschrieben wird, sollte das Installationsprogramm den Benutzer benachrichtigen.
-   Wenn ein neueres Add-in ein vorangegandes Add-in überschrieben hat, sollte der Benutzer in der Lage sein, die vorherige Add-in-Funktionalität wiederherzustellen und das Standard-Add-in für diesen Dateityp oder-Speicher wieder als Standard zu nutzen.

## <a name="note-to-implementers"></a>Hinweis für Implementierer

Vor dem Erstellen eines Filters oder Eigenschaften Handlers sollten Entwickler Folgendes berücksichtigen:

-   Diese Handler sind Prozess interne Erweiterungen, die in Prozesse geladen werden, die Sie nicht steuern, wie z. b. den Filterdaemonprozess, Windows-Explorer (grep-Suche) und Hosts von Drittanbietern wie Windows Mail).
-   Sie müssen sicheren Code schreiben, der robust genug ist, um willkürlich beschädigte Formen Ihres Datei Formats zu verarbeiten, die für Angriffe auf das System erstellt wurden.
-   Das Add-in darf keine Ressourcen ausgeben, die für die Host Prozesse Probleme verursachen.
-   Das Add-in darf nicht abstürzen, da dadurch auch die Host Prozesse abstürzen und der Filter Vorgang verlangsamt wird.
-   Da diese Handler in einem Hintergrundsystem Prozess ausgeführt werden, müssen Sie schnell mit einem minimalen CPU-und e/a-Verbrauch ausgeführt werden, um die Leistungsanforderungen des Systems zu erfüllen.

Daher sollten diese Add-Ins von Entwicklern mit Fachkenntnissen zum Erstellen von Code auf Systemebene geschrieben werden.

## <a name="additional-resources"></a>Weitere Ressourcen

-   Weitere Informationen zum Erstellen einer shelldatenquelle finden Sie unter [Implementieren der grundlegenden Ordner Objekt Schnittstellen](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).
-   Informationen zu Datenquellen, für die das standardmäßige [**\_ shellansichts**](/windows/win32/api/shlobj_core/ns-shlobj_core-sfv_create) Objekt (defview) der Shell verwendet werden muss, finden Sie unter [Implementieren einer Ordneransicht](../lwef/nse-folderview.md), der [**shkreateshellfolderview**](/windows/win32/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview) -Funktion und der SFV Create-Struktur. Datenquellen, die das standardmäßige Objekt Ansichts Objekt (defview) der Shell verwenden, müssen die folgenden Schnittstellen implementieren: [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), [**IShellFolder2**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder2), [**ipersistfolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder), [**IPersistFolder2**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2)und (optional) [**IPersistFolder3**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder3). Wenn die **IShellFolder** -Implementierung " **shaliateshellfolderview** " nicht zum Erstellen der defview verwendet, benötigt das shellansichts Objekt möglicherweise [**ifolderview**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifolderview).
-   [**Isearchfolderitemfactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) ist die primäre Schnittstelle für Consumer der Shell-Datenquelle, die als dbfolder bezeichnet wird. Weitere Informationen zu dbfolder finden Sie in der Beschreibung der Str-Analyse \_ \_ mit \_ Eigenschafts Konstanten unter [**Binden von Kontext Zeichenfolgen-Schlüsseln**](../shell/str-constants.md). Siehe auch [Association Arrays](/previous-versions/windows/desktop/legacy/ee872122(v=vs.85)) und [**ipropertysystem:: getpropertydescriptionlistfromstring**](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring).
-   Weitere Informationen zu OLE DB finden Sie unter Übersicht über die [OLE DB Programmierung](https://msdn.microsoft.com/library/5d8sd9we(VS.71).aspx). Informationen zu den .NET Framework Datenanbieter für OLE DB finden Sie in der Dokumentation zum [System. Data. OleDb-Namespace](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1) .
-   Informationen zu den von der Community unterstützten Nachrichten Boards für Suchtechnologien finden Sie unter [Windows: Suchforen](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads) auf MSDN.
-   Verwandte Codebeispiele finden Sie unter [Codebeispiele für Windows-Suche](-search-samples-ovw.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Windows Search](-search-3x-wds-overview.md)
</dt> <dt>

[Von Windows Search unterstützte Sprachen](-search-3x-wds-language-support.md)
</dt> <dt>

[Verwenden von verwaltetem Code mit Shelldaten und Windows Search](-search-3x-wds-managed-code.md)
</dt> <dt>

[Entwicklerhandbuch für Windows Search](-search-developers-guide-entry-page.md)
</dt> </dl>

 

 
