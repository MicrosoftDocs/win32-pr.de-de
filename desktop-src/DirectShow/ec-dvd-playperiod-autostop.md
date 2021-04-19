---
description: Gibt an, dass der Navigator die Wiedergabe des Segments abgeschlossen hat, das in einem IDvdControl2::P layperiodintitleautoend angegeben ist.
ms.assetid: 1716eabe-f106-436a-8a6a-ca43cee9341c
title: EC_DVD_PLAYPERIOD_AUTOSTOP (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYPERIOD_AUTOSTOP
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c2081c8a5b7e5b6bd2165781af9552722ed9ddee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366965"
---
# <a name="ec_dvd_playperiod_autostop"></a><span data-ttu-id="9e33a-103">EC- \_ DVD- \_ playperiod \_ autostopps</span><span class="sxs-lookup"><span data-stu-id="9e33a-103">EC\_DVD\_PLAYPERIOD\_AUTOSTOP</span></span>

<span data-ttu-id="9e33a-104">Gibt an, dass der Navigator die Wiedergabe des Segments abgeschlossen hat, das in einem [**IDvdControl2::P layperiodintitleautoend**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playperiodintitleautostop)angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="9e33a-104">Indicates that the Navigator has finished playing the segment specified in a call to [**IDvdControl2::PlayPeriodInTitleAutoStop**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playperiodintitleautostop).</span></span>

## <a name="parameters"></a><span data-ttu-id="9e33a-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e33a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e33a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="9e33a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="9e33a-107">Keinen.</span><span class="sxs-lookup"><span data-stu-id="9e33a-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="9e33a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="9e33a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="9e33a-109">Keinen.</span><span class="sxs-lookup"><span data-stu-id="9e33a-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e33a-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e33a-110">Remarks</span></span>

<span data-ttu-id="9e33a-111">Dieses Ereignis wird in der Titel Domäne ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="9e33a-111">This event is raised in the Title domain.</span></span>

<span data-ttu-id="9e33a-112">Dieses Ereignis wird auch gesendet, wenn die Wiedergabe abgebrochen wird, bevor der Navigator die Wiedergabe des angegebenen Segments beendet.</span><span class="sxs-lookup"><span data-stu-id="9e33a-112">This event is also sent when playback is canceled before the Navigator finishes playing the specified segment.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e33a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e33a-113">Requirements</span></span>



| <span data-ttu-id="9e33a-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e33a-114">Requirement</span></span> | <span data-ttu-id="9e33a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="9e33a-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e33a-116">Header</span><span class="sxs-lookup"><span data-stu-id="9e33a-116">Header</span></span><br/> | <dl> <span data-ttu-id="9e33a-117"><dt>Dvdevcode. h (Include DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9e33a-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e33a-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e33a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e33a-119">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="9e33a-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="9e33a-120">DVD-Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="9e33a-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="9e33a-121">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="9e33a-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="9e33a-122">**IDvdControl2::P layperiodintitleautostoppt**</span><span class="sxs-lookup"><span data-stu-id="9e33a-122">**IDvdControl2::PlayPeriodInTitleAutoStop**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playperiodintitleautostop)
</dt> </dl>

 

 




