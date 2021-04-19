---
description: Signalisiert, dass ein DVD-Laufwerk ausworfen wurde.
ms.assetid: 031156c2-f0f0-4a9e-b792-4d656ec49aef
title: EC_DVD_DISC_EJECTED (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_DISC_EJECTED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: ab6c1333245b589d4f13bafcba89eada3ef98ab0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358062"
---
# <a name="ec_dvd_disc_ejected"></a><span data-ttu-id="a1f0f-103">EC- \_ DVD- \_ CD- \_ aussteht</span><span class="sxs-lookup"><span data-stu-id="a1f0f-103">EC\_DVD\_DISC\_EJECTED</span></span>

<span data-ttu-id="a1f0f-104">Signalisiert, dass ein DVD-Laufwerk ausworfen wurde.</span><span class="sxs-lookup"><span data-stu-id="a1f0f-104">Signals that a DVD disc was ejected.</span></span>

## <a name="parameters"></a><span data-ttu-id="a1f0f-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1f0f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1f0f-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="a1f0f-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="a1f0f-107">Keinen.</span><span class="sxs-lookup"><span data-stu-id="a1f0f-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="a1f0f-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="a1f0f-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="a1f0f-109">Keinen.</span><span class="sxs-lookup"><span data-stu-id="a1f0f-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a1f0f-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1f0f-110">Remarks</span></span>

<span data-ttu-id="a1f0f-111">Die Wiedergabe wird automatisch beendet, wenn ein Laufwerk aussteht.</span><span class="sxs-lookup"><span data-stu-id="a1f0f-111">Playback automatically stops when a disc is ejected.</span></span> <span data-ttu-id="a1f0f-112">Die Anwendung muss als Reaktion auf dieses Ereignis keine besonderen Aktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="a1f0f-112">The application does not have to take any special action in response to this event.</span></span>

<span data-ttu-id="a1f0f-113">Dieses Ereignis wird in allen Domänen ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="a1f0f-113">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1f0f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1f0f-114">Requirements</span></span>



| <span data-ttu-id="a1f0f-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1f0f-115">Requirement</span></span> | <span data-ttu-id="a1f0f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a1f0f-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1f0f-117">Header</span><span class="sxs-lookup"><span data-stu-id="a1f0f-117">Header</span></span><br/> | <dl> <span data-ttu-id="a1f0f-118"><dt>Dvdevcode. h (Include DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a1f0f-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1f0f-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1f0f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1f0f-120">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="a1f0f-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="a1f0f-121">DVD-Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="a1f0f-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="a1f0f-122">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="a1f0f-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




