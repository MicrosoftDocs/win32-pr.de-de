---
description: Wird durch eine streamsenke ausgelöst, wenn der Übergang in den Status "wird ausgeführt" versetzt wird.
ms.assetid: 95ac658b-bec0-442d-85ef-61966b40a2f2
title: Mestreamsink Started-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 407ab885da04746034b7126a8d9bb9389d2928f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348516"
---
# <a name="mestreamsinkstarted-event"></a><span data-ttu-id="25e25-103">Mestreamsink Started-Ereignis</span><span class="sxs-lookup"><span data-stu-id="25e25-103">MEStreamSinkStarted event</span></span>

<span data-ttu-id="25e25-104">Wird durch eine streamsenke ausgelöst, wenn der Übergang in den Status "wird ausgeführt" versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="25e25-104">Raised by a stream sink when it completes the transition to the running state.</span></span> <span data-ttu-id="25e25-105">Der Übergang zu "wird ausgeführt" erfolgt, wenn die [**imfpresentationclock:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start) -Methode auf der Präsentations Uhr der Senke aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="25e25-105">The transition to running occurs when the [**IMFPresentationClock::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start) method is called on the sink's presentation clock.</span></span> <span data-ttu-id="25e25-106">Die Medien Senke empfängt die Benachrichtigung über die [**imfclockstaatink:: onclockstart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) -Methode oder die [**imfclockstaatink:: onclockrestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) -Methode.</span><span class="sxs-lookup"><span data-stu-id="25e25-106">The media sink receives the notification through its [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) or [**IMFClockStateSink::OnClockRestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) method.</span></span>

## <a name="event-values"></a><span data-ttu-id="25e25-107">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="25e25-107">Event values</span></span>

<span data-ttu-id="25e25-108">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="25e25-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="25e25-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="25e25-109">VARTYPE</span></span>              | <span data-ttu-id="25e25-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="25e25-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="25e25-111">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="25e25-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="25e25-112">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="25e25-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="25e25-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25e25-113">Requirements</span></span>



| <span data-ttu-id="25e25-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25e25-114">Requirement</span></span> | <span data-ttu-id="25e25-115">Wert</span><span class="sxs-lookup"><span data-stu-id="25e25-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25e25-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="25e25-116">Minimum supported client</span></span><br/> | <span data-ttu-id="25e25-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25e25-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="25e25-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="25e25-118">Minimum supported server</span></span><br/> | <span data-ttu-id="25e25-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25e25-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="25e25-120">Header</span><span class="sxs-lookup"><span data-stu-id="25e25-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="25e25-121"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="25e25-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25e25-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25e25-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25e25-123">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="25e25-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="25e25-124">Medien senken</span><span class="sxs-lookup"><span data-stu-id="25e25-124">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




