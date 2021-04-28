---
description: 'EC_DVD_VOBU_Offset: Wird gesendet, wenn der DVD-Navigator ein PCI-Paket analysiert.'
ms.assetid: e2e65007-7c34-4be4-86b9-9491061891e5
title: EC_DVD_VOBU_Offset (Dvdevcode.h)
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
ms.openlocfilehash: 9223f2d5bb25d7b950dba8fb19c152cf3184af93
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119768"
---
# <a name="ec_dvd_vobu_offset"></a><span data-ttu-id="71417-103">EC \_ DVD \_ VOBU \_ Offset</span><span class="sxs-lookup"><span data-stu-id="71417-103">EC\_DVD\_VOBU\_Offset</span></span>

<span data-ttu-id="71417-104">Wird gesendet, wenn [der DVD-Navigator](dvd-navigator-filter.md) ein PCI-Paket analysiert.</span><span class="sxs-lookup"><span data-stu-id="71417-104">Sent when the [DVD Navigator](dvd-navigator-filter.md) parses a PCI packet.</span></span>

## <a name="parameters"></a><span data-ttu-id="71417-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="71417-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71417-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="71417-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="71417-107">Der Blockoffset der letzten Videoobjekteinheit (VOBU).</span><span class="sxs-lookup"><span data-stu-id="71417-107">The block offset of the most recent video object unit (VOBU).</span></span>

</dd> <dt>

<span data-ttu-id="71417-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="71417-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="71417-109">Die aktuelle Anzahl von Videotiteln (VTSN).</span><span class="sxs-lookup"><span data-stu-id="71417-109">The current video title set number (VTSN).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="71417-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="71417-110">Remarks</span></span>

<span data-ttu-id="71417-111">Dieses Ereignis ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="71417-111">This event is disabled by default.</span></span> <span data-ttu-id="71417-112">Um dieses Ereignis zu aktivieren, rufen Sie [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) auf, und legen Sie die **Option DVD \_ EnableLoggingEvents** auf **TRUE fest.**</span><span class="sxs-lookup"><span data-stu-id="71417-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="71417-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71417-113">Requirements</span></span>



| <span data-ttu-id="71417-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71417-114">Requirement</span></span> | <span data-ttu-id="71417-115">Wert</span><span class="sxs-lookup"><span data-stu-id="71417-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71417-116">Header</span><span class="sxs-lookup"><span data-stu-id="71417-116">Header</span></span><br/> | <dl> <span data-ttu-id="71417-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span><span class="sxs-lookup"><span data-stu-id="71417-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71417-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="71417-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71417-119">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="71417-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="71417-120">DVD-Ereignisbenachrichtigungscodes</span><span class="sxs-lookup"><span data-stu-id="71417-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="71417-121">Ereignisbenachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="71417-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




