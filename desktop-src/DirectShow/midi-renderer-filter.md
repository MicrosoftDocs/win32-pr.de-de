---
description: Der-rendererfilterfilter rendert die Daten vom Typ "MIDI" aus dem-
ms.assetid: 2675a21d-41d0-4095-96c4-f12f52c00d5a
title: MIDI-rendererfilter (Windows. Devices. MIDI. h)
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
ms.openlocfilehash: 060bb00629b78fb1edbfbfd193aeaf7514c98ba4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371480"
---
# <a name="midi-renderer-filter"></a><span data-ttu-id="fe1c1-103">MIDI-rendererfilter</span><span class="sxs-lookup"><span data-stu-id="fe1c1-103">MIDI Renderer Filter</span></span>

<span data-ttu-id="fe1c1-104">Der-rendererfilterfilter rendert die Daten vom Typ "MIDI" [aus dem-](midi-parser-filter.md)</span><span class="sxs-lookup"><span data-stu-id="fe1c1-104">The MIDI Renderer filter renders MIDI data from the [MIDI Parser](midi-parser-filter.md) filter.</span></span>



|                                          |                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe1c1-105">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="fe1c1-105">Filter Interfaces</span></span>                        | <span data-ttu-id="fe1c1-106">[**Iamclockslave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave), [**iamdirectsound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound), [**iamresourcecontrol**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**ibasicaudio**](/windows/desktop/api/Control/nn-control-ibasicaudio), [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition), [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)</span><span class="sxs-lookup"><span data-stu-id="fe1c1-106">[**IAMClockSlave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave), [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound), [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)</span></span> |
| <span data-ttu-id="fe1c1-107">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="fe1c1-107">Input Pin Media Types</span></span>                    | <span data-ttu-id="fe1c1-108">MediaType \_ MIDI, mediasubtype \_ null</span><span class="sxs-lookup"><span data-stu-id="fe1c1-108">MEDIATYPE\_Midi, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="fe1c1-109">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="fe1c1-109">Input Pin Interfaces</span></span>                     | <span data-ttu-id="fe1c1-110">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="fe1c1-110">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="fe1c1-111">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="fe1c1-111">Output Pin Media Types</span></span>                   | <span data-ttu-id="fe1c1-112">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="fe1c1-112">Not applicable</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="fe1c1-113">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="fe1c1-113">Output Pin Interfaces</span></span>                    | <span data-ttu-id="fe1c1-114">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="fe1c1-114">Not applicable</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="fe1c1-115">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="fe1c1-115">Filter CLSID</span></span>                             | <span data-ttu-id="fe1c1-116">CLSID \_ avimidirendering</span><span class="sxs-lookup"><span data-stu-id="fe1c1-116">CLSID\_AVIMIDIRender</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="fe1c1-117">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="fe1c1-117">Property Page CLSID</span></span>                      | <span data-ttu-id="fe1c1-118">Keine Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="fe1c1-118">No property page</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="fe1c1-119">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="fe1c1-119">Executable</span></span>                               | <span data-ttu-id="fe1c1-120">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="fe1c1-120">quartz.dll</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="fe1c1-121">Verdienst</span><span class="sxs-lookup"><span data-stu-id="fe1c1-121">Merit</span></span>](merit.md)                       | <span data-ttu-id="fe1c1-122">\_bevorzugter Vorteil</span><span class="sxs-lookup"><span data-stu-id="fe1c1-122">MERIT\_PREFERRED</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="fe1c1-123">Filter Kategorie</span><span class="sxs-lookup"><span data-stu-id="fe1c1-123">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="fe1c1-124">CLSID \_ midirenderercategory</span><span class="sxs-lookup"><span data-stu-id="fe1c1-124">CLSID\_MidiRendererCategory</span></span>                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="fe1c1-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe1c1-125">Remarks</span></span>

<span data-ttu-id="fe1c1-126">Die GUID für den Formattyp ist **null**, aber der Format Block enthält die folgende Struktur:</span><span class="sxs-lookup"><span data-stu-id="fe1c1-126">The GUID for the format type is **NULL**, but the format block contains the following structure:</span></span>


```C++
typedef struct _MIDIFORMAT {
    DWORD       dwDivision;
    DWORD       dwReserved[7];
} MIDIFORMAT, FAR * LPMIDIFORMAT;
```



<span data-ttu-id="fe1c1-127">Der **dwdivision** -Member gibt die Zeiteinteilung der Datei an.</span><span class="sxs-lookup"><span data-stu-id="fe1c1-127">The **dwDivision** member specifies the time division of the file.</span></span> <span data-ttu-id="fe1c1-128">Die Zeiteinteilung wird in der Kopfzeile einer beliebigen Standard-MIDI-Datei (SMF) im Block angegeben `MThd` .</span><span class="sxs-lookup"><span data-stu-id="fe1c1-128">The time division is given in the header of any standard MIDI file (SMF), in the `MThd` chunk.</span></span> <span data-ttu-id="fe1c1-129">Der MIDI-Renderer legt diese Eigenschaft für den Datenstrom von MIDI fest, indem er die **midistreamproperty** -Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="fe1c1-129">The MIDI Renderer sets this property on the MIDI data stream by calling the **midiStreamProperty** function.</span></span>

<span data-ttu-id="fe1c1-130">Die Beispiele aus dem Code des MIDI-Parsers enthalten eine Sekunde der Daten von MIDI.</span><span class="sxs-lookup"><span data-stu-id="fe1c1-130">Samples from the MIDI Parser filter contain one second of MIDI data.</span></span> <span data-ttu-id="fe1c1-131">Der MIDI-Renderer verwendet die **midistreamout** -Funktion, um die Daten des Datenstroms zu Rendering</span><span class="sxs-lookup"><span data-stu-id="fe1c1-131">The MIDI Renderer uses the **midiStreamOut** function to render the MIDI data.</span></span> <span data-ttu-id="fe1c1-132">Jedes Beispiel ist ein Synchronisierungs Punkt: der Anfang des Puffers enthält alle Befehle, die erforderlich sind, um den korrekten Zustand für das Rendern dieses Puffers festzulegen.</span><span class="sxs-lookup"><span data-stu-id="fe1c1-132">Each sample is a synchronization point: the start of the buffer contains all of the commands necessary to set the correct state for rendering that buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe1c1-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe1c1-133">Requirements</span></span>



| <span data-ttu-id="fe1c1-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe1c1-134">Requirement</span></span> | <span data-ttu-id="fe1c1-135">Wert</span><span class="sxs-lookup"><span data-stu-id="fe1c1-135">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe1c1-136">Header</span><span class="sxs-lookup"><span data-stu-id="fe1c1-136">Header</span></span><br/> | <dl> <span data-ttu-id="fe1c1-137"><dt>Windows. Devices. MIDI. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe1c1-137"><dt>Windows.devices.midi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe1c1-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe1c1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe1c1-139">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="fe1c1-139">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




