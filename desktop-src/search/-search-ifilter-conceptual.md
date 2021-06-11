---
description: Erfahren Sie, wie Sie Filterhandler in Windows Search. Bei der Suche werden Filter verwendet, um Elemente für die Aufnahme in einen Volltextindex zu extrahieren.
ms.assetid: 7b24986b-972d-4674-846b-f856b908edf4
title: Entwickeln von Filterhandlern für Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa86c0a1e41ababf6f00db72a26784beb93e1879
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988859"
---
# <a name="developing-filter-handlers-for-windows-search"></a><span data-ttu-id="faca3-104">Entwickeln von Filterhandlern für Windows Search</span><span class="sxs-lookup"><span data-stu-id="faca3-104">Developing Filter Handlers for Windows Search</span></span>

<span data-ttu-id="faca3-105">Microsoft Windows Search verwendet Filter, um den Inhalt von Elementen für die Aufnahme in einen Volltextindex zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="faca3-105">Microsoft Windows Search uses filters to extract the content of items for inclusion in a full-text index.</span></span> <span data-ttu-id="faca3-106">Sie können die Windows Search, um neue oder proprietäre Dateitypen zu indizieren, indem Sie Filter schreiben, um den Inhalt zu extrahieren, und Eigenschaftenhandler, um die Eigenschaften von Dateien zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="faca3-106">You can extend Windows Search to index new or proprietary file types by writing filters to extract the content, and property handlers to extract the properties of files.</span></span>

<span data-ttu-id="faca3-107">Dieser Abschnitt enthält das konzeptionelle Framework, das zum Implementieren eines Filterhandlers (einer Implementierung der [**IFilter-Schnittstelle) erforderlich**](/windows/win32/api/filter/nn-filter-ifilter) ist.</span><span class="sxs-lookup"><span data-stu-id="faca3-107">This section provides the conceptual framework that is necessary for implementing a filter handler (an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface).</span></span>

- [<span data-ttu-id="faca3-108">Grundlegendes zu Filterhandlern in Windows Search</span><span class="sxs-lookup"><span data-stu-id="faca3-108">Understanding Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)
- [<span data-ttu-id="faca3-109">Bewährte Methoden zum Erstellen von Filterhandlern in Windows Search</span><span class="sxs-lookup"><span data-stu-id="faca3-109">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)
- [<span data-ttu-id="faca3-110">Zurückgeben von Eigenschaften von einem Filterhandler</span><span class="sxs-lookup"><span data-stu-id="faca3-110">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)
- [<span data-ttu-id="faca3-111">Filterhandler, die mit Windows gesendet werden</span><span class="sxs-lookup"><span data-stu-id="faca3-111">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)
- [<span data-ttu-id="faca3-112">Implementieren von Filterhandlern in Windows Search</span><span class="sxs-lookup"><span data-stu-id="faca3-112">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)
- [<span data-ttu-id="faca3-113">Registrieren von Filterhandlern</span><span class="sxs-lookup"><span data-stu-id="faca3-113">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)
- [<span data-ttu-id="faca3-114">Testen von Filterhandlern</span><span class="sxs-lookup"><span data-stu-id="faca3-114">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)

## <a name="additional-resources"></a><span data-ttu-id="faca3-115">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="faca3-115">Additional Resources</span></span>

- <span data-ttu-id="faca3-116">Das [IFilterSample-Codebeispiel,](-search-sample-ifiltersample.md) das auf [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)verfügbar ist, veranschaulicht das Erstellen einer IFilter-Basisklasse für die Implementierung der [**IFilter-Schnittstelle.**](/windows/win32/api/filter/nn-filter-ifilter)</span><span class="sxs-lookup"><span data-stu-id="faca3-116">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
- <span data-ttu-id="faca3-117">Eine Übersicht über den Indizierungsprozess finden Sie unter [Der Indizierungsprozess](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="faca3-117">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="faca3-118">Eine Übersicht über Dateitypen finden Sie unter [Dateitypen.](../shell/fa-file-types.md)</span><span class="sxs-lookup"><span data-stu-id="faca3-118">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="faca3-119">Informationen zum Abfragen von Dateiassoziationsattributen für einen Dateityp finden Sie unter [PerceivedTypes, SystemFileAssociations und Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="faca3-119">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>
