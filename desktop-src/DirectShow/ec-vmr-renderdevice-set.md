---
description: Wird gesendet, wenn der VMR seinen renderingmechanismus ausgewählt hat.
ms.assetid: 815d1254-c6e3-4a6c-ba4a-bf3da7d35d1f
title: EC_VMR_RENDERDEVICE_SET (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9855b23e25a2c3b955c1499b9505efffcc5637e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355943"
---
# <a name="ec_vmr_renderdevice_set"></a><span data-ttu-id="564fb-103">auf EC \_ VMR \_ renderdevice \_ festgelegt</span><span class="sxs-lookup"><span data-stu-id="564fb-103">EC\_VMR\_RENDERDEVICE\_SET</span></span>

<span data-ttu-id="564fb-104">Wird gesendet, wenn der VMR seinen renderingmechanismus ausgewählt hat.</span><span class="sxs-lookup"><span data-stu-id="564fb-104">Sent when the VMR has selected its rendering mechanism.</span></span>

## <a name="parameters"></a><span data-ttu-id="564fb-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="564fb-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="564fb-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="564fb-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="564fb-107">Kann einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="564fb-107">May be one of the following values:</span></span>



| <span data-ttu-id="564fb-108">Wert</span><span class="sxs-lookup"><span data-stu-id="564fb-108">Value</span></span>                        | <span data-ttu-id="564fb-109">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="564fb-109">Meaning</span></span>                                                  |
|------------------------------|----------------------------------------------------------|
| <span data-ttu-id="564fb-110">VMR- \_ Rendering- \_ Geräte \_ Überlagerung</span><span class="sxs-lookup"><span data-stu-id="564fb-110">VMR\_RENDER\_DEVICE\_OVERLAY</span></span> | <span data-ttu-id="564fb-111">Die VMR wird auf die Überlagerungs Oberfläche (nur VMR-7) renderren.</span><span class="sxs-lookup"><span data-stu-id="564fb-111">The VMR will render to the overlay surface (VMR-7 only).</span></span> |
| <span data-ttu-id="564fb-112">VMR- \_ Rendering- \_ Gerät \_ vidmem</span><span class="sxs-lookup"><span data-stu-id="564fb-112">VMR\_RENDER\_DEVICE\_VIDMEM</span></span>  | <span data-ttu-id="564fb-113">VMR wird in den Videospeicher Rendering.</span><span class="sxs-lookup"><span data-stu-id="564fb-113">The VMR will render to video memory.</span></span>                     |
| <span data-ttu-id="564fb-114">VMR- \_ Rendering- \_ Geräte- \_ sysmem</span><span class="sxs-lookup"><span data-stu-id="564fb-114">VMR\_RENDER\_DEVICE\_SYSMEM</span></span>  | <span data-ttu-id="564fb-115">VMR wird in den Systemspeicher (nur VMR-7).</span><span class="sxs-lookup"><span data-stu-id="564fb-115">The VMR will render to system memory (VMR-7 only).</span></span>       |



 

</dd> <dt>

<span data-ttu-id="564fb-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="564fb-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="564fb-117">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="564fb-117">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="564fb-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="564fb-118">Remarks</span></span>

<span data-ttu-id="564fb-119">Dieses Ereignis wird von VMR-7 und VMR-9 gesendet und an Anwendungen weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="564fb-119">This event is sent by both the VMR-7 and the VMR-9 and it is forwarded to applications.</span></span> <span data-ttu-id="564fb-120">Beachten Sie, dass VMR-9 nur Videospeicher-Renderingziele unterstützt.</span><span class="sxs-lookup"><span data-stu-id="564fb-120">Note that the VMR-9 only supports video memory render targets.</span></span>

## <a name="requirements"></a><span data-ttu-id="564fb-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="564fb-121">Requirements</span></span>



| <span data-ttu-id="564fb-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="564fb-122">Requirement</span></span> | <span data-ttu-id="564fb-123">Wert</span><span class="sxs-lookup"><span data-stu-id="564fb-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="564fb-124">Header</span><span class="sxs-lookup"><span data-stu-id="564fb-124">Header</span></span><br/> | <dl> <span data-ttu-id="564fb-125"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="564fb-125"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="564fb-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="564fb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="564fb-127">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="564fb-127">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="564fb-128">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="564fb-128">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




