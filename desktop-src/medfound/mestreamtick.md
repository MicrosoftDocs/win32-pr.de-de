---
description: Signalisiert, dass für einen Mediendaten Strom keine Daten zu einem angegebenen Zeitpunkt verfügbar sind.
ms.assetid: 1a00fff1-c3ab-4965-a663-3c15bb48ea98
title: Mestreamtick-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27123569e991043a534883964ba94e4955d60a40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372870"
---
# <a name="mestreamtick-event"></a><span data-ttu-id="340ba-103">Mestreamtick-Ereignis</span><span class="sxs-lookup"><span data-stu-id="340ba-103">MEStreamTick event</span></span>

<span data-ttu-id="340ba-104">Signalisiert, dass für einen Mediendaten Strom keine Daten zu einem angegebenen Zeitpunkt verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="340ba-104">Signals that a media stream does not have data available at a specified time.</span></span>

## <a name="event-values"></a><span data-ttu-id="340ba-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="340ba-105">Event values</span></span>

<span data-ttu-id="340ba-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="340ba-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="340ba-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="340ba-107">VARTYPE</span></span>           | <span data-ttu-id="340ba-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="340ba-108">Description</span></span>                                                                   |
|-------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="340ba-109">VT \_ I8</span><span class="sxs-lookup"><span data-stu-id="340ba-109">VT\_I8</span></span><br/> | <span data-ttu-id="340ba-110">Der Zeitpunkt, zu dem die Lücke auftritt, in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="340ba-110">Time at which the gap occurs, in 100-nanosecond units.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="340ba-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="340ba-111">Remarks</span></span>

<span data-ttu-id="340ba-112">Dieses Ereignis signalisiert eine Lücke in den Daten.</span><span class="sxs-lookup"><span data-stu-id="340ba-112">This event signals a gap in the data.</span></span> <span data-ttu-id="340ba-113">Das Ereignis benachrichtigt Downstreamkomponenten, dass zum angegebenen Zeitpunkt keine Daten erwartet werden.</span><span class="sxs-lookup"><span data-stu-id="340ba-113">The event notifies downstream components not to expect any data at the specified time.</span></span>

<span data-ttu-id="340ba-114">Das Ereignis sollte von dem Objekt gesendet werden, das die Zeitstempel für die Medien Beispiele im Stream generiert.</span><span class="sxs-lookup"><span data-stu-id="340ba-114">The event should be sent by whichever object generates the time stamps for the media samples in the stream.</span></span> <span data-ttu-id="340ba-115">Abhängig vom Format der Daten ist dies entweder:</span><span class="sxs-lookup"><span data-stu-id="340ba-115">Depending on the format of the data, this is either:</span></span>

-   <span data-ttu-id="340ba-116">Der Mediendaten Strom in der Medienquelle ([**IMF Mediastream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) -Schnittstelle) oder</span><span class="sxs-lookup"><span data-stu-id="340ba-116">The media stream on the media source ([**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) interface), or</span></span>
-   <span data-ttu-id="340ba-117">Die decodertransformation ([**IMF Transform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle).</span><span class="sxs-lookup"><span data-stu-id="340ba-117">The decoder transform ([**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface).</span></span>

<span data-ttu-id="340ba-118">Während der Lücke sollte das Objekt das Ereignis so oft senden, wie es normalerweise Beispiele erzeugt.</span><span class="sxs-lookup"><span data-stu-id="340ba-118">During the gap, the object should send the event about as often as it would normally produce samples.</span></span> <span data-ttu-id="340ba-119">Senden Sie für ein Video ein Ereignis für jeden fehlenden Frame.</span><span class="sxs-lookup"><span data-stu-id="340ba-119">For video, send one event for each missing frame.</span></span> <span data-ttu-id="340ba-120">Senden Sie das Ereignis für Audiodaten mindestens einmal pro Sekunde während der Lücke.</span><span class="sxs-lookup"><span data-stu-id="340ba-120">For audio, send the event at least once per second during the gap.</span></span> <span data-ttu-id="340ba-121">Der Wert des Ereignisses ist der Zeitstempel der fehlenden Stichprobe.</span><span class="sxs-lookup"><span data-stu-id="340ba-121">The value of the event is the time stamp of the missing sample.</span></span> <span data-ttu-id="340ba-122">Senden Sie beliebig viele mestreamtick-Ereignisse, um die Lücke in den Daten zu füllen.</span><span class="sxs-lookup"><span data-stu-id="340ba-122">Send as many MEStreamTick events as needed to fill the gap in the data.</span></span>

<span data-ttu-id="340ba-123">Wenn eine Medienquelle über mehrere Datenströme verfügt und eine Lücke in mehr als einem Stream besteht, sollte jeder Stream mestreamtick-Ereignisse senden.</span><span class="sxs-lookup"><span data-stu-id="340ba-123">If a media source has several streams and there is a gap in more than one stream, each stream should send MEStreamTick events.</span></span> <span data-ttu-id="340ba-124">Wenn beispielsweise eine Lücke in den Audio-und Videodaten vorliegt, senden beide Streams das Ereignis.</span><span class="sxs-lookup"><span data-stu-id="340ba-124">For example, if there is a gap in both audio and video data, then both streams send the event.</span></span>

<span data-ttu-id="340ba-125">Das mestreamtick-Ereignis schließt eine [**IMF Mediastream:: requestsample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) -Anforderung nicht ab.</span><span class="sxs-lookup"><span data-stu-id="340ba-125">The MEStreamTick event does not complete an [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) request.</span></span> <span data-ttu-id="340ba-126">Die Medienquelle muss weiterhin ein [memediasample](memediasample.md) -Ereignis für jeden **requestsample**-Anforderer senden.</span><span class="sxs-lookup"><span data-stu-id="340ba-126">The media source must still send an [MEMediaSample](memediasample.md) event for each call to **RequestSample**.</span></span>

<span data-ttu-id="340ba-127">Medien senken können dieses Ereignis nicht direkt verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="340ba-127">Media sinks cannot consume this event directly.</span></span> <span data-ttu-id="340ba-128">Um eine Lücke im Stream an eine Medien Senke zu signalisieren, nennen Sie [**imfstreamsink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) mit einem **mfstreamsink- \_ markermarker \_** .</span><span class="sxs-lookup"><span data-stu-id="340ba-128">To signal a gap in the stream to a media sink, call [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) with an **MFSTREAMSINK\_MARKER\_TICK** marker.</span></span> <span data-ttu-id="340ba-129">Bei Bedarf werden von der Media Foundation Pipeline mestreamtick-Ereignisse in **mfstreamsink- \_ \_ markermarker** konvertiert.</span><span class="sxs-lookup"><span data-stu-id="340ba-129">The Media Foundation pipeline converts MEStreamTick events to **MFSTREAMSINK\_MARKER\_TICK** markers when needed.</span></span>

<span data-ttu-id="340ba-130">Legen Sie das Attribut " [**\_ discontinuity" der MF SampleExtension**](mfsampleextension-discontinuity-attribute.md) -Eigenschaft nicht auf das nächste Medien Beispiel nach einem mestreamtick-Ereignis fest.</span><span class="sxs-lookup"><span data-stu-id="340ba-130">Do not set the [**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute on the next media sample after an MEStreamTick event.</span></span> <span data-ttu-id="340ba-131">Das Attribut " **mfsampleextension \_ discontinuity** " impliziert, dass der Zeitstempel mit vorherigen Zeitstempeln diskontinuierlich ist, wohingegen "mestreamtick" impliziert, dass Zeitstempel kontinuierlich sind, aber einige Daten fehlen.</span><span class="sxs-lookup"><span data-stu-id="340ba-131">The **MFSampleExtension\_Discontinuity** attribute implies that the time stamp is discontinuous with previous time stamps, whereas MEStreamTick implies that time stamps are continuous but some data is missing.</span></span>

> [!Note]  
> <span data-ttu-id="340ba-132">In einer früheren Version der Dokumentation wurde fälschlicherweise angegeben, dass das Beispiel nach einem mestreamtick-Ereignis das Attribut " [**MF SampleExtension \_ discontinuity**](mfsampleextension-discontinuity-attribute.md) " aufweisen sollte.</span><span class="sxs-lookup"><span data-stu-id="340ba-132">An earlier version of the documentation incorrectly stated that the sample after an MEStreamTick event should have the [**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="340ba-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="340ba-133">Requirements</span></span>



| <span data-ttu-id="340ba-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="340ba-134">Requirement</span></span> | <span data-ttu-id="340ba-135">Wert</span><span class="sxs-lookup"><span data-stu-id="340ba-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="340ba-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="340ba-136">Minimum supported client</span></span><br/> | <span data-ttu-id="340ba-137">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="340ba-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="340ba-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="340ba-138">Minimum supported server</span></span><br/> | <span data-ttu-id="340ba-139">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="340ba-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="340ba-140">Header</span><span class="sxs-lookup"><span data-stu-id="340ba-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="340ba-141"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="340ba-141"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="340ba-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="340ba-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="340ba-143">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="340ba-143">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




