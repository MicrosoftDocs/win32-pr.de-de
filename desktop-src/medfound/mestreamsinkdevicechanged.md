---
description: Wird von den streamsenken des erweiterten Videorenderers (EVR) ausgelöst, wenn sich das Videogerät ändert.
ms.assetid: 5b663d6b-5df8-4321-a6a5-a21b9810065a
title: Mestreamsinkdevicechanged-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 651fc34a56ca52cfb9e0b3f20e6e4d6b5366f541
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343720"
---
# <a name="mestreamsinkdevicechanged-event"></a><span data-ttu-id="e2b39-103">Mestreamsinkdevicechanged-Ereignis</span><span class="sxs-lookup"><span data-stu-id="e2b39-103">MEStreamSinkDeviceChanged event</span></span>

<span data-ttu-id="e2b39-104">Wird von den streamsenken des erweiterten Videorenderers (EVR) ausgelöst, wenn sich das Videogerät ändert.</span><span class="sxs-lookup"><span data-stu-id="e2b39-104">Raised by the stream sinks of the enhanced video renderer (EVR) if the video device changes.</span></span> <span data-ttu-id="e2b39-105">Beispielsweise löst der EVR dieses Ereignis aus, wenn es ein [**\_ \_ geändertes**](../directshow/ec-display-changed.md) Ereignis der EC-Anzeige empfängt.</span><span class="sxs-lookup"><span data-stu-id="e2b39-105">For example, the EVR raises this event when it receives an [**EC\_DISPLAY\_CHANGED**](../directshow/ec-display-changed.md) event.</span></span>

<span data-ttu-id="e2b39-106">Die Media Foundation Pipeline antwortet auf dieses Ereignis, indem alle Beispiel Anforderungen, bei denen das Gerät geändert wurde, erneut übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="e2b39-106">The Media Foundation pipeline responds to this event by resubmitting all sample requests that failed while the device was changing.</span></span>

## <a name="event-values"></a><span data-ttu-id="e2b39-107">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="e2b39-107">Event values</span></span>

<span data-ttu-id="e2b39-108">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="e2b39-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="e2b39-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e2b39-109">VARTYPE</span></span>              | <span data-ttu-id="e2b39-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e2b39-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="e2b39-111">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="e2b39-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="e2b39-112">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="e2b39-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="e2b39-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2b39-113">Requirements</span></span>



| <span data-ttu-id="e2b39-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2b39-114">Requirement</span></span> | <span data-ttu-id="e2b39-115">Wert</span><span class="sxs-lookup"><span data-stu-id="e2b39-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2b39-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e2b39-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e2b39-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2b39-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e2b39-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e2b39-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e2b39-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2b39-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e2b39-120">Header</span><span class="sxs-lookup"><span data-stu-id="e2b39-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2b39-121"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e2b39-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2b39-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2b39-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2b39-123">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e2b39-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="e2b39-124">Medien senken</span><span class="sxs-lookup"><span data-stu-id="e2b39-124">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 
