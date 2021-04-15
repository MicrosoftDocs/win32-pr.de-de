---
description: Wird von einer Medienquelle ausgelöst, wenn Sie neu gestartet wird oder einen Datenstrom sucht, der bereits aktiv ist.
ms.assetid: 2d91a267-e109-45f5-886b-11b883cc5509
title: Meupdatedstream-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e3b2e6fdc5928a08306b344c02b5eaafc37e957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529603"
---
# <a name="meupdatedstream-event"></a><span data-ttu-id="2f230-103">Meupdatedstream-Ereignis</span><span class="sxs-lookup"><span data-stu-id="2f230-103">MEUpdatedStream event</span></span>

<span data-ttu-id="2f230-104">Wird von einer Medienquelle ausgelöst, wenn Sie neu gestartet wird oder einen Datenstrom sucht, der bereits aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="2f230-104">Raised by a media source when it restarts or seeks a stream that is already active.</span></span>

<span data-ttu-id="2f230-105">Wenn die [**imfmediasource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) -Methode für eine Medienquelle aufgerufen wird, sendet die Medienquelle ein Ereignis für jeden ausgewählten Stream:</span><span class="sxs-lookup"><span data-stu-id="2f230-105">When the [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method is called on a media source, the media source sends one event for each selected stream:</span></span>

-   <span data-ttu-id="2f230-106">Die Quelle sendet das Ereignis [menewstream](menewstream.md) , wenn der Datenstrom nicht im vorherigen [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)aufgerufen wurde, oder dies ist der erste **Start Start** für diese Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="2f230-106">The source sends the [MENewStream](menewstream.md) event if the stream was not selected in the previous call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), or this is the very first call to **Start** on this media source.</span></span>

-   <span data-ttu-id="2f230-107">Die Quelle sendet das meupdatedstream-Ereignis, wenn der Stream bereits im vorherigen Aufrufen von " [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)" ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="2f230-107">The source sends the MEUpdatedStream event if the stream was already selected in the previous call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span></span>

<span data-ttu-id="2f230-108">Für nicht ausgewählte Streams werden keine Ereignisse gesendet.</span><span class="sxs-lookup"><span data-stu-id="2f230-108">No events are sent for unselected streams.</span></span>

## <a name="event-values"></a><span data-ttu-id="2f230-109">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="2f230-109">Event values</span></span>

<span data-ttu-id="2f230-110">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="2f230-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="2f230-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="2f230-111">VARTYPE</span></span>                | <span data-ttu-id="2f230-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2f230-112">Description</span></span>                                                                                        |
|------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f230-113">VT \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="2f230-113">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="2f230-114">Ein Zeiger auf die [**imfmediastream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) -Schnittstelle des Streams.</span><span class="sxs-lookup"><span data-stu-id="2f230-114">Pointer to the stream's [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="2f230-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f230-115">Remarks</span></span>

<span data-ttu-id="2f230-116">Beim ersten [**Start Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) , bei dem ein Stream aktiv wird, sendet die Medienquelle ein [menewstream](menewstream.md) -Ereignis für den Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="2f230-116">On the first call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) in which a stream becomes active, the media source sends an [MENewStream](menewstream.md) event for the stream.</span></span> <span data-ttu-id="2f230-117">Bei nachfolgenden Aufrufen des **Starts** sendet die Medienquelle ein meupdatedstream-Ereignis, bis der Stream deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="2f230-117">On subsequent calls to **Start**, the media source sends an MEUpdatedStream event, until the stream is deselected.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f230-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f230-118">Requirements</span></span>



| <span data-ttu-id="2f230-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f230-119">Requirement</span></span> | <span data-ttu-id="2f230-120">Wert</span><span class="sxs-lookup"><span data-stu-id="2f230-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f230-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2f230-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2f230-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f230-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2f230-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2f230-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2f230-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f230-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2f230-125">Header</span><span class="sxs-lookup"><span data-stu-id="2f230-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f230-126"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f230-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f230-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f230-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f230-128">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2f230-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




