---
description: Wird gesendet, wenn sich die aktuelle Programm Kette (PGC) ändert.
ms.assetid: 80fcd059-6ab4-4116-ac3a-012c451237b3
title: EC_DVD_PROGRAM_CHAIN_CHANGE (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PROGRAM_CHAIN_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: eefd45ac1d147a0409417f215e56a4db490dfdbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368359"
---
# <a name="ec_dvd_program_chain_change"></a><span data-ttu-id="ff3d1-103">Änderung der EC- \_ DVD- \_ Programm \_ Kette \_</span><span class="sxs-lookup"><span data-stu-id="ff3d1-103">EC\_DVD\_PROGRAM\_CHAIN\_CHANGE</span></span>

<span data-ttu-id="ff3d1-104">Wird gesendet, wenn sich die aktuelle Programm Kette (PGC) ändert.</span><span class="sxs-lookup"><span data-stu-id="ff3d1-104">Sent when current program chain (PGC) changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="ff3d1-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff3d1-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff3d1-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="ff3d1-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="ff3d1-107">Die neue Programm Ketten Nummer (pgcn).</span><span class="sxs-lookup"><span data-stu-id="ff3d1-107">The new program chain number (PGCN).</span></span>

</dd> <dt>

<span data-ttu-id="ff3d1-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="ff3d1-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="ff3d1-109">Der Gebiets Schema Bezeichner (Locale Identifier, LCID) der Audiosprache.</span><span class="sxs-lookup"><span data-stu-id="ff3d1-109">The locale identifier (LCID) of the audio language.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ff3d1-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff3d1-110">Remarks</span></span>

<span data-ttu-id="ff3d1-111">Dieses Ereignis ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ff3d1-111">This event is disabled by default.</span></span> <span data-ttu-id="ff3d1-112">Um dieses Ereignis zu aktivieren, nennen Sie [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) , und legen Sie die Option **DVD \_ notifypositionchange** auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="ff3d1-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_NotifyPositionChange** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff3d1-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff3d1-113">Requirements</span></span>



| <span data-ttu-id="ff3d1-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ff3d1-114">Requirement</span></span> | <span data-ttu-id="ff3d1-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ff3d1-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff3d1-116">Header</span><span class="sxs-lookup"><span data-stu-id="ff3d1-116">Header</span></span><br/> | <dl> <span data-ttu-id="ff3d1-117"><dt>Dvdevcode. h (Include DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ff3d1-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff3d1-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff3d1-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff3d1-119">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="ff3d1-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="ff3d1-120">DVD-Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="ff3d1-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="ff3d1-121">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="ff3d1-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




