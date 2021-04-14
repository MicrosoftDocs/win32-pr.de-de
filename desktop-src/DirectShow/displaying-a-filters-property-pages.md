---
description: Anzeigen der Eigenschaften Seiten eines Filters
ms.assetid: 4a5f6938-7b33-4350-b8fa-cf78c5c44bcd
title: Anzeigen der Eigenschaften Seiten eines Filters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0845a12b73363dc6ed93654439fd31826bf9cfc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392369"
---
# <a name="displaying-a-filters-property-pages"></a><span data-ttu-id="16e8c-103">Anzeigen der Eigenschaften Seiten eines Filters</span><span class="sxs-lookup"><span data-stu-id="16e8c-103">Displaying a Filter's Property Pages</span></span>

<span data-ttu-id="16e8c-104">Eine Eigenschaften Seite ist eine Möglichkeit für einen Filter, um Eigenschaften zu unterstützen, die vom Benutzer festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="16e8c-104">A property page is one way for a filter to support properties that the user can set.</span></span> <span data-ttu-id="16e8c-105">In diesem Artikel wird beschrieben, wie die Eigenschaften Seiten eines Filters in einer Anwendung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="16e8c-105">This article describes how to display a filter's property pages in an application.</span></span> <span data-ttu-id="16e8c-106">Weitere Informationen zu Eigenschaften Seiten finden Sie in der Platform SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="16e8c-106">For more information about property pages, see the Platform SDK documentation.</span></span>

> [!Note]  
> <span data-ttu-id="16e8c-107">Obwohl viele der mit DirectShow bereitgestellten Filtereigenschaften Seiten unterstützen, sind Sie für das Debuggen vorgesehen und werden für die Anwendungs Verwendung nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="16e8c-107">Although many of the filters provided with DirectShow support property pages, they are intended for debugging purposes, and are not recommended for application use.</span></span> <span data-ttu-id="16e8c-108">In den meisten Fällen wird die entsprechende Funktionalität über eine benutzerdefinierte Schnittstelle für den Filter bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="16e8c-108">In most cases the equivalent functionality is provided through a custom interface on the filter.</span></span> <span data-ttu-id="16e8c-109">Eine Anwendung sollte diese Filterprogramm gesteuert steuern, anstatt ihre Eigenschaften Seiten für Benutzer verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="16e8c-109">An application should control these filters programmatically, rather than expose their property pages to users.</span></span>

 

<span data-ttu-id="16e8c-110">Filter mit Eigenschaften Seiten machen die **ISpecifyPropertyPages** -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="16e8c-110">Filters with property pages expose the **ISpecifyPropertyPages** interface.</span></span> <span data-ttu-id="16e8c-111">Um zu ermitteln, ob ein Filter eine Eigenschaften Seite definiert, Fragen Sie mithilfe von **QueryInterface** den Filter für diese Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="16e8c-111">To determine whether a filter defines a property page, query the filter for this interface using **QueryInterface**.</span></span>

<span data-ttu-id="16e8c-112">Wenn Sie eine Instanz eines Filters (durch Aufrufen von **CoCreateInstance**) direkt erstellt haben, verfügen Sie bereits über einen Zeiger auf den Filter.</span><span class="sxs-lookup"><span data-stu-id="16e8c-112">If you directly created an instance of a filter (by calling **CoCreateInstance**), you already have a pointer to the filter.</span></span> <span data-ttu-id="16e8c-113">Wenn dies nicht der Fall ist, können Sie die Filter im Diagramm mithilfe der [**ifiltergraph:: enumfilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) -Methode auflisten.</span><span class="sxs-lookup"><span data-stu-id="16e8c-113">If not, you can enumerate the filters in the graph, using the [**IFilterGraph::EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) method.</span></span> <span data-ttu-id="16e8c-114">Weitere Informationen finden Sie unter Auflisten von [Objekten in einem Filter Diagramm](enumerating-objects-in-a-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="16e8c-114">For details, see [Enumerating Objects in a Filter Graph](enumerating-objects-in-a-filter-graph.md).</span></span>

<span data-ttu-id="16e8c-115">Sobald Sie über den **ISpecifyPropertyPages** -Schnittstellen Zeiger verfügen, rufen Sie die Eigenschaften Seiten des Filters ab, indem Sie die **ISpecifyPropertyPages:: GetPages** -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="16e8c-115">Once you have the **ISpecifyPropertyPages** interface pointer, retrieve the filter's property pages by calling the **ISpecifyPropertyPages::GetPages** method.</span></span> <span data-ttu-id="16e8c-116">Diese Methode füllt ein Gezähltes Array von global eindeutigen Bezeichnern (GUIDs) mit der Klassen-ID (CLSID) der einzelnen Eigenschaften Seiten.</span><span class="sxs-lookup"><span data-stu-id="16e8c-116">This method fills a counted array of globally unique identifiers (GUIDs) with the class identifier (CLSID) of each property page.</span></span> <span data-ttu-id="16e8c-117">Ein Gezähltes Array wird durch eine **cauuid** -Struktur definiert, die Sie zuordnen müssen, aber nicht initialisieren müssen.</span><span class="sxs-lookup"><span data-stu-id="16e8c-117">A counted array is defined by a **CAUUID** structure, which you must allocate but do not have to initialize.</span></span> <span data-ttu-id="16e8c-118">Die **GetPages** -Methode ordnet das Array zu, das im **pelems** -Member der **cauuid** -Struktur enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="16e8c-118">The **GetPages** method allocates the array, which is contained in the **pElems** member of the **CAUUID** structure.</span></span> <span data-ttu-id="16e8c-119">Wenn Sie den Vorgang abgeschlossen haben, können Sie das Array freigeben, indem Sie die **CoTaskMemFree** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="16e8c-119">When you are done, free the array by calling the **CoTaskMemFree** function.</span></span>

<span data-ttu-id="16e8c-120">Die **OleCreatePropertyFrame** -Funktion bietet eine einfache Möglichkeit, die Eigenschaften Seiten in einem modalen Dialogfeld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="16e8c-120">The **OleCreatePropertyFrame** function provides a simple way to display the property pages inside a modal dialog box.</span></span>


```C++
IBaseFilter *pFilter;
/* Obtain the filter's IBaseFilter interface. (Not shown) */
ISpecifyPropertyPages *pProp;
HRESULT hr = pFilter->QueryInterface(IID_ISpecifyPropertyPages, (void **)&pProp);
if (SUCCEEDED(hr)) 
{
    // Get the filter's name and IUnknown pointer.
    FILTER_INFO FilterInfo;
    hr = pFilter->QueryFilterInfo(&FilterInfo); 
    IUnknown *pFilterUnk;
    pFilter->QueryInterface(IID_IUnknown, (void **)&pFilterUnk);

    // Show the page. 
    CAUUID caGUID;
    pProp->GetPages(&caGUID);
    pProp->Release();
    OleCreatePropertyFrame(
        hWnd,                   // Parent window
        0, 0,                   // Reserved
        FilterInfo.achName,     // Caption for the dialog box
        1,                      // Number of objects (just the filter)
        &pFilterUnk,            // Array of object pointers. 
        caGUID.cElems,          // Number of property pages
        caGUID.pElems,          // Array of property page CLSIDs
        0,                      // Locale identifier
        0, NULL                 // Reserved
    );

    // Clean up.
    pFilterUnk->Release();
    FilterInfo.pGraph->Release(); 
    CoTaskMemFree(caGUID.pElems);
}
```



## <a name="related-topics"></a><span data-ttu-id="16e8c-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="16e8c-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16e8c-122">Grundlegende DirectShow-Aufgaben</span><span class="sxs-lookup"><span data-stu-id="16e8c-122">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> </dl>

 

 



