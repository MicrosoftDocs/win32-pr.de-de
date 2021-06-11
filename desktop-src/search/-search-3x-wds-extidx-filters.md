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
# <a name="best-practices-for-creating-filter-handlers-in-windows-search"></a><span data-ttu-id="47206-104">Bewährte Methoden zum Erstellen von Filterhandlern in Windows Search</span><span class="sxs-lookup"><span data-stu-id="47206-104">Best Practices for Creating Filter Handlers in Windows Search</span></span>

<span data-ttu-id="47206-105">Microsoft Windows Search verwendet Filter, um den Inhalt von Elementen für die Aufnahme in einen Volltextindex zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="47206-105">Microsoft Windows Search uses filters to extract the content of items for inclusion in a full-text index.</span></span> <span data-ttu-id="47206-106">Sie können Windows Search, um neue oder proprietäre Dateitypen zu indizieren, indem Sie Filterhandler schreiben, um den Inhalt zu extrahieren, und Eigenschaftenhandler, um die Eigenschaften von Dateien zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="47206-106">You can extend Windows Search to index new or proprietary file types by writing filter handlers to extract the content, and property handlers to extract the properties of files.</span></span> <span data-ttu-id="47206-107">Filter werden Dateitypen zugeordnet, wie durch Dateierweiterungen, MIME-Typen oder Klassenbezeichner (CLSIDs) angegeben.</span><span class="sxs-lookup"><span data-stu-id="47206-107">Filters are associated with file types, as denoted by file name extensions, MIME types or class identifiers (CLSIDs).</span></span> <span data-ttu-id="47206-108">Während ein Filter mehrere Dateitypen verarbeiten kann, funktioniert jeder Typ nur mit einem Filter.</span><span class="sxs-lookup"><span data-stu-id="47206-108">While one filter can handle multiple file types, each type works with only one filter.</span></span>

<span data-ttu-id="47206-109">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="47206-109">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="47206-110">Nativer Code</span><span class="sxs-lookup"><span data-stu-id="47206-110">Native Code</span></span>](#native-code)
-   [<span data-ttu-id="47206-111">Sichere Codemethoden für Windows Search</span><span class="sxs-lookup"><span data-stu-id="47206-111">Secure Code Practices for Windows Search</span></span>](#secure-code-practices-for-windows-search)
-   [<span data-ttu-id="47206-112">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="47206-112">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="47206-113">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="47206-113">Related topics</span></span>](#related-topics)

## <a name="native-code"></a><span data-ttu-id="47206-114">nativer Code</span><span class="sxs-lookup"><span data-stu-id="47206-114">Native Code</span></span>

<span data-ttu-id="47206-115">In Windows 7 und höher werden Filter, die in verwaltetem Code geschrieben wurden, explizit blockiert.</span><span class="sxs-lookup"><span data-stu-id="47206-115">In Windows 7 and later, filters written in managed code are explicitly blocked.</span></span> <span data-ttu-id="47206-116">Filter MÜSSEN aufgrund potenzieller CLR-Versionsprobleme mit dem Prozess, in dem mehrere Add-Ins ausgeführt werden, in nativem Code geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="47206-116">Filters MUST be written in native code due to potential CLR versioning issues with the process that multiple add-ins run in.</span></span>

## <a name="secure-code-practices-for-windows-search"></a><span data-ttu-id="47206-117">Sichere Codemethoden für Windows Search</span><span class="sxs-lookup"><span data-stu-id="47206-117">Secure Code Practices for Windows Search</span></span>

<span data-ttu-id="47206-118">Im Folgenden finden Sie Methoden zum Schreiben sicherer Anwendungen für die Verwendung mit Windows Search.</span><span class="sxs-lookup"><span data-stu-id="47206-118">The following are practices for writing secure applications for use with Windows Search.</span></span>

<span data-ttu-id="47206-119">**Für Abfrageanwendungen:**</span><span class="sxs-lookup"><span data-stu-id="47206-119">**For query applications:**</span></span>

-   <span data-ttu-id="47206-120">Beim Schreiben von Suchclients sollten Sie die API auswählen, die in einem Sicherheitskontext ausgeführt wird, der dem Benutzer die geringsten Berechtigungen zulässt.</span><span class="sxs-lookup"><span data-stu-id="47206-120">When writing search clients, you should choose the API that runs in a security context that allows the user the least privilege.</span></span> <span data-ttu-id="47206-121">ASP-Seiten können z. B. das IXSSO-Abfrageobjekt verwenden, das als Benutzerprozess ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="47206-121">For example, ASP pages can use the IXSSO query object, which runs as a user process.</span></span>

<span data-ttu-id="47206-122">**Für IFilters und Sprachressourcen:**</span><span class="sxs-lookup"><span data-stu-id="47206-122">**For IFilters and Language Resources:**</span></span>

-   <span data-ttu-id="47206-123">Wenn ein neuer Filterhandler für einen Dateityp als Ersatz für eine vorhandene Filterregistrierung installiert wird, sollte das Installationsprogramm die aktuelle Registrierung speichern und wiederherstellen, wenn der neue Filterhandler deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="47206-123">If a new filter handler for a file type is being installed as a replacement for an existing filter registration, the installer should save the current registration and restore it if the new filter handler is uninstalled.</span></span> <span data-ttu-id="47206-124">Es gibt keinen Mechanismus zum Verketten von Filtern.</span><span class="sxs-lookup"><span data-stu-id="47206-124">There is no mechanism to chain filters.</span></span> <span data-ttu-id="47206-125">Daher ist der neue Filterhandler für die Replikation aller erforderlichen Funktionen des alten Filters verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="47206-125">Hence, the new filter handler is responsible for replicating any necessary functionality of the old filter.</span></span>
-   <span data-ttu-id="47206-126">IFilter, Wörterbrechen und Wortstammnoten für Windows Search im kontext der lokalen Sicherheit ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="47206-126">IFilters, word breakers, and stemmers for Windows Search run in the Local Security context.</span></span> <span data-ttu-id="47206-127">Sie sollten geschrieben werden, um Puffer zu verwalten und ordnungsgemäß zu stapeln.</span><span class="sxs-lookup"><span data-stu-id="47206-127">They should be written to manage buffers and to stack correctly.</span></span> <span data-ttu-id="47206-128">Alle Zeichenfolgenkopien müssen explizite Überprüfungen zum Schutz vor Pufferüberläufen enthalten.</span><span class="sxs-lookup"><span data-stu-id="47206-128">All string copies must have explicit checks to guard against buffer overruns.</span></span> <span data-ttu-id="47206-129">Sie sollten immer die zugeordnete Größe des Puffers überprüfen und die Größe der Daten mit der Größe des Puffers testen.</span><span class="sxs-lookup"><span data-stu-id="47206-129">You should always verify the allocated size of the buffer and test the size of the data against the size of the buffer.</span></span> <span data-ttu-id="47206-130">Pufferüberläufe sind ein gängiges Verfahren zum Ausnutzen von Code, der keine Puffergrößenbeschränkungen erzwingt.</span><span class="sxs-lookup"><span data-stu-id="47206-130">Buffer overruns are a common technique for exploiting code that does not enforce buffer size restrictions.</span></span>
-   <span data-ttu-id="47206-131">[**IFilter-,**](/windows/win32/api/filter/nn-filter-ifilter)Wortbruch- und Wortstammwortkomponenten sollten niemals die [ExitProcess-Funktion](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) oder eine ähnliche API aufrufen, die einen Prozess und alle seine Threads beendet.</span><span class="sxs-lookup"><span data-stu-id="47206-131">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), word breaker and stemmer components should never call the [ExitProcess Function](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) function or similar API that terminates a process and all its threads.</span></span>
-   <span data-ttu-id="47206-132">Weisen Sie keine Ressourcen im DllMain-Einstiegspunkt zu oder geben Sie sie frei.</span><span class="sxs-lookup"><span data-stu-id="47206-132">Do not allocate or free resources in the DllMain entry point.</span></span> <span data-ttu-id="47206-133">Dies kann zu Fehlern bei Belastungstests mit geringen Ressourcen führen.</span><span class="sxs-lookup"><span data-stu-id="47206-133">This can lead to failures during low-resource stress tests.</span></span>
-   <span data-ttu-id="47206-134">Codieren Sie alle Objekte so, dass sie threadsicher sind.</span><span class="sxs-lookup"><span data-stu-id="47206-134">Code all objects to be thread-safe.</span></span> <span data-ttu-id="47206-135">Windows Search aufruft jede Instanz einer Wörterpause oder wortstammendes Wortstamm in einem Thread gleichzeitig, kann jedoch mehrere Instanzen gleichzeitig über mehrere Threads hinweg aufrufen.</span><span class="sxs-lookup"><span data-stu-id="47206-135">Windows Search calls any one instance of a word breaker or stemmer in one thread at a time, but it may call multiple instances at the same time across multiple threads.</span></span>
-   <span data-ttu-id="47206-136">Vermeiden Sie das Erstellen temporärer Dateien oder das Schreiben in die Registrierung.</span><span class="sxs-lookup"><span data-stu-id="47206-136">Avoid creating temporary files or writing to the registry.</span></span>
-   <span data-ttu-id="47206-137">Wenn Sie die Microsoft Visual C++-Compiler, stellen Sie sicher, dass Sie Ihre Anwendung mit der **Option /GS kompilieren.**</span><span class="sxs-lookup"><span data-stu-id="47206-137">If you use the Microsoft Visual C++ compiler, ensure that you compile your application using the **/GS** option.</span></span> <span data-ttu-id="47206-138">Die **Option /GS** wird verwendet, um Pufferüberläufe zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="47206-138">The **/GS** option is used to detect buffer overruns.</span></span> <span data-ttu-id="47206-139">Die Option /GS platziert Sicherheitsüberprüfungen in den kompilierten Code.</span><span class="sxs-lookup"><span data-stu-id="47206-139">The /GS option places security checks into the compiled code.</span></span> <span data-ttu-id="47206-140">Weitere Informationen finden Sie unter [DllGetClassObject Function](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx)  / **GS** (Buffer Security Check) im Abschnitt Visual C++ Compiler Options des Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="47206-140">For more information, see [DllGetClassObject Function](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx) /**GS** (Buffer Security Check) in the Visual C++ Compiler Options section of the Platform SDK.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="47206-141">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="47206-141">Additional Resources</span></span>

-   <span data-ttu-id="47206-142">Das [IFilterSample-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample) veranschaulicht, wie eine IFilter-Basisklasse zum Implementieren der [**IFilter-Schnittstelle erstellt**](/windows/win32/api/filter/nn-filter-ifilter) wird.</span><span class="sxs-lookup"><span data-stu-id="47206-142">The [IFilterSample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample) sample demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
-   <span data-ttu-id="47206-143">Eine Übersicht über den Indizierungsprozess finden Sie unter [Der Indizierungsprozess](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="47206-143">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
-   <span data-ttu-id="47206-144">Eine Übersicht über Dateitypen finden Sie unter [Dateitypen.](../shell/fa-file-types.md)</span><span class="sxs-lookup"><span data-stu-id="47206-144">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
-   <span data-ttu-id="47206-145">Informationen zum Abfragen von Dateiassoziationsattributen für einen Dateityp finden Sie unter [PerceivedTypes, SystemFileAssociations und Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="47206-145">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="47206-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="47206-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47206-147">Entwickeln von Filterhandlern</span><span class="sxs-lookup"><span data-stu-id="47206-147">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)
</dt> <dt>

[<span data-ttu-id="47206-148">Informationen zu Filterhandlern in Windows Search</span><span class="sxs-lookup"><span data-stu-id="47206-148">About Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)
</dt> <dt>

[<span data-ttu-id="47206-149">Zurückgeben von Eigenschaften von einem Filterhandler</span><span class="sxs-lookup"><span data-stu-id="47206-149">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)
</dt> <dt>

[<span data-ttu-id="47206-150">Filterhandler, die mit Windows gesendet werden</span><span class="sxs-lookup"><span data-stu-id="47206-150">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)
</dt> <dt>

[<span data-ttu-id="47206-151">Implementieren von Filterhandlern in Windows Search</span><span class="sxs-lookup"><span data-stu-id="47206-151">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)
</dt> <dt>

[<span data-ttu-id="47206-152">Registrieren von Filterhandlern</span><span class="sxs-lookup"><span data-stu-id="47206-152">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)
</dt> <dt>

[<span data-ttu-id="47206-153">Testen von Filterhandlern</span><span class="sxs-lookup"><span data-stu-id="47206-153">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)
</dt> </dl>

 

 
