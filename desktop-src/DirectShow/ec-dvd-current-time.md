---
description: Signalisiert den Anfang jeder Video Object Unit (vobu), ein Video Segment, das zwischen 0,4 und 1,0 Sekunden lang ist.
ms.assetid: 1f2def2f-3a6b-458b-b564-09b6cf74543c
title: EC_DVD_CURRENT_TIME (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CURRENT_TIME
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 0f1bb2f5f31efa881917ac71ea381cc0a82e8744
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354142"
---
# <a name="ec_dvd_current_time"></a><span data-ttu-id="45d0d-103">\_ \_ aktuelle \_ Uhrzeit der EC-DVD</span><span class="sxs-lookup"><span data-stu-id="45d0d-103">EC\_DVD\_CURRENT\_TIME</span></span>

<span data-ttu-id="45d0d-104">Signalisiert den Anfang jeder Video Object Unit (vobu), ein Video Segment, das zwischen 0,4 und 1,0 Sekunden lang ist.</span><span class="sxs-lookup"><span data-stu-id="45d0d-104">Signals the beginning of every video object unit (VOBU), a video segment which is 0.4 to 1.0 seconds in length.</span></span>

## <a name="parameters"></a><span data-ttu-id="45d0d-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="45d0d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45d0d-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="45d0d-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="45d0d-107">**DWORD** -Wert, der den aktuellen Wiedergabezeit Code in einem Binärformat (Binary Coded Decimal, BCD), Minuten, Sekunden, Frames (hh: mm: SS: FF) angibt.</span><span class="sxs-lookup"><span data-stu-id="45d0d-107">**DWORD** value indicating the current playback timecode in a binary coded decimal (BCD) hours, minutes, seconds, frames (HH:MM:SS:FF) format.</span></span> <span data-ttu-id="45d0d-108">Member der [**DVD- \_ Zeit Code**](/windows/win32/api/strmif/ns-strmif-dvd_timecode) Struktur.</span><span class="sxs-lookup"><span data-stu-id="45d0d-108">Member of the [**DVD\_TIMECODE**](/windows/win32/api/strmif/ns-strmif-dvd_timecode) structure.</span></span>

</dd> <dt>

<span data-ttu-id="45d0d-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="45d0d-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="45d0d-110">Boolescher Wert (**boolescher** Wert), der den Timecode angibt.</span><span class="sxs-lookup"><span data-stu-id="45d0d-110">Boolean (**BOOL**) value indicating the timecode.</span></span> <span data-ttu-id="45d0d-111">NULL (0) gibt 25 Frames pro Sekunde an, 1 gibt 30 Frames pro Sekunde an (nicht gelöscht).</span><span class="sxs-lookup"><span data-stu-id="45d0d-111">Zero (0) indicates 25 frames per second while 1 indicates 30 frames per second (nondropped).</span></span> <span data-ttu-id="45d0d-112">Der Wert 2 gibt an, dass die Wiedergabezeit nicht bestimmt werden kann.</span><span class="sxs-lookup"><span data-stu-id="45d0d-112">A value of 2 indicates the playback time cannot be determined.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45d0d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="45d0d-113">Remarks</span></span>

<span data-ttu-id="45d0d-114">Nur einfache lineare Filme signalisieren dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="45d0d-114">Only simple linear movies signal this event.</span></span>

<span data-ttu-id="45d0d-115">Dieses Ereignis wird in der Titel Domäne ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="45d0d-115">This event is raised in the title domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="45d0d-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="45d0d-116">Requirements</span></span>



| <span data-ttu-id="45d0d-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="45d0d-117">Requirement</span></span> | <span data-ttu-id="45d0d-118">Wert</span><span class="sxs-lookup"><span data-stu-id="45d0d-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45d0d-119">Header</span><span class="sxs-lookup"><span data-stu-id="45d0d-119">Header</span></span><br/> | <dl> <span data-ttu-id="45d0d-120"><dt>Dvdevcode. h (Include DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="45d0d-120"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45d0d-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45d0d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45d0d-122">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="45d0d-122">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="45d0d-123">DVD-Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="45d0d-123">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="45d0d-124">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="45d0d-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




