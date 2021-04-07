---
description: Wird von der Medien Sitzung ausgelöst, wenn eine Bereinigungs Anforderung abgeschlossen ist.
ms.assetid: 1ae97022-3fb2-4c5e-9262-d5bdc2a62bee
title: Mesessionscrubsamplecomplete-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b076c2f2978831cc30521fcf49d71c04620c4dee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863611"
---
# <a name="mesessionscrubsamplecomplete-event"></a><span data-ttu-id="3971b-103">Mesessionscrubsamplecomplete-Ereignis</span><span class="sxs-lookup"><span data-stu-id="3971b-103">MESessionScrubSampleComplete event</span></span>

<span data-ttu-id="3971b-104">Wird von der Medien Sitzung ausgelöst, wenn eine Bereinigungs Anforderung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="3971b-104">Raised by the Media Session when it completes a scrubbing request.</span></span>

<span data-ttu-id="3971b-105">Ein Scrubbing tritt auf, wenn die Wiedergabe Rate 0 (null) ist und die Anwendung [**imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)aufruft.</span><span class="sxs-lookup"><span data-stu-id="3971b-105">Scrubbing occurs when the playback rate is zero and the application calls [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span> <span data-ttu-id="3971b-106">Dieses Ereignis wird ausgelöst, nachdem jede streamsenke die Bereinigungs Anforderung abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="3971b-106">This event is raised after every stream sink has completed the scrubbing request.</span></span>

## <a name="event-values"></a><span data-ttu-id="3971b-107">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="3971b-107">Event values</span></span>

<span data-ttu-id="3971b-108">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="3971b-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="3971b-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="3971b-109">VARTYPE</span></span>              | <span data-ttu-id="3971b-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3971b-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="3971b-111">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="3971b-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="3971b-112">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="3971b-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="3971b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3971b-113">Requirements</span></span>



| <span data-ttu-id="3971b-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3971b-114">Requirement</span></span> | <span data-ttu-id="3971b-115">Wert</span><span class="sxs-lookup"><span data-stu-id="3971b-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3971b-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3971b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3971b-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3971b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3971b-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3971b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3971b-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3971b-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3971b-120">Header</span><span class="sxs-lookup"><span data-stu-id="3971b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3971b-121"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3971b-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3971b-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3971b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3971b-123">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3971b-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="3971b-124">Mestreamsinkscrubsamplecomplete</span><span class="sxs-lookup"><span data-stu-id="3971b-124">MEStreamSinkScrubSampleComplete</span></span>](mestreamsinkscrubsamplecomplete.md)
</dt> </dl>

 

 




