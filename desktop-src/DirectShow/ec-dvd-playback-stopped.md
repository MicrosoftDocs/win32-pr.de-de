---
description: Gibt an, dass die DVD-Wiedergabe beendet wurde. Dieses Ereignis wird gesendet, wenn ein Titel oder ein Kapitel abgeschlossen ist und der DVD-Navigator keine andere Verzweigungs Anweisung für die nachfolgende Wiedergabe findet. Das Ereignis wird nicht gesendet, wenn die Anwendung die Wiedergabe beendet.
ms.assetid: c8617307-d70e-48af-8e85-69105595aa10
title: EC_DVD_PLAYBACK_STOPPED (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYBACK_STOPPED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 2304d83aea532b764777b683c57c3bdd4d5df79a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367635"
---
# <a name="ec_dvd_playback_stopped"></a><span data-ttu-id="8997b-105">EC- \_ DVD- \_ Wiedergabe \_ beendet</span><span class="sxs-lookup"><span data-stu-id="8997b-105">EC\_DVD\_PLAYBACK\_STOPPED</span></span>

<span data-ttu-id="8997b-106">Gibt an, dass die DVD-Wiedergabe beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="8997b-106">Indicates that DVD playback has been stopped.</span></span> <span data-ttu-id="8997b-107">Dieses Ereignis wird gesendet, wenn ein Titel oder ein Kapitel abgeschlossen ist und der [DVD-Navigator](dvd-navigator-filter.md) keine andere Verzweigungs Anweisung für die nachfolgende Wiedergabe findet.</span><span class="sxs-lookup"><span data-stu-id="8997b-107">This event is sent when a title or chapter completes and the [DVD Navigator](dvd-navigator-filter.md) does not find any other branching instruction for subsequent playback.</span></span> <span data-ttu-id="8997b-108">Das Ereignis wird nicht gesendet, wenn die Anwendung die Wiedergabe beendet.</span><span class="sxs-lookup"><span data-stu-id="8997b-108">The event is not sent when the application stops playback.</span></span>

## <a name="parameters"></a><span data-ttu-id="8997b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8997b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8997b-110"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="8997b-110"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="8997b-111">Ein Member der [**DVD- \_ PB \_**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_pb_stopped) hat die Enumeration beendet und gibt an, warum die Wiedergabe beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="8997b-111">A member of the [**DVD\_PB\_STOPPED**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_pb_stopped) enumeration, indicating why playback stopped.</span></span>

</dd> <dt>

<span data-ttu-id="8997b-112"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="8997b-112"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="8997b-113">Keinen.</span><span class="sxs-lookup"><span data-stu-id="8997b-113">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8997b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8997b-114">Remarks</span></span>

<span data-ttu-id="8997b-115">Dieses Ereignis wird in allen Domänen ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="8997b-115">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="8997b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8997b-116">Requirements</span></span>



| <span data-ttu-id="8997b-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8997b-117">Requirement</span></span> | <span data-ttu-id="8997b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="8997b-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8997b-119">Header</span><span class="sxs-lookup"><span data-stu-id="8997b-119">Header</span></span><br/> | <dl> <span data-ttu-id="8997b-120"><dt>Dvdevcode. h (Include DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8997b-120"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8997b-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8997b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8997b-122">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="8997b-122">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="8997b-123">DVD-Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="8997b-123">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="8997b-124">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="8997b-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




