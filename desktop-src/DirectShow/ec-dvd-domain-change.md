---
description: Gibt die neue Domäne des DVD-Players an.
ms.assetid: 4faa46d6-2ba2-44a3-b237-acac3b32f8b1
title: EC_DVD_DOMAIN_CHANGE (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_DOMAIN_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 815b6b2dd318d0b7716f4cf640ef3f83dacd0d60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368360"
---
# <a name="ec_dvd_domain_change"></a><span data-ttu-id="b1414-103">Änderung der EC- \_ DVD- \_ Domäne \_</span><span class="sxs-lookup"><span data-stu-id="b1414-103">EC\_DVD\_DOMAIN\_CHANGE</span></span>

<span data-ttu-id="b1414-104">Gibt die neue Domäne des DVD-Players an.</span><span class="sxs-lookup"><span data-stu-id="b1414-104">Indicates the DVD player's new domain.</span></span>

## <a name="parameters"></a><span data-ttu-id="b1414-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1414-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1414-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="b1414-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="b1414-107">**DWORD** -Wert, der die neue Domäne angibt.</span><span class="sxs-lookup"><span data-stu-id="b1414-107">**DWORD** value indicating the new domain.</span></span> <span data-ttu-id="b1414-108">Member des enumerierten Datentyps der [**DVD- \_ Domäne**](/windows/win32/api/strmif/ne-strmif-dvd_domain) .</span><span class="sxs-lookup"><span data-stu-id="b1414-108">Member of the [**DVD\_DOMAIN**](/windows/win32/api/strmif/ne-strmif-dvd_domain) enumerated data type.</span></span>

</dd> <dt>

<span data-ttu-id="b1414-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="b1414-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="b1414-110">Keinen.</span><span class="sxs-lookup"><span data-stu-id="b1414-110">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b1414-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1414-111">Remarks</span></span>

<span data-ttu-id="b1414-112">Der DVD-Player signalisiert dieses Ereignis, wenn die Domänen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="b1414-112">The DVD player signals this event whenever it changes domains.</span></span>

<span data-ttu-id="b1414-113">Dieses Ereignis wird in allen DVD-Domänen ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="b1414-113">This event is raised in all DVD domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1414-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1414-114">Requirements</span></span>



| <span data-ttu-id="b1414-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1414-115">Requirement</span></span> | <span data-ttu-id="b1414-116">Wert</span><span class="sxs-lookup"><span data-stu-id="b1414-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1414-117">Header</span><span class="sxs-lookup"><span data-stu-id="b1414-117">Header</span></span><br/> | <dl> <span data-ttu-id="b1414-118"><dt>Dvdevcode. h (Include DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b1414-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1414-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1414-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1414-120">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="b1414-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="b1414-121">DVD-Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="b1414-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="b1414-122">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="b1414-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




