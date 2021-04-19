---
description: Wird durch eine streamsenke ausgelöst, wenn eine Bereinigungs Anforderung abgeschlossen ist.
ms.assetid: 451c7e09-868e-4c05-b970-d222b97223f2
title: Mestreamsinkscrubsamplecomplete-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81f29d478635d5a9ba7e7c5356c49ebd8da216f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359530"
---
# <a name="mestreamsinkscrubsamplecomplete-event"></a><span data-ttu-id="e3ef8-103">Mestreamsinkscrubsamplecomplete-Ereignis</span><span class="sxs-lookup"><span data-stu-id="e3ef8-103">MEStreamSinkScrubSampleComplete event</span></span>

<span data-ttu-id="e3ef8-104">Wird durch eine streamsenke ausgelöst, wenn eine Bereinigungs Anforderung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="e3ef8-104">Raised by a stream sink when it completes a scrubbing request.</span></span>

<span data-ttu-id="e3ef8-105">Ein Scrubbing tritt auf, wenn die Wiedergabe Rate 0 (null) ist und die Präsentationszeit mit einer angegebenen sreiben-Zeit gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="e3ef8-105">Scrubbing occurs when the playback rate is zero and the presentation clock is started with a specified srubbing time.</span></span> <span data-ttu-id="e3ef8-106">Wenn eine Medien Senke Scrubbing unterstützt, löst jeder Datenstrom auf der Senke dieses Ereignis aus, wenn die [**imfclockstaatink:: onclockstart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) -Methode aufgerufen wird, während die Wiedergabe Rate 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="e3ef8-106">If a media sink supports scrubbing, every stream on the sink raises this event whenever the [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) method is called while the playback rate is zero.</span></span>

<span data-ttu-id="e3ef8-107">Wenn der Stream während des Bereinigungs Vorgang Daten rendert, sendet er das Ereignis, sobald die Daten gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="e3ef8-107">If the stream renders data while scrubbing, it sends the event as soon as the data is rendered.</span></span> <span data-ttu-id="e3ef8-108">Wenn der Stream keine Daten gerendet, sendet er das Ereignis sofort nach dem Aufruf von [**onclockstart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) .</span><span class="sxs-lookup"><span data-stu-id="e3ef8-108">If the stream does not render data, it sends the event immediately after [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) is called.</span></span>

## <a name="event-values"></a><span data-ttu-id="e3ef8-109">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="e3ef8-109">Event values</span></span>

<span data-ttu-id="e3ef8-110">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="e3ef8-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="e3ef8-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e3ef8-111">VARTYPE</span></span>              | <span data-ttu-id="e3ef8-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e3ef8-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="e3ef8-113">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="e3ef8-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="e3ef8-114">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="e3ef8-114">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="e3ef8-115">Attribute</span><span class="sxs-lookup"><span data-stu-id="e3ef8-115">Attributes</span></span>

<span data-ttu-id="e3ef8-116">Für dieses Ereignis sind die folgenden Attribute definiert:</span><span class="sxs-lookup"><span data-stu-id="e3ef8-116">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="e3ef8-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="e3ef8-117">Attribute</span></span>                                                                              | <span data-ttu-id="e3ef8-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e3ef8-118">Description</span></span>                                                                                                                                                   |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3ef8-119">**\_ \_ scrubsample-Zeit für MF-Ereignis \_**</span><span class="sxs-lookup"><span data-stu-id="e3ef8-119">**MF\_EVENT\_SCRUBSAMPLE\_TIME**</span></span>](mf-event-scrubsample-time-attribute.md)<br/> | <span data-ttu-id="e3ef8-120">Präsentationszeit, für die Daten gerendert wurden.</span><span class="sxs-lookup"><span data-stu-id="e3ef8-120">Presentation time for which data was rendered.</span></span> <span data-ttu-id="e3ef8-121">Wenn die Medien Senke während des Bereinigungs Vorgang keine Daten enthält, wird dieses Attribut nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e3ef8-121">If the media sink does not render data while scrubbing, it does not set this attribute.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="e3ef8-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3ef8-122">Requirements</span></span>



| <span data-ttu-id="e3ef8-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3ef8-123">Requirement</span></span> | <span data-ttu-id="e3ef8-124">Wert</span><span class="sxs-lookup"><span data-stu-id="e3ef8-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3ef8-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e3ef8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e3ef8-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3ef8-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e3ef8-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e3ef8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e3ef8-128">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3ef8-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e3ef8-129">Header</span><span class="sxs-lookup"><span data-stu-id="e3ef8-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3ef8-130"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e3ef8-130"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3ef8-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3ef8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3ef8-132">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e3ef8-132">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="e3ef8-133">Medien senken</span><span class="sxs-lookup"><span data-stu-id="e3ef8-133">Media Sinks</span></span>](media-sinks.md)
</dt> <dt>

[<span data-ttu-id="e3ef8-134">Mesessionscrubsamplecomplete</span><span class="sxs-lookup"><span data-stu-id="e3ef8-134">MESessionScrubSampleComplete</span></span>](mesessionscrubsamplecomplete.md)
</dt> </dl>

 

 




