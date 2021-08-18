---
description: Erfahren Sie mehr über bewährte Methoden zum Erstellen von Filterhandlern in Windows Search. Die Suche verwendet Filter, um Elemente für die Aufnahme in einen Volltextindex zu extrahieren.
ms.assetid: 7b86a1b4-c8a9-400d-a9f1-a3b821c0269d
title: Bewährte Methoden für Filterhandler in Windows Suche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8320cf0f85bf86f7d61df09437271af67d0e4096fc3a917d037914854c9bad3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463699"
---
# <a name="best-practices-for-creating-filter-handlers-in-windows-search"></a>Bewährte Methoden zum Erstellen von Filterhandlern in Windows Search

Microsoft Windows Search verwendet Filter, um den Inhalt von Elementen für die Aufnahme in einen Volltextindex zu extrahieren. Sie können Windows Search erweitern, um neue oder proprietäre Dateitypen zu indizierung, indem Sie Filterhandler schreiben, um den Inhalt zu extrahieren, und Eigenschaftenhandler, um die Eigenschaften von Dateien zu extrahieren. Filter werden Dateitypen zugeordnet, wie durch Dateinamenerweiterungen, MIME-Typen oder Klassenbezeichner (CLSIDs) angegeben. Während ein Filter mehrere Dateitypen verarbeiten kann, funktioniert jeder Typ nur mit einem Filter.

Dieses Thema enthält folgende Abschnitte:

-   [Nativer Code](#native-code)
-   [Sichere Codemethoden für die Windows Suche](#secure-code-practices-for-windows-search)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="native-code"></a>nativer Code

In Windows 7 und höher werden in verwaltetem Code geschriebene Filter explizit blockiert. Filter MÜSSEN aufgrund potenzieller CLR-Versionsprobleme mit dem Prozess, in dem mehrere Add-Ins ausgeführt werden, in nativem Code geschrieben werden.

## <a name="secure-code-practices-for-windows-search"></a>Sichere Codemethoden für die Windows Suche

Im Folgenden finden Sie Methoden zum Schreiben sicherer Anwendungen für die Verwendung mit Windows Search.

**Für Abfrageanwendungen:**

-   Beim Schreiben von Suchclients sollten Sie die API auswählen, die in einem Sicherheitskontext ausgeführt wird, der dem Benutzer die geringsten Rechte gewährt. ASP-Seiten können beispielsweise das IXSSO-Abfrageobjekt verwenden, das als Benutzerprozess ausgeführt wird.

**Für IFilters und Sprachressourcen:**

-   Wenn ein neuer Filterhandler für einen Dateityp als Ersatz für eine vorhandene Filterregistrierung installiert wird, sollte das Installationsprogramm die aktuelle Registrierung speichern und wiederherstellen, wenn der neue Filterhandler deinstalliert wird. Es gibt keinen Mechanismus zum Verketten von Filtern. Daher ist der neue Filterhandler für die Replikation aller erforderlichen Funktionen des alten Filters verantwortlich.
-   IFilters, Wörterumbrüche und Wortstammstammwörter für Windows Search werden im Kontext der lokalen Sicherheit ausgeführt. Sie sollten geschrieben werden, um Puffer zu verwalten und ordnungsgemäß zu stapeln. Alle Zeichenfolgenkopien müssen explizite Überprüfungen aufweisen, um sich vor Pufferüberläufen zu schützen. Sie sollten immer die zugeordnete Größe des Puffers überprüfen und die Größe der Daten anhand der Größe des Puffers testen. Pufferüberläufe sind ein gängiges Verfahren zum Ausnutzen von Code, der keine Einschränkungen der Puffergröße erzwingt.
-   [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), Wörterumbruch- und Wortstammerkennungskomponenten sollten niemals die [Funktion ExitProcess Function](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) oder eine ähnliche API aufrufen, die einen Prozess und alle zugehörigen Threads beendet.
-   Zuordnen oder Freigeben von Ressourcen im DllMain-Einstiegspunkt nicht. Dies kann bei Belastungstests mit geringen Ressourcen zu Fehlern führen.
-   Coden Sie alle Objekte, um threadsicher zu sein. Windows Die Suche ruft eine beliebige Instanz einer Wörterpause oder Wortstammsuche in einem Thread gleichzeitig auf, kann aber mehrere Instanzen gleichzeitig über mehrere Threads hinweg aufrufen.
-   Vermeiden Sie das Erstellen temporärer Dateien oder das Schreiben in die Registrierung.
-   Wenn Sie den Microsoft Visual C++ Compiler verwenden, stellen Sie sicher, dass Sie Ihre Anwendung mit der Option **/GS** kompilieren. Die **Option /GS** wird verwendet, um Pufferüberläufe zu erkennen. Die Option /GS platziert Sicherheitsüberprüfungen in den kompilierten Code. Weitere Informationen finden Sie unter [DllGetClassObject Function](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx)  / **GS** (Buffer Security Check) im Abschnitt Visual C++ Compiler Options des Platform SDK.

## <a name="additional-resources"></a>Weitere Ressourcen

-   Im [IFilterSample-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample) wird veranschaulicht, wie Sie eine IFilter-Basisklasse zum Implementieren der [**IFilter-Schnittstelle**](/windows/win32/api/filter/nn-filter-ifilter) erstellen.
-   Eine Übersicht über den Indizierungsprozess finden Sie unter [Der Indizierungsprozess.](-search-indexing-process-overview.md)
-   Eine Übersicht über Dateitypen finden Sie unter [Dateitypen.](../shell/fa-file-types.md)
-   Informationen zum Abfragen von Dateizuordnungsattributen für einen Dateityp finden Sie unter [PerceivedTypes, SystemFileAssociations und Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln von Filterhandlern](-search-ifilter-conceptual.md)
</dt> <dt>

[Informationen zu Filterhandlern in Windows Search](-search-ifilter-about.md)
</dt> <dt>

[Zurückgeben von Eigenschaften aus einem Filterhandler](-search-ifilter-property-filtering.md)
</dt> <dt>

[Filterhandler, die mit Windows](-search-ifilter-implementations.md)
</dt> <dt>

[Implementieren von Filterhandlern in Windows Suche](-search-ifilter-constructing-filters.md)
</dt> <dt>

[Registrieren von Filterhandlern](-search-ifilter-registering-filters.md)
</dt> <dt>

[Testen von Filterhandlern](-search-ifilter-testing-filters.md)
</dt> </dl>

 

 
