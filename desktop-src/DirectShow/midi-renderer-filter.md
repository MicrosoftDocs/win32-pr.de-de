---
description: Der FILTERS-Rendererfilter rendert DIE DATEN aus dem FILTERS Parser-Filter.
ms.assetid: 2675a21d-41d0-4095-96c4-f12f52c00d5a
title: RENDERerfilter FÜR DEN RENDERER (Windows.devices.xp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MIDI
api_type:
- HeaderDef
api_location:
- windows.devices.midi.h
ms.openlocfilehash: 5fa27ceda0c249f88f4684979382495167cb9238
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909408"
---
# <a name="midi-renderer-filter"></a><span data-ttu-id="decb8-103">FILTERS-Rendererfilter</span><span class="sxs-lookup"><span data-stu-id="decb8-103">MIDI Renderer Filter</span></span>

<span data-ttu-id="decb8-104">Der FILTERS-Rendererfilter rendert DIE DATEN aus dem [FILTERS Parser-Filter.](midi-parser-filter.md)</span><span class="sxs-lookup"><span data-stu-id="decb8-104">The MIDI Renderer filter renders MIDI data from the [MIDI Parser](midi-parser-filter.md) filter.</span></span>



| <span data-ttu-id="decb8-105">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="decb8-105">Label</span></span> | <span data-ttu-id="decb8-106">Wert</span><span class="sxs-lookup"><span data-stu-id="decb8-106">Value</span></span> |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="decb8-107">Filterschnittstellen</span><span class="sxs-lookup"><span data-stu-id="decb8-107">Filter Interfaces</span></span>                        | <span data-ttu-id="decb8-108">[**IAMClockSlave,**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave) [**IAMDirectSound,**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) [**IAMResourceControl,**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IBasicAudio,**](/windows/desktop/api/Control/nn-control-ibasicaudio) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IQualityControl,**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)</span><span class="sxs-lookup"><span data-stu-id="decb8-108">[**IAMClockSlave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave), [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound), [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)</span></span> |
| <span data-ttu-id="decb8-109">Eingabe-Stecknadelmedientypen</span><span class="sxs-lookup"><span data-stu-id="decb8-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="decb8-110">\_MEDIATYPE- Und MEDIASUBTYPE \_ NULL-Werte</span><span class="sxs-lookup"><span data-stu-id="decb8-110">MEDIATYPE\_Midi, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="decb8-111">Eingabe-Pin-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="decb8-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="decb8-112">[**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="decb8-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="decb8-113">Medientypen des Ausgabepins</span><span class="sxs-lookup"><span data-stu-id="decb8-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="decb8-114">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="decb8-114">Not applicable</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="decb8-115">Ausgabe-Pin-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="decb8-115">Output Pin Interfaces</span></span>                    | <span data-ttu-id="decb8-116">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="decb8-116">Not applicable</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="decb8-117">Filtern von CLSID</span><span class="sxs-lookup"><span data-stu-id="decb8-117">Filter CLSID</span></span>                             | <span data-ttu-id="decb8-118">CLSID \_ AVIMIDIRender</span><span class="sxs-lookup"><span data-stu-id="decb8-118">CLSID\_AVIMIDIRender</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="decb8-119">CLSID der Eigenschaftenseite</span><span class="sxs-lookup"><span data-stu-id="decb8-119">Property Page CLSID</span></span>                      | <span data-ttu-id="decb8-120">Keine Eigenschaftenseite</span><span class="sxs-lookup"><span data-stu-id="decb8-120">No property page</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="decb8-121">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="decb8-121">Executable</span></span>                               | <span data-ttu-id="decb8-122">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="decb8-122">quartz.dll</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="decb8-123">Verdienst</span><span class="sxs-lookup"><span data-stu-id="decb8-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="decb8-124">\_VORGEZOGENE VORZEICHEN</span><span class="sxs-lookup"><span data-stu-id="decb8-124">MERIT\_PREFERRED</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="decb8-125">Filterkategorie</span><span class="sxs-lookup"><span data-stu-id="decb8-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="decb8-126">CLSID- \_ Und -Vererbungskategorie</span><span class="sxs-lookup"><span data-stu-id="decb8-126">CLSID\_MidiRendererCategory</span></span>                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="decb8-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="decb8-127">Remarks</span></span>

<span data-ttu-id="decb8-128">Die GUID für den Formattyp ist **NULL,** aber der Formatblock enthält die folgende Struktur:</span><span class="sxs-lookup"><span data-stu-id="decb8-128">The GUID for the format type is **NULL**, but the format block contains the following structure:</span></span>


```C++
typedef struct _MIDIFORMAT {
    DWORD       dwDivision;
    DWORD       dwReserved[7];
} MIDIFORMAT, FAR * LPMIDIFORMAT;
```



<span data-ttu-id="decb8-129">Das **dwDivision-Element** gibt die Zeitdivision der Datei an.</span><span class="sxs-lookup"><span data-stu-id="decb8-129">The **dwDivision** member specifies the time division of the file.</span></span> <span data-ttu-id="decb8-130">Die Zeitdivision wird im Header einer beliebigen STANDARD-FORMAT-Datei (SMF) im `MThd` Block angegeben.</span><span class="sxs-lookup"><span data-stu-id="decb8-130">The time division is given in the header of any standard MIDI file (SMF), in the `MThd` chunk.</span></span> <span data-ttu-id="decb8-131">Der RENDERING-Renderer legt diese Eigenschaft für denDATENÜBERTRAGUNG-Datenstrom fest, indem er die **funktion "streamsStreamProperty"** aufruft.</span><span class="sxs-lookup"><span data-stu-id="decb8-131">The MIDI Renderer sets this property on the MIDI data stream by calling the **midiStreamProperty** function.</span></span>

<span data-ttu-id="decb8-132">Beispiele aus dem FILTER DES PARSER-Parsers enthalten eine Sekunde vonTEN-Daten.</span><span class="sxs-lookup"><span data-stu-id="decb8-132">Samples from the MIDI Parser filter contain one second of MIDI data.</span></span> <span data-ttu-id="decb8-133">Der RENDERING-Renderer verwendet die **funktion "streamStreamOut",** um die DANN-Daten zu rendern.</span><span class="sxs-lookup"><span data-stu-id="decb8-133">The MIDI Renderer uses the **midiStreamOut** function to render the MIDI data.</span></span> <span data-ttu-id="decb8-134">Jedes Beispiel ist ein Synchronisierungspunkt: Der Anfang des Puffers enthält alle Befehle, die zum Festlegen des richtigen Zustands für das Rendern dieses Puffers erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="decb8-134">Each sample is a synchronization point: the start of the buffer contains all of the commands necessary to set the correct state for rendering that buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="decb8-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="decb8-135">Requirements</span></span>



| <span data-ttu-id="decb8-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="decb8-136">Requirement</span></span> | <span data-ttu-id="decb8-137">Wert</span><span class="sxs-lookup"><span data-stu-id="decb8-137">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="decb8-138">Header</span><span class="sxs-lookup"><span data-stu-id="decb8-138">Header</span></span><br/> | <dl> <span data-ttu-id="decb8-139"><dt>Windows.devices.format.h</dt></span><span class="sxs-lookup"><span data-stu-id="decb8-139"><dt>Windows.devices.midi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="decb8-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="decb8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="decb8-141">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="decb8-141">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




