---
description: Wird durch eine streamsenke ausgelöst, wenn der Stream genug vorab Rollendaten empfangen hat, um das Rendering zu beginnen. Dieses Ereignis wird von Medien senken ausgelöst, die die imfmediasinkpreroll-Schnittstelle unterstützen.
ms.assetid: 1ecb1805-73ce-4741-b969-6eb88982ee26
title: Mestreamsinkprerolled-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 312daa90c995ccbbe8667cfa5acdf47975248474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754289"
---
# <a name="mestreamsinkprerolled-event"></a><span data-ttu-id="11200-104">Mestreamsinkprerolled-Ereignis</span><span class="sxs-lookup"><span data-stu-id="11200-104">MEStreamSinkPrerolled event</span></span>

<span data-ttu-id="11200-105">Wird durch eine streamsenke ausgelöst, wenn der Stream genug vorab Rollendaten empfangen hat, um das Rendering zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="11200-105">Raised by a stream sink when the stream has received enough pre-roll data to begin rendering.</span></span> <span data-ttu-id="11200-106">Dieses Ereignis wird von Medien senken ausgelöst, die die [**imfmediasinkpreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) -Schnittstelle unterstützen.</span><span class="sxs-lookup"><span data-stu-id="11200-106">This event is raised by media sinks that support the [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) interface.</span></span>

## <a name="event-values"></a><span data-ttu-id="11200-107">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="11200-107">Event values</span></span>

<span data-ttu-id="11200-108">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="11200-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="11200-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="11200-109">VARTYPE</span></span>              | <span data-ttu-id="11200-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11200-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="11200-111">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="11200-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="11200-112">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="11200-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="11200-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11200-113">Requirements</span></span>



| <span data-ttu-id="11200-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11200-114">Requirement</span></span> | <span data-ttu-id="11200-115">Wert</span><span class="sxs-lookup"><span data-stu-id="11200-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11200-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11200-116">Minimum supported client</span></span><br/> | <span data-ttu-id="11200-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11200-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="11200-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11200-118">Minimum supported server</span></span><br/> | <span data-ttu-id="11200-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11200-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="11200-120">Header</span><span class="sxs-lookup"><span data-stu-id="11200-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="11200-121"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11200-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11200-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11200-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11200-123">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="11200-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="11200-124">Medien senken</span><span class="sxs-lookup"><span data-stu-id="11200-124">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




