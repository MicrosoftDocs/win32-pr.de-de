---
description: AVI-160-Filter
ms.assetid: addde51d-2982-4964-b16a-406fea89a0ce
title: AVI-160-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 212ab58eb3800e0ad5531ebc5c50d3b054e7866c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909468"
---
# <a name="avi-compressor-filter"></a><span data-ttu-id="a4364-103">AVI-160-Filter</span><span class="sxs-lookup"><span data-stu-id="a4364-103">AVI Compressor Filter</span></span>

<span data-ttu-id="a4364-104">Mit dem FILTER AVI-Filter können Codecs des Videokomprimierungs-Managers (Video Compression Manager, VCM) einem Filterdiagramm beitreten.</span><span class="sxs-lookup"><span data-stu-id="a4364-104">The AVI Compressor filter enables Video Compression Manager (VCM) codecs to join a filter graph.</span></span> <span data-ttu-id="a4364-105">Jeder Codec wird als separate Instanz des Filters angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a4364-105">Each codec appears as a separate instance of the filter.</span></span> <span data-ttu-id="a4364-106">Sie können diesen Filter nicht direkt mit CoCreateInstance erstellen.</span><span class="sxs-lookup"><span data-stu-id="a4364-106">You cannot directly create this filter with CoCreateInstance.</span></span> <span data-ttu-id="a4364-107">Stattdessen müssen Sie den Systemgeräte-Enumerator verwenden.</span><span class="sxs-lookup"><span data-stu-id="a4364-107">Instead, you must use the system device enumerator.</span></span> <span data-ttu-id="a4364-108">Weitere Informationen finden Sie unter [Verwenden des Systemgeräte-Enumerators](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="a4364-108">For more information, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

<span data-ttu-id="a4364-109">Der Eingabepin des Filters stellt eine Verbindung mit Filtern her, die nicht komprimierte Videodaten ausgeben, z. B. Videoaufnahmefilter oder [den AVI-Splitterfilter.](avi-splitter-filter.md)</span><span class="sxs-lookup"><span data-stu-id="a4364-109">The filter's input pin connects to filters that output uncompressed video data, such as video capture filters or the [AVI Splitter Filter](avi-splitter-filter.md).</span></span> <span data-ttu-id="a4364-110">Der Ausgabepin des Filters stellt in der Regel eine Verbindung mit einem MUX-Filter her, z. B. mit dem [AVI Mux-Filter.](avi-mux-filter.md)</span><span class="sxs-lookup"><span data-stu-id="a4364-110">The filter's output pin typically connects to a MUX filter, such as the [AVI Mux Filter](avi-mux-filter.md).</span></span>

<span data-ttu-id="a4364-111">Wenn der Codec ein VFW-Konfigurationsdialogfeld im alten Stil oder das Dialogfeld About unterstützt, kann eine Anwendung es über die [**IAMVfwCompressDialogs-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a4364-111">If the codec supports an old-style VFW configuration dialog box or About dialog box, an application can display it using the [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) interface.</span></span>

> [!Note]  
> <span data-ttu-id="a4364-112">MPEG-Komprimierungsfilter werden nie als VCM-Codecs implementiert, sondern nur als native DirectShow-Filter.</span><span class="sxs-lookup"><span data-stu-id="a4364-112">MPEG compressors are never implemented as VCM codecs, but only as native DirectShow filters.</span></span>

 



| <span data-ttu-id="a4364-113">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="a4364-113">Label</span></span> | <span data-ttu-id="a4364-114">Wert</span><span class="sxs-lookup"><span data-stu-id="a4364-114">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4364-115">Filterschnittstellen</span><span class="sxs-lookup"><span data-stu-id="a4364-115">Filter Interfaces</span></span>                        | <span data-ttu-id="a4364-116">[**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages</span><span class="sxs-lookup"><span data-stu-id="a4364-116">[**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages</span></span>                                                                                                             |
| <span data-ttu-id="a4364-117">Eingabe-Stecknadelmedientypen</span><span class="sxs-lookup"><span data-stu-id="a4364-117">Input Pin Media Types</span></span>                    | <span data-ttu-id="a4364-118">MEDIATYPE \_ Video, MEDIASUBTYPE \_ NULL</span><span class="sxs-lookup"><span data-stu-id="a4364-118">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="a4364-119">Eingabe-Pin-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a4364-119">Input Pin Interfaces</span></span>                     | <span data-ttu-id="a4364-120">[**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="a4364-120">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                             |
| <span data-ttu-id="a4364-121">Medientypen des Ausgabepins</span><span class="sxs-lookup"><span data-stu-id="a4364-121">Output Pin Media Types</span></span>                   | <span data-ttu-id="a4364-122">MEDIATYPE \_ Video, MEDIASUBTYPE \_ NULL</span><span class="sxs-lookup"><span data-stu-id="a4364-122">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="a4364-123">Ausgabe-PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a4364-123">Output Pin Interfaces</span></span>                    | <span data-ttu-id="a4364-124">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="a4364-124">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="a4364-125">Filtern der CLSID</span><span class="sxs-lookup"><span data-stu-id="a4364-125">Filter CLSID</span></span>                             | <span data-ttu-id="a4364-126">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="a4364-126">Not applicable</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="a4364-127">Eigenschaftenseite CLSID</span><span class="sxs-lookup"><span data-stu-id="a4364-127">Property Page CLSID</span></span>                      | <span data-ttu-id="a4364-128">Keine Eigenschaftenseite.</span><span class="sxs-lookup"><span data-stu-id="a4364-128">No property page.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="a4364-129">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="a4364-129">Executable</span></span>                               | <span data-ttu-id="a4364-130">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="a4364-130">qcap.dll</span></span>                                                                                                                                                                                                                                           |
| [<span data-ttu-id="a4364-131">Verdienst</span><span class="sxs-lookup"><span data-stu-id="a4364-131">Merit</span></span>](merit.md)                       | <span data-ttu-id="a4364-132">NICHT \_ \_ VERWENDEN \_</span><span class="sxs-lookup"><span data-stu-id="a4364-132">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="a4364-133">Filterkategorie</span><span class="sxs-lookup"><span data-stu-id="a4364-133">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="a4364-134">CLSID \_ VideoCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="a4364-134">CLSID\_VideoCompressorCategory</span></span>                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="a4364-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a4364-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4364-136">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="a4364-136">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



