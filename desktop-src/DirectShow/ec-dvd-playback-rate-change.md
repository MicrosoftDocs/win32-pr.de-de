---
description: Signalisiert, dass eine Änderungs Rate bei der DVD-Wiedergabe initiiert wurde.
ms.assetid: 2a1e3c21-1623-4e43-8c7b-1a34514442c9
title: EC_DVD_PLAYBACK_RATE_CHANGE (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYBACK_RATE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 20ddc41fd70906fabc522daa4dcb7714b71e4251
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366007"
---
# <a name="ec_dvd_playback_rate_change"></a><span data-ttu-id="8b1ce-103">Änderung der EC- \_ DVD- \_ Wiedergabe \_ Rate \_</span><span class="sxs-lookup"><span data-stu-id="8b1ce-103">EC\_DVD\_PLAYBACK\_RATE\_CHANGE</span></span>

<span data-ttu-id="8b1ce-104">Signalisiert, dass eine Änderungs Rate bei der DVD-Wiedergabe initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="8b1ce-104">Signals that a rate change in DVD playback has been initiated.</span></span>

## <a name="parameters"></a><span data-ttu-id="8b1ce-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b1ce-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b1ce-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="8b1ce-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="8b1ce-107">Lange Angabe der neuen Wiedergabe Rate.</span><span class="sxs-lookup"><span data-stu-id="8b1ce-107">LONG indicating the new playback rate.</span></span> <span data-ttu-id="8b1ce-108">Der Wert ist die tatsächliche Wiedergabe Rate multipliziert mit 10.000, sodass die Wiedergabe Rate 10000,0/ *lParam1* entspricht.</span><span class="sxs-lookup"><span data-stu-id="8b1ce-108">The value is the actual playback rate multiplied by 10,000, so the playback rate equals 10000.0 / *lParam1*.</span></span> <span data-ttu-id="8b1ce-109">Werte kleiner als 0 (null) geben den umgekehrten Wiedergabemodus an, und Werte größer als 0 (null) geben den vorwärts Wiedergabemodus</span><span class="sxs-lookup"><span data-stu-id="8b1ce-109">Values less than zero indicate reverse playback mode, and values greater than zero indicate forward playback mode.</span></span>

</dd> <dt>

<span data-ttu-id="8b1ce-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="8b1ce-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="8b1ce-111">Keinen.</span><span class="sxs-lookup"><span data-stu-id="8b1ce-111">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b1ce-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b1ce-112">Remarks</span></span>

<span data-ttu-id="8b1ce-113">Dieses Ereignis wird in der Titel Domäne ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="8b1ce-113">This event is raised in the title domain.</span></span>

<span data-ttu-id="8b1ce-114">Die Wiedergabe *Rate* ist die Umkehrung der Wiedergabe *Geschwindigkeit*.</span><span class="sxs-lookup"><span data-stu-id="8b1ce-114">Playback *rate* is the inverse of playback *speed*.</span></span> <span data-ttu-id="8b1ce-115">Wenn die Wiedergabegeschwindigkeit beispielsweise 2 x beträgt, ist die Rate 0,5.</span><span class="sxs-lookup"><span data-stu-id="8b1ce-115">For example, if playback speed is 2x, the rate is 0.5.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b1ce-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b1ce-116">Requirements</span></span>



| <span data-ttu-id="8b1ce-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b1ce-117">Requirement</span></span> | <span data-ttu-id="8b1ce-118">Wert</span><span class="sxs-lookup"><span data-stu-id="8b1ce-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b1ce-119">Header</span><span class="sxs-lookup"><span data-stu-id="8b1ce-119">Header</span></span><br/> | <dl> <span data-ttu-id="8b1ce-120"><dt>Dvdevcode. h (Include DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8b1ce-120"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b1ce-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b1ce-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b1ce-122">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="8b1ce-122">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="8b1ce-123">DVD-Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="8b1ce-123">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="8b1ce-124">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="8b1ce-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




