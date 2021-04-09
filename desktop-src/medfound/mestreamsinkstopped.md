---
description: Wird durch eine streamsenke ausgelöst, wenn der Übergang zum beendeten Zustand abgeschlossen wird. Der Übergang zu "beendet" tritt auf, wenn die imfpresentationclock-Stopp Methode auf der senkenpräsentationmuhr aufgerufen wird.
ms.assetid: 1a8c7faa-4d4a-4458-ad08-a760a15dc347
title: Mestreamsinkbeendete-Ereignis (mfobjects. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e35313ab3d43c950184a82e403fa6ad0eb5b4ab4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042580"
---
# <a name="mestreamsinkstopped-event"></a><span data-ttu-id="f87c5-104">Mestreamsinkbeendete-Ereignis</span><span class="sxs-lookup"><span data-stu-id="f87c5-104">MEStreamSinkStopped event</span></span>

<span data-ttu-id="f87c5-105">Wird durch eine streamsenke ausgelöst, wenn der Übergang zum beendeten Zustand abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="f87c5-105">Raised by a stream sink when it completes the transition to the stopped state.</span></span> <span data-ttu-id="f87c5-106">Der Übergang zu "beendet" tritt auf, wenn die [**imfpresentationclock:: Stopp**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-stop) -Methode auf der Präsentations Uhr der Senke aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f87c5-106">The transition to stopped occurs when the [**IMFPresentationClock::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-stop) method is called on the sink's presentation clock.</span></span>

## <a name="event-values"></a><span data-ttu-id="f87c5-107">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="f87c5-107">Event values</span></span>

<span data-ttu-id="f87c5-108">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="f87c5-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="f87c5-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="f87c5-109">VARTYPE</span></span>              | <span data-ttu-id="f87c5-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f87c5-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="f87c5-111">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="f87c5-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="f87c5-112">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="f87c5-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="f87c5-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f87c5-113">Requirements</span></span>



| <span data-ttu-id="f87c5-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f87c5-114">Requirement</span></span> | <span data-ttu-id="f87c5-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f87c5-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f87c5-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f87c5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f87c5-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f87c5-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f87c5-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f87c5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f87c5-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f87c5-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f87c5-120">Header</span><span class="sxs-lookup"><span data-stu-id="f87c5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f87c5-121"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f87c5-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f87c5-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f87c5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f87c5-123">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f87c5-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="f87c5-124">Medien senken</span><span class="sxs-lookup"><span data-stu-id="f87c5-124">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




