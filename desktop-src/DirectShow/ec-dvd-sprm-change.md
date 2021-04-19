---
description: Wird gesendet, wenn sich der Wert eines Systemparameter Registers (SPRM) ändert.
ms.assetid: 266b6de1-740d-4b3d-8487-5a9570d6c852
title: EC_DVD_SPRM_Change (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_SPRM_Change
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 1af5b8637a197973bca2129a8b8a0198d20248eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366919"
---
# <a name="ec_dvd_sprm_change"></a><span data-ttu-id="56e43-103">EC- \_ DVD- \_ SPRM- \_ Änderung</span><span class="sxs-lookup"><span data-stu-id="56e43-103">EC\_DVD\_SPRM\_Change</span></span>

<span data-ttu-id="56e43-104">Wird gesendet, wenn sich der Wert eines Systemparameter Registers (SPRM) ändert.</span><span class="sxs-lookup"><span data-stu-id="56e43-104">Sent when the value of a system parameter register (SPRM) changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="56e43-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="56e43-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56e43-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="56e43-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="56e43-107">Der null basierte Index des SPRM-Werts, der geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="56e43-107">The zero-based index of the SPRM value that changed.</span></span>

</dd> <dt>

<span data-ttu-id="56e43-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="56e43-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="56e43-109">Die unteren 16 Bits enthalten den neuen SPRM-Wert.</span><span class="sxs-lookup"><span data-stu-id="56e43-109">The lower 16 bits contains the new SPRM value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="56e43-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56e43-110">Remarks</span></span>

<span data-ttu-id="56e43-111">Dieses Ereignis ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="56e43-111">This event is disabled by default.</span></span> <span data-ttu-id="56e43-112">Um dieses Ereignis zu aktivieren, müssen Sie [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) aufrufen und die Option " **DVD \_ enableloggingevents** " auf " **true**" festlegen.</span><span class="sxs-lookup"><span data-stu-id="56e43-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="56e43-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56e43-113">Requirements</span></span>



| <span data-ttu-id="56e43-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56e43-114">Requirement</span></span> | <span data-ttu-id="56e43-115">Wert</span><span class="sxs-lookup"><span data-stu-id="56e43-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56e43-116">Header</span><span class="sxs-lookup"><span data-stu-id="56e43-116">Header</span></span><br/> | <dl> <span data-ttu-id="56e43-117"><dt>Dvdevcode. h (Include DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="56e43-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56e43-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56e43-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56e43-119">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="56e43-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="56e43-120">DVD-Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="56e43-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="56e43-121">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="56e43-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="56e43-122">**IDvdInfo2:: getallsprms**</span><span class="sxs-lookup"><span data-stu-id="56e43-122">**IDvdInfo2::GetAllSPRMs**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallsprms)
</dt> </dl>

 

 




