---
description: Microsoft Windows Search verwendet Filter zum Extrahieren des Inhalts von Elementen für die Aufnahme in einen Volltextindex.
ms.assetid: 7b24986b-972d-4674-846b-f856b908edf4
title: Entwickeln von Filter Handlern für Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab8f45892549dc3f392824c31c78884b209d283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041631"
---
# <a name="developing-filter-handlers-for-windows-search"></a><span data-ttu-id="e59ea-103">Entwickeln von Filter Handlern für Windows Search</span><span class="sxs-lookup"><span data-stu-id="e59ea-103">Developing Filter Handlers for Windows Search</span></span>

<span data-ttu-id="e59ea-104">Microsoft Windows Search verwendet Filter zum Extrahieren des Inhalts von Elementen für die Aufnahme in einen Volltextindex.</span><span class="sxs-lookup"><span data-stu-id="e59ea-104">Microsoft Windows Search uses filters to extract the content of items for inclusion in a full-text index.</span></span> <span data-ttu-id="e59ea-105">Sie können Windows Search erweitern, um neue oder proprietäre Dateitypen zu indizieren, indem Sie Filter zum Extrahieren des Inhalts schreiben und Eigenschaften Handler, um die Eigenschaften von Dateien zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="e59ea-105">You can extend Windows Search to index new or proprietary file types by writing filters to extract the content, and property handlers to extract the properties of files.</span></span>

<span data-ttu-id="e59ea-106">Dieser Abschnitt enthält das konzeptionelle Framework, das zum Implementieren eines Filter Handlers (einer Implementierung der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle) erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="e59ea-106">This section provides the conceptual framework that is necessary for implementing a filter handler (an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface).</span></span>

- [<span data-ttu-id="e59ea-107">Grundlegendes zu Filter Handlern in Windows Search</span><span class="sxs-lookup"><span data-stu-id="e59ea-107">Understanding Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)
- [<span data-ttu-id="e59ea-108">Bewährte Methoden zum Erstellen von Filter Handlern in Windows Search</span><span class="sxs-lookup"><span data-stu-id="e59ea-108">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)
- [<span data-ttu-id="e59ea-109">Zurückgeben von Eigenschaften aus einem Filter Handler</span><span class="sxs-lookup"><span data-stu-id="e59ea-109">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)
- [<span data-ttu-id="e59ea-110">Filtern von Handlern, die mit Windows ausgeliefert werden</span><span class="sxs-lookup"><span data-stu-id="e59ea-110">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)
- [<span data-ttu-id="e59ea-111">Implementieren von Filter Handlern in Windows Search</span><span class="sxs-lookup"><span data-stu-id="e59ea-111">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)
- [<span data-ttu-id="e59ea-112">Registrieren von Filter Handlern</span><span class="sxs-lookup"><span data-stu-id="e59ea-112">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)
- [<span data-ttu-id="e59ea-113">Testen von Filter Handlern</span><span class="sxs-lookup"><span data-stu-id="e59ea-113">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)

## <a name="additional-resources"></a><span data-ttu-id="e59ea-114">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e59ea-114">Additional Resources</span></span>

- <span data-ttu-id="e59ea-115">Das in [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)verfügbare [ifiltersample](-search-sample-ifiltersample.md) -Codebeispiel veranschaulicht, wie eine IFilter-Basisklasse für die Implementierung der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e59ea-115">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
- <span data-ttu-id="e59ea-116">Eine Übersicht über den Indizierungsprozess finden Sie [im Abschnitt zur Indizierung](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e59ea-116">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="e59ea-117">Eine Übersicht über die Dateitypen finden Sie unter [Dateitypen](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="e59ea-117">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="e59ea-118">Informationen zum Abfragen von Datei Zuordnungs Attributen für einen Dateityp finden Sie unter " [wahrtentypen", "systemfileassociation" und "Anwendungs Registrierung](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))".</span><span class="sxs-lookup"><span data-stu-id="e59ea-118">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>
