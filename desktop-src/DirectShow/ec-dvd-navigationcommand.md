---
description: Wird gesendet, wenn der DVD-Navigator einen DVD-Navigations Befehl verarbeitet.
ms.assetid: 95e502b6-330f-4bc7-8adc-851913987370
title: EC_DVD_NavigationCommand (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_NavigationCommand
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: e81dbf108868cbaec4c44a436f2c8271bb5f282a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370629"
---
# <a name="ec_dvd_navigationcommand"></a><span data-ttu-id="c7173-103">EC \_ DVD \_ navigationcommand</span><span class="sxs-lookup"><span data-stu-id="c7173-103">EC\_DVD\_NavigationCommand</span></span>

<span data-ttu-id="c7173-104">Wird gesendet, wenn der [DVD-Navigator](dvd-navigator-filter.md) einen DVD-Navigations Befehl verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="c7173-104">Sent when the [DVD Navigator](dvd-navigator-filter.md) processes a DVD navigation command.</span></span>

## <a name="parameters"></a><span data-ttu-id="c7173-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7173-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7173-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="c7173-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="c7173-107">Die unteren 32 Bits des rohnavigations Befehls.</span><span class="sxs-lookup"><span data-stu-id="c7173-107">The lower 32 bits of the raw navigation command.</span></span>

</dd> <dt>

<span data-ttu-id="c7173-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="c7173-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="c7173-109">Die oberen 32 Bits des rohnavigations Befehls.</span><span class="sxs-lookup"><span data-stu-id="c7173-109">The upper 32 bits of the raw navigation command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7173-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7173-110">Remarks</span></span>

<span data-ttu-id="c7173-111">Dieses Ereignis ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c7173-111">This event is disabled by default.</span></span> <span data-ttu-id="c7173-112">Um dieses Ereignis zu aktivieren, müssen Sie [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) aufrufen und die Option " **DVD \_ enableloggingevents** " auf " **true**" festlegen.</span><span class="sxs-lookup"><span data-stu-id="c7173-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7173-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7173-113">Requirements</span></span>



| <span data-ttu-id="c7173-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7173-114">Requirement</span></span> | <span data-ttu-id="c7173-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c7173-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7173-116">Header</span><span class="sxs-lookup"><span data-stu-id="c7173-116">Header</span></span><br/> | <dl> <span data-ttu-id="c7173-117"><dt>Dvdevcode. h (Include DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c7173-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7173-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7173-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7173-119">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="c7173-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="c7173-120">DVD-Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="c7173-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="c7173-121">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="c7173-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




