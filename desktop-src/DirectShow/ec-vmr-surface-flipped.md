---
description: Wird gesendet, wenn der zuordnerpräsentator von VMR-7Die DirectDraw-Flip-Methode auf der dargestellten Oberfläche aufgerufen hat. Dadurch kann der VMR seine directxva-Tabelle der Oberflächen mit der DirectDraw-flippingkette synchronisieren.
ms.assetid: e298857b-0579-48b4-add0-72320bc52d63
title: EC_VMR_SURFACE_FLIPPED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1feafaa58f0cacdafde04591d494dbb9a9eb258e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373826"
---
# <a name="ec_vmr_surface_flipped"></a><span data-ttu-id="865b3-104">EC- \_ VMR- \_ Oberfläche \_ gekippt</span><span class="sxs-lookup"><span data-stu-id="865b3-104">EC\_VMR\_SURFACE\_FLIPPED</span></span>

<span data-ttu-id="865b3-105">Wird gesendet, wenn der zuordnerpräsentator von VMR-7Die DirectDraw-Flip-Methode auf der dargestellten Oberfläche aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="865b3-105">Sent when the VMR-7's allocator presenter has called the DirectDraw Flip method on the surface being presented.</span></span> <span data-ttu-id="865b3-106">Dadurch kann der VMR seine directxva-Tabelle der Oberflächen mit der DirectDraw-flippingkette synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="865b3-106">This allows the VMR to keep its DirectXVA table of surfaces synchronized with DirectDraw's flipping chain.</span></span>

## <a name="parameters"></a><span data-ttu-id="865b3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="865b3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="865b3-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="865b3-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="865b3-109">(**HRESULT**) Der von der DirectDraw-Flip-Methode zurückgegebene Status Code.</span><span class="sxs-lookup"><span data-stu-id="865b3-109">(**HRESULT**) Status code returned from the DirectDraw Flip method.</span></span>

</dd> <dt>

<span data-ttu-id="865b3-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="865b3-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="865b3-111">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="865b3-111">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="865b3-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="865b3-112">Remarks</span></span>

<span data-ttu-id="865b3-113">Benutzerdefinierte Zuweisung: Presenter für VMR-7 sollte dieses Ereignis senden.</span><span class="sxs-lookup"><span data-stu-id="865b3-113">Custom allocator-presenters for the VMR-7 should send this event.</span></span> <span data-ttu-id="865b3-114">Dieses Ereignis wird nicht an Anwendungen weitergeleitet und wird nicht mit "zuordcator-Presenter" für VMR-9 verwendet.</span><span class="sxs-lookup"><span data-stu-id="865b3-114">This event is not forwarded to applications and it is not used with allocator-presenters for the VMR-9.</span></span>

## <a name="requirements"></a><span data-ttu-id="865b3-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="865b3-115">Requirements</span></span>



| <span data-ttu-id="865b3-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="865b3-116">Requirement</span></span> | <span data-ttu-id="865b3-117">Wert</span><span class="sxs-lookup"><span data-stu-id="865b3-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="865b3-118">Header</span><span class="sxs-lookup"><span data-stu-id="865b3-118">Header</span></span><br/> | <dl> <span data-ttu-id="865b3-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="865b3-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="865b3-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="865b3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="865b3-121">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="865b3-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="865b3-122">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="865b3-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




