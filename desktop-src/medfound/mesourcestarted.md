---
description: Wird ausgelöst, wenn eine Medienquelle startet, ohne zu suchen.
ms.assetid: a52d8ee1-cb46-487d-a744-fca6db7c2353
title: Mesourcestarted-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c17ba7898a8bf33df4a3508afee9b7c0c9bc81c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528262"
---
# <a name="mesourcestarted-event"></a><span data-ttu-id="47a34-103">Mesourcestarted-Ereignis</span><span class="sxs-lookup"><span data-stu-id="47a34-103">MESourceStarted event</span></span>

<span data-ttu-id="47a34-104">Wird ausgelöst, wenn eine Medienquelle startet, ohne zu suchen.</span><span class="sxs-lookup"><span data-stu-id="47a34-104">Raised when a media source starts without seeking.</span></span>

## <a name="event-values"></a><span data-ttu-id="47a34-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="47a34-105">Event values</span></span>

<span data-ttu-id="47a34-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="47a34-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="47a34-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="47a34-107">VARTYPE</span></span>              | <span data-ttu-id="47a34-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47a34-108">Description</span></span>                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47a34-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="47a34-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="47a34-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="47a34-110">No event data.</span></span> <span data-ttu-id="47a34-111">Die Startzeit war von der aktuellen Position.</span><span class="sxs-lookup"><span data-stu-id="47a34-111">The start time was from the current position.</span></span><br/> <br/>                            |
| <span data-ttu-id="47a34-112">VT \_ I8</span><span class="sxs-lookup"><span data-stu-id="47a34-112">VT\_I8</span></span><br/>    | <span data-ttu-id="47a34-113">Die Startzeit in 100-Nanosecond-Einheiten in Relation zu den Zeitstempeln der Stichproben.</span><span class="sxs-lookup"><span data-stu-id="47a34-113">The starting time, in 100-nanosecond units, relative to the time stamps on the samples.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="47a34-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="47a34-114">Attributes</span></span>

<span data-ttu-id="47a34-115">Für dieses Ereignis sind die folgenden Attribute definiert:</span><span class="sxs-lookup"><span data-stu-id="47a34-115">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="47a34-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="47a34-116">Attribute</span></span>                                                                                     | <span data-ttu-id="47a34-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47a34-117">Description</span></span>                                                                                                                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="47a34-118">**Beginn der MF- \_ Ereignis \_ Quelle \_ \_**</span><span class="sxs-lookup"><span data-stu-id="47a34-118">**MF\_EVENT\_SOURCE\_ACTUAL\_START**</span></span>](mf-event-source-actual-start-attribute.md)<br/> | <span data-ttu-id="47a34-119">Startzeit.</span><span class="sxs-lookup"><span data-stu-id="47a34-119">Start time.</span></span> <span data-ttu-id="47a34-120">Die Medienquelle legt dieses Attribut fest, wenn es von seiner aktuellen Position neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="47a34-120">The media source sets this attribute if it restarts from its current position.</span></span><br/> <br/>                     |
| [<span data-ttu-id="47a34-121">**der MF- \_ Ereignis \_ Quelle wurde \_ \_ gestartet.**</span><span class="sxs-lookup"><span data-stu-id="47a34-121">**MF\_EVENT\_SOURCE\_FAKE\_START**</span></span>](mf-event-source-fake-start-attribute.md)<br/>     | <span data-ttu-id="47a34-122">Gibt an, ob die aktuelle Segment Topologie leer ist.</span><span class="sxs-lookup"><span data-stu-id="47a34-122">Specifies whether the current segment topology is empty.</span></span> <span data-ttu-id="47a34-123">Die Sequencer-Quelle legt dieses Attribut fest.</span><span class="sxs-lookup"><span data-stu-id="47a34-123">The sequencer source sets this attribute.</span></span><br/> <br/>             |
| [<span data-ttu-id="47a34-124">**der MF- \_ Ereignis \_ Quelle \_ ProjectStart**</span><span class="sxs-lookup"><span data-stu-id="47a34-124">**MF\_EVENT\_SOURCE\_PROJECTSTART**</span></span>](mf-event-source-projectstart-attribute.md)<br/>  | <span data-ttu-id="47a34-125">Die Startzeit für ein Segment relativ zum Beginn der Präsentation.</span><span class="sxs-lookup"><span data-stu-id="47a34-125">Start time for a segment, relative to the start of the presentation.</span></span> <span data-ttu-id="47a34-126">Die Sequencer-Quelle legt dieses Attribut fest.</span><span class="sxs-lookup"><span data-stu-id="47a34-126">The sequencer source sets this attribute.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="47a34-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47a34-127">Remarks</span></span>

<span data-ttu-id="47a34-128">Eine Medienquelle löst dieses Ereignis aus, wenn es von einem beendeten Zustand gestartet wird, oder startet von einem angehaltenen Zustand an derselben Position in der Quelle.</span><span class="sxs-lookup"><span data-stu-id="47a34-128">A media source raises this event when it starts from a stopped state, or starts from a paused state at the same position in the source.</span></span> <span data-ttu-id="47a34-129">Das-Ereignis wird ausgelöst, wenn die [**imfmediasource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) -Methode S OK zurückgibt \_ .</span><span class="sxs-lookup"><span data-stu-id="47a34-129">The event is raised if the [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method returns S\_OK.</span></span>

<span data-ttu-id="47a34-130">Wenn die Medienquelle von der aktuellen Position aus startet und der vorherige Zustand der Quelle ausgeführt oder angehalten wurde, können die Ereignisdaten leer (VT \_ Empty) sein.</span><span class="sxs-lookup"><span data-stu-id="47a34-130">If the media source starts from the current position and the source's previous state was running or paused, the event data can empty (VT\_EMPTY).</span></span> <span data-ttu-id="47a34-131">Wenn die Ereignisdaten VT \_ leer sind, kann die Medienquelle das [**\_ \_ \_ tatsächliche \_ Start Attribut der MF-Ereignis Quelle**](mf-event-source-actual-start-attribute.md) mit der tatsächlichen Startzeit festlegen.</span><span class="sxs-lookup"><span data-stu-id="47a34-131">If the event data is VT\_EMPTY, the media source might set the [**MF\_EVENT\_SOURCE\_ACTUAL\_START**](mf-event-source-actual-start-attribute.md) attribute with the actual starting time.</span></span>

<span data-ttu-id="47a34-132">Wenn die Medienquelle an einer neuen Position beginnt oder der vorherige Zustand der Quelle beendet wurde, müssen die Ereignisdaten die Startzeit (VT \_ I8) sein.</span><span class="sxs-lookup"><span data-stu-id="47a34-132">If the media source starts from a new position, or the source's previous state was stopped, the event data must be the starting time (VT\_I8).</span></span>

<span data-ttu-id="47a34-133">Wenn die [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) Methode eine Suche auslöst, sendet die Medienquelle das [mesourceseeked](mesourceseeked.md) -Ereignis anstelle von mesourcestarted.</span><span class="sxs-lookup"><span data-stu-id="47a34-133">If the [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method causes a seek, the media source sends the [MESourceSeeked](mesourceseeked.md) event instead of MESourceStarted.</span></span>

## <a name="requirements"></a><span data-ttu-id="47a34-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47a34-134">Requirements</span></span>



| <span data-ttu-id="47a34-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47a34-135">Requirement</span></span> | <span data-ttu-id="47a34-136">Wert</span><span class="sxs-lookup"><span data-stu-id="47a34-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47a34-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="47a34-137">Minimum supported client</span></span><br/> | <span data-ttu-id="47a34-138">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="47a34-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="47a34-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="47a34-139">Minimum supported server</span></span><br/> | <span data-ttu-id="47a34-140">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="47a34-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="47a34-141">Header</span><span class="sxs-lookup"><span data-stu-id="47a34-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="47a34-142"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="47a34-142"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47a34-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47a34-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47a34-144">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="47a34-144">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




