---
description: Der Videorenderer wurde zerstört oder aus dem Diagramm entfernt.
ms.assetid: facf35c2-d6a2-4373-bce5-171fd9325116
title: EC_WINDOW_DESTROYED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdd3e641c7fb911a8da10a4c89682fa266e862de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369579"
---
# <a name="ec_window_destroyed"></a><span data-ttu-id="b32e0-103">EC- \_ Fenster \_ zerstört</span><span class="sxs-lookup"><span data-stu-id="b32e0-103">EC\_WINDOW\_DESTROYED</span></span>

<span data-ttu-id="b32e0-104">Der Videorenderer wurde zerstört oder aus dem Diagramm entfernt.</span><span class="sxs-lookup"><span data-stu-id="b32e0-104">The video renderer was destroyed or removed from the graph.</span></span>

## <a name="parameters"></a><span data-ttu-id="b32e0-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="b32e0-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b32e0-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="b32e0-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="b32e0-107">(**IUnknown** \* ) Ein Zeiger auf die [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstelle des Video-Renderers.</span><span class="sxs-lookup"><span data-stu-id="b32e0-107">(**IUnknown**\*) Pointer to the video renderer's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span>

</dd> <dt>

<span data-ttu-id="b32e0-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="b32e0-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="b32e0-109">Keinen.</span><span class="sxs-lookup"><span data-stu-id="b32e0-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="b32e0-110">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="b32e0-110">Default Action</span></span>

<span data-ttu-id="b32e0-111">Der Filter Graph-Manager gibt dieses Fenster als Fokus über die [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) -Schnittstelle frei.</span><span class="sxs-lookup"><span data-stu-id="b32e0-111">The filter graph manager releases this window as the focus, through the [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) interface.</span></span> <span data-ttu-id="b32e0-112">Die Ereignis Benachrichtigung wird nicht an die Anwendung gesendet.</span><span class="sxs-lookup"><span data-stu-id="b32e0-112">It does not send the event notification to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="b32e0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b32e0-113">Remarks</span></span>

<span data-ttu-id="b32e0-114">Der Videorenderer sendet dieses Ereignis, wenn es das Filter Diagramm verlässt, in der [**ibasefilter:: joinfiltergraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) -Methode.</span><span class="sxs-lookup"><span data-stu-id="b32e0-114">The video renderer sends this event when it leaves the filter graph, in its [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) method.</span></span> <span data-ttu-id="b32e0-115">(Das Senden des Ereignisses, wenn der Filter zerstört wird, ist möglicherweise zu spät, da der Filter-Graph-Manager zu diesem Zeitpunkt ebenfalls zerstört werden kann.)</span><span class="sxs-lookup"><span data-stu-id="b32e0-115">(Sending the event when the filter is destroyed might be too late, because at that point the filter graph manager might also be destroyed.)</span></span>

<span data-ttu-id="b32e0-116">Dieses Ereignis ermöglicht anderen Filtern das Abrufen von Ressourcen, die vom Fenster Fokus abhängen, z. b. Audiogeräte.</span><span class="sxs-lookup"><span data-stu-id="b32e0-116">This event enables other filters to acquire resources that depend on window focus, such as audio devices.</span></span>

## <a name="requirements"></a><span data-ttu-id="b32e0-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b32e0-117">Requirements</span></span>



| <span data-ttu-id="b32e0-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b32e0-118">Requirement</span></span> | <span data-ttu-id="b32e0-119">Wert</span><span class="sxs-lookup"><span data-stu-id="b32e0-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b32e0-120">Header</span><span class="sxs-lookup"><span data-stu-id="b32e0-120">Header</span></span><br/> | <dl> <span data-ttu-id="b32e0-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="b32e0-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b32e0-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b32e0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b32e0-123">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="b32e0-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="b32e0-124">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="b32e0-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




