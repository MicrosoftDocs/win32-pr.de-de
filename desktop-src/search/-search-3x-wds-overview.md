---
description: Windows Search ist eine Plattform für die Desktop Suche, die über sofortige Suchfunktionen für die meisten gängigen Dateitypen und Datentypen verfügt. Entwickler von Drittanbietern können diese Funktionen auf neue Dateitypen und Datentypen ausweiten.
ms.assetid: 6da601c6-3742-40ad-99f2-8817f7f642b3
title: Übersicht über Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cee4cde62ce663c47ab4cafac0c74ca220fe6faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862183"
---
# <a name="windows-search-overview"></a>Übersicht über Windows Search

Windows Search ist eine Plattform für die Desktop Suche, die über sofortige Suchfunktionen für die meisten gängigen Dateitypen und Datentypen verfügt. Entwickler von Drittanbietern können diese Funktionen auf neue Dateitypen und Datentypen ausweiten.

Dieses Thema ist wie folgt organisiert:

-   [Introduction (Einführung)](#introduction)
    -   [Windows Search-Dienst](#windows-search-service)
    -   [Entwicklungsplattform](#development-platform)
    -   [Benutzeroberfläche](#user-interface)
-   [Technische Voraussetzungen](#technical-prerequisites)
    -   [SDK-Download und-Inhalt](#sdk-download-and-contents)
-   [Dokumentation zu Windows Search SDK](#windows-search-sdk-documentation)
-   [Verlauf der Windows-Suche](#history-of-windows-search)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Windows Search ist eine Standardkomponente von Windows 7 und Windows Vista und ist standardmäßig aktiviert. Windows Search ersetzt die Windows-Desktop Suche (WDS), die als Add-in für Windows XP und Windows Server 2003 verfügbar war.

Die Windows-Suche besteht aus drei Komponenten:

-   [Windows Suchdienst](#windows-search-service) (WSS)
-   [Entwicklungsplattform](#development-platform)
-   [User interface (Benutzeroberfläche)](#user-interface)

### <a name="windows-search-service"></a>Windows Search-Dienst

Der WSS organisiert die extrahierten Funktionen einer Sammlung von Dokumenten. Mithilfe des Windows Search-Protokolls kann ein Client mit einem Server kommunizieren, auf dem ein WSS gehostet wird, um Abfragen auszugeben und einem Administrator die Verwaltung des Index Servers zu ermöglichen. Beim Verarbeiten von Dateien analysiert WSS eine Reihe von Dokumenten, extrahiert nützliche Informationen und organisiert dann die extrahierten Informationen, sodass die Eigenschaften dieser Dokumente als Reaktion auf Abfragen effizient zurückgegeben werden können.

Eine Sammlung von Dokumenten, die abgefragt werden können, umfasst einen Katalog, bei dem es sich um die Organisationseinheit in Windows Search handelt. Ein Katalog stellt einen Satz indizierter Dokumente dar, die abgefragt werden können. Ein Katalog besteht aus einer Eigenschaften Tabelle mit dem Text oder Wert und dem entsprechenden Speicherort (Gebiets Schema), der in den Spalten der Tabelle gespeichert ist. Jede Zeile der Tabelle entspricht einem separaten Dokument im Geltungsbereich des Katalogs, und jede Spalte der Tabelle entspricht einer Eigenschaft. Ein Katalog kann einen invertierten Index (für die schnelle Wort Abstimmung) und einen Eigenschafts Cache (für den schnellen Abruf von Eigenschafts Werten) enthalten.

Der Indexer-Prozess wird als Windows-Dienst implementiert, der im Konto "LocalSystem" ausgeführt wird und immer für alle Benutzer ausgeführt wird (auch wenn kein Benutzer angemeldet ist), sodass Windows Search Folgendes erreichen kann:

-   Behalten Sie einen Index bei, der von allen Benutzern gemeinsam genutzt wird.
-   Gewährleisten von Sicherheitseinschränkungen für den Zugriff auf Inhalte
-   Verarbeiten von Remote Abfragen von Client Computern im Netzwerk.

Der Suchdienst ist so konzipiert, dass die Benutzer Leistung und die Systemleistung bei der Indizierung geschützt werden. Die folgenden Bedingungen bewirken, dass der Dienst eine Drosselung zurückgibt oder die Indizierung anhält:

-   Hohe CPU-Auslastung durch Prozesse, die sich nicht auf die Suche beziehen.
-   Hohe System-e/a-Rate einschließlich Datei Lese-und Schreibvorgängen, Auslagerungs Datei-und Dateicache-e/a und zugeordnete Datei-e/a.
-   Geringe Speicherverfügbarkeit.
-   Geringe Akku Lebensdauer.
-   Wenig Speicherplatz auf dem Laufwerk, auf dem der Index gespeichert ist.

### <a name="development-platform"></a>Entwicklungsplattform

Die bevorzugte Methode für den Zugriff auf die Such-APIs und die Erstellung von Windows Search-Anwendungen ist die Verwendung einer shelldatenquelle. Eine shelldatenquelle ist eine Komponente, die verwendet wird, um den Shellnamespace zu erweitern und Elemente in einem Datenspeicher verfügbar zu machen. Ein Datenspeicher ist ein Repository mit Daten. Ein Datenspeicher kann für das shellprogrammierungs Modell als Container verfügbar gemacht werden, der eine shelldatenquelle verwendet. Die Elemente in einem Datenspeicher können vom Windows-Suchsystem mithilfe eines Protokoll Handlers indiziert werden.

[Isearchfolderitemfactory](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) ist z. b. eine Komponente, die Instanzen der Suchordner-Datenquelle erstellen kann. Hierbei handelt es sich um eine von der Shell bereitgestellte virtuelle Datenquelle, die Abfragen für andere Datenquellen im Shellnamespace ausführen und Ergebnisse aufzählen kann. Dies kann entweder mithilfe des Indexers oder durch manuelles auflisten und Überprüfen von Elementen in den angegebenen Bereichen geschehen. Mit dieser Schnittstelle können Sie die Parameter für die Suche mithilfe von Methoden einrichten, mit denen Suchordner erstellt und geändert werden. Wenn Methoden dieser Schnittstelle nicht aufgerufen werden, werden stattdessen Standardwerte verwendet.

Das indirekte zugreifen auf die Windows-Suchfunktion über das Shell-Datenmodell wird bevorzugt, da Sie Zugriff auf die vollständige Shell-Funktionalität auf der Ebene des shelldatenmodells bietet. Beispielsweise können Sie den Bereich einer Suche auf eine Bibliothek festlegen (die in Windows 7 und höher verfügbar ist), um die Bibliotheks Ordner als Abfrage Bereich zu verwenden. Die Suchergebnisse werden von Windows Search von diesen Speicherorten aggregiert, wenn Sie sich in unterschiedlichen Indizes befinden (wenn sich die Ordner auf unterschiedlichen Computern befinden). Die Shell-Datenschicht erstellt außerdem eine ausführlichere Ansicht der Element Eigenschaften, wobei einige Eigenschaftswerte synthesiert werden. Außerdem wird der Zugriff auf Suchfunktionen für Datenspeicher ermöglicht, die nicht von Windows Search indiziert werden. Beispielsweise können Sie eine USB-Speichergeräte (Universal Serial Bus), ein tragbares Gerät, das das MTP-Protokoll verwendet, oder einen File Transfer Protocol (FTP)-Server durch die Shell-Datenquellen durchsuchen, die Zugriff auf diese Speichersysteme bereitstellen. Dies sorgt für eine bessere Benutzer Leistung.

Windows Search verfügt über einen Cache mit Eigenschafts Werten, die in der Implementierung des Windows-Suchdienst (WSS) verwendet werden. Diese Eigenschaftswerte können Programm gesteuert mithilfe des Windows Search-OLE DB Anbieters oder mithilfe von [isearchfolderitemfactory](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory)abgefragt werden, das Elemente in Suchergebnissen und Abfrage basierten Sichten darstellt. Windows Search sammelt und speichert dann Eigenschaften, die von Filter Handlern oder Eigenschaften Handlern ausgegeben werden, wenn ein Element wie ein Word-Dokument indiziert wird. Dieser Speicher wird verworfen und neu erstellt, wenn der Index neu erstellt wird.

Entwickler von Drittanbietern können Anwendungen erstellen, die die Daten im Index über programmgesteuerte Abfragen nutzen, und die Daten im Index erweitern, damit benutzerdefinierte Datei-und Elementtypen von Windows Search indiziert werden. Wenn Sie Abfrageergebnisse in Windows-Explorer anzeigen möchten, müssen Sie eine Shell-Datenquelle implementieren, bevor Sie einen Protokollhandler zum Erweitern des Indexes erstellen können. Wenn allerdings alle Abfragen Programm gesteuert werden (z. b. über OLE DB) und vom Code der Anwendung anstelle der Shell interpretiert werden, wird ein Shellnamespace weiterhin bevorzugt, ist aber nicht erforderlich.

Ein Protokollhandler ist erforderlich, damit Windows Informationen zum Inhalt der Datei, z. b. Elemente in Datenbanken oder benutzerdefinierten Dateitypen, abrufen kann. Obwohl Windows Search den Namen und die Eigenschaften der Datei indizieren kann, enthält Windows keine Informationen zum Inhalt der Datei. Folglich können solche Elemente in der Windows-Shell nicht indiziert oder verfügbar gemacht werden. Durch Implementieren eines benutzerdefinierten Protokoll Handlers können Sie diese Elemente verfügbar machen. Eine Liste der Handler, die von dem Entwickler Szenario identifiziert werden, das Sie zu erreichen versuchen, finden Sie unter "Übersicht über Handler" in der [Windows-Suche als Entwicklungsplattform](-search-3x-wds-development-ovr.md).

> [!Note]  
> Eine shelldatenquelle wird manchmal als Shellnamespace Erweiterung bezeichnet. Ein Handler wird manchmal als Shellerweiterung oder Shellerweiterungs Handler bezeichnet.

 

### <a name="user-interface"></a>Benutzeroberfläche

In Windows Vista und höher ist Windows Search in alle Windows-Explorer-Fenster integriert, sodass Sie sofort auf die Suche zugreifen können. Dadurch können Benutzer mithilfe von Dateinamen, Eigenschaften und voll Textinhalten schnell nach Dateien und Elementen suchen. Die Ergebnisse können auch weiter gefiltert werden, um die Suche zu verfeinern. Im folgenden finden Sie einige weitere Features von Windows Search:

-   Ein sofortiges Suchfeld in jedem Fenster ermöglicht das sofortige Filtern aller Elemente, die derzeit in der Ansicht angezeigt werden. Sofort Suchfelder werden im Startmenü angezeigt, um nach Programmen oder Dateien zu suchen, und in der oberen rechten Ecke aller Windows-Explorer-Fenster, um die angezeigten Ergebnisse zu filtern. Die sofortige Suche ist auch in andere Windows-Features, wie z. b. Windows Media Player, integriert, um verwandte Dateien zu suchen.
-   Dokumente können mit Schlüsselwörtern versehen werden, um Sie nach benutzerdefinierten Kriterien zu gruppieren, die vom Benutzer definiert werden. Tags sind Metadatenelemente, die vom Benutzer oder Anwendungen zugewiesen werden, um die Suche nach Dateien auf der Grundlage von Schlüsselwörtern zu vereinfachen, die möglicherweise nicht im Elementnamen oder-Inhalt vorliegen. Beispielsweise könnte eine Reihe von Bildern als "Arizona Vacation 2009" gekennzeichnet werden, um Sie später schnell abzurufen, indem Sie nach den enthaltenen Wörtern suchen.
-   Erweiterte Spaltenüberschriften in Windows-Explorer-Ansichten ermöglichen das Sortieren und Gruppieren von Dokumenten auf verschiedene Weise. Beispielsweise können Dateien nach Name, Änderungsdatum, Typ, Größe und Tags sortiert werden. Dokumente können auch nach einer dieser Eigenschaften gruppiert werden, und jede Gruppe kann wie gewünscht gefiltert (ausgeblendet oder angezeigt) werden.
-   Dokumente können nach Name, Änderungsdatum, Typ, Größe und Tags gestapelt werden. Stapel enthalten alle Dokumente mit der angegebenen Eigenschaft und befinden sich in einem Unterordner des ausgewählten Ordners.
-   Suchen können gespeichert werden (um später abgerufen zu werden), indem Sie im Fenster Suchbereich von Windows-Explorer auf die Schaltfläche **Suche speichern** klicken. Die Ergebnisse werden basierend auf den ursprünglichen Kriterien dynamisch erneut aufgefüllt, wenn die gespeicherte Suche geöffnet wird. Anweisungen finden Sie unter [Speichern der Suchergebnisse](https://windows.microsoft.com/windows-vista/Save-your-search-results).
-   Mit Vorschau Handlern und Miniatur Ansichts Handlern können Benutzer in Windows-Explorer eine Vorschau der Dokumente anzeigen, ohne die Anwendung zu öffnen, die Sie erstellt hat.

## <a name="technical-prerequisites"></a>Technische Voraussetzungen

Bevor Sie mit dem Lesen der Dokumentation zu Windows Search SDK beginnen, sollten Sie über grundlegende Kenntnisse der folgenden Konzepte verfügen:

-   So implementieren Sie eine shelldatenquelle.
-   Gewusst wie: Implementieren eines Handlers.
-   Arbeiten mit nativem Code.

Eine shelldatenquelle ist eine Komponente, die verwendet wird, um den Shellnamespace zu erweitern und Elemente in einem Datenspeicher verfügbar zu machen. In der Vergangenheit wurde die shelldatenquelle als Shell-Namespace Erweiterung bezeichnet. Ein Handler ist ein Component Object Model (com)-Objekt, das Funktionen für ein shellelement bereitstellt. Eine Liste der Handler, die von dem Entwickler Szenario identifiziert werden, das Sie zu erreichen versuchen, finden Sie unter "Übersicht über Handler" in der [Windows-Suche als Entwicklungsplattform](-search-3x-wds-development-ovr.md).

Weitere Informationen zur Interoperabilitäts-Assembly von Windows Search SDK für die Arbeit mit COM-Objekten, die von Windows Search verfügbar gemacht werden, und anderen Programmen, die verwalteten Code verwenden, finden [Sie unter Verwenden von verwaltetem Code mit shelldaten und Windows Search](-search-3x-wds-managed-code.md). Beachten Sie jedoch, dass Filter, Eigenschaften Handler und Protokollhandler in nativem Code geschrieben werden müssen. Ursache hierfür sind potenzielle Probleme bei der Common Language Runtime (CLR) mit dem Prozess, in dem mehrere Add-Ins ausgeführt werden. Entwickler, die mit C++ noch nicht vertraut sind, können mit den ersten Schritten des [Visual C++ Developer Centers](https://msdn.microsoft.com/vstudio//default.aspx) und der [Windows-Entwicklung](../desktop-programming.md)beginnen.

### <a name="sdk-download-and-contents"></a>SDK-Download und-Inhalt

Zusätzlich zur Erfüllung der aufgelisteten technischen Voraussetzungen müssen Sie auch die [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) herunterladen, um die Windows Search-Bibliotheken zu erhalten. Die [Beispiele für Windows Search SDK](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8) enthalten nützliche Codebeispiele und eine Interoperabilitäts-Assembly für die Entwicklung mit verwaltetem Code. Weitere Informationen zur Verwendung der Codebeispiele finden Sie unter [Codebeispiele für Windows-Suche](-search-3x-wds-sampleentry.md).

## <a name="windows-search-sdk-documentation"></a>Dokumentation zu Windows Search SDK

Der Inhalt der Windows Search SDK-Dokumentation lautet wie folgt:

-   [Windows Search als Entwicklungsplattform](-search-3x-wds-development-ovr.md)

    Erläutert die wichtigsten Entwicklungsszenarien in Windows Search. Bietet eine Liste von Handlern, die durch das Entwicklungsszenario identifiziert werden, das Sie zu erreichen versuchen, Richtlinien für den Add-in-Installer und Implementierungs Hinweise.

-   [Entwicklerhandbuch für Windows Search](-search-developers-guide-entry-page.md)

    Enthält Erläuterungen zum [Verwalten des Indexes](-search-3x-wds-mngidx-overview.md), [Programm gesteuertes Abfragen des Indexes](-search-3x-wds-qryidx-overview.md), [Erweitern des Indexes](-search-3x-wds-extidx-overview.md)und [Erweitern von Sprachressourcen](extending-language-resources-in-windows-search.md).

-   [Referenz zur Windows-Suche](-search-reference-entry-page.md)

    Dokumentiert die folgenden Kategorien von Windows Search-Schnittstellen: [Protokollhandler](-search-protocol-handlers-interfaces-entry-page.md), [Abfragen](-search-querying-interfaces-entry-page.md), [Crawl Bereich](-search-crawl-scope-interfaces-entry-page.md), [Daten-Add-ins](-search-data-addins-interfaces-entry-page.md), [Index Verwaltung](-search-index-mgt-interfaces-entry-page.md)und [Benachrichtigungen](-search-notifications-interfaces-entry-page.md). Die Referenz Dokumentation umfasst auch [Konstanten und Enumerationen](-search-constants-and-enumerations-entry-page.md), [Strukturen](-search-structures-entry-page.md), [Eigenschaften](-search-3x-wds-propertymappings.md)Zuordnungen und das [gespeicherte Format der Such Datei](-search-savedsearchfileformat.md).

-   [Code Beispiele für Windows Search](-search-samples-ovw.md)

    Beschreibt die verfügbaren Codebeispiele für die Such-API.

-   [Verbundsuche in Windows 10](-search-federated-search-overview.md)

    Beschreibt die Windows 7-Unterstützung für das Durchsuchen von Verbund zu Remote Daten speichern mithilfe von OpenSearch-Technologien, die Benutzern den Zugriff auf und die Interaktion mit ihren Remote Daten aus Windows Explorer ermöglichen.

-   [Verwandte Suchtechnologien](-search-3x-wds-sampleentry.md)

    Listet Technologien im Zusammenhang mit Windows Search: Unternehmenssuche, SharePoint Enterprise-Suche und ältere Anwendungen wie Windows-Desktop Suche 2. x und Platform SDK: Index Dienst.

-   [Glossar für Windows-Suche](search-glossary.md)

    Definiert wesentliche Begriffe, die in Windows Search und shelltechnologien verwendet werden.

## <a name="history-of-windows-search"></a>Verlauf der Windows-Suche

Windows Search ersetzt die Windows-Desktop Suche (WDS), die als Add-in für Windows XP und Windows Server 2003 verfügbar war. WDS hat den Legacy-Indizierungs Dienst aus früheren Windows-Versionen durch Erweiterungen in Bezug auf Leistung, Benutzerfreundlichkeit und Erweiterbarkeit ersetzt. Die neue Entwicklungsplattform unterstützt Anforderungen, die ein sichereres und stabileres System erzielen. Obwohl die neue Abfrage Plattform nicht mit der Microsoft Windows-Desktop Suche (WDS) 2. x kompatibel ist, können Filter und Protokollhandler, die für frühere Versionen von WDS geschrieben wurden, aktualisiert werden, damit Sie mit Windows Search funktionieren. Windows Search unterstützt auch ein neues Eigenschaften System. Informationen zu filtern, Eigenschaften Handlern und Protokoll Handlern finden Sie unter [Erweitern des Indexes](-search-3x-wds-extidx-overview.md).

Windows Search ist in Windows Vista und höher integriert und steht als verteilbares Update für WDS 2. x zur Verfügung, um die folgenden Betriebssysteme zu unterstützen:

-   32-Bit-Versionen von Windows XP mit Service Pack 2 (SP2).
-   Alle x64-basierten Versionen von Windows XP.
-   Windows Server 2003 mit Service Pack 1 (SP1) und höher.
-   Alle x64-basierten Versionen von Windows Server 2003.

Auf Systemen, auf denen diese Betriebssysteme ausgeführt werden, muss Windows Search installiert sein, damit für Windows Search geschriebene Anwendungen ausgeführt werden können. Weitere Informationen finden Sie [im KB-Artikel 917013: Beschreibung der Windows-Desktop Suche 3,01 und der Multilingual User Interface Pack für die Windows-Desktop Suche 3,01](https://support.microsoft.com/kb/917013).

## <a name="additional-resources"></a>Weitere Ressourcen

-   Weitere Informationen zum Erstellen einer shelldatenquelle finden Sie unter [Implementieren der grundlegenden Ordner Objekt Schnittstellen](/previous-versions//bb776815(v=vs.85)).
-   Weitere Informationen zu [isearchfolderitemfactory](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) und der Datenquelle des Daten Bank Ordners finden Sie in der Beschreibung der Str-Analyse \_ mit der Properties- \_ \_ Konstante in [Bindungs Kontext-Zeichen folgen Schlüsseln](../shell/str-constants.md). Siehe auch [Association Arrays](/previous-versions/windows/desktop/legacy/ee872122(v=vs.85)) und [ipropertysystem:: getpropertydescriptionlistfromstring](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring).
-   Weitere Informationen zu OLE DB finden Sie unter Übersicht über die [OLE DB Programmierung](/cpp/data/oledb/ole-db-programming-overview?view=vs-2019). Informationen zu den .NET Framework Datenanbieter für OLE DB finden Sie in der Dokumentation zum [System. Data. OleDb-Namespace](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1&preserve-view=true) .
-   Eine Übersicht über Dateityp Handler (auch als Shellerweiterungs Handler und Such Handler bezeichnet) finden Sie unter [Windows Search als Entwicklungsplattform](-search-3x-wds-development-ovr.md).
-   Informationen zu Suchtechnologien von der Community unterstützten Nachrichten Boards finden Sie im [MSDN-Forum: Entwicklung von Windows-Desktop-suchen](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).
-   Verwandte Codebeispiele finden Sie unter [Codebeispiele für Windows-Suche](-search-samples-ovw.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Search als Entwicklungsplattform](-search-3x-wds-development-ovr.md)
</dt> <dt>

[Von Windows Search unterstützte Sprachen](-search-3x-wds-language-support.md)
</dt> <dt>

[Verwenden von verwaltetem Code mit Shelldaten und Windows Search](-search-3x-wds-managed-code.md)
</dt> </dl>

 

 
