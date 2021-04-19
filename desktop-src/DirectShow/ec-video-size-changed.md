---
description: Die Größe des nativen Videos wurde geändert.
ms.assetid: 276f37b3-f981-4a01-bb37-1ee77248668f
title: EC_VIDEO_SIZE_CHANGED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b29a70ceab583d8dfc51b417fb701a2988b2e96f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367037"
---
# <a name="ec_video_size_changed"></a><span data-ttu-id="7a7ca-103">Größe des EC- \_ Videos \_ \_ geändert</span><span class="sxs-lookup"><span data-stu-id="7a7ca-103">EC\_VIDEO\_SIZE\_CHANGED</span></span>

<span data-ttu-id="7a7ca-104">Die Größe des nativen Videos wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="7a7ca-104">The native video size has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="7a7ca-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a7ca-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a7ca-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="7a7ca-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="7a7ca-107">(**DWORD**) Word in niedriger Ordnung gibt die neue Breite in Pixel an. hohes Wort gibt die neue Höhe in Pixel an.</span><span class="sxs-lookup"><span data-stu-id="7a7ca-107">(**DWORD**) Low-order WORD specifies the new width, in pixels; high-order WORD specifies the new height, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="7a7ca-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="7a7ca-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="7a7ca-109">Keinen.</span><span class="sxs-lookup"><span data-stu-id="7a7ca-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="7a7ca-110">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="7a7ca-110">Default Action</span></span>

<span data-ttu-id="7a7ca-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="7a7ca-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a7ca-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a7ca-112">Remarks</span></span>

<span data-ttu-id="7a7ca-113">Videorenderer Senden dieses Ereignis möglicherweise, wenn Sie eine Änderung an der systemeigenen Videogröße erkennen.</span><span class="sxs-lookup"><span data-stu-id="7a7ca-113">Video renderers may send this event if they detect a change in the native video size.</span></span>

<span data-ttu-id="7a7ca-114">Der [Video Mischungs-Renderer 7](video-mixing-renderer-filter-7.md) (VMR-7) und der [Video Mischungs-Renderer 9](video-mixing-renderer-filter-9.md) (VMR-9) senden dieses Ereignis im Fenstermodus, aber nicht im fensterlosen Modus oder im Modus für renderlos.</span><span class="sxs-lookup"><span data-stu-id="7a7ca-114">The [Video Mixing Renderer 7](video-mixing-renderer-filter-7.md) (VMR-7) and the [Video Mixing Renderer 9](video-mixing-renderer-filter-9.md) (VMR-9) send this event in windowed mode, but not in windowless mode or renderless mode.</span></span> <span data-ttu-id="7a7ca-115">Weitere Informationen zum Fenster-Modus in der VMR finden Sie unter [Video Rendering](video-rendering.md).</span><span class="sxs-lookup"><span data-stu-id="7a7ca-115">For more information about windowed mode in the VMR, see [Video Rendering](video-rendering.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a7ca-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a7ca-116">Requirements</span></span>



| <span data-ttu-id="7a7ca-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a7ca-117">Requirement</span></span> | <span data-ttu-id="7a7ca-118">Wert</span><span class="sxs-lookup"><span data-stu-id="7a7ca-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7a7ca-119">Header</span><span class="sxs-lookup"><span data-stu-id="7a7ca-119">Header</span></span><br/> | <dl> <span data-ttu-id="7a7ca-120"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a7ca-120"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a7ca-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a7ca-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a7ca-122">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="7a7ca-122">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="7a7ca-123">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="7a7ca-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




