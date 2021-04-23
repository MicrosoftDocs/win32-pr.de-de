---
description: Analog Video Crossbar Filter
ms.assetid: 668f6a8b-a4ed-4e4a-956c-a87f165225fa
title: Analog Video Crossbar Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d17d8700131dbc658a5233d56f339c39eac7a3a0
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909598"
---
# <a name="analog-video-crossbar-filter"></a><span data-ttu-id="17e66-103">Analog Video Crossbar Filter</span><span class="sxs-lookup"><span data-stu-id="17e66-103">Analog Video Crossbar Filter</span></span>

<span data-ttu-id="17e66-104">Der Analog Video Crossbar-Filter stellt eine Video-Querleiste auf einem Videoaufnahmegerät dar, das die Windows-Treibermodell (WDM) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="17e66-104">The Analog Video Crossbar filter represents a video crossbar on a video capture device that supports the Windows Driver Model (WDM).</span></span>

<span data-ttu-id="17e66-105">Dieser Filter ist ein Wrapperfilter für Querleisten auf WDM-Streaminggeräten.</span><span class="sxs-lookup"><span data-stu-id="17e66-105">This filter is a wrapper filter for crossbars on WDM streaming devices.</span></span> <span data-ttu-id="17e66-106">Der Angezeigte Name des Filters wird vom Gerät übernommen.</span><span class="sxs-lookup"><span data-stu-id="17e66-106">The filter's friendly name is taken from the device.</span></span> <span data-ttu-id="17e66-107">Jeder Ausgabepin stellt einen Hardwarepfad für analoges Basebandvideo dar.</span><span class="sxs-lookup"><span data-stu-id="17e66-107">Each output pin represents a hardware path for analog baseband video.</span></span> <span data-ttu-id="17e66-108">Einer der Eingabepins stammt von einem TV-Tuner [(tv tuner Filter).](tv-tuner-filter.md)</span><span class="sxs-lookup"><span data-stu-id="17e66-108">One of the input pins comes from a TV Tuner (the [TV Tuner Filter](tv-tuner-filter.md)).</span></span> <span data-ttu-id="17e66-109">Andere Eingabepins unterstützen Video- oder Audiostreams.</span><span class="sxs-lookup"><span data-stu-id="17e66-109">Other input pins support video or audio streams.</span></span> <span data-ttu-id="17e66-110">Der Filter unterstützt alle Medienuntertypen und Formate, die für die Downstreamverbindungen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="17e66-110">The filter supports any media subtypes and formats that are supported on the downstream connections.</span></span>

<span data-ttu-id="17e66-111">Sie können diesen Filter nicht direkt mit CoCreateInstance erstellen.</span><span class="sxs-lookup"><span data-stu-id="17e66-111">You cannot directly create this filter with CoCreateInstance.</span></span> <span data-ttu-id="17e66-112">Die [**ICaptureGraphBuilder2-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) fügt diesen Filter bei Bedarf automatisch dem Diagramm hinzu.</span><span class="sxs-lookup"><span data-stu-id="17e66-112">The [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface automatically adds this filter to the graph as needed.</span></span>

<span data-ttu-id="17e66-113">Weitere Informationen zu Wrapperfiltern und WDM-Streaminggeräten finden Sie unter [How Hardware Devices Participate in the Filter Graph](how-hardware-devices-participate-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="17e66-113">For more information on wrapper filters and WDM streaming devices, see [How Hardware Devices Participate in the Filter Graph](how-hardware-devices-participate-in-the-filter-graph.md).</span></span>



| <span data-ttu-id="17e66-114">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="17e66-114">Label</span></span> | <span data-ttu-id="17e66-115">Wert</span><span class="sxs-lookup"><span data-stu-id="17e66-115">Value</span></span> |
|------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17e66-116">Filterschnittstellen</span><span class="sxs-lookup"><span data-stu-id="17e66-116">Filter Interfaces</span></span>                        | <span data-ttu-id="17e66-117">[**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar), ISpecifyPropertyPages, IPersistPropertyBag, IPersistStream</span><span class="sxs-lookup"><span data-stu-id="17e66-117">[**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar), ISpecifyPropertyPages, IPersistPropertyBag, IPersistStream</span></span> |
| <span data-ttu-id="17e66-118">Eingabepin-Medientypen</span><span class="sxs-lookup"><span data-stu-id="17e66-118">Input Pin Media Types</span></span>                    | <span data-ttu-id="17e66-119">MEDIATYPE \_ AnalogAudio, MEDIATYPE \_ AnalogVideo</span><span class="sxs-lookup"><span data-stu-id="17e66-119">MEDIATYPE\_AnalogAudio, MEDIATYPE\_AnalogVideo</span></span>                                                 |
| <span data-ttu-id="17e66-120">Eingabepinschnittstellen</span><span class="sxs-lookup"><span data-stu-id="17e66-120">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="17e66-121">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="17e66-121">**IKsPropertySet**</span></span>](ikspropertyset.md)                                                       |
| <span data-ttu-id="17e66-122">Ausgabepin-Medientypen</span><span class="sxs-lookup"><span data-stu-id="17e66-122">Output Pin Media Types</span></span>                   | <span data-ttu-id="17e66-123">MEDIATYPE \_ AnalogAudio, MEDIATYPE \_ AnalogVideo</span><span class="sxs-lookup"><span data-stu-id="17e66-123">MEDIATYPE\_AnalogAudio, MEDIATYPE\_AnalogVideo</span></span>                                                 |
| <span data-ttu-id="17e66-124">Ausgabe-Pin-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="17e66-124">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="17e66-125">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="17e66-125">**IKsPropertySet**</span></span>](ikspropertyset.md)                                                       |
| <span data-ttu-id="17e66-126">Filtern von CLSID</span><span class="sxs-lookup"><span data-stu-id="17e66-126">Filter CLSID</span></span>                             | <span data-ttu-id="17e66-127">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="17e66-127">Not applicable</span></span>                                                                                 |
| <span data-ttu-id="17e66-128">CLSID der Eigenschaftenseite</span><span class="sxs-lookup"><span data-stu-id="17e66-128">Property Page CLSID</span></span>                      | <span data-ttu-id="17e66-129">CLSID \_ CrossbarFilterPropertyPage</span><span class="sxs-lookup"><span data-stu-id="17e66-129">CLSID\_CrossbarFilterPropertyPage</span></span>                                                              |
| <span data-ttu-id="17e66-130">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="17e66-130">Executable</span></span>                               | <span data-ttu-id="17e66-131">ksxbar.ax</span><span class="sxs-lookup"><span data-stu-id="17e66-131">ksxbar.ax</span></span>                                                                                      |
| [<span data-ttu-id="17e66-132">Verdienst</span><span class="sxs-lookup"><span data-stu-id="17e66-132">Merit</span></span>](merit.md)                       | <span data-ttu-id="17e66-133">Treiberabhängig.</span><span class="sxs-lookup"><span data-stu-id="17e66-133">Driver-dependent.</span></span>                                                                              |
| [<span data-ttu-id="17e66-134">Filterkategorie</span><span class="sxs-lookup"><span data-stu-id="17e66-134">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="17e66-135">AM \_ KSCATEGORY \_ CROSSBAR</span><span class="sxs-lookup"><span data-stu-id="17e66-135">AM\_KSCATEGORY\_CROSSBAR</span></span>                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="17e66-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="17e66-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17e66-137">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="17e66-137">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="17e66-138">Arbeiten mit Querleisten</span><span class="sxs-lookup"><span data-stu-id="17e66-138">Working with Crossbars</span></span>](working-with-crossbars.md)
</dt> </dl>

 

 



