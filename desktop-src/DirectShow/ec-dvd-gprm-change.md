---
description: Wird gesendet, wenn sich der Wert eines allgemeinen Parameter Registers (GPRM) ändert.
ms.assetid: 3e0c400e-9ea5-458c-9eca-97d66a440590
title: EC_DVD_GPRM_Change (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_GPRM_Change
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: f67a8646a72689c2570462f7dc4aeee6b2474136
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360330"
---
# <a name="ec_dvd_gprm_change"></a><span data-ttu-id="993a0-103">Änderungen an der EC- \_ DVD- \_ GPRM \_</span><span class="sxs-lookup"><span data-stu-id="993a0-103">EC\_DVD\_GPRM\_Change</span></span>

<span data-ttu-id="993a0-104">Wird gesendet, wenn sich der Wert eines allgemeinen Parameter Registers (GPRM) ändert.</span><span class="sxs-lookup"><span data-stu-id="993a0-104">Sent when the value of a general parameter register (GPRM) changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="993a0-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="993a0-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="993a0-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="993a0-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="993a0-107">Der null basierte Index des GPRM-Werts, der geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="993a0-107">The zero-based index of the GPRM value that changed.</span></span>

</dd> <dt>

<span data-ttu-id="993a0-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="993a0-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="993a0-109">Die unteren 16 Bits enthalten den neuen GPRM-Wert.</span><span class="sxs-lookup"><span data-stu-id="993a0-109">The lower 16 bits contains the new GPRM value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="993a0-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="993a0-110">Remarks</span></span>

<span data-ttu-id="993a0-111">Dieses Ereignis ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="993a0-111">This event is disabled by default.</span></span> <span data-ttu-id="993a0-112">Um dieses Ereignis zu aktivieren, müssen Sie [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) aufrufen und die Option " **DVD \_ enableloggingevents** " auf " **true**" festlegen.</span><span class="sxs-lookup"><span data-stu-id="993a0-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="993a0-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="993a0-113">Requirements</span></span>



| <span data-ttu-id="993a0-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="993a0-114">Requirement</span></span> | <span data-ttu-id="993a0-115">Wert</span><span class="sxs-lookup"><span data-stu-id="993a0-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="993a0-116">Header</span><span class="sxs-lookup"><span data-stu-id="993a0-116">Header</span></span><br/> | <dl> <span data-ttu-id="993a0-117"><dt>Dvdevcode. h (Include DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="993a0-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="993a0-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="993a0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="993a0-119">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="993a0-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="993a0-120">DVD-Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="993a0-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="993a0-121">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="993a0-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="993a0-122">**IDvdInfo2:: getallgprms**</span><span class="sxs-lookup"><span data-stu-id="993a0-122">**IDvdInfo2::GetAllGPRMs**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallgprms)
</dt> </dl>

 

 




