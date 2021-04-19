---
description: Wird von einer streamsenke gesendet, wenn das downstreamformat ungültig geworden ist und erneut ausgehandelt werden muss.
ms.assetid: 732B3BDD-F394-430F-B895-AF18ED61114D
title: Mestreamsinkformatinvalidate-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39c4453c0d5720ffb57f1277946f9cf891ed443
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348441"
---
# <a name="mestreamsinkformatinvalidated-event"></a><span data-ttu-id="8bfdf-103">Mestreamsinkformatinvalidate-Ereignis</span><span class="sxs-lookup"><span data-stu-id="8bfdf-103">MEStreamSinkFormatInvalidated event</span></span>

<span data-ttu-id="8bfdf-104">Wird von einer streamsenke gesendet, wenn das downstreamformat ungültig geworden ist und erneut ausgehandelt werden muss.</span><span class="sxs-lookup"><span data-stu-id="8bfdf-104">Sent by a stream sink when the downstream format has become invalidated and it needs to be renegotiated.</span></span>

## <a name="event-values"></a><span data-ttu-id="8bfdf-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="8bfdf-105">Event values</span></span>

<span data-ttu-id="8bfdf-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="8bfdf-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="8bfdf-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="8bfdf-107">VARTYPE</span></span>              | <span data-ttu-id="8bfdf-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8bfdf-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="8bfdf-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="8bfdf-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="8bfdf-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="8bfdf-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="8bfdf-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8bfdf-111">Remarks</span></span>

<span data-ttu-id="8bfdf-112">Daten, die in der Senke in der Warteschlange nach der aktuellen Wiedergabe Position eingereiht wurden, sollten erneut gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="8bfdf-112">Data that was queued to the sink, past the current playback position, should be resent.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bfdf-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8bfdf-113">Requirements</span></span>



| <span data-ttu-id="8bfdf-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8bfdf-114">Requirement</span></span> | <span data-ttu-id="8bfdf-115">Wert</span><span class="sxs-lookup"><span data-stu-id="8bfdf-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bfdf-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8bfdf-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8bfdf-117">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="8bfdf-117">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                                      |
| <span data-ttu-id="8bfdf-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8bfdf-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8bfdf-119">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="8bfdf-119">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                                           |
| <span data-ttu-id="8bfdf-120">Header</span><span class="sxs-lookup"><span data-stu-id="8bfdf-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bfdf-121"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8bfdf-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bfdf-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8bfdf-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bfdf-123">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8bfdf-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




