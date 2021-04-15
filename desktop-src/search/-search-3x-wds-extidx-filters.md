---
description: Microsoft Windows Search verwendet Filter zum Extrahieren des Inhalts von Elementen für die Aufnahme in einen Volltextindex.
ms.assetid: 7b86a1b4-c8a9-400d-a9f1-a3b821c0269d
title: Bewährte Methoden für Filter Handler in Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 544992e252d9ec0e3a7c402d1c348d3e3bfa9a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525538"
---
# <a name="best-practices-for-creating-filter-handlers-in-windows-search"></a>Bewährte Methoden zum Erstellen von Filter Handlern in Windows Search

Microsoft Windows Search verwendet Filter zum Extrahieren des Inhalts von Elementen für die Aufnahme in einen Volltextindex. Sie können die Windows-Suche erweitern, um neue oder proprietäre Dateitypen zu indizieren, indem Sie Filter Handler zum Extrahieren des Inhalts schreiben und Eigenschaften Handler, um die Eigenschaften von Dateien zu extrahieren. Filter sind Dateitypen zugeordnet, die durch Dateinamen Erweiterungen, MIME-Typen oder Klassen Bezeichner (CLSIDs) bezeichnet werden. Obwohl ein Filter mehrere Dateitypen verarbeiten kann, kann jeder Typ nur mit einem einzigen Filter verwendet werden.

Dieses Thema enthält folgende Abschnitte:

-   [Nativer Code](#native-code)
-   [Methoden für den sicheren Code für Windows Search](#secure-code-practices-for-windows-search)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="native-code"></a>nativer Code

In Windows 7 und höher werden in verwaltetem Code geschriebene Filter explizit blockiert. Filter müssen in nativem Code geschrieben werden, da mögliche Probleme bei der CLR-Versionsverwaltung mit dem Prozess auftreten, in dem mehrere Add-Ins ausgeführt werden.

## <a name="secure-code-practices-for-windows-search"></a>Methoden für den sicheren Code für Windows Search

Im folgenden werden Methoden zum Schreiben sicherer Anwendungen für die Verwendung mit Windows Search beschrieben.

**Für Abfrage Anwendungen:**

-   Wenn Sie Such Clients schreiben, sollten Sie die API auswählen, die in einem Sicherheitskontext ausgeführt wird, der dem Benutzer die geringsten Rechte gewährt. Beispielsweise können ASP-Seiten das ixsso-Abfrageobjekt verwenden, das als Benutzer Prozess ausgeführt wird.

**Für IFilters und Sprachressourcen:**

-   Wenn ein neuer Filter Handler für einen Dateityp als Ersatz für eine vorhandene Filter Registrierung installiert wird, sollte der Installer die aktuelle Registrierung speichern und wiederherstellen, wenn der neue Filter Handler deinstalliert wird. Es gibt keinen Mechanismus zum Verketten von Filtern. Daher ist der neue Filter Handler für die Replikation aller notwendigen Funktionen des alten Filters verantwortlich.
-   IFilters, Wörter Trennungen und Wort Stamm Erkennungen für Windows Search werden im lokalen Sicherheitskontext ausgeführt. Sie sollten so geschrieben werden, dass Sie Puffer verwalten und ordnungsgemäß stapeln. Alle Zeichen folgen Kopien müssen über explizite Überprüfungen zum Schutz vor Pufferüberläufen verfügen. Sie sollten stets die zugeordnete Größe des Puffers überprüfen und die Größe der Daten mit der Größe des Puffers testen. Pufferüberläufe sind eine gängige Methode für die Ausnutzung von Code, der keine Einschränkungen der Puffergröße erzwingt.
-   Die Komponenten " [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)", "Wörter Trennung" und "Wort Stamm Erkennung" sollten niemals die Funktion " [ExitProcess](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) " oder eine ähnliche API aufzurufen, die einen Prozess und alle Threads beendet.
-   Weisen Sie dem DllMain-Einstiegspunkt keine Ressourcen zu. Dies kann zu Fehlern bei Belastungstests mit geringer Auslastung führen.
-   Codieren Sie alle Objekte, die Thread sicher sind. Windows Search Ruft eine beliebige Instanz einer Wörter Trennung oder Wort Stamm Erkennung in jeweils einem Thread auf, aber es können mehrere Instanzen gleichzeitig über mehrere Threads hinweg aufgerufen werden.
-   Vermeiden Sie das Erstellen temporärer Dateien oder das Schreiben in die Registrierung.
-   Wenn Sie den Microsoft Visual C++-Compiler verwenden, stellen Sie sicher, dass Sie die Anwendung mithilfe der **/GS** -Option kompilieren. Die **/GS** -Option wird verwendet, um Pufferüberläufe zu erkennen. Mit der Option/GS werden Sicherheitsüberprüfungen in den kompilierten Code eingefügt. Weitere Informationen finden Sie unter [DllGetClassObject Function](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx)  / **GS** (Buffer Security Check) im Abschnitt Visual C++ Compileroptionen des Platform SDK.

## <a name="additional-resources"></a>Weitere Ressourcen

-   Das [ifiltersample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample) -Beispiel veranschaulicht, wie eine IFilter-Basisklasse für die Implementierung der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle erstellt wird.
-   Eine Übersicht über den Indizierungsprozess finden Sie [im Abschnitt zur Indizierung](-search-indexing-process-overview.md).
-   Eine Übersicht über die Dateitypen finden Sie unter [Dateitypen](../shell/fa-file-types.md).
-   Informationen zum Abfragen von Datei Zuordnungs Attributen für einen Dateityp finden Sie unter " [wahrtentypen", "systemfileassociation" und "Anwendungs Registrierung](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))".

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln von Filter Handlern](-search-ifilter-conceptual.md)
</dt> <dt>

[Informationen zu Filter Handlern in Windows Search](-search-ifilter-about.md)
</dt> <dt>

[Zurückgeben von Eigenschaften aus einem Filter Handler](-search-ifilter-property-filtering.md)
</dt> <dt>

[Filtern von Handlern, die mit Windows ausgeliefert werden](-search-ifilter-implementations.md)
</dt> <dt>

[Implementieren von Filter Handlern in Windows Search](-search-ifilter-constructing-filters.md)
</dt> <dt>

[Registrieren von Filter Handlern](-search-ifilter-registering-filters.md)
</dt> <dt>

[Testen von Filter Handlern](-search-ifilter-testing-filters.md)
</dt> </dl>

 

 
