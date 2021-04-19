---
description: Signalisiert, dass der DVD-Player die Wiedergabe eines neuen Programms in der DVD- \_ Domänen \_ Titel Domäne gestartet hat.
ms.assetid: c0745615-d527-4d93-9118-30419c6c811e
title: EC_DVD_CHAPTER_START (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CHAPTER_START
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 87a4408f1631d8a23cf42e790688856d6c246393
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354044"
---
# <a name="ec_dvd_chapter_start"></a><span data-ttu-id="872f3-103">EC- \_ DVD- \_ Kapitel \_ Start</span><span class="sxs-lookup"><span data-stu-id="872f3-103">EC\_DVD\_CHAPTER\_START</span></span>

<span data-ttu-id="872f3-104">Signalisiert, dass der DVD-Player die Wiedergabe eines neuen Programms in der DVD- \_ Domänen \_ Titel Domäne gestartet hat.</span><span class="sxs-lookup"><span data-stu-id="872f3-104">Signals that the DVD player started playback of a new program in the DVD\_DOMAIN\_Title domain.</span></span>

## <a name="parameters"></a><span data-ttu-id="872f3-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="872f3-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="872f3-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="872f3-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="872f3-107">**DWORD** -Wert, der die neue Kapitel Nummer (Programm) angibt.</span><span class="sxs-lookup"><span data-stu-id="872f3-107">**DWORD** value indicating the new chapter (program) number.</span></span>

</dd> <dt>

<span data-ttu-id="872f3-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="872f3-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="872f3-109">Keinen.</span><span class="sxs-lookup"><span data-stu-id="872f3-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="872f3-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="872f3-110">Remarks</span></span>

<span data-ttu-id="872f3-111">Nur einfache lineare Filme signalisieren dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="872f3-111">Only simple linear movies signal this event.</span></span>

<span data-ttu-id="872f3-112">Dieses Ereignis wird in der Titel Domäne ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="872f3-112">This event is raised in the title domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="872f3-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="872f3-113">Requirements</span></span>



| <span data-ttu-id="872f3-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="872f3-114">Requirement</span></span> | <span data-ttu-id="872f3-115">Wert</span><span class="sxs-lookup"><span data-stu-id="872f3-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="872f3-116">Header</span><span class="sxs-lookup"><span data-stu-id="872f3-116">Header</span></span><br/> | <dl> <span data-ttu-id="872f3-117"><dt>Dvdevcode. h (Include DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="872f3-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="872f3-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="872f3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="872f3-119">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="872f3-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="872f3-120">DVD-Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="872f3-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="872f3-121">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="872f3-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="872f3-122">**DVD- \_ Domänen Enumeration**</span><span class="sxs-lookup"><span data-stu-id="872f3-122">**DVD\_DOMAIN Enumeration**</span></span>](/windows/win32/api/strmif/ne-strmif-dvd_domain)
</dt> </dl>

 

 




