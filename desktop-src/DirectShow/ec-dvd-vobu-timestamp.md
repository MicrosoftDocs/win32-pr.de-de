---
description: Wird gesendet, wenn der DVD-Navigator ein PCI-Paket analysiert.
ms.assetid: 25548c23-22f0-47cb-9062-273ad39d3007
title: EC_DVD_VOBU_Timestamp (dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VOBU_Timestamp
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 762a900a83154ce38ee00fcf4173ebc32b41cf30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364609"
---
# <a name="ec_dvd_vobu_timestamp"></a><span data-ttu-id="10bea-103">Zeitstempel für EC- \_ DVD- \_ vobu \_</span><span class="sxs-lookup"><span data-stu-id="10bea-103">EC\_DVD\_VOBU\_Timestamp</span></span>

<span data-ttu-id="10bea-104">Wird gesendet, wenn der [DVD-Navigator](dvd-navigator-filter.md) ein PCI-Paket analysiert.</span><span class="sxs-lookup"><span data-stu-id="10bea-104">Sent when the [DVD Navigator](dvd-navigator-filter.md) parses a PCI packet.</span></span>

<span data-ttu-id="10bea-105">Bei den Ereignisdaten handelt es sich um den Zeitstempel der neuesten Grafik Objekt Einheit (vobu).</span><span class="sxs-lookup"><span data-stu-id="10bea-105">The event data is the time stamp of the most recent video object unit (VOBU).</span></span>

## <a name="parameters"></a><span data-ttu-id="10bea-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="10bea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10bea-107"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="10bea-107"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="10bea-108">Enthält das **DWORD** mit niedriger Ordnung des Zeitstempels.</span><span class="sxs-lookup"><span data-stu-id="10bea-108">Contains the low-order **DWORD** of the time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="10bea-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="10bea-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="10bea-110">Enthält das höchst wertige **DWORD** des Zeitstempels.</span><span class="sxs-lookup"><span data-stu-id="10bea-110">Contains the high-order **DWORD** of the time stamp.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10bea-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10bea-111">Remarks</span></span>

<span data-ttu-id="10bea-112">Dieses Ereignis ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="10bea-112">This event is disabled by default.</span></span> <span data-ttu-id="10bea-113">Um dieses Ereignis zu aktivieren, müssen Sie [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) aufrufen und die Option " **DVD \_ enableloggingevents** " auf " **true**" festlegen.</span><span class="sxs-lookup"><span data-stu-id="10bea-113">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

<span data-ttu-id="10bea-114">Rekonstruieren Sie den Zeitstempel wie folgt:</span><span class="sxs-lookup"><span data-stu-id="10bea-114">Reconstruct the time stamp as follows:</span></span>


```C++
LARGE_INTEGER li;
li.LowPart = DWORD( lParam1 );
li.HighPart = DWORD( lParam2 );
```



## <a name="requirements"></a><span data-ttu-id="10bea-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10bea-115">Requirements</span></span>



| <span data-ttu-id="10bea-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10bea-116">Requirement</span></span> | <span data-ttu-id="10bea-117">Wert</span><span class="sxs-lookup"><span data-stu-id="10bea-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10bea-118">Header</span><span class="sxs-lookup"><span data-stu-id="10bea-118">Header</span></span><br/> | <dl> <span data-ttu-id="10bea-119"><dt>Dvdevcode. h (Include DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="10bea-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10bea-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10bea-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10bea-121">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="10bea-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="10bea-122">DVD-Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="10bea-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="10bea-123">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="10bea-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




