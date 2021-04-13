---
description: TV-Tuner-Filter
ms.assetid: a8e101dc-78ab-495f-9086-7b1d1e87c357
title: TV-Tuner-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81dd03b965275f5e9b9405b027c8e66a7fb0f157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348558"
---
# <a name="tv-tuner-filter"></a><span data-ttu-id="ea527-103">TV-Tuner-Filter</span><span class="sxs-lookup"><span data-stu-id="ea527-103">TV Tuner Filter</span></span>

<span data-ttu-id="ea527-104">Der TV-Tuner-Filter wählt einen analogen Broadcast-oder Kabelkanal aus, der angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ea527-104">The TV Tuner filter selects an analog broadcast or cable channel to be viewed.</span></span> <span data-ttu-id="ea527-105">Der einzelne Ausgabestream ist ein Hardware Pfad für das analoge Baseband-Video.</span><span class="sxs-lookup"><span data-stu-id="ea527-105">The single output stream is a hardware path for analog baseband video.</span></span> <span data-ttu-id="ea527-106">Diese Ausgabe sollte eine Verbindung mit dem analogen Video Querbalken Filter herstellen.</span><span class="sxs-lookup"><span data-stu-id="ea527-106">This output should connect to the Analog Video Crossbar filter.</span></span> <span data-ttu-id="ea527-107">Die Eingabe Pins enthalten eine Eingabe für Kabel-und Antennen Eingaben.</span><span class="sxs-lookup"><span data-stu-id="ea527-107">The input pins include an input for cable and an antenna input.</span></span>



|                                          |                                                                                                                                                                                   |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea527-108">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ea527-108">Filter Interfaces</span></span>                        | <span data-ttu-id="ea527-109">[**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**iamtvtuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner), **ISpecifyPropertyPages**, **IPersistPropertyBag**, **iksobject**, [**ikspropertyset**](ikspropertyset.md)</span><span class="sxs-lookup"><span data-stu-id="ea527-109">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner), **ISpecifyPropertyPages**, **IPersistPropertyBag**, **IKsObject**, [**IKsPropertySet**](ikspropertyset.md)</span></span> |
| <span data-ttu-id="ea527-110">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="ea527-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="ea527-111">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="ea527-111">Not applicable.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="ea527-112">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="ea527-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="ea527-113">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="ea527-113">Not applicable.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="ea527-114">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="ea527-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="ea527-115">Video: MediaType \_ Analog gvideo, ksdataformat \_ -Untertyp \_ keine Audiodatei: MediaType \_ Analog gaudiodatei, mediasubtype \_ null</span><span class="sxs-lookup"><span data-stu-id="ea527-115">Video: MEDIATYPE\_AnalogVideo, KSDATAFORMAT\_SUBTYPE\_NONE Audio: MEDIATYPE\_AnalogAudio, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="ea527-116">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ea527-116">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="ea527-117">**IPin**</span><span class="sxs-lookup"><span data-stu-id="ea527-117">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                                                                                                                                              |
| <span data-ttu-id="ea527-118">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="ea527-118">Filter CLSID</span></span>                             | <span data-ttu-id="ea527-119">CLSID- \_ tvtunerfilter</span><span class="sxs-lookup"><span data-stu-id="ea527-119">CLSID\_TVTunerFilter</span></span>                                                                                                                                                              |
| <span data-ttu-id="ea527-120">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="ea527-120">Property Page CLSID</span></span>                      | <span data-ttu-id="ea527-121">CLSID \_ tvtunerfilterpropertypage</span><span class="sxs-lookup"><span data-stu-id="ea527-121">CLSID\_TVTunerFilterPropertyPage</span></span>                                                                                                                                                  |
| <span data-ttu-id="ea527-122">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="ea527-122">Executable</span></span>                               | <span data-ttu-id="ea527-123">KSTVTune.ax</span><span class="sxs-lookup"><span data-stu-id="ea527-123">KSTVTune.ax</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="ea527-124">Verdienst</span><span class="sxs-lookup"><span data-stu-id="ea527-124">Merit</span></span>](merit.md)                       | <span data-ttu-id="ea527-125">das Verdienst wird \_ \_ nicht \_ verwendet.</span><span class="sxs-lookup"><span data-stu-id="ea527-125">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                               |
| [<span data-ttu-id="ea527-126">Filter Kategorie</span><span class="sxs-lookup"><span data-stu-id="ea527-126">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="ea527-127">AM \_ kscategory- \_ TvTuner</span><span class="sxs-lookup"><span data-stu-id="ea527-127">AM\_KSCATEGORY\_TVTUNER</span></span>                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="ea527-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ea527-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea527-129">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="ea527-129">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



