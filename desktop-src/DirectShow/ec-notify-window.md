---
description: Benachrichtigt einen Filter über das Fenster des Video-Renderers.
ms.assetid: 65d2f40e-c42c-4d71-b9b3-7662a8be0953
title: EC_NOTIFY_WINDOW (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3165247f05e2fb945f02fee43149b84480bd4b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372450"
---
# <a name="ec_notify_window"></a><span data-ttu-id="b6881-103">EC- \_ Benachrichtigungs \_ Fenster</span><span class="sxs-lookup"><span data-stu-id="b6881-103">EC\_NOTIFY\_WINDOW</span></span>

<span data-ttu-id="b6881-104">Benachrichtigt einen Filter über das Fenster des Video-Renderers.</span><span class="sxs-lookup"><span data-stu-id="b6881-104">Notifies a filter of the video renderer's window.</span></span>

## <a name="parameters"></a><span data-ttu-id="b6881-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6881-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6881-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="b6881-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="b6881-107">(**HWND**) Handle für das Fenster.</span><span class="sxs-lookup"><span data-stu-id="b6881-107">(**HWND**) Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="b6881-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="b6881-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="b6881-109">Keinen.</span><span class="sxs-lookup"><span data-stu-id="b6881-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="b6881-110">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="b6881-110">Default Action</span></span>

<span data-ttu-id="b6881-111">Dieses Ereignis wird intern von DirectShow verwendet.</span><span class="sxs-lookup"><span data-stu-id="b6881-111">This event is used internally by DirectShow.</span></span> <span data-ttu-id="b6881-112">Der Filter Graph-Manager übergibt dieses Ereignis nicht an die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b6881-112">The filter graph manager does not pass this event to the application.</span></span> <span data-ttu-id="b6881-113">Anwendungen können die Standardaktion für dieses Ereignis nicht überschreiben.</span><span class="sxs-lookup"><span data-stu-id="b6881-113">Applications cannot override the default action for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6881-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6881-114">Remarks</span></span>

<span data-ttu-id="b6881-115">Wenn ein Videorenderer verbunden ist, überprüft er, ob der upstreamausgabepin die [**imediaeventsink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) -Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b6881-115">When a video renderer is connected, it checks whether the upstream output pin supports the [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface.</span></span> <span data-ttu-id="b6881-116">Wenn dies der Fall ist, sendet der Renderer dieses Ereignis an den upstreamfilter.</span><span class="sxs-lookup"><span data-stu-id="b6881-116">If so, the renderer sends this event to the upstream filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6881-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6881-117">Requirements</span></span>



| <span data-ttu-id="b6881-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6881-118">Requirement</span></span> | <span data-ttu-id="b6881-119">Wert</span><span class="sxs-lookup"><span data-stu-id="b6881-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b6881-120">Header</span><span class="sxs-lookup"><span data-stu-id="b6881-120">Header</span></span><br/> | <dl> <span data-ttu-id="b6881-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6881-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6881-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6881-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6881-123">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="b6881-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="b6881-124">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="b6881-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




