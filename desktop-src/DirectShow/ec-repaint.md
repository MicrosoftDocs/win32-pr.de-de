---
description: Ein Videorenderer erfordert ein Repaint.
ms.assetid: 2e756dea-366c-4024-8fc8-6feabaef1954
title: EC_REPAINT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba86b54d6d465330ec1635ed7301ce774ef7cb27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352018"
---
# <a name="ec_repaint"></a><span data-ttu-id="8a5d6-103">EC- \_ Repaint</span><span class="sxs-lookup"><span data-stu-id="8a5d6-103">EC\_REPAINT</span></span>

<span data-ttu-id="8a5d6-104">Ein Videorenderer erfordert ein Repaint.</span><span class="sxs-lookup"><span data-stu-id="8a5d6-104">A video renderer requires a repaint.</span></span>

## <a name="parameters"></a><span data-ttu-id="8a5d6-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a5d6-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a5d6-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="8a5d6-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="8a5d6-107">(**IUnknown** \* ) Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der Eingabe-PIN des Video-Renderers oder **null**.</span><span class="sxs-lookup"><span data-stu-id="8a5d6-107">(**IUnknown**\*) Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the video renderer's input pin, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8a5d6-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="8a5d6-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="8a5d6-109">Keinen.</span><span class="sxs-lookup"><span data-stu-id="8a5d6-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="8a5d6-110">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="8a5d6-110">Default Action</span></span>

<span data-ttu-id="8a5d6-111">Der *lParam1* -Parameter kann die Eingabe-PIN des Video-Renderers angeben.</span><span class="sxs-lookup"><span data-stu-id="8a5d6-111">The *lParam1* parameter might specify the video renderer's input pin.</span></span> <span data-ttu-id="8a5d6-112">Wenn dies der Fall ist, sucht der Filter Diagramm-Manager nach der mit dieser Pin verbundenen Ausgabe-PIN und fragt Sie nach der [**imediaeventsink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="8a5d6-112">If so, the filter graph manager finds the output pin connected to that pin and queries it for the [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface.</span></span> <span data-ttu-id="8a5d6-113">Wenn die Ausgabe-PIN **imediaeventsink** unterstützt, ruft der Filter Graph-Manager [**imediaeventsink:: notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) mit dem EC \_ Repaint-Ereignis Code auf.</span><span class="sxs-lookup"><span data-stu-id="8a5d6-113">If the output pin supports **IMediaEventSink**, the filter graph manager calls [**IMediaEventSink::Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) with the EC\_REPAINT event code.</span></span> <span data-ttu-id="8a5d6-114">Dadurch erhält der Upstream-Filter die Möglichkeit, das letzte Beispiel erneut zu senden.</span><span class="sxs-lookup"><span data-stu-id="8a5d6-114">This gives the upstream filter the opportunity to re-send the last sample.</span></span>

<span data-ttu-id="8a5d6-115">Wenn *lParam1* **null** ist oder wenn die PIN [**imediaeventsink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)nicht unterstützt, oder wenn die [**Benachrichtigungs**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) Methode fehlschlägt, verarbeitet der Filter Graph-Manager das EC \_ Repaint-Ereignis allein.</span><span class="sxs-lookup"><span data-stu-id="8a5d6-115">If *lParam1* is **NULL**, or if the pin does not support [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink), or if the [**Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) method fails, the filter graph manager handles the EC\_REPAINT event by itself.</span></span> <span data-ttu-id="8a5d6-116">Das Verhalten hängt vom Status des Diagramms ab:</span><span class="sxs-lookup"><span data-stu-id="8a5d6-116">Its behavior depends on the state of the graph:</span></span>

-   <span data-ttu-id="8a5d6-117">Wird ausgeführt: ignoriert das Ereignis.</span><span class="sxs-lookup"><span data-stu-id="8a5d6-117">Running: Ignores the event.</span></span> <span data-ttu-id="8a5d6-118">(Der Renderer empfängt das nächste Beispiel im Stream.)</span><span class="sxs-lookup"><span data-stu-id="8a5d6-118">(The renderer will receive the next sample in the stream.)</span></span>
-   <span data-ttu-id="8a5d6-119">Angehalten: sucht im Diagramm nach dem aktuellen Speicherort, wodurch der Filter geleert und die Daten erneut in die Warteschlange eingereiht werden.</span><span class="sxs-lookup"><span data-stu-id="8a5d6-119">Paused: Seeks the graph to its current location, thereby flushing the filter and re-queuing the data.</span></span>
-   <span data-ttu-id="8a5d6-120">Beendet: hält das Diagramm an und hält es an, sodass die Daten erneut in die Warteschlange eingereiht werden.</span><span class="sxs-lookup"><span data-stu-id="8a5d6-120">Stopped: Pauses and stops the graph, thereby re-queuing the data.</span></span>

<span data-ttu-id="8a5d6-121">Standardmäßig übergibt der Filter Graph-Manager dieses Ereignis nicht an die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="8a5d6-121">By default, the filter graph manager does not pass this event to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a5d6-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a5d6-122">Remarks</span></span>

<span data-ttu-id="8a5d6-123">Videorenderer senden diese Nachricht, wenn Sie eine [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) -Meldung empfangen und keine anzuzeigenden Daten aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8a5d6-123">Video renderers send this message when they receive a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message and have no data to display.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a5d6-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a5d6-124">Requirements</span></span>



| <span data-ttu-id="8a5d6-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8a5d6-125">Requirement</span></span> | <span data-ttu-id="8a5d6-126">Wert</span><span class="sxs-lookup"><span data-stu-id="8a5d6-126">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8a5d6-127">Header</span><span class="sxs-lookup"><span data-stu-id="8a5d6-127">Header</span></span><br/> | <dl> <span data-ttu-id="8a5d6-128"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a5d6-128"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a5d6-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a5d6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a5d6-130">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="8a5d6-130">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="8a5d6-131">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="8a5d6-131">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

