---
description: Gibt an, dass der DVD-Navigator entweder mit dem wiedergeben oder Beenden der Karaoke-Daten begonnen hat.
ms.assetid: 910bf809-a56a-4d02-9c7e-429769a4ec2b
title: EC_DVD_KARAOKE_MODE (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_KARAOKE_MODE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: fb83bc1de9c2933b53935c056b192eca74c4245c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364894"
---
# <a name="ec_dvd_karaoke_mode"></a><span data-ttu-id="2ffab-103">EC- \_ DVD- \_ Karaoke- \_ Modus</span><span class="sxs-lookup"><span data-stu-id="2ffab-103">EC\_DVD\_KARAOKE\_MODE</span></span>

<span data-ttu-id="2ffab-104">Gibt an, dass der [DVD-Navigator](data-flow-in-the-dvd-navigator.md) entweder mit dem wiedergeben oder Beenden der Karaoke-Daten begonnen hat.</span><span class="sxs-lookup"><span data-stu-id="2ffab-104">Indicates that the [DVD Navigator](data-flow-in-the-dvd-navigator.md) has either begun playing or finished playing karaoke data.</span></span>

## <a name="parameters"></a><span data-ttu-id="2ffab-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ffab-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ffab-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="2ffab-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="2ffab-107">Boolescher Wert.</span><span class="sxs-lookup"><span data-stu-id="2ffab-107">Boolean value.</span></span> <span data-ttu-id="2ffab-108">**True** gibt an, dass eine Karaoke-Spur wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2ffab-108">If **TRUE**, a karaoke track is being played.</span></span> <span data-ttu-id="2ffab-109">Andernfalls wird kein Karaoke-Track abgespielt.</span><span class="sxs-lookup"><span data-stu-id="2ffab-109">Otherwise, no karaoke track is being played.</span></span>

</dd> <dt>

<span data-ttu-id="2ffab-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="2ffab-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="2ffab-111">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="2ffab-111">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2ffab-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ffab-112">Remarks</span></span>

<span data-ttu-id="2ffab-113">Der DVD-Player signalisiert dieses Ereignis, wenn die Domänen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="2ffab-113">The DVD player signals this event whenever it changes domains.</span></span>

<span data-ttu-id="2ffab-114">Dieses Ereignis wird in allen DVD-Domänen ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="2ffab-114">This event is raised in all DVD domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ffab-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ffab-115">Requirements</span></span>



| <span data-ttu-id="2ffab-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ffab-116">Requirement</span></span> | <span data-ttu-id="2ffab-117">Wert</span><span class="sxs-lookup"><span data-stu-id="2ffab-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ffab-118">Header</span><span class="sxs-lookup"><span data-stu-id="2ffab-118">Header</span></span><br/> | <dl> <span data-ttu-id="2ffab-119"><dt>Dvdevcode. h (Include DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2ffab-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ffab-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2ffab-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ffab-121">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="2ffab-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="2ffab-122">DVD-Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="2ffab-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="2ffab-123">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="2ffab-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




