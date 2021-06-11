---
description: Erfahren Sie mehr über bewährte Methoden zum Erstellen von Filterhandlern in Windows Search. Bei der Suche werden Filter verwendet, um Elemente für die Aufnahme in einen Volltextindex zu extrahieren.
ms.assetid: 7b86a1b4-c8a9-400d-a9f1-a3b821c0269d
title: Bewährte Methoden für Filterhandler in Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a864cb2651d6236a212f3bf356eed3380869284
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989305"
---
# <a name="best-practices-for-creating-filter-handlers-in-windows-search"></a>Bewährte Methoden zum Erstellen von Filterhandlern in Windows Search

Microsoft Windows Search verwendet Filter, um den Inhalt von Elementen für die Aufnahme in einen Volltextindex zu extrahieren. Sie können Windows Search, um neue oder proprietäre Dateitypen zu indizieren, indem Sie Filterhandler schreiben, um den Inhalt zu extrahieren, und Eigenschaftenhandler, um die Eigenschaften von Dateien zu extrahieren. Filter werden Dateitypen zugeordnet, wie durch Dateierweiterungen, MIME-Typen oder Klassenbezeichner (CLSIDs) angegeben. Während ein Filter mehrere Dateitypen verarbeiten kann, funktioniert jeder Typ nur mit einem Filter.

Dieses Thema enthält folgende Abschnitte:

-   [Nativer Code](#native-code)
-   [Sichere Codemethoden für Windows Search](#secure-code-practices-for-windows-search)
-   [Weitere Ressourcen](#additional-resources)
-   [Verwandte Themen](#related-topics)

## <a name="native-code"></a>nativer Code

In Windows 7 und höher werden Filter, die in verwaltetem Code geschrieben wurden, explizit blockiert. Filter MÜSSEN aufgrund potenzieller CLR-Versionsprobleme mit dem Prozess, in dem mehrere Add-Ins ausgeführt werden, in nativem Code geschrieben werden.

## <a name="secure-code-practices-for-windows-search"></a>Sichere Codemethoden für Windows Search

Im Folgenden finden Sie Methoden zum Schreiben sicherer Anwendungen für die Verwendung mit Windows Search.

**Für Abfrageanwendungen:**

-   Beim Schreiben von Suchclients sollten Sie die API auswählen, die in einem Sicherheitskontext ausgeführt wird, der dem Benutzer die geringsten Berechtigungen zulässt. ASP-Seiten können z. B. das IXSSO-Abfrageobjekt verwenden, das als Benutzerprozess ausgeführt wird.

**Für IFilters und Sprachressourcen:**

-   Wenn ein neuer Filterhandler für einen Dateityp als Ersatz für eine vorhandene Filterregistrierung installiert wird, sollte das Installationsprogramm die aktuelle Registrierung speichern und wiederherstellen, wenn der neue Filterhandler deinstalliert wird. Es gibt keinen Mechanismus zum Verketten von Filtern. Daher ist der neue Filterhandler für die Replikation aller erforderlichen Funktionen des alten Filters verantwortlich.
-   IFilter, Wörterbrechen und Wortstammnoten für Windows Search im kontext der lokalen Sicherheit ausgeführt werden. Sie sollten geschrieben werden, um Puffer zu verwalten und ordnungsgemäß zu stapeln. Alle Zeichenfolgenkopien müssen explizite Überprüfungen zum Schutz vor Pufferüberläufen enthalten. Sie sollten immer die zugeordnete Größe des Puffers überprüfen und die Größe der Daten mit der Größe des Puffers testen. Pufferüberläufe sind ein gängiges Verfahren zum Ausnutzen von Code, der keine Puffergrößenbeschränkungen erzwingt.
-   [**IFilter-,**](/windows/win32/api/filter/nn-filter-ifilter)Wortbruch- und Wortstammwortkomponenten sollten niemals die [ExitProcess-Funktion](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) oder eine ähnliche API aufrufen, die einen Prozess und alle seine Threads beendet.
-   Weisen Sie keine Ressourcen im DllMain-Einstiegspunkt zu oder geben Sie sie frei. Dies kann zu Fehlern bei Belastungstests mit geringen Ressourcen führen.
-   Codieren Sie alle Objekte so, dass sie threadsicher sind. Windows Search aufruft jede Instanz einer Wörterpause oder wortstammendes Wortstamm in einem Thread gleichzeitig, kann jedoch mehrere Instanzen gleichzeitig über mehrere Threads hinweg aufrufen.
-   Vermeiden Sie das Erstellen temporärer Dateien oder das Schreiben in die Registrierung.
-   Wenn Sie die Microsoft Visual C++-Compiler, stellen Sie sicher, dass Sie Ihre Anwendung mit der **Option /GS kompilieren.** Die **Option /GS** wird verwendet, um Pufferüberläufe zu erkennen. Die Option /GS platziert Sicherheitsüberprüfungen in den kompilierten Code. Weitere Informationen finden Sie unter [DllGetClassObject Function](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx)  / **GS** (Buffer Security Check) im Abschnitt Visual C++ Compiler Options des Platform SDK.

## <a name="additional-resources"></a>Weitere Ressourcen

-   Das [IFilterSample-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample) veranschaulicht, wie eine IFilter-Basisklasse zum Implementieren der [**IFilter-Schnittstelle erstellt**](/windows/win32/api/filter/nn-filter-ifilter) wird.
-   Eine Übersicht über den Indizierungsprozess finden Sie unter [Der Indizierungsprozess](-search-indexing-process-overview.md).
-   Eine Übersicht über Dateitypen finden Sie unter [Dateitypen.](../shell/fa-file-types.md)
-   Informationen zum Abfragen von Dateiassoziationsattributen für einen Dateityp finden Sie unter [PerceivedTypes, SystemFileAssociations und Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln von Filterhandlern](-search-ifilter-conceptual.md)
</dt> <dt>

[Informationen zu Filterhandlern in Windows Search](-search-ifilter-about.md)
</dt> <dt>

[Zurückgeben von Eigenschaften von einem Filterhandler](-search-ifilter-property-filtering.md)
</dt> <dt>

[Filterhandler, die mit Windows gesendet werden](-search-ifilter-implementations.md)
</dt> <dt>

[Implementieren von Filterhandlern in Windows Search](-search-ifilter-constructing-filters.md)
</dt> <dt>

[Registrieren von Filterhandlern](-search-ifilter-registering-filters.md)
</dt> <dt>

[Testen von Filterhandlern](-search-ifilter-testing-filters.md)
</dt> </dl>

 

 
