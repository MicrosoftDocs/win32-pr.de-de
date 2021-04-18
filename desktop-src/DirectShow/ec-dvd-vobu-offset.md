---
description: Wird gesendet, wenn der DVD-Navigator ein PCI-Paket analysiert.
ms.assetid: e2e65007-7c34-4be4-86b9-9491061891e5
title: EC_DVD_VOBU_Offset (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VOBU_Offset
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 531207d4d8b0debb29dd5d02e01e400218e4a2bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357567"
---
# <a name="ec_dvd_vobu_offset"></a><span data-ttu-id="94856-103">EC- \_ DVD- \_ vobu- \_ Offset</span><span class="sxs-lookup"><span data-stu-id="94856-103">EC\_DVD\_VOBU\_Offset</span></span>

<span data-ttu-id="94856-104">Wird gesendet, wenn der [DVD-Navigator](dvd-navigator-filter.md) ein PCI-Paket analysiert.</span><span class="sxs-lookup"><span data-stu-id="94856-104">Sent when the [DVD Navigator](dvd-navigator-filter.md) parses a PCI packet.</span></span>

## <a name="parameters"></a><span data-ttu-id="94856-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="94856-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94856-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="94856-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="94856-107">Der Block Offset der letzten Video Object Unit (vobu).</span><span class="sxs-lookup"><span data-stu-id="94856-107">The block offset of the most recent video object unit (VOBU).</span></span>

</dd> <dt>

<span data-ttu-id="94856-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="94856-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="94856-109">Die aktuelle Videotitel Satz Nummer (VTN).</span><span class="sxs-lookup"><span data-stu-id="94856-109">The current video title set number (VTSN).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94856-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94856-110">Remarks</span></span>

<span data-ttu-id="94856-111">Dieses Ereignis ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="94856-111">This event is disabled by default.</span></span> <span data-ttu-id="94856-112">Um dieses Ereignis zu aktivieren, müssen Sie [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) aufrufen und die Option " **DVD \_ enableloggingevents** " auf " **true**" festlegen.</span><span class="sxs-lookup"><span data-stu-id="94856-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="94856-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94856-113">Requirements</span></span>



| <span data-ttu-id="94856-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94856-114">Requirement</span></span> | <span data-ttu-id="94856-115">Wert</span><span class="sxs-lookup"><span data-stu-id="94856-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94856-116">Header</span><span class="sxs-lookup"><span data-stu-id="94856-116">Header</span></span><br/> | <dl> <span data-ttu-id="94856-117"><dt>Dvdevcode. h (Include DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="94856-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94856-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94856-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94856-119">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="94856-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="94856-120">DVD-Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="94856-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="94856-121">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="94856-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




