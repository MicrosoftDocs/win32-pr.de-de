---
description: Wird gesendet, wenn sich der aktuelle Video Titel Satz (VTS) ändert.
ms.assetid: 7b8849c8-c71e-44d6-b33a-8e80247bdb22
title: EC_DVD_TITLE_SET_CHANGE (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_TITLE_SET_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c5685cfb909a7fa24c39dff969076269845a663e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366964"
---
# <a name="ec_dvd_title_set_change"></a><span data-ttu-id="a0876-103">\_Änderung der \_ Titel \_ Gruppe \_ für EC-DVD</span><span class="sxs-lookup"><span data-stu-id="a0876-103">EC\_DVD\_TITLE\_SET\_CHANGE</span></span>

<span data-ttu-id="a0876-104">Wird gesendet, wenn sich der aktuelle Video Titel Satz (VTS) ändert.</span><span class="sxs-lookup"><span data-stu-id="a0876-104">Sent when current Video Title Set (VTS) changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="a0876-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0876-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0876-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="a0876-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="a0876-107">Die neue Video Titel Satz Nummer (VTN).</span><span class="sxs-lookup"><span data-stu-id="a0876-107">The new Video Title Set Number (VTSN).</span></span>

</dd> <dt>

<span data-ttu-id="a0876-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="a0876-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="a0876-109">Keinen.</span><span class="sxs-lookup"><span data-stu-id="a0876-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a0876-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a0876-110">Remarks</span></span>

<span data-ttu-id="a0876-111">Dieses Ereignis ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a0876-111">This event is disabled by default.</span></span> <span data-ttu-id="a0876-112">Um dieses Ereignis zu aktivieren, nennen Sie [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) , und legen Sie die Option **DVD \_ notifypositionchange** auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="a0876-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_NotifyPositionChange** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0876-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0876-113">Requirements</span></span>



| <span data-ttu-id="a0876-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0876-114">Requirement</span></span> | <span data-ttu-id="a0876-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a0876-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0876-116">Header</span><span class="sxs-lookup"><span data-stu-id="a0876-116">Header</span></span><br/> | <dl> <span data-ttu-id="a0876-117"><dt>Dvdevcode. h (Include DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0876-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0876-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0876-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0876-119">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="a0876-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="a0876-120">DVD-Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="a0876-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="a0876-121">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="a0876-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




