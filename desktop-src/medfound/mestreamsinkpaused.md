---
description: Wird durch eine streamsenke ausgelöst, wenn der Übergang zum angehaltenen Zustand abgeschlossen wird.
ms.assetid: 84ab62fc-1525-433c-8af5-70659122703c
title: Mestreamsink angeh Ed-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17016285f2b88a1fc266b79f5eee45fea31f824c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347496"
---
# <a name="mestreamsinkpaused-event"></a><span data-ttu-id="87976-103">Mestreamsink-Ereignis</span><span class="sxs-lookup"><span data-stu-id="87976-103">MEStreamSinkPaused event</span></span>

<span data-ttu-id="87976-104">Wird durch eine streamsenke ausgelöst, wenn der Übergang zum angehaltenen Zustand abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="87976-104">Raised by a stream sink when it completes the transition to the paused state.</span></span> <span data-ttu-id="87976-105">Der Übergang zum Anhalten erfolgt, wenn die [**imfpresentationclock::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-pause) -Methode auf der Präsentations Uhr der Senke aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="87976-105">The transition to paused occurs when the [**IMFPresentationClock::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-pause) method is called on the sink's presentation clock.</span></span>

## <a name="event-values"></a><span data-ttu-id="87976-106">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="87976-106">Event values</span></span>

<span data-ttu-id="87976-107">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="87976-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="87976-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="87976-108">VARTYPE</span></span>              | <span data-ttu-id="87976-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="87976-109">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="87976-110">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="87976-110">VT\_EMPTY</span></span><br/> | <span data-ttu-id="87976-111">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="87976-111">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="87976-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="87976-112">Requirements</span></span>



| <span data-ttu-id="87976-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="87976-113">Requirement</span></span> | <span data-ttu-id="87976-114">Wert</span><span class="sxs-lookup"><span data-stu-id="87976-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87976-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="87976-115">Minimum supported client</span></span><br/> | <span data-ttu-id="87976-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="87976-116">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="87976-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="87976-117">Minimum supported server</span></span><br/> | <span data-ttu-id="87976-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="87976-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="87976-119">Header</span><span class="sxs-lookup"><span data-stu-id="87976-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="87976-120"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="87976-120"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87976-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87976-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87976-122">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="87976-122">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="87976-123">Medien senken</span><span class="sxs-lookup"><span data-stu-id="87976-123">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




