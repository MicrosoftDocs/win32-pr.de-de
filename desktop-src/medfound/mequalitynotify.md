---
description: Bietet dem Quality Manager Feedback zur Wiedergabequalität.
ms.assetid: 1b4b6a2d-411e-42d1-a44b-bb1928e1c063
title: Mequalitynotify-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d8f486bfebfd137ba341176af0fdad257776df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528271"
---
# <a name="mequalitynotify-event"></a><span data-ttu-id="ea673-103">Mequalitynotify-Ereignis</span><span class="sxs-lookup"><span data-stu-id="ea673-103">MEQualityNotify event</span></span>

<span data-ttu-id="ea673-104">Bietet dem Quality Manager Feedback zur Wiedergabequalität.</span><span class="sxs-lookup"><span data-stu-id="ea673-104">Provides feedback to the quality manager about playback quality.</span></span>

## <a name="event-values"></a><span data-ttu-id="ea673-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="ea673-105">Event values</span></span>

<span data-ttu-id="ea673-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="ea673-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="ea673-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ea673-107">VARTYPE</span></span>           | <span data-ttu-id="ea673-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea673-108">Description</span></span>                         |
|-------------------|-------------------------------------|
| <span data-ttu-id="ea673-109">VT \_ I8</span><span class="sxs-lookup"><span data-stu-id="ea673-109">VT\_I8</span></span><br/> | <span data-ttu-id="ea673-110">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ea673-110">See Remarks.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="ea673-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea673-111">Remarks</span></span>

<span data-ttu-id="ea673-112">Dieses Ereignis wird von einigen Pipeline Komponenten ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="ea673-112">This event is raised by some pipeline components.</span></span> <span data-ttu-id="ea673-113">Die Medien Sitzung leitet das Ereignis an den Quality Manager weiter, indem die [**imfqualitymanager:: notifyqualityevent**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyqualityevent) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ea673-113">The Media Session forwards the event to the quality manager by calling the [**IMFQualityManager::NotifyQualityEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyqualityevent) method.</span></span>

<span data-ttu-id="ea673-114">Der erweiterte Typ des Ereignisses gibt die Bedeutung der Ereignisdaten an.</span><span class="sxs-lookup"><span data-stu-id="ea673-114">The event's extended type indicates the meaning of the event data.</span></span>



| <span data-ttu-id="ea673-115">Erweiterter Typ</span><span class="sxs-lookup"><span data-stu-id="ea673-115">Extended type</span></span>                            | <span data-ttu-id="ea673-116">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="ea673-116">Event data</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea673-117">Verarbeitungs Wartezeit für die MF- \_ Qualität \_ Benachrichtigen \_ \_</span><span class="sxs-lookup"><span data-stu-id="ea673-117">MF\_QUALITY\_NOTIFY\_PROCESSING\_LATENCY</span></span> | <span data-ttu-id="ea673-118">Ungefähre Verarbeitungs Wartezeit, die von der Komponente eingeführt wurde, in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="ea673-118">Approximate processing latency introduced by the component, in 100-nanosecond units.</span></span><br/> <span data-ttu-id="ea673-119">Verarbeitungs Latenz ist die Latenzzeit, die eine Komponente in die Pipeline einführt, indem ein Beispiel verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="ea673-119">Processing latency is the amount of latency that a component introduces into the pipeline by processing a sample.</span></span> <span data-ttu-id="ea673-120">In einigen Fällen kann die Wartezeit nicht einfach durch Betrachtung der Aufrufe von [**imfqualitymanager:: notifyprocessinput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput) und [**imfqualitymanager:: notifyprocessoutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput)abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="ea673-120">In some cases, the latency cannot be derived simply by looking at the calls to [**IMFQualityManager::NotifyProcessInput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput) and [**IMFQualityManager::NotifyProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput).</span></span> <span data-ttu-id="ea673-121">Beispielsweise gibt es möglicherweise keine 1:1-Entsprechung zwischen Eingabe Beispielen und Ausgabe Beispielen.</span><span class="sxs-lookup"><span data-stu-id="ea673-121">For example, there may not be a one-to-one correspondence between input samples and output samples.</span></span> <span data-ttu-id="ea673-122">In diesem Fall sendet die Komponente möglicherweise ein mequalitynotify-Ereignis mit der Verarbeitungs Latenz.</span><span class="sxs-lookup"><span data-stu-id="ea673-122">In this case, the component might send an MEQualityNotify event with the processing latency.</span></span> <span data-ttu-id="ea673-123">Wenn die Verarbeitungs Latenz geändert wird, kann die Komponente während des Streamings jederzeit ein neues Ereignis senden.</span><span class="sxs-lookup"><span data-stu-id="ea673-123">If the processing latency changes, the component can send a new event at any time during streaming.</span></span><br/> |
| <span data-ttu-id="ea673-124">Beispiel Verzögerung für die MF- \_ Qualitäts \_ Benachrichtigung \_ \_</span><span class="sxs-lookup"><span data-stu-id="ea673-124">MF\_QUALITY\_NOTIFY\_SAMPLE\_LAG</span></span>         | <span data-ttu-id="ea673-125">Verzögerungszeit für das Beispiel in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="ea673-125">Lag time for the sample, in 100-nanosecond units.</span></span> <span data-ttu-id="ea673-126">Wenn der Wert positiv ist, war das Beispiel spät.</span><span class="sxs-lookup"><span data-stu-id="ea673-126">If the value is positive, the sample was late.</span></span> <span data-ttu-id="ea673-127">Wenn der Wert negativ ist, war das Beispiel früh.</span><span class="sxs-lookup"><span data-stu-id="ea673-127">If the value is negative, the sample was early.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="ea673-128">Um den erweiterten Typ abzurufen, nennen Sie [**imfmediaevent:: getextendedtype**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).</span><span class="sxs-lookup"><span data-stu-id="ea673-128">To get the extended type, call [**IMFMediaEvent::GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).</span></span>

<span data-ttu-id="ea673-129">Pipeline Komponenten sind nicht erforderlich, um dieses Ereignis zu senden.</span><span class="sxs-lookup"><span data-stu-id="ea673-129">Pipeline components are not required to send this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea673-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea673-130">Requirements</span></span>



| <span data-ttu-id="ea673-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea673-131">Requirement</span></span> | <span data-ttu-id="ea673-132">Wert</span><span class="sxs-lookup"><span data-stu-id="ea673-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea673-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ea673-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ea673-134">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea673-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ea673-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ea673-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ea673-136">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea673-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ea673-137">Header</span><span class="sxs-lookup"><span data-stu-id="ea673-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea673-138"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea673-138"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea673-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea673-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea673-140">**IMF-Manager**</span><span class="sxs-lookup"><span data-stu-id="ea673-140">**IMFQualityManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)
</dt> <dt>

[<span data-ttu-id="ea673-141">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ea673-141">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




