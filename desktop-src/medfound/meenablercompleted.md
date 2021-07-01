---
description: Wird von einem Content Enabler-Objekt ausgelöst, wenn die Objekte, die die Aktion aktivieren, abgeschlossen sind.
ms.assetid: 5162800c-9c55-40de-be66-a98765324f76
title: MEEnablerCompleted-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f05459a648f6b357fd483baa9fc56809540e64a1
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119445"
---
# <a name="meenablercompleted-event"></a><span data-ttu-id="62ec8-103">MEEnablerCompleted-Ereignis</span><span class="sxs-lookup"><span data-stu-id="62ec8-103">MEEnablerCompleted event</span></span>

<span data-ttu-id="62ec8-104">Wird von einem Content Enabler-Objekt ausgelöst, wenn die Aktivierungsaktion des Objekts abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="62ec8-104">Raised by a content enabler object when the object's enabling action is completed.</span></span> <span data-ttu-id="62ec8-105">Objekte, die die [**SCHNITTSTELLE "CONTENTContentEnabler"**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) verfügbar machen, können dieses Ereignis auslösen.</span><span class="sxs-lookup"><span data-stu-id="62ec8-105">Objects that expose the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface can raise this event.</span></span> <span data-ttu-id="62ec8-106">Das -Ereignis wird ausgelöst, wenn einer der folgenden Ereignisse auftritt:</span><span class="sxs-lookup"><span data-stu-id="62ec8-106">The event is raised if either of the following occurs:</span></span>

-   <span data-ttu-id="62ec8-107">Die [**ASYNCHRONOUSContentEnabler::AutomaticEnable-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) wird asynchron abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="62ec8-107">The [**IMFContentEnabler::AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) method completes asynchronously.</span></span>
-   <span data-ttu-id="62ec8-108">Die Anwendung ruft [**DIECONTENTContentEnabler::MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable)auf, und dann schließt die Anwendung die HTTP POST-Anforderung ab, wie in der **MonitorEnable-Methode** beschrieben.</span><span class="sxs-lookup"><span data-stu-id="62ec8-108">The application calls [**IMFContentEnabler::MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable), and then the application completes the HTTP POST request, as described in the **MonitorEnable** method.</span></span>

## <a name="event-values"></a><span data-ttu-id="62ec8-109">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="62ec8-109">Event values</span></span>

<span data-ttu-id="62ec8-110">Mögliche Werte, die von [**DERMEDIAEVENT::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind:</span><span class="sxs-lookup"><span data-stu-id="62ec8-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="62ec8-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="62ec8-111">VARTYPE</span></span>              | <span data-ttu-id="62ec8-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="62ec8-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="62ec8-113">VT \_ EMPTY</span><span class="sxs-lookup"><span data-stu-id="62ec8-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="62ec8-114">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="62ec8-114">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="62ec8-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62ec8-115">Remarks</span></span>

<span data-ttu-id="62ec8-116">Der Statuscode des Ereignisses kann einen der folgenden Werte enthalten.</span><span class="sxs-lookup"><span data-stu-id="62ec8-116">The status code from the event may contain one of the following values.</span></span>



| <span data-ttu-id="62ec8-117">Wert</span><span class="sxs-lookup"><span data-stu-id="62ec8-117">Value</span></span>                                     | <span data-ttu-id="62ec8-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="62ec8-118">Description</span></span>                                                                                                                                                                                |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62ec8-119">**S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="62ec8-119">**S\_OK**</span></span>                            | <span data-ttu-id="62ec8-120">Der Vorgang wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="62ec8-120">The operation succeeded.</span></span>                                                                                                                                                        |
| <span data-ttu-id="62ec8-121">**NS \_ E \_ DRM \_ LICENSE \_ NOTACQUIRED**</span><span class="sxs-lookup"><span data-stu-id="62ec8-121">**NS\_E\_DRM\_LICENSE\_NOTACQUIRED**</span></span> | <span data-ttu-id="62ec8-122">Die DRM-Lizenz wurde nicht erworben.</span><span class="sxs-lookup"><span data-stu-id="62ec8-122">The DRM license was not acquired.</span></span> <span data-ttu-id="62ec8-123">Wenn beim vorherigen Versuch [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable)verwendet wurde, sollte die Anwendung versuchen, nicht automatisch zu erwerben.</span><span class="sxs-lookup"><span data-stu-id="62ec8-123">If the previous attempt used [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable), the application should try non-silent acquisition.</span></span> |
| <span data-ttu-id="62ec8-124">**NS \_ S \_ DRM \_ MONITOR \_ CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="62ec8-124">**NS\_S\_DRM\_MONITOR\_CANCELLED**</span></span>   | <span data-ttu-id="62ec8-125">Der [**MonitorEnable-Vorgang**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable) wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="62ec8-125">The [**MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable) operation was canceled.</span></span>                                                                                            |



 

<span data-ttu-id="62ec8-126">Um dieses Ereignis zu empfangen, fragen Sie die [**SCHNITTSTELLE "CONTENTContentEnabler"**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) nach der [**SCHNITTSTELLE "ARRANGEMediaEventGenerator"**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) ab.</span><span class="sxs-lookup"><span data-stu-id="62ec8-126">To receive this event, query the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="62ec8-127">Rufen Sie dann [**DENMEDIAEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent)auf, wie im Thema [Medienereignisgeneratoren](media-event-generators.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="62ec8-127">Then call [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), as described in the topic [Media Event Generators](media-event-generators.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="62ec8-128">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="62ec8-128">Requirements</span></span>



| <span data-ttu-id="62ec8-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62ec8-129">Requirement</span></span> | <span data-ttu-id="62ec8-130">Wert</span><span class="sxs-lookup"><span data-stu-id="62ec8-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62ec8-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="62ec8-131">Minimum supported client</span></span><br/> | <span data-ttu-id="62ec8-132">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="62ec8-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="62ec8-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="62ec8-133">Minimum supported server</span></span><br/> | <span data-ttu-id="62ec8-134">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="62ec8-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="62ec8-135">Header</span><span class="sxs-lookup"><span data-stu-id="62ec8-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="62ec8-136"><dt>Mfobjects.h (einschließlich Mfidl.h)</dt></span><span class="sxs-lookup"><span data-stu-id="62ec8-136"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62ec8-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62ec8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62ec8-138">**CONTENTContentEnabler**</span><span class="sxs-lookup"><span data-stu-id="62ec8-138">**IMFContentEnabler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[<span data-ttu-id="62ec8-139">Medienereignisgeneratoren</span><span class="sxs-lookup"><span data-stu-id="62ec8-139">Media Event Generators</span></span>](media-event-generators.md)
</dt> <dt>

[<span data-ttu-id="62ec8-140">Media Foundation Ereignisse</span><span class="sxs-lookup"><span data-stu-id="62ec8-140">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




