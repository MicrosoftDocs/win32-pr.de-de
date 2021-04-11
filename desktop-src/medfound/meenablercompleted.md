---
description: Wird von einem inhaltsenabler-Objekt ausgelöst, wenn die Aktion zum Aktivieren von Objekten abgeschlossen ist.
ms.assetid: 5162800c-9c55-40de-be66-a98765324f76
title: Meenablerabgeschlossene-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a74f7379ccc2983abd2327e1250bcf1ca14e688
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130745"
---
# <a name="meenablercompleted-event"></a><span data-ttu-id="fa27f-103">Meenablerabgeschlossene-Ereignis</span><span class="sxs-lookup"><span data-stu-id="fa27f-103">MEEnablerCompleted event</span></span>

<span data-ttu-id="fa27f-104">Wird von einem inhaltsenabler-Objekt ausgelöst, wenn die Aktivierungs Aktion des Objekts abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="fa27f-104">Raised by a content enabler object when the object's enabling action is completed.</span></span> <span data-ttu-id="fa27f-105">Objekte, die die [**imbcontentenabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) -Schnittstelle verfügbar machen, können dieses Ereignis erhöhen.</span><span class="sxs-lookup"><span data-stu-id="fa27f-105">Objects that expose the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface can raise this event.</span></span> <span data-ttu-id="fa27f-106">Das-Ereignis wird ausgelöst, wenn eines der folgenden Ereignisse eintritt:</span><span class="sxs-lookup"><span data-stu-id="fa27f-106">The event is raised if either of the following occurs:</span></span>

-   <span data-ttu-id="fa27f-107">Die [**imfcontentenabler:: automaticenable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) -Methode wird asynchron abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="fa27f-107">The [**IMFContentEnabler::AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) method completes asynchronously.</span></span>
-   <span data-ttu-id="fa27f-108">Die Anwendung ruft [**IMF contentenabler:: monitorenable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable)auf, und die Anwendung schließt dann die HTTP POST-Anforderung ab, wie in der **monitorenable** -Methode beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fa27f-108">The application calls [**IMFContentEnabler::MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable), and then the application completes the HTTP POST request, as described in the **MonitorEnable** method.</span></span>

## <a name="event-values"></a><span data-ttu-id="fa27f-109">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="fa27f-109">Event values</span></span>

<span data-ttu-id="fa27f-110">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="fa27f-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="fa27f-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="fa27f-111">VARTYPE</span></span>              | <span data-ttu-id="fa27f-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fa27f-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="fa27f-113">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="fa27f-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="fa27f-114">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="fa27f-114">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="fa27f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fa27f-115">Remarks</span></span>

<span data-ttu-id="fa27f-116">Der Statuscode aus dem Ereignis kann einen der folgenden Werte enthalten.</span><span class="sxs-lookup"><span data-stu-id="fa27f-116">The status code from the event may contain one of the following values.</span></span>



|                                      |                                                                                                                                                                                 |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa27f-117">**S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="fa27f-117">**S\_OK**</span></span>                            | <span data-ttu-id="fa27f-118">Der Vorgang wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fa27f-118">The operation succeeded.</span></span>                                                                                                                                                        |
| <span data-ttu-id="fa27f-119">**NS \_ E \_ DRM- \_ Lizenz \_ notbezogen**</span><span class="sxs-lookup"><span data-stu-id="fa27f-119">**NS\_E\_DRM\_LICENSE\_NOTACQUIRED**</span></span> | <span data-ttu-id="fa27f-120">Die DRM-Lizenz wurde nicht erworben.</span><span class="sxs-lookup"><span data-stu-id="fa27f-120">The DRM license was not acquired.</span></span> <span data-ttu-id="fa27f-121">Wenn beim vorherigen Versuch [**automaticenable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable)verwendet wurde, sollte die Anwendung den nicht automatischen Erwerb testen.</span><span class="sxs-lookup"><span data-stu-id="fa27f-121">If the previous attempt used [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable), the application should try non-silent acquisition.</span></span> |
| <span data-ttu-id="fa27f-122">**NS \_ S- \_ DRM- \_ Monitor \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="fa27f-122">**NS\_S\_DRM\_MONITOR\_CANCELLED**</span></span>   | <span data-ttu-id="fa27f-123">Der [**monitorenable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable) -Vorgang wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="fa27f-123">The [**MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable) operation was canceled.</span></span>                                                                                            |



 

<span data-ttu-id="fa27f-124">Um dieses Ereignis zu erhalten, Fragen Sie die [**imfcontentenabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) -Schnittstelle für die [**imfmediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="fa27f-124">To receive this event, query the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="fa27f-125">Aufrufen Sie dann [**imfmediaeventgenerator:: begingetevent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), wie im Thema [Medienereignis-Generatoren](media-event-generators.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fa27f-125">Then call [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), as described in the topic [Media Event Generators](media-event-generators.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fa27f-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa27f-126">Requirements</span></span>



| <span data-ttu-id="fa27f-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fa27f-127">Requirement</span></span> | <span data-ttu-id="fa27f-128">Wert</span><span class="sxs-lookup"><span data-stu-id="fa27f-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa27f-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fa27f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fa27f-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fa27f-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fa27f-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fa27f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fa27f-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fa27f-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fa27f-133">Header</span><span class="sxs-lookup"><span data-stu-id="fa27f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa27f-134"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fa27f-134"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa27f-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa27f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa27f-136">**IMF contentenabler**</span><span class="sxs-lookup"><span data-stu-id="fa27f-136">**IMFContentEnabler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[<span data-ttu-id="fa27f-137">Medienereignis Generatoren</span><span class="sxs-lookup"><span data-stu-id="fa27f-137">Media Event Generators</span></span>](media-event-generators.md)
</dt> <dt>

[<span data-ttu-id="fa27f-138">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fa27f-138">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




