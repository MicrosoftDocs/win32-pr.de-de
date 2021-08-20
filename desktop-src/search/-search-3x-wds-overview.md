---
description: Windows Die Suche ist eine Desktopsuchplattform, die über Funktionen für die sofortige Suche für die gängigsten Dateitypen und Datentypen verfügt, und Drittanbieterentwickler können diese Funktionen auf neue Dateitypen und Datentypen erweitern.
ms.assetid: 6da601c6-3742-40ad-99f2-8817f7f642b3
title: Übersicht über Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a38b757936e9f960d71ac5d1a9759208b4b580af2526e23d4e5d88cde41a206
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033128"
---
# <a name="windows-search-overview"></a>Übersicht über Windows Search

Windows Die Suche ist eine Desktopsuchplattform, die über Funktionen für die sofortige Suche für die gängigsten Dateitypen und Datentypen verfügt, und Drittanbieterentwickler können diese Funktionen auf neue Dateitypen und Datentypen erweitern.

Dieses Thema ist wie folgt organisiert:

-   [Introduction (Einführung)](#introduction)
    -   [Windows Search-Dienst](#windows-search-service)
    -   [Entwicklungsplattform](#development-platform)
    -   [Benutzeroberfläche](#user-interface)
-   [Technische Voraussetzungen](#technical-prerequisites)
    -   [SDK-Download und -Inhalt](#sdk-download-and-contents)
-   [Windows Suchen der SDK-Dokumentation](#windows-search-sdk-documentation)
-   [Verlauf der Windows Suche](#history-of-windows-search)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Windows Search ist eine Standardkomponente von Windows 7 und Windows Vista und standardmäßig aktiviert. Windows Search ersetzt Windows Desktopsuche (WDS), die als Add-In für Windows XP und Windows Server 2003 verfügbar war.

Windows Die Suche besteht aus drei Komponenten:

-   [Windows-Suchdienst](#windows-search-service) (WSS)
-   [Entwicklungsplattform](#development-platform)
-   [User interface (Benutzeroberfläche)](#user-interface)

### <a name="windows-search-service"></a>Windows Search-Dienst

Der WSS organisiert die extrahierten Features einer Sammlung von Dokumenten. Das Windows-Suchprotokoll ermöglicht einem Client die Kommunikation mit einem Server, der eine WSS hostet, sowohl um Abfragen auszugeben als auch einem Administrator die Verwaltung des Indizierungsservers zu ermöglichen. Bei der Verarbeitung von Dateien analysiert WSS eine Reihe von Dokumenten, extrahiert nützliche Informationen und organisiert dann die extrahierten Informationen so, dass Eigenschaften dieser Dokumente als Reaktion auf Abfragen effizient zurückgegeben werden können.

Eine Sammlung von Dokumenten, die abgefragt werden können, umfasst einen Katalog, der die höchste Organisationseinheit in Windows Search darstellt. Ein Katalog stellt einen Satz indizierter Dokumente dar, die abgefragt werden können. Ein Katalog besteht aus einer Eigenschaftentabelle mit dem Text oder Wert und der entsprechenden Position (Gebietsschema), die in Spalten der Tabelle gespeichert sind. Jede Zeile der Tabelle entspricht einem separaten Dokument im Bereich des Katalogs, und jede Spalte der Tabelle entspricht einer -Eigenschaft. Ein Katalog kann einen invertierten Index (für den schnellen Wortabgleich) und einen Eigenschaftencache (zum schnellen Abrufen von Eigenschaftswerten) enthalten.

Der Indexerprozess wird als Windows Dienst implementiert, der im LocalSystem-Konto ausgeführt wird und immer für alle Benutzer ausgeführt wird (auch wenn kein Benutzer angemeldet ist), wodurch Windows Search Folgendes erreichen kann:

-   Verwalten Sie einen Index, der von allen Benutzern gemeinsam genutzt wird.
-   Beibehalten von Sicherheitseinschränkungen für den Inhaltszugriff.
-   Verarbeiten von Remoteabfragen von Clientcomputern im Netzwerk.

Die Suchdienst wurde entwickelt, um die Benutzerfreundlichkeit und Systemleistung bei der Indizierung zu schützen. Die folgenden Bedingungen bewirken, dass der Dienst die Indizierung zurückdrosselt oder anzuhalten:

-   Hohe CPU-Auslastung durch nicht suchbezogene Prozesse.
-   Hohe System-E/A-Rate, einschließlich Dateilese- und Schreibvorgänge, Seitendatei- und Dateicache-E/A und zugeordneter Datei-E/A.
-   Geringe Arbeitsspeicherverfügbarkeit.
-   Niedrige Akkulaufzeit.
-   Wenig Speicherplatz auf dem Laufwerk, auf dem der Index gespeichert wird.

### <a name="development-platform"></a>Entwicklungsplattform

Die bevorzugte Möglichkeit, auf die Such-APIs zuzugreifen und Windows Search-Anwendungen zu erstellen, ist eine Shell-Datenquelle. Eine Shell-Datenquelle ist eine Komponente, die verwendet wird, um den Shellnamespace zu erweitern und Elemente in einem Datenspeicher verfügbar zu machen. Ein Datenspeicher ist ein Repository von Daten. Ein Datenspeicher kann für das Shell-Programmiermodell als Container verfügbar gemacht werden, der eine Shell-Datenquelle verwendet. Die Elemente in einem Datenspeicher können vom Windows Search-System mithilfe eines Protokollhandlers indiziert werden.

Beispielsweise ist [ISearchFolderItemFactory](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) eine Komponente, die Instanzen der Suchordnerdatenquelle erstellen kann. Dabei handelt es sich um eine Art "virtuelle" Datenquelle, die von der Shell bereitgestellt wird und Abfragen über andere Datenquellen im Shellnamespace ausführen und Ergebnisse auflisten kann. Dies kann entweder mithilfe des Indexers oder durch manuelles Aufzählen und Überprüfen von Elementen in den angegebenen Bereichen möglich sein. Mit dieser Schnittstelle können Sie die Parameter der Suche mithilfe von Methoden einrichten, die Suchordner erstellen und ändern. Wenn Methoden dieser Schnittstelle nicht aufgerufen werden, werden stattdessen Standardwerte verwendet.

Der indirekte Zugriff auf die Windows Search-Funktion über das Shell-Datenmodell wird bevorzugt, da es Zugriff auf die vollständige Shell-Funktionalität auf der Ebene des Shell-Datenmodells bietet. Sie können z. B. den Bereich einer Suche auf eine Bibliothek festlegen (ein Feature, das in Windows 7 und höher verfügbar ist), um die Bibliotheksordner als Bereich der Abfrage zu verwenden. Windows Die Suche aggregiert dann die Suchergebnisse von diesen Speicherorten, wenn sie sich in unterschiedlichen Indizes befinden (wenn sich die Ordner auf verschiedenen Computern befinden). Die Shell-Datenebene erstellt auch eine vollständigere Ansicht der Eigenschaften von Elementen, die einige Eigenschaftswerte synthetisiert. Es bietet auch Zugriff auf Suchfunktionen für Datenspeicher, die nicht von Windows Search indiziert werden. Beispielsweise können Sie ein USB-Speichergerät (Universal Serial Bus), ein portables Gerät, das das MTP-Protokoll verwendet, oder einen FTP-Server (File Transfer Protocol) über die Shell-Datenquellen durchsuchen, die Zugriff auf diese Speichersysteme bieten. Dadurch wird eine bessere Benutzererfahrung sichergestellt.

Windows Die Suche verfügt über einen Cache von Eigenschaftswerten, der in der Implementierung des Windows Search Service (WSS) verwendet wird. Diese Eigenschaftswerte können programmgesteuert mithilfe des Windows Search OLE DB-Anbieters oder über [ISearchFolderItemFactory](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory)abgefragt werden, das Elemente in Suchergebnissen und abfragebasierten Ansichten darstellt. Windows Die Suche sammelt und speichert eigenschaften, die von Filterhandlern oder Eigenschaftenhandlern ausgegeben werden, wenn ein Element wie ein Word-Dokument indiziert wird. Dieser Speicher wird verworfen und neu erstellt, wenn der Index neu erstellt wird.

Drittanbieterentwickler können Anwendungen erstellen, die die Daten im Index über programmgesteuerte Abfragen nutzen, und die Daten im Index für benutzerdefinierte Datei- und Elementtypen erweitern, die durch Windows Search indiziert werden sollen. Wenn Sie Abfrageergebnisse in Windows Explorer anzeigen möchten, müssen Sie eine Shell-Datenquelle implementieren, bevor Sie einen Protokollhandler zum Erweitern des Indexes erstellen können. Wenn jedoch alle Abfragen programmatisch sind (z.B. über OLE DB) und nicht vom Code der Anwendung und nicht von der Shell interpretiert werden, wird ein Shellnamespace immer noch bevorzugt, aber nicht benötigt.

Für Windows ist ein Protokollhandler erforderlich, um Informationen zu Dateiinhalten abzurufen, z. B. Elemente in Datenbanken oder benutzerdefinierte Dateitypen. Während Windows Search den Namen und die Eigenschaften der Datei indizieren kann, enthält Windows keine Informationen zum Inhalt der Datei. Daher können solche Elemente nicht in der Windows Shell indiziert oder verfügbar gemacht werden. Durch Implementieren eines benutzerdefinierten Protokollhandlers können Sie diese Elemente verfügbar machen. Eine Liste der Handler, die durch das Entwicklerszenario identifiziert werden, das Sie erreichen möchten, finden Sie unter "Übersicht über Handler" in [Windows Search as a Development Platform (Suche als Entwicklungsplattform).](-search-3x-wds-development-ovr.md)

> [!Note]  
> Eine Shell-Datenquelle wird manchmal als Shellnamespaceerweiterung bezeichnet. Ein Handler wird manchmal als Shellerweiterung oder Shellerweiterungshandler bezeichnet.

 

### <a name="user-interface"></a>Benutzeroberfläche

In Windows Vista und höher ist Windows Search in alle Explorer-Fenster Windows integriert, um sofortigen Zugriff auf die Suche zu erhalten. Dadurch können Benutzer schnell nach Dateien und Elementen nach Dateinamen, Eigenschaften und Volltextinhalten suchen. Die Ergebnisse können auch weiter gefiltert werden, um die Suche zu verfeinern. Im Folgenden finden Sie einige weitere Features von Windows Search:

-   Ein Sofortsuchfeld in jedem Fenster ermöglicht die sofortige Filterung aller aktuell angezeigten Elemente. Direktsuchfelder werden im Startmenü angezeigt, um nach Programmen oder Dateien zu suchen, und in der oberen rechten Ecke aller Windows Explorer-Fenster, um die angezeigten Ergebnisse zu filtern. Die sofortige Suche ist auch in einige andere features Windows integriert, z. B. Windows Media Player, um verwandte Dateien zu suchen.
-   Dokumente können mit Schlüsselwörtern gekennzeichnet werden, um sie nach benutzerdefinierten Kriterien zu gruppieren, die vom Benutzer definiert werden. Tags sind Metadatenelemente, die vom Benutzer oder den Anwendungen zugewiesen werden, um die Suche nach Dateien basierend auf Schlüsselwörtern zu vereinfachen, die sich möglicherweise nicht im Elementnamen oder -inhalt befinden. Beispielsweise kann ein Satz von Bildern als "Arizona Vacation 2009" markiert werden, um später schnell abzurufen, indem nach einem der enthaltenen Wörter gesucht wird.
-   Erweiterte Spaltenüberschriften in Windows Explorer-Ansichten ermöglichen das Sortieren und Gruppieren von Dokumenten auf unterschiedliche Weise. Beispielsweise können Dateien nach Namen, Datumsänderung, Typ, Größe und Tags sortiert werden. Dokumente können auch nach einer dieser Eigenschaften gruppiert werden, und jede Gruppe kann nach Bedarf gefiltert (ausgeblendet oder angezeigt) werden.
-   Dokumente können nach Name, Datumsänderung, Typ, Größe und Tags gestapelt werden. Stapel enthalten alle Dokumente, die über die angegebene Eigenschaft verfügen und sich in einem beliebigen Unterordner des ausgewählten Ordners befinden.
-   Suchvorgänge können gespeichert werden (um später abgerufen zu werden), indem Sie im Suchbereich im Windows-Explorer auf die Schaltfläche **Suche speichern** klicken. Die Ergebnisse werden basierend auf den ursprünglichen Kriterien dynamisch neu aufgefüllt, wenn die gespeicherte Suche geöffnet wird. Anweisungen finden [Sie](https://windows.microsoft.com/windows-vista/Save-your-search-results)unter Speichern von Suchergebnissen.
-   Vorschauhandler und Miniaturansichtshandler ermöglichen Benutzern das Anzeigen einer Vorschau von Dokumenten in Windows Explorer, ohne die Anwendung öffnen zu müssen, die sie erstellt hat.

## <a name="technical-prerequisites"></a>Technische Voraussetzungen

Bevor Sie mit dem Lesen der Windows Search SDK-Dokumentation beginnen, sollten Sie über grundlegende Kenntnisse der folgenden Konzepte verfügen:

-   Implementieren einer Shell-Datenquelle.
-   Implementieren eines Handlers.
-   Arbeiten in nativem Code.

Eine Shell-Datenquelle ist eine Komponente, die verwendet wird, um den Shellnamespace zu erweitern und Elemente in einem Datenspeicher verfügbar zu machen. In der Vergangenheit wurde die Shell-Datenquelle als Shellnamespaceerweiterung bezeichnet. Ein Handler ist ein com-Objekt (Component Object Model), das Funktionen für ein Shellelement bereitstellt. Eine Liste der Handler, die durch das Entwicklerszenario identifiziert werden, das Sie erreichen möchten, finden Sie unter "Übersicht über Handler" in [Windows Suchen als Entwicklungsplattform.](-search-3x-wds-development-ovr.md)

Weitere Informationen zur Interoperabilitätsassembly Windows Search SDK für die Arbeit mit COM-Objekten, die von Windows Search und anderen Programmen verfügbar gemacht werden, die verwalteten Code verwenden, finden Sie unter [Verwenden von verwaltetem Code mit Shelldaten und Windows Suchen.](-search-3x-wds-managed-code.md) Beachten Sie jedoch, dass Filter, Eigenschaftenhandler und Protokollhandler in nativem Code geschrieben werden müssen. Dies liegt an potenziellen CLR-Versionsproblemen (Common Language Runtime) beim Prozess, in dem mehrere Add-Ins ausgeführt werden. Entwickler, die noch nicht mit C++ arbeiten, können mit dem [Visual C++ Developer Center](https://msdn.microsoft.com/vstudio//default.aspx) und Windows Development [Erste Schritte](../desktop-programming.md)beginnen.

### <a name="sdk-download-and-contents"></a>SDK-Download und -Inhalt

Zusätzlich zur Erfüllung der aufgeführten technischen Anforderungen müssen Sie auch das [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) herunterladen, um die Windows Search-Bibliotheken zu erhalten. Die [Windows Search SDK-Beispiele](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8) enthalten nützliche Codebeispiele und eine Interoperabilitätsassembly für die Entwicklung mit verwaltetem Code. Weitere Informationen zur Verwendung der Codebeispiele finden Sie unter [Windows Codebeispiele für](-search-3x-wds-sampleentry.md)die Suche.

## <a name="windows-search-sdk-documentation"></a>Windows Suchen der SDK-Dokumentation

Die Dokumentation zum Windows Search SDK sieht wie folgt aus:

-   [Windows Search als Entwicklungsplattform](-search-3x-wds-development-ovr.md)

    Beschreibt die wichtigsten Entwicklungsszenarien in Windows Search. Enthält eine Liste der Handler, die durch das Entwicklungsszenario identifiziert werden, das Sie erreichen möchten, Richtlinien für Add-In-Installationsprogramme und Implementierungshinweise.

-   [Windows Search Developer es Guide (Entwicklerhandbuch durchsuchen)](-search-developers-guide-entry-page.md)

    Enthält Erläuterungen zum [Verwalten des Indexes,](-search-3x-wds-mngidx-overview.md) [zum programmgesteuerten Abfragen des Indexes,](-search-3x-wds-qryidx-overview.md)zum Erweitern des [Indexes](-search-3x-wds-extidx-overview.md)und [zum Erweitern von Sprachressourcen.](extending-language-resources-in-windows-search.md)

-   [Windows Suchreferenz](-search-reference-entry-page.md)

    Dokumentiert die folgenden Kategorien von Windows Search-Schnittstellen: [Protokollhandler,](-search-protocol-handlers-interfaces-entry-page.md)Abfragen, [Durchforstungsbereich,](-search-crawl-scope-interfaces-entry-page.md) [Daten-Add-Ins,](-search-data-addins-interfaces-entry-page.md) [Indexverwaltung](-search-index-mgt-interfaces-entry-page.md)und [Benachrichtigungen.](-search-notifications-interfaces-entry-page.md) [](-search-querying-interfaces-entry-page.md) Die Referenzdokumentation enthält auch [Konstanten und Enumerationen,](-search-constants-and-enumerations-entry-page.md) [Strukturen,](-search-structures-entry-page.md) [Eigenschaftenzuordnungen](-search-3x-wds-propertymappings.md)und das [Gespeicherte Suchdateiformat](-search-savedsearchfileformat.md).

-   [Windows Suchen von Codebeispielen](-search-samples-ovw.md)

    Beschreibt die verfügbaren Such-API-Codebeispiele.

-   [Verbundsuche in Windows 10](-search-federated-search-overview.md)

    Beschreibt Windows 7-Unterstützung für den Suchverbund mit Remotedatenspeichern mithilfe von OpenSearch Technologien, die Benutzern den Zugriff auf und die Interaktion mit ihren Remotedaten über Windows Explorer ermöglichen.

-   [Verwandte Suchtechnologien](-search-3x-wds-sampleentry.md)

    Listet Technologien im Zusammenhang mit Windows Search: Enterprise Search, SharePoint Enterprise Search und Legacyanwendungen wie Windows DesktopSuche 2.x und Plattform-SDK: Indizierungsdienst.

-   [Windows Search Glossary](search-glossary.md)

    Definiert wichtige Begriffe, die in Windows Search- und Shell-Technologien verwendet werden.

## <a name="history-of-windows-search"></a>Verlauf der Windows Suche

Windows Search ersetzt Windows Desktopsuche (WDS), die als Add-In für Windows XP und Windows Server 2003 verfügbar war. WDS hat den Legacyindizierungsdienst aus früheren Versionen von Windows durch Verbesserungen an Leistung, Benutzerfreundlichkeit und Erweiterbarkeit ersetzt. Die neue Entwicklungsplattform unterstützt Anforderungen, die ein sichereres und stabileres System erzeugen. Obwohl die neue Abfrageplattform nicht mit Microsoft Windows Desktop Search (WDS) 2.x kompatibel ist, können Filter und Protokollhandler, die für frühere Versionen von WDS geschrieben wurden, aktualisiert werden, um mit Windows Search zu arbeiten. Windows Search unterstützt auch ein neues Eigenschaftensystem. Informationen zu Filtern, Eigenschaftenhandlern und Protokollhandlern finden Sie unter [Erweitern des Indexes.](-search-3x-wds-extidx-overview.md)

Windows Search ist in Windows Vista und höher integriert und als verteilbares Update für WDS 2.x verfügbar, um die folgenden Betriebssysteme zu unterstützen:

-   32-Bit-Versionen von Windows XP mit Service Pack 2 (SP2).
-   Alle x64-basierten Versionen von Windows XP.
-   Windows Server 2003 mit Service Pack 1 (SP1) und höher.
-   Alle x64-basierten Versionen von Windows Server 2003.

Auf Systemen, auf denen diese Betriebssysteme ausgeführt werden, muss Windows Search installiert sein, um Anwendungen auszuführen, die für Windows Search geschrieben wurden. Weitere Informationen finden Sie im [KB-Artikel 917013: Beschreibung von Windows Desktopsuche 3.01 und im mehrsprachige Benutzeroberfläche Pack für Windows Desktopsuche 3.01.](https://support.microsoft.com/kb/917013)

## <a name="additional-resources"></a>Weitere Ressourcen

-   Informationen zum Erstellen einer Shelldatenquelle finden Sie unter [Implementieren der grundlegenden Ordnerobjektschnittstellen.](/previous-versions//bb776815(v=vs.85))
-   Weitere Informationen zu [ISearchFolderItemFactory](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) und der Datenbankordnerdatenquelle finden Sie in der Beschreibung der STR \_ PARSE WITH \_ PROPERTIES-Konstante unter Binden von \_ [Kontextzeichenfolgenschlüsseln.](../shell/str-constants.md) Siehe auch [Zuordnungsarrays](/previous-versions/windows/desktop/legacy/ee872122(v=vs.85)) und [IPropertySystem::GetPropertyDescriptionListFromString.](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring)
-   Informationen zu OLE DB finden Sie unter [OLE DB Programmierübersicht.](/cpp/data/oledb/ole-db-programming-overview?view=vs-2019) Informationen zum .NET Framework Datenanbieter für OLE DB finden Sie in der Dokumentation [zum System.Data.OleDb-Namespace.](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1&preserve-view=true)
-   Eine Übersicht über Dateityphandler (auch als Shellerweiterungshandler und Suchhandler bezeichnet) finden Sie unter [Windows Search as a Development Platform](-search-3x-wds-development-ovr.md).
-   Von der Community unterstützte Meldungsboards zu Suchtechnologien finden Sie im [MSDN-Forum: Windows Entwicklung der Desktopsuche.](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads)
-   Verwandte Codebeispiele finden Sie unter [Windows Suchen von Codebeispielen.](-search-samples-ovw.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Search als Entwicklungsplattform](-search-3x-wds-development-ovr.md)
</dt> <dt>

[Von Windows Search unterstützte Sprachen](-search-3x-wds-language-support.md)
</dt> <dt>

[Verwenden von verwaltetem Code mit Shelldaten und Windows Search](-search-3x-wds-managed-code.md)
</dt> </dl>

 

 
