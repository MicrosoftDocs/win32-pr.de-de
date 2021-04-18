---
description: Wird durch eine Medienquelle ausgelöst, wenn ein neuer Stream gestartet wird.
ms.assetid: 1bc8b265-b7a1-4068-89f7-c0da03dfb874
title: Menewstream-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60394d442b24dcdc234ada2dd3fd418e6ab7b54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347301"
---
# <a name="menewstream-event"></a><span data-ttu-id="00a48-103">Menewstream-Ereignis</span><span class="sxs-lookup"><span data-stu-id="00a48-103">MENewStream event</span></span>

<span data-ttu-id="00a48-104">Wird durch eine Medienquelle ausgelöst, wenn ein neuer Stream gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="00a48-104">Raised by a media source when it starts a new stream.</span></span>

<span data-ttu-id="00a48-105">Wenn die [**imfmediasource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) -Methode für eine Medienquelle aufgerufen wird, sendet die Medienquelle ein Ereignis für jeden ausgewählten Stream:</span><span class="sxs-lookup"><span data-stu-id="00a48-105">When the [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method is called on a media source, the media source sends one event for each selected stream:</span></span>

-   <span data-ttu-id="00a48-106">Die Quelle sendet das Ereignis menewstream, wenn der Datenstrom nicht im vorherigen [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)aufgerufen wurde, oder dies ist der erste **Start Start** für diese Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="00a48-106">The source sends the MENewStream event if the stream was not selected in the previous call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), or this is the very first call to **Start** on this media source.</span></span>

-   <span data-ttu-id="00a48-107">Die Quelle sendet das [meupdatedstream](meupdatedstream.md) -Ereignis, wenn der Stream bereits im vorherigen Aufrufen von " [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)" ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="00a48-107">The source sends the [MEUpdatedStream](meupdatedstream.md) event if the stream was already selected in the previous call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span></span>

<span data-ttu-id="00a48-108">Für nicht ausgewählte Streams werden keine Ereignisse gesendet.</span><span class="sxs-lookup"><span data-stu-id="00a48-108">No events are sent for unselected streams.</span></span>

## <a name="event-values"></a><span data-ttu-id="00a48-109">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="00a48-109">Event values</span></span>

<span data-ttu-id="00a48-110">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="00a48-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="00a48-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="00a48-111">VARTYPE</span></span>                | <span data-ttu-id="00a48-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="00a48-112">Description</span></span>                                                                                                   |
|------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00a48-113">VT \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="00a48-113">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="00a48-114">Enthält einen Zeiger auf die [**imfmediastream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) -Schnittstelle des Streams.</span><span class="sxs-lookup"><span data-stu-id="00a48-114">Contains a pointer to the stream's [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) interface.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="00a48-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00a48-115">Requirements</span></span>



| <span data-ttu-id="00a48-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00a48-116">Requirement</span></span> | <span data-ttu-id="00a48-117">Wert</span><span class="sxs-lookup"><span data-stu-id="00a48-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00a48-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="00a48-118">Minimum supported client</span></span><br/> | <span data-ttu-id="00a48-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00a48-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="00a48-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="00a48-120">Minimum supported server</span></span><br/> | <span data-ttu-id="00a48-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00a48-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="00a48-122">Header</span><span class="sxs-lookup"><span data-stu-id="00a48-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="00a48-123"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00a48-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00a48-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00a48-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00a48-125">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="00a48-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




