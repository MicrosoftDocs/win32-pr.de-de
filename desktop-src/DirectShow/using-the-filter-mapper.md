---
description: Verwenden des Filter Mappers
ms.assetid: 3f774350-4508-437f-98d1-cca91220f339
title: Verwenden des Filter Mappers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c2d7acf85a7b415fc161cd21e17d069b46c3f40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866452"
---
# <a name="using-the-filter-mapper"></a><span data-ttu-id="7eee2-103">Verwenden des Filter Mappers</span><span class="sxs-lookup"><span data-stu-id="7eee2-103">Using the Filter Mapper</span></span>

<span data-ttu-id="7eee2-104">Der [Filter Mapper](filter-mapper.md) ist ein COM-Objekt, das DirectShow-Filter auf der Grundlage verschiedener Suchkriterien auflistet.</span><span class="sxs-lookup"><span data-stu-id="7eee2-104">The [Filter Mapper](filter-mapper.md) is a COM object that enumerates DirectShow filters based on various search criteria.</span></span> <span data-ttu-id="7eee2-105">Der Filter Mapper kann weniger effizient sein als der Enumerator des System Geräts. Wenn Sie also Filter aus einer bestimmten Kategorie benötigen, sollten Sie den Enumerator des System Geräts verwenden.</span><span class="sxs-lookup"><span data-stu-id="7eee2-105">The Filter Mapper can be less efficient than the System Device Enumerator, so if you need filters from a particular category, you should use the System Device Enumerator.</span></span> <span data-ttu-id="7eee2-106">Wenn Sie jedoch einen Filter suchen müssen, der eine bestimmte Kombination von Medientypen unterstützt, aber nicht in eine Kategorie mit klarer Ausschneiden fällt, müssen Sie möglicherweise den Filter Mapper verwenden.</span><span class="sxs-lookup"><span data-stu-id="7eee2-106">But if you need to locate a filter that supports a certain combination of media types, but does not fall into a clear-cut category, you might need to use the Filter Mapper.</span></span> <span data-ttu-id="7eee2-107">(Ein Beispiel wäre ein rendererfilter oder ein Decoderfilter.)</span><span class="sxs-lookup"><span data-stu-id="7eee2-107">(An example would be a renderer filter or a decoder filter.)</span></span>

<span data-ttu-id="7eee2-108">Der Filter Mapper macht die [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7eee2-108">The Filter Mapper exposes the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface.</span></span> <span data-ttu-id="7eee2-109">Um nach einem Filter zu suchen, wird die [**IFilterMapper2:: enummatchingfilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="7eee2-109">To search for a filter, call the [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method.</span></span> <span data-ttu-id="7eee2-110">Diese Methode nimmt mehrere Parameter an, die die Suchkriterien definieren, und gibt einen Enumerator für die übereinstimmenden Filter zurück.</span><span class="sxs-lookup"><span data-stu-id="7eee2-110">This method takes several parameters that define the search criteria, and returns an enumerator for the matching filters.</span></span> <span data-ttu-id="7eee2-111">Der Enumerator unterstützt die [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) -Schnittstelle und stellt einen eindeutigen Moniker für jeden übereinstimmenden Filter bereit.</span><span class="sxs-lookup"><span data-stu-id="7eee2-111">The enumerator supports the [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) interface, and supplies a unique moniker for each matching filter.</span></span>

<span data-ttu-id="7eee2-112">Im folgenden Beispiel werden Filter aufgelistet, die die Eingabe von digitalen Videos (DV) akzeptieren und mindestens eine Ausgabe-PIN eines beliebigen Medientyps aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7eee2-112">The following example enumerates filters that accept digital video (DV) input and have at least one output pin, of any media type.</span></span> <span data-ttu-id="7eee2-113">(Der [DV-Video Decoder](dv-video-decoder-filter.md) -Filter entspricht diesen Kriterien.)</span><span class="sxs-lookup"><span data-stu-id="7eee2-113">(The [DV Video Decoder](dv-video-decoder-filter.md) filter matches these criteria.)</span></span>


```C++
IFilterMapper2 *pMapper = NULL;
IEnumMoniker *pEnum = NULL;

hr = CoCreateInstance(CLSID_FilterMapper2, 
    NULL, CLSCTX_INPROC, IID_IFilterMapper2, 
    (void **) &pMapper);

if (FAILED(hr))
{
    // Error handling omitted for clarity.
}

GUID arrayInTypes[2];
arrayInTypes[0] = MEDIATYPE_Video;
arrayInTypes[1] = MEDIASUBTYPE_dvsd;

hr = pMapper->EnumMatchingFilters(
        &pEnum,
        0,                  // Reserved.
        TRUE,               // Use exact match?
        MERIT_DO_NOT_USE+1, // Minimum merit.
        TRUE,               // At least one input pin?
        1,                  // Number of major type/subtype pairs for input.
        arrayInTypes,       // Array of major type/subtype pairs for input.
        NULL,               // Input medium.
        NULL,               // Input pin category.
        FALSE,              // Must be a renderer?
        TRUE,               // At least one output pin?
        0,                  // Number of major type/subtype pairs for output.
        NULL,               // Array of major type/subtype pairs for output.
        NULL,               // Output medium.
        NULL);              // Output pin category.

// Enumerate the monikers.
IMoniker *pMoniker;
ULONG cFetched;
while (pEnum->Next(1, &pMoniker, &cFetched) == S_OK)
{
    IPropertyBag *pPropBag = NULL;
    hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
       (void **)&pPropBag);

    if (SUCCEEDED(hr))
    {
        // To retrieve the friendly name of the filter, do the following:
        VARIANT varName;
        VariantInit(&varName);
        hr = pPropBag->Read(L"FriendlyName", &varName, 0);
        if (SUCCEEDED(hr))
        {
            // Display the name in your UI somehow.
        }
        VariantClear(&varName);

        // To create an instance of the filter, do the following:
        IBaseFilter *pFilter;
        hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter, (void**)&pFilter);
        // Now add the filter to the graph. Remember to release pFilter later.
    
        // Clean up.
        pPropBag->Release();
    }
    pMoniker->Release();
}

// Clean up.
pMapper->Release();
pEnum->Release();
```



<span data-ttu-id="7eee2-114">Die [**enummatchingfilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) -Methode verfügt über eine relativ große Anzahl von Parametern, die im Beispiel kommentiert werden.</span><span class="sxs-lookup"><span data-stu-id="7eee2-114">The [**EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method has a fairly large number of parameters, which are commented in the example.</span></span> <span data-ttu-id="7eee2-115">Die wichtigsten für dieses Beispiel sind:</span><span class="sxs-lookup"><span data-stu-id="7eee2-115">The significant ones for this example include:</span></span>

-   <span data-ttu-id="7eee2-116">Minimalwert: der Filter muss über einen Wert verfügen, der über einen Wert verfügt, der \_ \_ nicht \_ verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7eee2-116">Minimum merit value: The filter must have a merit value above MERIT\_DO\_NOT\_USE.</span></span>
-   <span data-ttu-id="7eee2-117">Eingabetypen: der Aufrufer übergibt ein Array mit Paaren von Haupttypen und Untertypen.</span><span class="sxs-lookup"><span data-stu-id="7eee2-117">Input types: The caller passes an array containing pairs of major types and subtypes.</span></span> <span data-ttu-id="7eee2-118">Nur Filter, die mindestens eines dieser Paare unterstützen, stimmen zu.</span><span class="sxs-lookup"><span data-stu-id="7eee2-118">Only filters that support at least one of these pairs will match.</span></span>
-   <span data-ttu-id="7eee2-119">Exakte Entsprechung: bei einem Filter können **null** -Werte für den Haupttyp, den Untertyp, die PIN-Kategorie oder das Medium registriert werden.</span><span class="sxs-lookup"><span data-stu-id="7eee2-119">Exact match: A filter can register **NULL** values for major type, subtype, pin category, or medium.</span></span> <span data-ttu-id="7eee2-120">Wenn Sie keine genaue Übereinstimmung angeben, fungiert ein **null** -Wert als Platzhalter, der mit jedem von Ihnen angegebenen Wert übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="7eee2-120">Unless you specify exact matching, a **NULL** value acts as a wildcard, matching any value that you specify.</span></span> <span data-ttu-id="7eee2-121">Mit der exakten Übereinstimmung muss der Filter genau mit Ihren Kriterien übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7eee2-121">With exact matching, the filter must exactly match your criteria.</span></span> <span data-ttu-id="7eee2-122">Wenn Sie jedoch einen **null** -Parameter in den Suchkriterien angeben, fungiert er immer als Platzhalter-oder "kein Pflege"-Wert, der mit einem beliebigen Filter übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="7eee2-122">However, if you give a **NULL** parameter in the search criteria, it always acts as a wildcard or "don't care" value, matching any filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7eee2-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7eee2-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7eee2-124">Auflisten von Geräten und Filtern</span><span class="sxs-lookup"><span data-stu-id="7eee2-124">Enumerating Devices and Filters</span></span>](enumerating-devices-and-filters.md)
</dt> <dt>

[<span data-ttu-id="7eee2-125">Intelligent Connect</span><span class="sxs-lookup"><span data-stu-id="7eee2-125">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> </dl>

 

 
