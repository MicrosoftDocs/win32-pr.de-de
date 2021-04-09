---
description: AVI-Kompressor-Filter
ms.assetid: addde51d-2982-4964-b16a-406fea89a0ce
title: AVI-Kompressor-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58f3ef342d1ea740503d9fc1e9e9b898aadc3801
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103859967"
---
# <a name="avi-compressor-filter"></a><span data-ttu-id="950b0-103">AVI-Kompressor-Filter</span><span class="sxs-lookup"><span data-stu-id="950b0-103">AVI Compressor Filter</span></span>

<span data-ttu-id="950b0-104">Der AVI-Kompressor-Filter ermöglicht die Verknüpfung von Video Komprimierungs-Manager-Codecs (VCM) mit einem Filter Diagramm.</span><span class="sxs-lookup"><span data-stu-id="950b0-104">The AVI Compressor filter enables Video Compression Manager (VCM) codecs to join a filter graph.</span></span> <span data-ttu-id="950b0-105">Jeder Codec wird als separate Instanz des Filters angezeigt.</span><span class="sxs-lookup"><span data-stu-id="950b0-105">Each codec appears as a separate instance of the filter.</span></span> <span data-ttu-id="950b0-106">Dieser Filter kann nicht direkt mit cokreatanstance erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="950b0-106">You cannot directly create this filter with CoCreateInstance.</span></span> <span data-ttu-id="950b0-107">Stattdessen müssen Sie den Enumerator für Systemgeräte verwenden.</span><span class="sxs-lookup"><span data-stu-id="950b0-107">Instead, you must use the system device enumerator.</span></span> <span data-ttu-id="950b0-108">Weitere Informationen finden Sie unter [using the System Device Enumerator](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="950b0-108">For more information, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

<span data-ttu-id="950b0-109">Die Eingabe-PIN des Filters stellt eine Verbindung mit Filtern her, die unkomprimierte Videodaten ausgeben, z. b. Video Erfassungs Filter oder den [avi-Splitter Filter](avi-splitter-filter.md)</span><span class="sxs-lookup"><span data-stu-id="950b0-109">The filter's input pin connects to filters that output uncompressed video data, such as video capture filters or the [AVI Splitter Filter](avi-splitter-filter.md).</span></span> <span data-ttu-id="950b0-110">Die Ausgabepin des Filters stellt in der Regel eine Verbindung mit einem MUX-Filter her, z. b. dem [AVI MUX](avi-mux-filter.md)</span><span class="sxs-lookup"><span data-stu-id="950b0-110">The filter's output pin typically connects to a MUX filter, such as the [AVI Mux Filter](avi-mux-filter.md).</span></span>

<span data-ttu-id="950b0-111">Wenn der Codec ein Dialogfeld oder ein Dialogfeld für eine VFW-Konfiguration im alten Stil unterstützt, kann eine Anwendung Sie mithilfe der [**iamvfwcompressdialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) -Schnittstelle anzeigen.</span><span class="sxs-lookup"><span data-stu-id="950b0-111">If the codec supports an old-style VFW configuration dialog box or About dialog box, an application can display it using the [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) interface.</span></span>

> [!Note]  
> <span data-ttu-id="950b0-112">MPEG-Kompressoren werden nie als VCM-Codecs implementiert, sondern nur als Native DirectShow-Filter.</span><span class="sxs-lookup"><span data-stu-id="950b0-112">MPEG compressors are never implemented as VCM codecs, but only as native DirectShow filters.</span></span>

 



|                                          |                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="950b0-113">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="950b0-113">Filter Interfaces</span></span>                        | <span data-ttu-id="950b0-114">[**Iamvfwcompressdialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs), [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages</span><span class="sxs-lookup"><span data-stu-id="950b0-114">[**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages</span></span>                                                                                                             |
| <span data-ttu-id="950b0-115">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="950b0-115">Input Pin Media Types</span></span>                    | <span data-ttu-id="950b0-116">MediaType- \_ Video, mediasubtype \_ null</span><span class="sxs-lookup"><span data-stu-id="950b0-116">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="950b0-117">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="950b0-117">Input Pin Interfaces</span></span>                     | <span data-ttu-id="950b0-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="950b0-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                             |
| <span data-ttu-id="950b0-119">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="950b0-119">Output Pin Media Types</span></span>                   | <span data-ttu-id="950b0-120">MediaType- \_ Video, mediasubtype \_ null</span><span class="sxs-lookup"><span data-stu-id="950b0-120">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="950b0-121">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="950b0-121">Output Pin Interfaces</span></span>                    | <span data-ttu-id="950b0-122">[**Iamstreamconfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition), [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="950b0-122">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="950b0-123">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="950b0-123">Filter CLSID</span></span>                             | <span data-ttu-id="950b0-124">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="950b0-124">Not applicable</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="950b0-125">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="950b0-125">Property Page CLSID</span></span>                      | <span data-ttu-id="950b0-126">Keine Eigenschaften Seite.</span><span class="sxs-lookup"><span data-stu-id="950b0-126">No property page.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="950b0-127">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="950b0-127">Executable</span></span>                               | <span data-ttu-id="950b0-128">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="950b0-128">qcap.dll</span></span>                                                                                                                                                                                                                                           |
| [<span data-ttu-id="950b0-129">Verdienst</span><span class="sxs-lookup"><span data-stu-id="950b0-129">Merit</span></span>](merit.md)                       | <span data-ttu-id="950b0-130">das Verdienst wird \_ \_ nicht \_ verwendet.</span><span class="sxs-lookup"><span data-stu-id="950b0-130">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="950b0-131">Filter Kategorie</span><span class="sxs-lookup"><span data-stu-id="950b0-131">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="950b0-132">CLSID \_ videocompressorcategory</span><span class="sxs-lookup"><span data-stu-id="950b0-132">CLSID\_VideoCompressorCategory</span></span>                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="950b0-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="950b0-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="950b0-134">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="950b0-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



