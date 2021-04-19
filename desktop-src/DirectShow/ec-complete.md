---
description: Alle Daten aus einem bestimmten Stream wurden gerendert.
ms.assetid: 46037d53-085d-4fd0-91a0-408702cbfce5
title: EC_COMPLETE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cd6d548a56173b9c6ea83426ddab3fa8556e312
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361512"
---
# <a name="ec_complete"></a><span data-ttu-id="0ce20-103">EC \_ Complete</span><span class="sxs-lookup"><span data-stu-id="0ce20-103">EC\_COMPLETE</span></span>

<span data-ttu-id="0ce20-104">Alle Daten aus einem bestimmten Stream wurden gerendert.</span><span class="sxs-lookup"><span data-stu-id="0ce20-104">All data from a particular stream has been rendered.</span></span>

## <a name="parameters"></a><span data-ttu-id="0ce20-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ce20-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ce20-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="0ce20-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="0ce20-107">(**HRESULT**) Der Status des Streams bei Abschluss.</span><span class="sxs-lookup"><span data-stu-id="0ce20-107">(**HRESULT**) Status of the stream on completion.</span></span> <span data-ttu-id="0ce20-108">Wenn während der Wiedergabe keine Fehler aufgetreten sind, ist der Wert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0ce20-108">If no errors occurred during playback, the value is S\_OK.</span></span>

</dd> <dt>

<span data-ttu-id="0ce20-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="0ce20-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="0ce20-110">(**IUnknown** \* ) 0 (null) oder ein Zeiger auf die [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstelle des Renderers.</span><span class="sxs-lookup"><span data-stu-id="0ce20-110">(**IUnknown**\*) Zero, or a pointer to the renderer's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="0ce20-111">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="0ce20-111">Default Action</span></span>

<span data-ttu-id="0ce20-112">Standardmäßig führt der Filter Graph-Manager dieses Ereignis nicht an die Anwendung weiter.</span><span class="sxs-lookup"><span data-stu-id="0ce20-112">By default, the filter graph manager does not forward this event to the application.</span></span> <span data-ttu-id="0ce20-113">Nachdem jedoch alle Streams im Graph-Bericht " **EC" \_ vollständig** sind, stellt der Filter Graph-Manager ein separates **EC \_ Complete** -Ereignis für die Anwendung zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="0ce20-113">However, after all the streams in the graph report **EC\_COMPLETE**, the filter graph manager posts a separate **EC\_COMPLETE** event to the application.</span></span>

<span data-ttu-id="0ce20-114">Wenn die Standardaktion für dieses Ereignis deaktiviert ist, empfängt die Anwendung alle **EC \_ Complete** -Ereignisse von den Renderer.</span><span class="sxs-lookup"><span data-stu-id="0ce20-114">If the default action is disabled for this event, the application receives all of the **EC\_COMPLETE** events from the renderers.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ce20-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ce20-115">Remarks</span></span>

<span data-ttu-id="0ce20-116">Ein rendererfilter sendet dieses Ereignis, wenn es einen Hinweis zum Ende des Streams empfängt.</span><span class="sxs-lookup"><span data-stu-id="0ce20-116">A renderer filter sends this event when it receives an end-of-stream notice.</span></span> <span data-ttu-id="0ce20-117">(Das Ende des Streams wird durch die [**IPin:: EndOf Stream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) -Methode signalisiert.) Der Filter sendet genau ein **EC \_ Complete** -Ereignis für jeden Stream.</span><span class="sxs-lookup"><span data-stu-id="0ce20-117">(End-of-stream is signaled through the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.) The filter sends exactly one **EC\_COMPLETE** event for each stream.</span></span> <span data-ttu-id="0ce20-118">Der Filter muss alle ausstehenden Stichproben verarbeiten, bevor das Ereignis gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="0ce20-118">The filter must process any pending samples before it sends the event.</span></span> <span data-ttu-id="0ce20-119">Durch das Beenden eines Renderers wird jeder zwischengespeicherte streamingstatus zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="0ce20-119">Stopping a renderer resets any end-of-stream state that was cached.</span></span>

<span data-ttu-id="0ce20-120">Wenn der Renderer angehalten wurde, wird **EC \_ Complete** nicht gesendet, bis die [**imediafilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0ce20-120">If the renderer is paused, it does not send **EC\_COMPLETE** until the [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method is called.</span></span> <span data-ttu-id="0ce20-121">Darüber hinaus sendet Sie weiterhin **EC \_ Complete** -Ereignisse für jeden Übergang von der Pause bis zum Ausführen, bis der Filter beendet oder geleert wurde.</span><span class="sxs-lookup"><span data-stu-id="0ce20-121">Furthermore, it continues to send **EC\_COMPLETE** events for each transition from pause to run, until the filter is either stopped or flushed.</span></span>

<span data-ttu-id="0ce20-122">Filter legen Sie den *lParam2* -Parameter auf einen [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Zeiger fest.</span><span class="sxs-lookup"><span data-stu-id="0ce20-122">Filters set the *lParam2* parameter to an [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) pointer.</span></span> <span data-ttu-id="0ce20-123">Wenn die Standardaktion aktiviert ist, legt der Filter Graph-Manager diesen Parameter auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="0ce20-123">If the default action is enabled, the filter graph manager sets this parameter to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ce20-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ce20-124">Requirements</span></span>



| <span data-ttu-id="0ce20-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ce20-125">Requirement</span></span> | <span data-ttu-id="0ce20-126">Wert</span><span class="sxs-lookup"><span data-stu-id="0ce20-126">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0ce20-127">Header</span><span class="sxs-lookup"><span data-stu-id="0ce20-127">Header</span></span><br/> | <dl> <span data-ttu-id="0ce20-128"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ce20-128"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ce20-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ce20-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ce20-130">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="0ce20-130">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="0ce20-131">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="0ce20-131">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="0ce20-132">Alternative Videorenderer</span><span class="sxs-lookup"><span data-stu-id="0ce20-132">Alternative Video Renderers</span></span>](alternative-video-renderers.md)
</dt> </dl>

 

 




