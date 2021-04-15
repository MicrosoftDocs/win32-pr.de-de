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
# <a name="best-practices-for-creating-filter-handlers-in-windows-search"></a><span data-ttu-id="f8cc7-103">Bewährte Methoden zum Erstellen von Filter Handlern in Windows Search</span><span class="sxs-lookup"><span data-stu-id="f8cc7-103">Best Practices for Creating Filter Handlers in Windows Search</span></span>

<span data-ttu-id="f8cc7-104">Microsoft Windows Search verwendet Filter zum Extrahieren des Inhalts von Elementen für die Aufnahme in einen Volltextindex.</span><span class="sxs-lookup"><span data-stu-id="f8cc7-104">Microsoft Windows Search uses filters to extract the content of items for inclusion in a full-text index.</span></span> <span data-ttu-id="f8cc7-105">Sie können die Windows-Suche erweitern, um neue oder proprietäre Dateitypen zu indizieren, indem Sie Filter Handler zum Extrahieren des Inhalts schreiben und Eigenschaften Handler, um die Eigenschaften von Dateien zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="f8cc7-105">You can extend Windows Search to index new or proprietary file types by writing filter handlers to extract the content, and property handlers to extract the properties of files.</span></span> <span data-ttu-id="f8cc7-106">Filter sind Dateitypen zugeordnet, die durch Dateinamen Erweiterungen, MIME-Typen oder Klassen Bezeichner (CLSIDs) bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="f8cc7-106">Filters are associated with file types, as denoted by file name extensions, MIME types or class identifiers (CLSIDs).</span></span> <span data-ttu-id="f8cc7-107">Obwohl ein Filter mehrere Dateitypen verarbeiten kann, kann jeder Typ nur mit einem einzigen Filter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f8cc7-107">While one filter can handle multiple file types, each type works with only one filter.</span></span>

<span data-ttu-id="f8cc7-108">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="f8cc7-108">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="f8cc7-109">Nativer Code</span><span class="sxs-lookup"><span data-stu-id="f8cc7-109">Native Code</span></span>](#native-code)
-   [<span data-ttu-id="f8cc7-110">Methoden für den sicheren Code für Windows Search</span><span class="sxs-lookup"><span data-stu-id="f8cc7-110">Secure Code Practices for Windows Search</span></span>](#secure-code-practices-for-windows-search)
-   [<span data-ttu-id="f8cc7-111">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f8cc7-111">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="f8cc7-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f8cc7-112">Related topics</span></span>](#related-topics)

## <a name="native-code"></a><span data-ttu-id="f8cc7-113">nativer Code</span><span class="sxs-lookup"><span data-stu-id="f8cc7-113">Native Code</span></span>

<span data-ttu-id="f8cc7-114">In Windows 7 und höher werden in verwaltetem Code geschriebene Filter explizit blockiert.</span><span class="sxs-lookup"><span data-stu-id="f8cc7-114">In Windows 7 and later, filters written in managed code are explicitly blocked.</span></span> <span data-ttu-id="f8cc7-115">Filter müssen in nativem Code geschrieben werden, da mögliche Probleme bei der CLR-Versionsverwaltung mit dem Prozess auftreten, in dem mehrere Add-Ins ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f8cc7-115">Filters MUST be written in native code due to potential CLR versioning issues with the process that multiple add-ins run in.</span></span>

## <a name="secure-code-practices-for-windows-search"></a><span data-ttu-id="f8cc7-116">Methoden für den sicheren Code für Windows Search</span><span class="sxs-lookup"><span data-stu-id="f8cc7-116">Secure Code Practices for Windows Search</span></span>

<span data-ttu-id="f8cc7-117">Im folgenden werden Methoden zum Schreiben sicherer Anwendungen für die Verwendung mit Windows Search beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f8cc7-117">The following are practices for writing secure applications for use with Windows Search.</span></span>

<span data-ttu-id="f8cc7-118">**Für Abfrage Anwendungen:**</span><span class="sxs-lookup"><span data-stu-id="f8cc7-118">**For query applications:**</span></span>

-   <span data-ttu-id="f8cc7-119">Wenn Sie Such Clients schreiben, sollten Sie die API auswählen, die in einem Sicherheitskontext ausgeführt wird, der dem Benutzer die geringsten Rechte gewährt.</span><span class="sxs-lookup"><span data-stu-id="f8cc7-119">When writing search clients, you should choose the API that runs in a security context that allows the user the least privilege.</span></span> <span data-ttu-id="f8cc7-120">Beispielsweise können ASP-Seiten das ixsso-Abfrageobjekt verwenden, das als Benutzer Prozess ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f8cc7-120">For example, ASP pages can use the IXSSO query object, which runs as a user process.</span></span>

<span data-ttu-id="f8cc7-121">**Für IFilters und Sprachressourcen:**</span><span class="sxs-lookup"><span data-stu-id="f8cc7-121">**For IFilters and Language Resources:**</span></span>

-   <span data-ttu-id="f8cc7-122">Wenn ein neuer Filter Handler für einen Dateityp als Ersatz für eine vorhandene Filter Registrierung installiert wird, sollte der Installer die aktuelle Registrierung speichern und wiederherstellen, wenn der neue Filter Handler deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="f8cc7-122">If a new filter handler for a file type is being installed as a replacement for an existing filter registration, the installer should save the current registration and restore it if the new filter handler is uninstalled.</span></span> <span data-ttu-id="f8cc7-123">Es gibt keinen Mechanismus zum Verketten von Filtern.</span><span class="sxs-lookup"><span data-stu-id="f8cc7-123">There is no mechanism to chain filters.</span></span> <span data-ttu-id="f8cc7-124">Daher ist der neue Filter Handler für die Replikation aller notwendigen Funktionen des alten Filters verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="f8cc7-124">Hence, the new filter handler is responsible for replicating any necessary functionality of the old filter.</span></span>
-   <span data-ttu-id="f8cc7-125">IFilters, Wörter Trennungen und Wort Stamm Erkennungen für Windows Search werden im lokalen Sicherheitskontext ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f8cc7-125">IFilters, word breakers, and stemmers for Windows Search run in the Local Security context.</span></span> <span data-ttu-id="f8cc7-126">Sie sollten so geschrieben werden, dass Sie Puffer verwalten und ordnungsgemäß stapeln.</span><span class="sxs-lookup"><span data-stu-id="f8cc7-126">They should be written to manage buffers and to stack correctly.</span></span> <span data-ttu-id="f8cc7-127">Alle Zeichen folgen Kopien müssen über explizite Überprüfungen zum Schutz vor Pufferüberläufen verfügen.</span><span class="sxs-lookup"><span data-stu-id="f8cc7-127">All string copies must have explicit checks to guard against buffer overruns.</span></span> <span data-ttu-id="f8cc7-128">Sie sollten stets die zugeordnete Größe des Puffers überprüfen und die Größe der Daten mit der Größe des Puffers testen.</span><span class="sxs-lookup"><span data-stu-id="f8cc7-128">You should always verify the allocated size of the buffer and test the size of the data against the size of the buffer.</span></span> <span data-ttu-id="f8cc7-129">Pufferüberläufe sind eine gängige Methode für die Ausnutzung von Code, der keine Einschränkungen der Puffergröße erzwingt.</span><span class="sxs-lookup"><span data-stu-id="f8cc7-129">Buffer overruns are a common technique for exploiting code that does not enforce buffer size restrictions.</span></span>
-   <span data-ttu-id="f8cc7-130">Die Komponenten " [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)", "Wörter Trennung" und "Wort Stamm Erkennung" sollten niemals die Funktion " [ExitProcess](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) " oder eine ähnliche API aufzurufen, die einen Prozess und alle Threads beendet.</span><span class="sxs-lookup"><span data-stu-id="f8cc7-130">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), word breaker and stemmer components should never call the [ExitProcess Function](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) function or similar API that terminates a process and all its threads.</span></span>
-   <span data-ttu-id="f8cc7-131">Weisen Sie dem DllMain-Einstiegspunkt keine Ressourcen zu.</span><span class="sxs-lookup"><span data-stu-id="f8cc7-131">Do not allocate or free resources in the DllMain entry point.</span></span> <span data-ttu-id="f8cc7-132">Dies kann zu Fehlern bei Belastungstests mit geringer Auslastung führen.</span><span class="sxs-lookup"><span data-stu-id="f8cc7-132">This can lead to failures during low-resource stress tests.</span></span>
-   <span data-ttu-id="f8cc7-133">Codieren Sie alle Objekte, die Thread sicher sind.</span><span class="sxs-lookup"><span data-stu-id="f8cc7-133">Code all objects to be thread-safe.</span></span> <span data-ttu-id="f8cc7-134">Windows Search Ruft eine beliebige Instanz einer Wörter Trennung oder Wort Stamm Erkennung in jeweils einem Thread auf, aber es können mehrere Instanzen gleichzeitig über mehrere Threads hinweg aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f8cc7-134">Windows Search calls any one instance of a word breaker or stemmer in one thread at a time, but it may call multiple instances at the same time across multiple threads.</span></span>
-   <span data-ttu-id="f8cc7-135">Vermeiden Sie das Erstellen temporärer Dateien oder das Schreiben in die Registrierung.</span><span class="sxs-lookup"><span data-stu-id="f8cc7-135">Avoid creating temporary files or writing to the registry.</span></span>
-   <span data-ttu-id="f8cc7-136">Wenn Sie den Microsoft Visual C++-Compiler verwenden, stellen Sie sicher, dass Sie die Anwendung mithilfe der **/GS** -Option kompilieren.</span><span class="sxs-lookup"><span data-stu-id="f8cc7-136">If you use the Microsoft Visual C++ compiler, ensure that you compile your application using the **/GS** option.</span></span> <span data-ttu-id="f8cc7-137">Die **/GS** -Option wird verwendet, um Pufferüberläufe zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="f8cc7-137">The **/GS** option is used to detect buffer overruns.</span></span> <span data-ttu-id="f8cc7-138">Mit der Option/GS werden Sicherheitsüberprüfungen in den kompilierten Code eingefügt.</span><span class="sxs-lookup"><span data-stu-id="f8cc7-138">The /GS option places security checks into the compiled code.</span></span> <span data-ttu-id="f8cc7-139">Weitere Informationen finden Sie unter [DllGetClassObject Function](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx)  / **GS** (Buffer Security Check) im Abschnitt Visual C++ Compileroptionen des Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="f8cc7-139">For more information, see [DllGetClassObject Function](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx) /**GS** (Buffer Security Check) in the Visual C++ Compiler Options section of the Platform SDK.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f8cc7-140">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f8cc7-140">Additional Resources</span></span>

-   <span data-ttu-id="f8cc7-141">Das [ifiltersample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample) -Beispiel veranschaulicht, wie eine IFilter-Basisklasse für die Implementierung der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f8cc7-141">The [IFilterSample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample) sample demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
-   <span data-ttu-id="f8cc7-142">Eine Übersicht über den Indizierungsprozess finden Sie [im Abschnitt zur Indizierung](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f8cc7-142">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
-   <span data-ttu-id="f8cc7-143">Eine Übersicht über die Dateitypen finden Sie unter [Dateitypen](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="f8cc7-143">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
-   <span data-ttu-id="f8cc7-144">Informationen zum Abfragen von Datei Zuordnungs Attributen für einen Dateityp finden Sie unter " [wahrtentypen", "systemfileassociation" und "Anwendungs Registrierung](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))".</span><span class="sxs-lookup"><span data-stu-id="f8cc7-144">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8cc7-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f8cc7-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8cc7-146">Entwickeln von Filter Handlern</span><span class="sxs-lookup"><span data-stu-id="f8cc7-146">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)
</dt> <dt>

[<span data-ttu-id="f8cc7-147">Informationen zu Filter Handlern in Windows Search</span><span class="sxs-lookup"><span data-stu-id="f8cc7-147">About Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)
</dt> <dt>

[<span data-ttu-id="f8cc7-148">Zurückgeben von Eigenschaften aus einem Filter Handler</span><span class="sxs-lookup"><span data-stu-id="f8cc7-148">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)
</dt> <dt>

[<span data-ttu-id="f8cc7-149">Filtern von Handlern, die mit Windows ausgeliefert werden</span><span class="sxs-lookup"><span data-stu-id="f8cc7-149">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)
</dt> <dt>

[<span data-ttu-id="f8cc7-150">Implementieren von Filter Handlern in Windows Search</span><span class="sxs-lookup"><span data-stu-id="f8cc7-150">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)
</dt> <dt>

[<span data-ttu-id="f8cc7-151">Registrieren von Filter Handlern</span><span class="sxs-lookup"><span data-stu-id="f8cc7-151">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)
</dt> <dt>

[<span data-ttu-id="f8cc7-152">Testen von Filter Handlern</span><span class="sxs-lookup"><span data-stu-id="f8cc7-152">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)
</dt> </dl>

 

 
