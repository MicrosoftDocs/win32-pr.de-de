---
description: Verwenden von dmos in DirectShow
ms.assetid: 47d75b9c-8b0d-4235-8ac1-02ae1502c0e7
title: Verwenden von dmos in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c90513649756a49067e523390292d4b44e1eac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131885"
---
# <a name="using-dmos-in-directshow"></a><span data-ttu-id="92085-103">Verwenden von dmos in DirectShow</span><span class="sxs-lookup"><span data-stu-id="92085-103">Using DMOs in DirectShow</span></span>

<span data-ttu-id="92085-104">Anwendungen, die auf DirectShow basieren, können DMOS in einem Filter Diagramm über den [DMO-Wrapper](dmo-wrapper-filter.md) Filter verwenden.</span><span class="sxs-lookup"><span data-stu-id="92085-104">Applications based on DirectShow can use DMOs in a filter graph, through the [DMO Wrapper](dmo-wrapper-filter.md) filter.</span></span> <span data-ttu-id="92085-105">Mit diesem Filter wird ein DMO aggregiert und alle Details der Verwendung des DMO behandelt, z. b. das Übergeben von Daten an und aus dem DMO, das Zuordnen von [**imediabuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) -Objekten usw.</span><span class="sxs-lookup"><span data-stu-id="92085-105">This filter aggregates a DMO and handles all the details of using the DMO, such as passing data to and from the DMO, allocating [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) objects, and so forth.</span></span>

<span data-ttu-id="92085-106">Da der DMO durch den Filter aggregiert wird, kann die Anwendung den Filter nach allen vom DMO verfügbar gemachten com-Schnittstellen Abfragen.</span><span class="sxs-lookup"><span data-stu-id="92085-106">Because the DMO is aggregated by the filter, the application can query the filter for any COM interfaces that the DMO exposes.</span></span> <span data-ttu-id="92085-107">Die Anwendung sollte den Filter jedoch alle Streamingvorgänge für den DMO verarbeiten lassen.</span><span class="sxs-lookup"><span data-stu-id="92085-107">However, the application should let the filter handle all streaming operations on the DMO.</span></span> <span data-ttu-id="92085-108">Legen Sie z. b. keine Medientypen fest, verarbeiten Sie alle Puffer, leeren Sie den DMO, Sperren Sie DMO, aktivieren oder deaktivieren Sie die Qualitätskontrolle, oder legen Sie Video Optimierungen fest.</span><span class="sxs-lookup"><span data-stu-id="92085-108">For example, do not set media types, process any buffers, flush the DMO, lock the DMO, enable or disable quality control, or set video optimizations.</span></span>

<span data-ttu-id="92085-109">Wenn Sie die Klassen-ID (CLSID) eines bestimmten DMO kennen, das Sie verwenden möchten, können Sie den DMO-Wrapper Filter mit diesem DMO wie folgt initialisieren:</span><span class="sxs-lookup"><span data-stu-id="92085-109">If you know the class identifier (CLSID) of a specific DMO that you want to use, you can initialize the DMO Wrapper filter with that DMO, as follows:</span></span>

1.  <span data-ttu-id="92085-110">Rufen Sie **cokreateinstance** auf, um den DMO-Wrapper Filter zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="92085-110">Call **CoCreateInstance** to create the DMO Wrapper filter.</span></span>
2.  <span data-ttu-id="92085-111">Fragen Sie den DMO-Wrapper Filter für die [**idmowrapperfilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="92085-111">Query the DMO Wrapper filter for the [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter) interface.</span></span>
3.  <span data-ttu-id="92085-112">Nennen Sie die [**idmuwrapperfilter:: init**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) -Methode.</span><span class="sxs-lookup"><span data-stu-id="92085-112">Call the [**IDMOWrapperFilter::Init**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) method.</span></span> <span data-ttu-id="92085-113">Geben Sie die CLSID des DMO und die GUID der Kategorie des DMO an.</span><span class="sxs-lookup"><span data-stu-id="92085-113">Specify the CLSID of the DMO and the GUID of the DMO's category.</span></span> <span data-ttu-id="92085-114">Eine Liste der DMO-Kategorien finden Sie unter [DMO-GUIDs](dmo-guids.md).</span><span class="sxs-lookup"><span data-stu-id="92085-114">For a list of DMO categories, see [DMO GUIDs](dmo-guids.md).</span></span>

<span data-ttu-id="92085-115">Diese Schritte sind im folgenden Code dargestellt:</span><span class="sxs-lookup"><span data-stu-id="92085-115">The following code shows these steps:</span></span>


```C++
// Create the DMO Wrapper filter.
IBaseFilter *pFilter;
HRESULT hr = CoCreateInstance(CLSID_DMOWrapperFilter, NULL, 
    CLSCTX_INPROC_SERVER, IID_IBaseFilter, 
    reinterpret_cast<void**>(&pFilter));

if (SUCCEEDED(hr)) 
{
    // Query for IDMOWrapperFilter.
    IDMOWrapperFilter *pDmoWrapper;
    hr = pFilter->QueryInterface(IID_IDMOWrapperFilter, 
        reinterpret_cast<void**>(&pDmoWrapper));

    if (SUCCEEDED(hr)) 
    {     
        // Initialize the filter.
        hr = pDmoWrapper->Init(CLSID_MyDMO, DMOCATEGORY_VIDEO_EFFECT); 
        pDmoWrapper->Release();

        if (SUCCEEDED(hr)) 
        {
            // Add the filter to the graph.
            hr = pGraph->AddFilter(pFilter, L"My DMO");
        }
    }
    pFilter->Release();
}
```



<span data-ttu-id="92085-116">Die [**dmuenum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) -Funktion Listet DMOS in der Registrierung auf.</span><span class="sxs-lookup"><span data-stu-id="92085-116">The [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) function enumerates DMOs in the registry.</span></span> <span data-ttu-id="92085-117">Diese Funktion verwendet einen anderen Satz von Kategorien-GUIDs, die für DirectShow-Filter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="92085-117">This function uses a different set of category GUIDs from the ones used for DirectShow filters.</span></span>

<span data-ttu-id="92085-118">**Verwenden des Enumerators für System Geräte mit DMOS**</span><span class="sxs-lookup"><span data-stu-id="92085-118">**Using the System Device Enumerator with DMOs**</span></span>

<span data-ttu-id="92085-119">Anstatt ein DMO direkt zu erstellen, können Sie den [Enumerator für System Geräte](system-device-enumerator.md)verwenden, der jede von der **dmoenum** -Methode unterstützte DMO-Kategorie auflisten kann.</span><span class="sxs-lookup"><span data-stu-id="92085-119">Instead of creating a DMO directly, you can use the [System Device Enumerator](system-device-enumerator.md), which can enumerate any DMO category that is supported by the **DMOEnum** method.</span></span> <span data-ttu-id="92085-120">Der Enumerator für System Geräte enthält auch DMOS, wenn er bestimmte DirectShow-Filter Kategorien auflistet.</span><span class="sxs-lookup"><span data-stu-id="92085-120">The System Device Enumerator also includes DMOs when it enumerates certain DirectShow filter categories.</span></span> <span data-ttu-id="92085-121">Die folgende Tabelle zeigt die Zuordnung zwischen DMO-Kategorien und DirectShow-Kategorien.</span><span class="sxs-lookup"><span data-stu-id="92085-121">The following table shows the mapping between DMO categories and DirectShow categories.</span></span>



|                             |                                |
|-----------------------------|--------------------------------|
| <span data-ttu-id="92085-122">DMO-Kategorie</span><span class="sxs-lookup"><span data-stu-id="92085-122">DMO Category</span></span>                | <span data-ttu-id="92085-123">DirectShow-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="92085-123">DirectShow Equivalent</span></span>          |
| <span data-ttu-id="92085-124">dmucategory \_ - \_ Audioencoder</span><span class="sxs-lookup"><span data-stu-id="92085-124">DMOCATEGORY\_AUDIO\_ENCODER</span></span> | <span data-ttu-id="92085-125">CLSID \_ audiocompressorcategory</span><span class="sxs-lookup"><span data-stu-id="92085-125">CLSID\_AudioCompressorCategory</span></span> |
| <span data-ttu-id="92085-126">dmucategory \_ - \_ Audiodecoder</span><span class="sxs-lookup"><span data-stu-id="92085-126">DMOCATEGORY\_AUDIO\_DECODER</span></span> | <span data-ttu-id="92085-127">CLSID \_ legacyamfiltercategory</span><span class="sxs-lookup"><span data-stu-id="92085-127">CLSID\_LegacyAmFilterCategory</span></span>  |
| <span data-ttu-id="92085-128">dmucategory- \_ Video \_ Encoder</span><span class="sxs-lookup"><span data-stu-id="92085-128">DMOCATEGORY\_VIDEO\_ENCODER</span></span> | <span data-ttu-id="92085-129">CLSID \_ videocompressorcategory</span><span class="sxs-lookup"><span data-stu-id="92085-129">CLSID\_VideoCompressorCategory</span></span> |
| <span data-ttu-id="92085-130">dmucategory- \_ Video \_ Decoder</span><span class="sxs-lookup"><span data-stu-id="92085-130">DMOCATEGORY\_VIDEO\_DECODER</span></span> | <span data-ttu-id="92085-131">CLSID \_ legacyamfiltercategory</span><span class="sxs-lookup"><span data-stu-id="92085-131">CLSID\_LegacyAmFilterCategory</span></span>  |



 

<span data-ttu-id="92085-132">Der Enumerator für System Geräte gibt eine Liste der monikerobjekte zurück.</span><span class="sxs-lookup"><span data-stu-id="92085-132">The System Device Enumerator returns a list of moniker objects.</span></span> <span data-ttu-id="92085-133">Wenn der Moniker ein DMO darstellt, erstellt die **IMoniker:: BindTo Object** -Methode automatisch den DMO-Wrapper Filter und initialisiert ihn mit diesem DMO.</span><span class="sxs-lookup"><span data-stu-id="92085-133">If the moniker represents a DMO, the **IMoniker::BindToObject** method automatically creates the DMO Wrapper filter and initializes it with that DMO.</span></span> <span data-ttu-id="92085-134">Folglich ist die Tatsache, dass ein DMO beteiligt ist, für die Anwendung transparent.</span><span class="sxs-lookup"><span data-stu-id="92085-134">Thus, the fact that a DMO is involved is transparent to the application.</span></span> <span data-ttu-id="92085-135">Weitere Informationen zur Verwendung des Enumerators für Systemgeräte finden Sie unter [using the System Device Enumerator](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="92085-135">For more information on using the System Device Enumerator, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

<span data-ttu-id="92085-136">**Einschränkungen**</span><span class="sxs-lookup"><span data-stu-id="92085-136">**Limitations**</span></span>

<span data-ttu-id="92085-137">Bei der Verwendung von dmos in DirectShow sind einige Einschränkungen zu beachten:</span><span class="sxs-lookup"><span data-stu-id="92085-137">There are some limitations when using DMOs in DirectShow:</span></span>

-   <span data-ttu-id="92085-138">Der DMO-Wrapper Filter unterstützt keine DMOS mit NULL Eingaben, mehreren Eingaben oder null Ausgaben.</span><span class="sxs-lookup"><span data-stu-id="92085-138">The DMO Wrapper filter does not support DMOs with zero inputs, multiple inputs, or zero outputs.</span></span>
-   <span data-ttu-id="92085-139">Alle Pin-Verbindungen im DMO-Wrapper Filter verwenden die [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="92085-139">All pin connections on the DMO Wrapper Filter use the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>
-   <span data-ttu-id="92085-140">DirectShow-Bearbeitungs Dienste unterstützen keine DMO-basierten Effekte oder Übergänge.</span><span class="sxs-lookup"><span data-stu-id="92085-140">DirectShow Editing Services does not support DMO-based effects or transitions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="92085-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="92085-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92085-142">Verwenden von dmos</span><span class="sxs-lookup"><span data-stu-id="92085-142">Using DMOs</span></span>](using-dmos.md)
</dt> </dl>

 

 



