---
description: Der Videorenderer schaltet den Vollbildmodus aus.
ms.assetid: f720a9b6-930a-4ed7-9798-1c72fa7a11ff
title: EC_FULLSCREEN_LOST (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf36b5652ea5f7cde26950a18de086af0862dac7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370724"
---
# <a name="ec_fullscreen_lost"></a><span data-ttu-id="b31c0-103">EC- \_ Vollbildschirm \_ Verlust</span><span class="sxs-lookup"><span data-stu-id="b31c0-103">EC\_FULLSCREEN\_LOST</span></span>

<span data-ttu-id="b31c0-104">Der Videorenderer schaltet den Vollbildmodus aus.</span><span class="sxs-lookup"><span data-stu-id="b31c0-104">The video renderer is switching out of full-screen mode.</span></span>

## <a name="parameters"></a><span data-ttu-id="b31c0-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="b31c0-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b31c0-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="b31c0-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="b31c0-107">Keinen.</span><span class="sxs-lookup"><span data-stu-id="b31c0-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="b31c0-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="b31c0-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="b31c0-109">(**IUnknown** \* ) Ein Zeiger auf die [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstelle des Videorenderer oder **null**.</span><span class="sxs-lookup"><span data-stu-id="b31c0-109">(**IUnknown**\*) Pointer to the video renderer's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface, or **NULL**.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="b31c0-110">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="b31c0-110">Default Action</span></span>

<span data-ttu-id="b31c0-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="b31c0-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="b31c0-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b31c0-112">Remarks</span></span>

<span data-ttu-id="b31c0-113">Wenn der [Vollbild-Renderer](full-screen-renderer-filter.md) die Aktivierung verliert, sendet er dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="b31c0-113">When the [Full Screen Renderer](full-screen-renderer-filter.md) loses activation, it sends this event.</span></span> <span data-ttu-id="b31c0-114">Wenn ein anderer Videorenderer aus dem Vollbildmodus wechselt, sendet der Filter Graph-Manager dieses Ereignis als Antwort auf ein [**EC- \_ Aktivierungs**](ec-activate.md) Ereignis vom Renderer.</span><span class="sxs-lookup"><span data-stu-id="b31c0-114">When another video renderer switches out of full-screen mode, the filter graph manager sends this event, in response to an [**EC\_ACTIVATE**](ec-activate.md) event from the renderer.</span></span>

## <a name="requirements"></a><span data-ttu-id="b31c0-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b31c0-115">Requirements</span></span>



| <span data-ttu-id="b31c0-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b31c0-116">Requirement</span></span> | <span data-ttu-id="b31c0-117">Wert</span><span class="sxs-lookup"><span data-stu-id="b31c0-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b31c0-118">Header</span><span class="sxs-lookup"><span data-stu-id="b31c0-118">Header</span></span><br/> | <dl> <span data-ttu-id="b31c0-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="b31c0-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b31c0-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b31c0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b31c0-121">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="b31c0-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="b31c0-122">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="b31c0-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




