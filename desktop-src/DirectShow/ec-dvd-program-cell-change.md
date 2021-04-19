---
description: Wird gesendet, wenn sich die Nummer oder Zellnummer des DVD-Programms ändert.
ms.assetid: a500e86d-cd42-4716-9c57-828a72c4e1df
title: EC_DVD_PROGRAM_CELL_CHANGE (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PROGRAM_CELL_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: d41f691016c3e41cfc3e14ed1ce6fff276dcc70e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357981"
---
# <a name="ec_dvd_program_cell_change"></a><span data-ttu-id="8ef9e-103">Änderung des EC- \_ DVD- \_ Programms \_ \_</span><span class="sxs-lookup"><span data-stu-id="8ef9e-103">EC\_DVD\_PROGRAM\_CELL\_CHANGE</span></span>

<span data-ttu-id="8ef9e-104">Wird gesendet, wenn sich die Nummer oder Zellnummer des DVD-Programms ändert.</span><span class="sxs-lookup"><span data-stu-id="8ef9e-104">Sent when the DVD program number or cell number changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="8ef9e-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ef9e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ef9e-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="8ef9e-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="8ef9e-107">Die neue Programmnummer.</span><span class="sxs-lookup"><span data-stu-id="8ef9e-107">The new program number.</span></span>

</dd> <dt>

<span data-ttu-id="8ef9e-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="8ef9e-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="8ef9e-109">Die neue Zellnummer.</span><span class="sxs-lookup"><span data-stu-id="8ef9e-109">The new cell number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8ef9e-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ef9e-110">Remarks</span></span>

<span data-ttu-id="8ef9e-111">Dieses Ereignis ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="8ef9e-111">This event is disabled by default.</span></span> <span data-ttu-id="8ef9e-112">Um dieses Ereignis zu aktivieren, nennen Sie [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) , und legen Sie die Option **DVD \_ notifypositionchange** auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="8ef9e-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_NotifyPositionChange** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ef9e-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ef9e-113">Requirements</span></span>



| <span data-ttu-id="8ef9e-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ef9e-114">Requirement</span></span> | <span data-ttu-id="8ef9e-115">Wert</span><span class="sxs-lookup"><span data-stu-id="8ef9e-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ef9e-116">Header</span><span class="sxs-lookup"><span data-stu-id="8ef9e-116">Header</span></span><br/> | <dl> <span data-ttu-id="8ef9e-117"><dt>Dvdevcode. h (Include DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8ef9e-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ef9e-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ef9e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ef9e-119">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="8ef9e-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="8ef9e-120">DVD-Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="8ef9e-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="8ef9e-121">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="8ef9e-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




