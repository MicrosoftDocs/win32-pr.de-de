---
description: Verwenden von DMOs in DirectShow
ms.assetid: 47d75b9c-8b0d-4235-8ac1-02ae1502c0e7
title: Verwenden von DMOs in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdddc643d39798dc09807e9ecfa15c38a6e0c2cf
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908688"
---
# <a name="using-dmos-in-directshow"></a><span data-ttu-id="4a250-103">Verwenden von DMOs in DirectShow</span><span class="sxs-lookup"><span data-stu-id="4a250-103">Using DMOs in DirectShow</span></span>

<span data-ttu-id="4a250-104">Anwendungen, die auf DirectShow basieren, können DMOs in einem Filterdiagramm über den [DMO-Wrapperfilter](dmo-wrapper-filter.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="4a250-104">Applications based on DirectShow can use DMOs in a filter graph, through the [DMO Wrapper](dmo-wrapper-filter.md) filter.</span></span> <span data-ttu-id="4a250-105">Dieser Filter aggregiert einen DMO und verarbeitet alle Details der Verwendung des DMO, z. B. das Übergeben von Daten an und von DMO, das Zuordnen von [**IMediaBuffer-Objekten**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) usw.</span><span class="sxs-lookup"><span data-stu-id="4a250-105">This filter aggregates a DMO and handles all the details of using the DMO, such as passing data to and from the DMO, allocating [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) objects, and so forth.</span></span>

<span data-ttu-id="4a250-106">Da der DMO-Filter aggregiert wird, kann die Anwendung den Filter für alle COM-Schnittstellen abfragen, die von DMO verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="4a250-106">Because the DMO is aggregated by the filter, the application can query the filter for any COM interfaces that the DMO exposes.</span></span> <span data-ttu-id="4a250-107">Die Anwendung sollte es dem Filter jedoch gestatten, alle Streamingvorgänge auf dem DMO zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="4a250-107">However, the application should let the filter handle all streaming operations on the DMO.</span></span> <span data-ttu-id="4a250-108">Legen Sie z. B. keine Medientypen fest, verarbeiten Sie puffer, leeren Sie den DMO, sperren Sie den DMO, aktivieren oder deaktivieren Sie die Qualitätskontrolle, oder legen Sie Videooptimierungen fest.</span><span class="sxs-lookup"><span data-stu-id="4a250-108">For example, do not set media types, process any buffers, flush the DMO, lock the DMO, enable or disable quality control, or set video optimizations.</span></span>

<span data-ttu-id="4a250-109">Wenn Sie den Klassenbezeichner (CLSID) eines bestimmten DMO kennen, den Sie verwenden möchten, können Sie den DMO-Wrapperfilter wie folgt mit diesem DMO initialisieren:</span><span class="sxs-lookup"><span data-stu-id="4a250-109">If you know the class identifier (CLSID) of a specific DMO that you want to use, you can initialize the DMO Wrapper filter with that DMO, as follows:</span></span>

1.  <span data-ttu-id="4a250-110">Rufen **Sie CoCreateInstance auf,** um den DMO-Wrapperfilter zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4a250-110">Call **CoCreateInstance** to create the DMO Wrapper filter.</span></span>
2.  <span data-ttu-id="4a250-111">Fragen Sie den DMO-Wrapperfilter für die [**IDMOWrapperFilter-Schnittstelle**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter) ab.</span><span class="sxs-lookup"><span data-stu-id="4a250-111">Query the DMO Wrapper filter for the [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter) interface.</span></span>
3.  <span data-ttu-id="4a250-112">Rufen Sie die [**IDMOWrapperFilter::Init-Methode**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) auf.</span><span class="sxs-lookup"><span data-stu-id="4a250-112">Call the [**IDMOWrapperFilter::Init**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) method.</span></span> <span data-ttu-id="4a250-113">Geben Sie die CLSID des DMO und die GUID der Kategorie des DMO an.</span><span class="sxs-lookup"><span data-stu-id="4a250-113">Specify the CLSID of the DMO and the GUID of the DMO's category.</span></span> <span data-ttu-id="4a250-114">Eine Liste der DMO-Kategorien finden Sie unter [DMO-GUIDs.](dmo-guids.md)</span><span class="sxs-lookup"><span data-stu-id="4a250-114">For a list of DMO categories, see [DMO GUIDs](dmo-guids.md).</span></span>

<span data-ttu-id="4a250-115">Diese Schritte sind im folgenden Code dargestellt:</span><span class="sxs-lookup"><span data-stu-id="4a250-115">The following code shows these steps:</span></span>


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



<span data-ttu-id="4a250-116">Die [**DMOEnum-Funktion**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) aufzählt DMOs in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="4a250-116">The [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) function enumerates DMOs in the registry.</span></span> <span data-ttu-id="4a250-117">Diese Funktion verwendet einen anderen Satz von Kategorie-GUIDs als diejenigen, die für DirectShow-Filter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a250-117">This function uses a different set of category GUIDs from the ones used for DirectShow filters.</span></span>

<span data-ttu-id="4a250-118">**Verwenden des Systemgeräte-Enumerators mit DMOs**</span><span class="sxs-lookup"><span data-stu-id="4a250-118">**Using the System Device Enumerator with DMOs**</span></span>

<span data-ttu-id="4a250-119">Anstatt einen DMO direkt zu erstellen, können Sie den [Systemgeräte-Enumerator](system-device-enumerator.md)verwenden, der jede DMO-Kategorie aufzählen kann, die von der **DMOEnum-Methode unterstützt** wird.</span><span class="sxs-lookup"><span data-stu-id="4a250-119">Instead of creating a DMO directly, you can use the [System Device Enumerator](system-device-enumerator.md), which can enumerate any DMO category that is supported by the **DMOEnum** method.</span></span> <span data-ttu-id="4a250-120">Der Systemgeräte-Enumerator enthält auch DMOs, wenn er bestimmte DirectShow-Filterkategorien auflistet.</span><span class="sxs-lookup"><span data-stu-id="4a250-120">The System Device Enumerator also includes DMOs when it enumerates certain DirectShow filter categories.</span></span> <span data-ttu-id="4a250-121">Die folgende Tabelle zeigt die Zuordnung zwischen DMO-Kategorien und DirectShow-Kategorien.</span><span class="sxs-lookup"><span data-stu-id="4a250-121">The following table shows the mapping between DMO categories and DirectShow categories.</span></span>



| <span data-ttu-id="4a250-122">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="4a250-122">Label</span></span> | <span data-ttu-id="4a250-123">Wert</span><span class="sxs-lookup"><span data-stu-id="4a250-123">Value</span></span> |
|-----------------------------|--------------------------------|
| <span data-ttu-id="4a250-124">DMO-Kategorie</span><span class="sxs-lookup"><span data-stu-id="4a250-124">DMO Category</span></span>                | <span data-ttu-id="4a250-125">DirectShow-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="4a250-125">DirectShow Equivalent</span></span>          |
| <span data-ttu-id="4a250-126">\_DMOCATEGORY-AUDIOENCODER \_</span><span class="sxs-lookup"><span data-stu-id="4a250-126">DMOCATEGORY\_AUDIO\_ENCODER</span></span> | <span data-ttu-id="4a250-127">CLSID \_ AudioCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="4a250-127">CLSID\_AudioCompressorCategory</span></span> |
| <span data-ttu-id="4a250-128">\_DMOCATEGORY-AUDIODECODER \_</span><span class="sxs-lookup"><span data-stu-id="4a250-128">DMOCATEGORY\_AUDIO\_DECODER</span></span> | <span data-ttu-id="4a250-129">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="4a250-129">CLSID\_LegacyAmFilterCategory</span></span>  |
| <span data-ttu-id="4a250-130">DMOCATEGORY \_ VIDEO \_ ENCODER</span><span class="sxs-lookup"><span data-stu-id="4a250-130">DMOCATEGORY\_VIDEO\_ENCODER</span></span> | <span data-ttu-id="4a250-131">CLSID \_ VideoCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="4a250-131">CLSID\_VideoCompressorCategory</span></span> |
| <span data-ttu-id="4a250-132">\_DMOCATEGORY-VIDEODECODER \_</span><span class="sxs-lookup"><span data-stu-id="4a250-132">DMOCATEGORY\_VIDEO\_DECODER</span></span> | <span data-ttu-id="4a250-133">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="4a250-133">CLSID\_LegacyAmFilterCategory</span></span>  |



 

<span data-ttu-id="4a250-134">Der Systemgeräte-Enumerator gibt eine Liste von Monikerobjekten zurück.</span><span class="sxs-lookup"><span data-stu-id="4a250-134">The System Device Enumerator returns a list of moniker objects.</span></span> <span data-ttu-id="4a250-135">Wenn der Moniker einen DMO darstellt, erstellt die **IMoniker::BindToObject-Methode** automatisch den DMO-Wrapperfilter und initialisiert ihn mit diesem DMO.</span><span class="sxs-lookup"><span data-stu-id="4a250-135">If the moniker represents a DMO, the **IMoniker::BindToObject** method automatically creates the DMO Wrapper filter and initializes it with that DMO.</span></span> <span data-ttu-id="4a250-136">Daher ist die Tatsache, dass ein DMO beteiligt ist, für die Anwendung transparent.</span><span class="sxs-lookup"><span data-stu-id="4a250-136">Thus, the fact that a DMO is involved is transparent to the application.</span></span> <span data-ttu-id="4a250-137">Weitere Informationen zur Verwendung des Systemgeräte-Enumerators finden Sie unter [Verwenden des Systemgeräte-Enumerators.](using-the-system-device-enumerator.md)</span><span class="sxs-lookup"><span data-stu-id="4a250-137">For more information on using the System Device Enumerator, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

<span data-ttu-id="4a250-138">**Einschränkungen**</span><span class="sxs-lookup"><span data-stu-id="4a250-138">**Limitations**</span></span>

<span data-ttu-id="4a250-139">Es gibt einige Einschränkungen bei der Verwendung von DMOs in DirectShow:</span><span class="sxs-lookup"><span data-stu-id="4a250-139">There are some limitations when using DMOs in DirectShow:</span></span>

-   <span data-ttu-id="4a250-140">Der DMO-Wrapperfilter unterstützt keine DMOs mit null Eingaben, mehreren Eingaben oder null Ausgaben.</span><span class="sxs-lookup"><span data-stu-id="4a250-140">The DMO Wrapper filter does not support DMOs with zero inputs, multiple inputs, or zero outputs.</span></span>
-   <span data-ttu-id="4a250-141">Alle Pinverbindungen im DMO-Wrapperfilter verwenden die [**IMemInputPin-Schnittstelle.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)</span><span class="sxs-lookup"><span data-stu-id="4a250-141">All pin connections on the DMO Wrapper Filter use the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>
-   <span data-ttu-id="4a250-142">DirectShow Editing Services unterstützt keine DMO-basierten Effekte oder Übergänge.</span><span class="sxs-lookup"><span data-stu-id="4a250-142">DirectShow Editing Services does not support DMO-based effects or transitions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a250-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4a250-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a250-144">Verwenden von DMOs</span><span class="sxs-lookup"><span data-stu-id="4a250-144">Using DMOs</span></span>](using-dmos.md)
</dt> </dl>

 

 



