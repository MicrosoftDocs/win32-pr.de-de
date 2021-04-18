---
description: Wird von einer streamsenke ausgelöst, um ein neues Medien Beispiel aus der Pipeline anzufordern.
ms.assetid: 35020a15-942f-4dd0-9ca4-815affdacecf
title: Mestreamsinkrequestsample-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1c5afbfa9f0cfe4b320b451e699612a4729c23a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343405"
---
# <a name="mestreamsinkrequestsample-event"></a><span data-ttu-id="598b4-103">Mestreamsinkrequestsample-Ereignis</span><span class="sxs-lookup"><span data-stu-id="598b4-103">MEStreamSinkRequestSample event</span></span>

<span data-ttu-id="598b4-104">Wird von einer streamsenke ausgelöst, um ein neues Medien Beispiel aus der Pipeline anzufordern.</span><span class="sxs-lookup"><span data-stu-id="598b4-104">Raised by a stream sink to request a new media sample from the pipeline.</span></span> <span data-ttu-id="598b4-105">Für jedes mestreamsinkrequestsample-Ereignis fordert die Pipeline Daten von der nächsten Upstreamkomponente an.</span><span class="sxs-lookup"><span data-stu-id="598b4-105">For each MEStreamSinkRequestSample event, the pipeline requests data from the next upstream component.</span></span>

## <a name="event-values"></a><span data-ttu-id="598b4-106">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="598b4-106">Event values</span></span>

<span data-ttu-id="598b4-107">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="598b4-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="598b4-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="598b4-108">VARTYPE</span></span>              | <span data-ttu-id="598b4-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="598b4-109">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="598b4-110">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="598b4-110">VT\_EMPTY</span></span><br/> | <span data-ttu-id="598b4-111">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="598b4-111">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="598b4-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="598b4-112">Requirements</span></span>



| <span data-ttu-id="598b4-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="598b4-113">Requirement</span></span> | <span data-ttu-id="598b4-114">Wert</span><span class="sxs-lookup"><span data-stu-id="598b4-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="598b4-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="598b4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="598b4-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="598b4-116">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="598b4-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="598b4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="598b4-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="598b4-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="598b4-119">Header</span><span class="sxs-lookup"><span data-stu-id="598b4-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="598b4-120"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="598b4-120"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="598b4-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="598b4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="598b4-122">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="598b4-122">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="598b4-123">Medien senken</span><span class="sxs-lookup"><span data-stu-id="598b4-123">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




