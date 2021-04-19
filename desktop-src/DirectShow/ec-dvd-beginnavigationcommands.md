---
description: Wird gesendet, wenn ein Satz von DVD-Navigations Befehlen gestartet wird.
ms.assetid: 9cdcb211-a9e3-4a15-81bd-7ada2b9d823a
title: EC_DVD_BeginNavigationCommands (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_BeginNavigationCommands
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: cda904c4fcc0b1acdd16c8fc4596eef332140ec4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371475"
---
# <a name="ec_dvd_beginnavigationcommands"></a><span data-ttu-id="70df2-103">EC- \_ DVD \_ beginnavigationcommands</span><span class="sxs-lookup"><span data-stu-id="70df2-103">EC\_DVD\_BeginNavigationCommands</span></span>

<span data-ttu-id="70df2-104">Wird gesendet, wenn ein Satz von DVD-Navigations Befehlen gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="70df2-104">Sent when a set of DVD navigation commands are starting.</span></span>

## <a name="parameters"></a><span data-ttu-id="70df2-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="70df2-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70df2-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="70df2-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="70df2-107">Ein Wert aus der [**DVD \_ navcmdtype**](/windows/win32/api/strmif/ne-strmif-dvd_navcmdtype) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="70df2-107">A value from the [**DVD\_NavCmdType**](/windows/win32/api/strmif/ne-strmif-dvd_navcmdtype) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="70df2-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="70df2-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="70df2-109">Keinen.</span><span class="sxs-lookup"><span data-stu-id="70df2-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="70df2-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70df2-110">Remarks</span></span>

<span data-ttu-id="70df2-111">Dieses Ereignis ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="70df2-111">This event is disabled by default.</span></span> <span data-ttu-id="70df2-112">Um dieses Ereignis zu aktivieren, müssen Sie [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) aufrufen und die Option " **DVD \_ enableloggingevents** " auf " **true**" festlegen.</span><span class="sxs-lookup"><span data-stu-id="70df2-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="70df2-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="70df2-113">Requirements</span></span>



| <span data-ttu-id="70df2-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="70df2-114">Requirement</span></span> | <span data-ttu-id="70df2-115">Wert</span><span class="sxs-lookup"><span data-stu-id="70df2-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70df2-116">Header</span><span class="sxs-lookup"><span data-stu-id="70df2-116">Header</span></span><br/> | <dl> <span data-ttu-id="70df2-117"><dt>Dvdevcode. h (Include DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="70df2-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70df2-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70df2-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70df2-119">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="70df2-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="70df2-120">DVD-Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="70df2-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="70df2-121">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="70df2-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




