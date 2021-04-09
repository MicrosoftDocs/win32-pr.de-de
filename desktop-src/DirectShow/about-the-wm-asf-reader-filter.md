---
description: Informationen zum WM-ASF-Reader-Filter
ms.assetid: e698c0da-88b2-497a-8a25-9d3b76c85a7d
title: Informationen zum WM-ASF-Reader-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 350e6597aa6aa66193af37a30ed54c37139d5f81
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860423"
---
# <a name="about-the-wm-asf-reader-filter"></a><span data-ttu-id="94105-103">Informationen zum WM-ASF-Reader-Filter</span><span class="sxs-lookup"><span data-stu-id="94105-103">About the WM ASF Reader Filter</span></span>

<span data-ttu-id="94105-104">Die Wiedergabe von ASF-Dateien wird vom [WM-ASF-Reader](wm-asf-reader-filter.md) -Filter behandelt.</span><span class="sxs-lookup"><span data-stu-id="94105-104">Playback of ASF files is handled by the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span> <span data-ttu-id="94105-105">Wenn der WM-ASF-Reader eine Datei liest, erstellt er automatisch eine Ausgabe-PIN für jeden Stream, einschließlich Webstreams, Skript befehlsstreams und beliebiger anderer Typen von beliebigem Stream.</span><span class="sxs-lookup"><span data-stu-id="94105-105">When the WM ASF Reader reads a file, it automatically creates an output pin for each stream, including web streams, script command streams, and any other type of arbitrary stream.</span></span> <span data-ttu-id="94105-106">Im Fall von Dateien mit mehreren Bitraten werden Pins nur für die aktuell ausgewählten Streams erstellt.</span><span class="sxs-lookup"><span data-stu-id="94105-106">In the case of multiple bit rate files, pins are created only for the currently selected streams.</span></span> <span data-ttu-id="94105-107">Um eine ASF-Datei mit dem WM-ASF-Reader-Filter wiederzugeben, müssen Sie [**igraphbuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) oder [**igraphbuilder:: addsourcefilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="94105-107">To play an ASF file with the WM ASF Reader filter, call [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) or [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).</span></span>

<span data-ttu-id="94105-108">Der WM-ASF-Reader unterstützt die Schnittstelle DirectShow [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , mit der Anwendungen eine temporale Suche innerhalb der Datei durchführen können.</span><span class="sxs-lookup"><span data-stu-id="94105-108">The WM ASF Reader supports the DirectShow [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, which enables applications to perform temporal seeking within the file.</span></span> <span data-ttu-id="94105-109">Die Wiedergabe mit einer anderen Geschwindigkeit als 1,0 (wie in [**imediaseeking::**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)\* angegeben) wird jedoch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="94105-109">However, playback at speeds other than 1.0 (as specified in [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)) is not supported.</span></span>

<span data-ttu-id="94105-110">Der WM-ASF-Lesefilter macht auch mehrere Windows Media-Format-SDK-Schnittstellen verfügbar, wie in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="94105-110">The WM ASF Reader filter also exposes several Windows Media Format SDK interfaces as described in the following table.</span></span> <span data-ttu-id="94105-111">Diese Schnittstellen sind in der Dokumentation zum Windows Media-Format SDK dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="94105-111">These interfaces are documented in the Windows Media Format SDK documentation.</span></span>



| <span data-ttu-id="94105-112">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="94105-112">Interface</span></span>                                             | <span data-ttu-id="94105-113">Verfügbar gemacht</span><span class="sxs-lookup"><span data-stu-id="94105-113">How exposed</span></span>                                 | <span data-ttu-id="94105-114">Kommentare</span><span class="sxs-lookup"><span data-stu-id="94105-114">Comments</span></span>                                                                                                                       |
|-------------------------------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="94105-115">**Iwmdrmreader**</span><span class="sxs-lookup"><span data-stu-id="94105-115">**IWMDRMReader**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | <span data-ttu-id="94105-116">Über **IServiceProvider** für den Filter.</span><span class="sxs-lookup"><span data-stu-id="94105-116">Through **IServiceProvider** on the filter.</span></span> | <span data-ttu-id="94105-117">Wird für Anwendungen bereitgestellt, die durch Digital Rights Management (DRM) geschützte Inhalte wiedergeben müssen.</span><span class="sxs-lookup"><span data-stu-id="94105-117">Provided for applications that need to play content protected by Digital Rights Management (DRM)..</span></span>                             |
| [<span data-ttu-id="94105-118">**Iwmheaderinfo**</span><span class="sxs-lookup"><span data-stu-id="94105-118">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | <span data-ttu-id="94105-119">**QueryInterface** für den Filter.</span><span class="sxs-lookup"><span data-stu-id="94105-119">**QueryInterface** on the filter.</span></span>           | <span data-ttu-id="94105-120">Bereitgestellt, damit Anwendungen Datei-und Inhalts Attribute sowie Marker-und Skriptinformationen sowie Metadaten lesen können.</span><span class="sxs-lookup"><span data-stu-id="94105-120">Provided so that applications can read file and content attributes, as well as marker and script information and metadata.</span></span>     |
| [<span data-ttu-id="94105-121">**Iwmreaderadvanced**</span><span class="sxs-lookup"><span data-stu-id="94105-121">**IWMReaderAdvanced**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | <span data-ttu-id="94105-122">**QueryInterface** für den Filter.</span><span class="sxs-lookup"><span data-stu-id="94105-122">**QueryInterface** on the filter.</span></span>           | <span data-ttu-id="94105-123">Teilweise für den Filter implementiert, damit Anwendungen auf die Informationsmethoden des WM-Reader-Objekts zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="94105-123">Partially implemented on the filter so that applications can access the informational methods on the WM Reader object.</span></span>         |
| [<span data-ttu-id="94105-124">**IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="94105-124">**IWMReaderAdvanced2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | <span data-ttu-id="94105-125">**QueryInterface** für den Filter.</span><span class="sxs-lookup"><span data-stu-id="94105-125">**QueryInterface** on the filter.</span></span>           | <span data-ttu-id="94105-126">Teilweise für den Filter implementiert, sodass Anwendungen auf die Informationsmethoden des Format-SDK-Reader-Objekts zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="94105-126">Partially implemented on the filter so that applications can access the informational methods on the Format SDK Reader Object.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="94105-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="94105-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94105-128">Lesen von ASF-Dateien in DirectShow</span><span class="sxs-lookup"><span data-stu-id="94105-128">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



