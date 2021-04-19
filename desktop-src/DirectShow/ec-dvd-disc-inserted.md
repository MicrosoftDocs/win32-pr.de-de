---
description: Signalisiert, dass eine DVD-CD in das Laufwerk eingefügt wurde.
ms.assetid: ce233c94-2eae-457c-919b-7c4d8334979a
title: EC_DVD_DISC_INSERTED (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_DISC_INSERTED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c98d32960e2ab6a21633899164b3ff84525f2aaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370059"
---
# <a name="ec_dvd_disc_inserted"></a><span data-ttu-id="d1364-103">EC- \_ DVD- \_ CD \_ eingefügt</span><span class="sxs-lookup"><span data-stu-id="d1364-103">EC\_DVD\_DISC\_INSERTED</span></span>

<span data-ttu-id="d1364-104">Signalisiert, dass eine DVD-CD in das Laufwerk eingefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="d1364-104">Signals that a DVD disc was inserted into the drive.</span></span>

## <a name="parameters"></a><span data-ttu-id="d1364-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1364-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1364-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="d1364-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="d1364-107">Keinen.</span><span class="sxs-lookup"><span data-stu-id="d1364-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="d1364-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="d1364-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="d1364-109">Keinen.</span><span class="sxs-lookup"><span data-stu-id="d1364-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1364-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d1364-110">Remarks</span></span>

<span data-ttu-id="d1364-111">Die Wiedergabe beginnt automatisch, wenn ein Laufwerk eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="d1364-111">Playback automatically begins when a disc is inserted.</span></span> <span data-ttu-id="d1364-112">Die Anwendung muss als Reaktion auf dieses Ereignis keine besonderen Aktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="d1364-112">The application does not have to take any special action in response to this event.</span></span>

<span data-ttu-id="d1364-113">Dieses Ereignis wird in allen Domänen ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="d1364-113">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1364-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1364-114">Requirements</span></span>



| <span data-ttu-id="d1364-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1364-115">Requirement</span></span> | <span data-ttu-id="d1364-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d1364-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1364-117">Header</span><span class="sxs-lookup"><span data-stu-id="d1364-117">Header</span></span><br/> | <dl> <span data-ttu-id="d1364-118"><dt>Dvdevcode. h (Include DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d1364-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1364-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1364-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1364-120">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="d1364-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="d1364-121">DVD-Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="d1364-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="d1364-122">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="d1364-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




