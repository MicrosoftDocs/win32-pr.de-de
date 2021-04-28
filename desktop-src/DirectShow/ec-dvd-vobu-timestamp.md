---
description: 'EC_DVD_VOBU_Timestamp: Wird gesendet, wenn der DVD-Navigator ein PCI-Paket analysiert.'
ms.assetid: 25548c23-22f0-47cb-9062-273ad39d3007
title: EC_DVD_VOBU_Timestamp (Dvdevcode.h)
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
ms.openlocfilehash: 6bd06eb99cae60960db64a6f32df5e4c932b362f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094618"
---
# <a name="ec_dvd_vobu_timestamp"></a><span data-ttu-id="f4912-103">EC \_ DVD \_ VOBU \_ Timestamp</span><span class="sxs-lookup"><span data-stu-id="f4912-103">EC\_DVD\_VOBU\_Timestamp</span></span>

<span data-ttu-id="f4912-104">Wird gesendet, wenn [der DVD-Navigator](dvd-navigator-filter.md) ein PCI-Paket analysiert.</span><span class="sxs-lookup"><span data-stu-id="f4912-104">Sent when the [DVD Navigator](dvd-navigator-filter.md) parses a PCI packet.</span></span>

<span data-ttu-id="f4912-105">Die Ereignisdaten sind der Zeitstempel der letzten Videoobjekteinheit (VOBU).</span><span class="sxs-lookup"><span data-stu-id="f4912-105">The event data is the time stamp of the most recent video object unit (VOBU).</span></span>

## <a name="parameters"></a><span data-ttu-id="f4912-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4912-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4912-107"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="f4912-107"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="f4912-108">Enthält das **low-order-DWORD** des Zeitstempels.</span><span class="sxs-lookup"><span data-stu-id="f4912-108">Contains the low-order **DWORD** of the time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="f4912-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="f4912-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="f4912-110">Enthält das obere **DWORD des** Zeitstempels.</span><span class="sxs-lookup"><span data-stu-id="f4912-110">Contains the high-order **DWORD** of the time stamp.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4912-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4912-111">Remarks</span></span>

<span data-ttu-id="f4912-112">Dieses Ereignis ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="f4912-112">This event is disabled by default.</span></span> <span data-ttu-id="f4912-113">Um dieses Ereignis zu aktivieren, rufen Sie [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) auf, und legen Sie die **Option DVD \_ EnableLoggingEvents** auf **TRUE fest.**</span><span class="sxs-lookup"><span data-stu-id="f4912-113">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

<span data-ttu-id="f4912-114">Rekonstruieren Sie den Zeitstempel wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f4912-114">Reconstruct the time stamp as follows:</span></span>


```C++
LARGE_INTEGER li;
li.LowPart = DWORD( lParam1 );
li.HighPart = DWORD( lParam2 );
```



## <a name="requirements"></a><span data-ttu-id="f4912-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4912-115">Requirements</span></span>



| <span data-ttu-id="f4912-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4912-116">Requirement</span></span> | <span data-ttu-id="f4912-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f4912-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4912-118">Header</span><span class="sxs-lookup"><span data-stu-id="f4912-118">Header</span></span><br/> | <dl> <span data-ttu-id="f4912-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span><span class="sxs-lookup"><span data-stu-id="f4912-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4912-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f4912-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4912-121">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="f4912-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="f4912-122">DVD-Ereignisbenachrichtigungscodes</span><span class="sxs-lookup"><span data-stu-id="f4912-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="f4912-123">Ereignisbenachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="f4912-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




