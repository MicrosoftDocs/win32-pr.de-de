---
description: Wird von einer streamsenke ausgelöst, wenn sich die Rate geändert hat.
ms.assetid: c61c71de-fd3c-429b-a29f-f9d2bbfcb531
title: Mestreamsinkratechanged-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a26adbdb64ffd5af0896d8aebe0cef474bee9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349359"
---
# <a name="mestreamsinkratechanged-event"></a><span data-ttu-id="d168f-103">Mestreamsinkratechanged-Ereignis</span><span class="sxs-lookup"><span data-stu-id="d168f-103">MEStreamSinkRateChanged event</span></span>

<span data-ttu-id="d168f-104">Wird von einer streamsenke ausgelöst, wenn sich die Rate geändert hat.</span><span class="sxs-lookup"><span data-stu-id="d168f-104">Raised by a stream sink when the rate has changed.</span></span>

## <a name="event-values"></a><span data-ttu-id="d168f-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="d168f-105">Event values</span></span>

<span data-ttu-id="d168f-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="d168f-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="d168f-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="d168f-107">VARTYPE</span></span>              | <span data-ttu-id="d168f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d168f-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="d168f-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="d168f-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="d168f-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="d168f-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="d168f-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d168f-111">Remarks</span></span>

<span data-ttu-id="d168f-112">Wenn eine streamsenke Raten Änderungen unterstützt, sendet Sie dieses Ereignis, nachdem die Raten Änderung durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="d168f-112">If a stream sink supports rate changes, it sends this event after the rate change is complete.</span></span> <span data-ttu-id="d168f-113">Das Ereignis wird einmal für jeden Aufrufe der [**imfclockstaatink:: onclockertrate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) -Methode der Senke gesendet.</span><span class="sxs-lookup"><span data-stu-id="d168f-113">The event is sent once for each call to the sink's [**IMFClockStateSink::OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) method.</span></span> <span data-ttu-id="d168f-114">Wenn die Raten Änderung nicht erfolgreich ist, ist der Ereignis Statuswert ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="d168f-114">If the rate change is not successful, the event status value is an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d168f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d168f-115">Requirements</span></span>



| <span data-ttu-id="d168f-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d168f-116">Requirement</span></span> | <span data-ttu-id="d168f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="d168f-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d168f-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d168f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d168f-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d168f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d168f-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d168f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d168f-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d168f-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d168f-122">Header</span><span class="sxs-lookup"><span data-stu-id="d168f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d168f-123"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d168f-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d168f-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d168f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d168f-125">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d168f-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="d168f-126">Medien senken</span><span class="sxs-lookup"><span data-stu-id="d168f-126">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




