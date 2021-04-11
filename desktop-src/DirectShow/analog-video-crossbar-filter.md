---
description: Navigationsleiste des analogen Videos
ms.assetid: 668f6a8b-a4ed-4e4a-956c-a87f165225fa
title: Navigationsleiste des analogen Videos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2eb086b85859a3e1e895cd322c68c56916ac19a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103957889"
---
# <a name="analog-video-crossbar-filter"></a><span data-ttu-id="67a2b-103">Navigationsleiste des analogen Videos</span><span class="sxs-lookup"><span data-stu-id="67a2b-103">Analog Video Crossbar Filter</span></span>

<span data-ttu-id="67a2b-104">Der Symbolleisten Filter für die analoge Video Darstellung stellt eine Video quer Leiste auf einem Video Erfassungsgerät dar, das die Windows-Treibermodell (WDM) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="67a2b-104">The Analog Video Crossbar filter represents a video crossbar on a video capture device that supports the Windows Driver Model (WDM).</span></span>

<span data-ttu-id="67a2b-105">Dieser Filter ist ein Wrapper Filter für crossbars auf WDM-Streaminggeräten.</span><span class="sxs-lookup"><span data-stu-id="67a2b-105">This filter is a wrapper filter for crossbars on WDM streaming devices.</span></span> <span data-ttu-id="67a2b-106">Der Anzeige Name des Filters wird vom Gerät übernommen.</span><span class="sxs-lookup"><span data-stu-id="67a2b-106">The filter's friendly name is taken from the device.</span></span> <span data-ttu-id="67a2b-107">Jeder Ausgabepin stellt einen Hardware Pfad für das analoge Baseband-Video dar.</span><span class="sxs-lookup"><span data-stu-id="67a2b-107">Each output pin represents a hardware path for analog baseband video.</span></span> <span data-ttu-id="67a2b-108">Einer der Eingabe Pins stammt von einem TV-Tuner (der [TV-Tuner-Filter](tv-tuner-filter.md)).</span><span class="sxs-lookup"><span data-stu-id="67a2b-108">One of the input pins comes from a TV Tuner (the [TV Tuner Filter](tv-tuner-filter.md)).</span></span> <span data-ttu-id="67a2b-109">Andere Eingabe-Pins unterstützen Video-oder Audiostreams.</span><span class="sxs-lookup"><span data-stu-id="67a2b-109">Other input pins support video or audio streams.</span></span> <span data-ttu-id="67a2b-110">Der Filter unterstützt alle Medien Untertypen und Formate, die von den downstreamverbindungen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="67a2b-110">The filter supports any media subtypes and formats that are supported on the downstream connections.</span></span>

<span data-ttu-id="67a2b-111">Dieser Filter kann nicht direkt mit cokreatanstance erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="67a2b-111">You cannot directly create this filter with CoCreateInstance.</span></span> <span data-ttu-id="67a2b-112">Die [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) -Schnittstelle fügt diesen Filter nach Bedarf automatisch dem Diagramm hinzu.</span><span class="sxs-lookup"><span data-stu-id="67a2b-112">The [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface automatically adds this filter to the graph as needed.</span></span>

<span data-ttu-id="67a2b-113">Weitere Informationen zu Wrapper Filtern und WDM-Streaminggeräten finden Sie unter [wie Hardware Geräte am Filter Diagramm teilnehmen](how-hardware-devices-participate-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="67a2b-113">For more information on wrapper filters and WDM streaming devices, see [How Hardware Devices Participate in the Filter Graph](how-hardware-devices-participate-in-the-filter-graph.md).</span></span>



|                                          |                                                                                                |
|------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67a2b-114">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="67a2b-114">Filter Interfaces</span></span>                        | <span data-ttu-id="67a2b-115">[**Iamcrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar), ISpecifyPropertyPages, IPersistPropertyBag, IPersistStream</span><span class="sxs-lookup"><span data-stu-id="67a2b-115">[**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar), ISpecifyPropertyPages, IPersistPropertyBag, IPersistStream</span></span> |
| <span data-ttu-id="67a2b-116">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="67a2b-116">Input Pin Media Types</span></span>                    | <span data-ttu-id="67a2b-117">MediaType \_ Analog gaudiodatei, MediaType \_ Analog gvideo</span><span class="sxs-lookup"><span data-stu-id="67a2b-117">MEDIATYPE\_AnalogAudio, MEDIATYPE\_AnalogVideo</span></span>                                                 |
| <span data-ttu-id="67a2b-118">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="67a2b-118">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="67a2b-119">**"Ikspropertyset"**</span><span class="sxs-lookup"><span data-stu-id="67a2b-119">**IKsPropertySet**</span></span>](ikspropertyset.md)                                                       |
| <span data-ttu-id="67a2b-120">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="67a2b-120">Output Pin Media Types</span></span>                   | <span data-ttu-id="67a2b-121">MediaType \_ Analog gaudiodatei, MediaType \_ Analog gvideo</span><span class="sxs-lookup"><span data-stu-id="67a2b-121">MEDIATYPE\_AnalogAudio, MEDIATYPE\_AnalogVideo</span></span>                                                 |
| <span data-ttu-id="67a2b-122">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="67a2b-122">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="67a2b-123">**"Ikspropertyset"**</span><span class="sxs-lookup"><span data-stu-id="67a2b-123">**IKsPropertySet**</span></span>](ikspropertyset.md)                                                       |
| <span data-ttu-id="67a2b-124">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="67a2b-124">Filter CLSID</span></span>                             | <span data-ttu-id="67a2b-125">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="67a2b-125">Not applicable</span></span>                                                                                 |
| <span data-ttu-id="67a2b-126">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="67a2b-126">Property Page CLSID</span></span>                      | <span data-ttu-id="67a2b-127">CLSID \_ crossbarfilterpropertypage</span><span class="sxs-lookup"><span data-stu-id="67a2b-127">CLSID\_CrossbarFilterPropertyPage</span></span>                                                              |
| <span data-ttu-id="67a2b-128">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="67a2b-128">Executable</span></span>                               | <span data-ttu-id="67a2b-129">ksxbar.ax</span><span class="sxs-lookup"><span data-stu-id="67a2b-129">ksxbar.ax</span></span>                                                                                      |
| [<span data-ttu-id="67a2b-130">Verdienst</span><span class="sxs-lookup"><span data-stu-id="67a2b-130">Merit</span></span>](merit.md)                       | <span data-ttu-id="67a2b-131">Treiber abhängig.</span><span class="sxs-lookup"><span data-stu-id="67a2b-131">Driver-dependent.</span></span>                                                                              |
| [<span data-ttu-id="67a2b-132">Filter Kategorie</span><span class="sxs-lookup"><span data-stu-id="67a2b-132">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="67a2b-133">AM- \_ kscategory- \_ Querstrich</span><span class="sxs-lookup"><span data-stu-id="67a2b-133">AM\_KSCATEGORY\_CROSSBAR</span></span>                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="67a2b-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="67a2b-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67a2b-135">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="67a2b-135">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="67a2b-136">Arbeiten mit quer leisten</span><span class="sxs-lookup"><span data-stu-id="67a2b-136">Working with Crossbars</span></span>](working-with-crossbars.md)
</dt> </dl>

 

 



