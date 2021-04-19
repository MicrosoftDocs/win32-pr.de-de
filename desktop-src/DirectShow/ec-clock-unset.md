---
description: Der Takt Anbieter wurde getrennt.
ms.assetid: 0a885b7a-840d-4112-85f7-ff6f2d87bb75
title: EC_CLOCK_UNSET (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85ead35d89eee94bbffb38a96f658ccb2bb6e6e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354187"
---
# <a name="ec_clock_unset"></a><span data-ttu-id="15e78-103">\_ \_ nicht festgelegte EC-Uhr</span><span class="sxs-lookup"><span data-stu-id="15e78-103">EC\_CLOCK\_UNSET</span></span>

<span data-ttu-id="15e78-104">Der Takt Anbieter wurde getrennt.</span><span class="sxs-lookup"><span data-stu-id="15e78-104">The clock provider was disconnected.</span></span>

## <a name="parameters"></a><span data-ttu-id="15e78-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="15e78-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15e78-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="15e78-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="15e78-107">Keinen.</span><span class="sxs-lookup"><span data-stu-id="15e78-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="15e78-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="15e78-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="15e78-109">Keinen.</span><span class="sxs-lookup"><span data-stu-id="15e78-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="15e78-110">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="15e78-110">Default Action</span></span>

<span data-ttu-id="15e78-111">Der Filter Graph-Manager wählt beim nächsten Befehl zum Anhalten oder ausführen eine neue Referenzuhr aus.</span><span class="sxs-lookup"><span data-stu-id="15e78-111">The Filter Graph Manager chooses a new reference clock on the next pause or run command.</span></span> <span data-ttu-id="15e78-112">Außerdem leitet es das Ereignis an die Anwendung weiter.</span><span class="sxs-lookup"><span data-stu-id="15e78-112">It also forwards the event to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="15e78-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15e78-113">Remarks</span></span>

<span data-ttu-id="15e78-114">Ksproxy signalisiert dieses Ereignis, wenn die PIN eines von der Uhr bereitgestellten Filters getrennt wird.</span><span class="sxs-lookup"><span data-stu-id="15e78-114">KSProxy signals this event when the pin of a clock-providing filter is disconnected.</span></span>

## <a name="requirements"></a><span data-ttu-id="15e78-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15e78-115">Requirements</span></span>



| <span data-ttu-id="15e78-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15e78-116">Requirement</span></span> | <span data-ttu-id="15e78-117">Wert</span><span class="sxs-lookup"><span data-stu-id="15e78-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="15e78-118">Header</span><span class="sxs-lookup"><span data-stu-id="15e78-118">Header</span></span><br/> | <dl> <span data-ttu-id="15e78-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="15e78-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15e78-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15e78-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15e78-121">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="15e78-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="15e78-122">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="15e78-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




