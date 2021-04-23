---
description: TV-Tunerfilter
ms.assetid: a8e101dc-78ab-495f-9086-7b1d1e87c357
title: TV-Tunerfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90f1fa68d7fc2723839882dd232e630dbe128634
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909028"
---
# <a name="tv-tuner-filter"></a><span data-ttu-id="adf1b-103">TV-Tunerfilter</span><span class="sxs-lookup"><span data-stu-id="adf1b-103">TV Tuner Filter</span></span>

<span data-ttu-id="adf1b-104">Der Filter TV Tuner wählt einen analogen Broadcast- oder Kabelkanal aus, der angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="adf1b-104">The TV Tuner filter selects an analog broadcast or cable channel to be viewed.</span></span> <span data-ttu-id="adf1b-105">Der einzelne Ausgabestream ist ein Hardwarepfad für analoge Basebandvideos.</span><span class="sxs-lookup"><span data-stu-id="adf1b-105">The single output stream is a hardware path for analog baseband video.</span></span> <span data-ttu-id="adf1b-106">Diese Ausgabe sollte eine Verbindung mit dem Analog Video Crossbar-Filter herstellen.</span><span class="sxs-lookup"><span data-stu-id="adf1b-106">This output should connect to the Analog Video Crossbar filter.</span></span> <span data-ttu-id="adf1b-107">Die Eingabepins enthalten eine Eingabe für Kabel und eine Antenne.</span><span class="sxs-lookup"><span data-stu-id="adf1b-107">The input pins include an input for cable and an antenna input.</span></span>



| <span data-ttu-id="adf1b-108">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="adf1b-108">Label</span></span> | <span data-ttu-id="adf1b-109">Wert</span><span class="sxs-lookup"><span data-stu-id="adf1b-109">Value</span></span> |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adf1b-110">Filterschnittstellen</span><span class="sxs-lookup"><span data-stu-id="adf1b-110">Filter Interfaces</span></span>                        | <span data-ttu-id="adf1b-111">[**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IAMTVTuner,**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) **ISpecifyPropertyPages,** **IPersistPropertyBag,** **IKsObject,** [**IKsPropertySet**](ikspropertyset.md)</span><span class="sxs-lookup"><span data-stu-id="adf1b-111">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner), **ISpecifyPropertyPages**, **IPersistPropertyBag**, **IKsObject**, [**IKsPropertySet**](ikspropertyset.md)</span></span> |
| <span data-ttu-id="adf1b-112">Eingabe-Stecknadelmedientypen</span><span class="sxs-lookup"><span data-stu-id="adf1b-112">Input Pin Media Types</span></span>                    | <span data-ttu-id="adf1b-113">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="adf1b-113">Not applicable.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="adf1b-114">Eingabe-Pin-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="adf1b-114">Input Pin Interfaces</span></span>                     | <span data-ttu-id="adf1b-115">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="adf1b-115">Not applicable.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="adf1b-116">Medientypen des Ausgabepins</span><span class="sxs-lookup"><span data-stu-id="adf1b-116">Output Pin Media Types</span></span>                   | <span data-ttu-id="adf1b-117">Video: MEDIATYPE \_ AnalogVideo, KSDATAFORMAT \_ SUBTYPE \_ NONE Audio: MEDIATYPE \_ AnalogAudio, MEDIASUBTYPE \_ NULL</span><span class="sxs-lookup"><span data-stu-id="adf1b-117">Video: MEDIATYPE\_AnalogVideo, KSDATAFORMAT\_SUBTYPE\_NONE Audio: MEDIATYPE\_AnalogAudio, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="adf1b-118">Ausgabe-Pin-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="adf1b-118">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="adf1b-119">**Ipin**</span><span class="sxs-lookup"><span data-stu-id="adf1b-119">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                                                                                                                                              |
| <span data-ttu-id="adf1b-120">Filtern von CLSID</span><span class="sxs-lookup"><span data-stu-id="adf1b-120">Filter CLSID</span></span>                             | <span data-ttu-id="adf1b-121">CLSID \_ TVTunerFilter</span><span class="sxs-lookup"><span data-stu-id="adf1b-121">CLSID\_TVTunerFilter</span></span>                                                                                                                                                              |
| <span data-ttu-id="adf1b-122">CLSID der Eigenschaftenseite</span><span class="sxs-lookup"><span data-stu-id="adf1b-122">Property Page CLSID</span></span>                      | <span data-ttu-id="adf1b-123">CLSID \_ TVTunerFilterPropertyPage</span><span class="sxs-lookup"><span data-stu-id="adf1b-123">CLSID\_TVTunerFilterPropertyPage</span></span>                                                                                                                                                  |
| <span data-ttu-id="adf1b-124">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="adf1b-124">Executable</span></span>                               | <span data-ttu-id="adf1b-125">KSTVTune.ax</span><span class="sxs-lookup"><span data-stu-id="adf1b-125">KSTVTune.ax</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="adf1b-126">Verdienst</span><span class="sxs-lookup"><span data-stu-id="adf1b-126">Merit</span></span>](merit.md)                       | <span data-ttu-id="adf1b-127">NICHT \_ \_ VERWENDEN \_</span><span class="sxs-lookup"><span data-stu-id="adf1b-127">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                               |
| [<span data-ttu-id="adf1b-128">Filterkategorie</span><span class="sxs-lookup"><span data-stu-id="adf1b-128">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="adf1b-129">AM \_ KSCATEGORY \_ TVTUNER</span><span class="sxs-lookup"><span data-stu-id="adf1b-129">AM\_KSCATEGORY\_TVTUNER</span></span>                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="adf1b-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="adf1b-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adf1b-131">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="adf1b-131">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



