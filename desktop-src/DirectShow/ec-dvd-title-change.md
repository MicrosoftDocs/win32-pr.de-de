---
description: Gibt an, wann die aktuelle DVD-Titel Nummer geändert wird.
ms.assetid: 9888f2ec-fc2d-4d6d-a03d-b381373337eb
title: EC_DVD_TITLE_CHANGE (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_TITLE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 9539d29704797b1c7b001d426250762d2ed27b3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365961"
---
# <a name="ec_dvd_title_change"></a><span data-ttu-id="d1cba-103">Änderung des EC- \_ DVD- \_ Titels \_</span><span class="sxs-lookup"><span data-stu-id="d1cba-103">EC\_DVD\_TITLE\_CHANGE</span></span>

<span data-ttu-id="d1cba-104">Gibt an, wann die aktuelle DVD-Titel Nummer geändert wird.</span><span class="sxs-lookup"><span data-stu-id="d1cba-104">Indicates when the current DVD title number changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="d1cba-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1cba-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1cba-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="d1cba-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="d1cba-107">**DWORD** -Wert, der die neue Titel Nummer angibt.</span><span class="sxs-lookup"><span data-stu-id="d1cba-107">**DWORD** value indicating the new title number.</span></span>

</dd> <dt>

<span data-ttu-id="d1cba-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="d1cba-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="d1cba-109">Keinen.</span><span class="sxs-lookup"><span data-stu-id="d1cba-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1cba-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d1cba-110">Remarks</span></span>

<span data-ttu-id="d1cba-111">Die Titelnummern liegen zwischen 1 und 99.</span><span class="sxs-lookup"><span data-stu-id="d1cba-111">Title numbers range from 1 to 99.</span></span> <span data-ttu-id="d1cba-112">Diese Zahl gibt den TTN an, bei dem es sich um die Titel Nummer in Bezug auf die gesamte Festplatte handelt, nicht um die VTS-TTN, bei der es sich \_ um die Titel Nummer in Bezug auf einen aktuellen VTS handelt.</span><span class="sxs-lookup"><span data-stu-id="d1cba-112">This number indicates the TTN, which is the title number with respect to the whole disc, not the VTS\_TTN which is the title number with respect to just a current VTS.</span></span>

<span data-ttu-id="d1cba-113">Dieses Ereignis wird in der Titel Domäne ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="d1cba-113">This event is raised in the title domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1cba-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1cba-114">Requirements</span></span>



| <span data-ttu-id="d1cba-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1cba-115">Requirement</span></span> | <span data-ttu-id="d1cba-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d1cba-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1cba-117">Header</span><span class="sxs-lookup"><span data-stu-id="d1cba-117">Header</span></span><br/> | <dl> <span data-ttu-id="d1cba-118"><dt>Dvdevcode. h (Include DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d1cba-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1cba-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1cba-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1cba-120">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="d1cba-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="d1cba-121">DVD-Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="d1cba-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="d1cba-122">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="d1cba-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




