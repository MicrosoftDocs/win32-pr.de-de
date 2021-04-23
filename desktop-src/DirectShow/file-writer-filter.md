---
description: File Writer-Filter
ms.assetid: 2bfbea8a-679f-4656-9ff3-fdf34aa0eb26
title: File Writer-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e991536d505ee1bdfcaaaca5ce8660c4480decf6
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909688"
---
# <a name="file-writer-filter"></a><span data-ttu-id="6d299-103">File Writer-Filter</span><span class="sxs-lookup"><span data-stu-id="6d299-103">File Writer Filter</span></span>

<span data-ttu-id="6d299-104">Der File Writer-Filter kann verwendet werden, um Dateien unabhängig vom Format auf den Datenträger zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="6d299-104">The File Writer filter can be used to write files to disc regardless of format.</span></span> <span data-ttu-id="6d299-105">Der Filter schreibt einfach auf den Datenträger, was er auf seinem Eingabepin empfängt, sodass er mit einem Multiplexer verbunden werden muss, der die Datei ordnungsgemäß formatieren kann.</span><span class="sxs-lookup"><span data-stu-id="6d299-105">The filter simply writes to disc whatever it receives on its input pin, so it must be connected upstream to a multiplexer that can format the file correctly.</span></span> <span data-ttu-id="6d299-106">Sie können eine neue Ausgabedatei mit dem Dateiwriter erstellen oder eine vorhandene Datei angeben. Wenn die Datei bereits vorhanden ist, wird sie vollständig mit den neuen Daten überschrieben.</span><span class="sxs-lookup"><span data-stu-id="6d299-106">You can create a new output file with the File Writer or specify an existing file; if the file already exists, it will be completely overwritten with the new data.</span></span>

<span data-ttu-id="6d299-107">Der Dateiwriterfilter verwendet die Zeitstempel des Eingabestreams als Dateioffsets und bietet zufälligen Zugriff auf die Datei.</span><span class="sxs-lookup"><span data-stu-id="6d299-107">The file writer filter uses the input stream's time stamps as file offsets and provides random access to the file.</span></span> <span data-ttu-id="6d299-108">IStream  wird unterstützt, um das Lesen und Schreiben des Dateiheaders zu ermöglichen, nachdem das Diagramm beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="6d299-108">It supports **IStream** to allow reading and writing the file header after the graph is stopped.</span></span> <span data-ttu-id="6d299-109">Zur Verbesserung der Leistung werden auch nicht gepufferte überlappende Schreibvorgänge unterstützt und die entsprechende Pufferaushandlung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="6d299-109">To improve performance it also supports unbuffered overlapped writes and handles the corresponding buffer negotiation.</span></span>

> [!Note]  
> <span data-ttu-id="6d299-110">Verwenden Sie zum Schreiben von ASF-Dateien den [WM ASF](wm-asf-writer-filter.md) Writer-Filter.</span><span class="sxs-lookup"><span data-stu-id="6d299-110">To write ASF files, use the [WM ASF Writer](wm-asf-writer-filter.md) filter.</span></span>

 



| <span data-ttu-id="6d299-111">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="6d299-111">Label</span></span> | <span data-ttu-id="6d299-112">Wert</span><span class="sxs-lookup"><span data-stu-id="6d299-112">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d299-113">Filterschnittstellen</span><span class="sxs-lookup"><span data-stu-id="6d299-113">Filter Interfaces</span></span>                        | <span data-ttu-id="6d299-114">[**IAMFilterMiscFlags,**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IFileSinkFilter,**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) [**IFileSinkFilter2,**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2) **IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="6d299-114">[**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), **IPersistStream**</span></span> |
| <span data-ttu-id="6d299-115">Eingabe-Stecknadelmedientypen</span><span class="sxs-lookup"><span data-stu-id="6d299-115">Input Pin Media Types</span></span>                    | <span data-ttu-id="6d299-116">\_MEDIATYPE-Stream, MEDIASUBTYPE \_ NULL</span><span class="sxs-lookup"><span data-stu-id="6d299-116">MEDIATYPE\_Stream, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                              |
| <span data-ttu-id="6d299-117">Eingabe-Pin-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="6d299-117">Input Pin Interfaces</span></span>                     | <span data-ttu-id="6d299-118">[**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl,**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) **IStream**</span><span class="sxs-lookup"><span data-stu-id="6d299-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), **IStream**</span></span>                                                                                |
| <span data-ttu-id="6d299-119">Medientypen des Ausgabepins</span><span class="sxs-lookup"><span data-stu-id="6d299-119">Output Pin Media Types</span></span>                   | <span data-ttu-id="6d299-120">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="6d299-120">Not applicable</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="6d299-121">Ausgabe-Pin-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="6d299-121">Output Pin Interfaces</span></span>                    | <span data-ttu-id="6d299-122">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="6d299-122">Not applicable</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="6d299-123">Filtern von CLSID</span><span class="sxs-lookup"><span data-stu-id="6d299-123">Filter CLSID</span></span>                             | <span data-ttu-id="6d299-124">CLSID \_ FileWriter</span><span class="sxs-lookup"><span data-stu-id="6d299-124">CLSID\_FileWriter</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="6d299-125">Eigenschaftenseite CLSID</span><span class="sxs-lookup"><span data-stu-id="6d299-125">Property Page CLSID</span></span>                      | <span data-ttu-id="6d299-126">Keine Eigenschaftenseite</span><span class="sxs-lookup"><span data-stu-id="6d299-126">No property page</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="6d299-127">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="6d299-127">Executable</span></span>                               | <span data-ttu-id="6d299-128">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="6d299-128">qcap.dll</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="6d299-129">Verdienst</span><span class="sxs-lookup"><span data-stu-id="6d299-129">Merit</span></span>](merit.md)                       | <span data-ttu-id="6d299-130">NICHT \_ \_ VERWENDEN \_</span><span class="sxs-lookup"><span data-stu-id="6d299-130">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                |
| [<span data-ttu-id="6d299-131">Filterkategorie</span><span class="sxs-lookup"><span data-stu-id="6d299-131">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="6d299-132">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="6d299-132">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="6d299-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6d299-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d299-134">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="6d299-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



