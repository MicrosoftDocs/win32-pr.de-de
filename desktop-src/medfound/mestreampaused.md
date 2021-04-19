---
description: Wird von einem Medienstream ausgelöst, wenn die imfmediasource::P ause-Methode asynchron abgeschlossen wird.
ms.assetid: 8fafb9a1-95a4-44b6-acd6-fb007d515915
title: Mestreampaused-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ca78147c7cdd7cb6e391052111e11ef0ac92b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348442"
---
# <a name="mestreampaused-event"></a><span data-ttu-id="ffa02-103">Mestreampaused-Ereignis</span><span class="sxs-lookup"><span data-stu-id="ffa02-103">MEStreamPaused event</span></span>

<span data-ttu-id="ffa02-104">Wird von einem Medienstream ausgelöst, wenn die [**imfmediasource::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) -Methode asynchron abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="ffa02-104">Raised by a media stream when the [**IMFMediaSource::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="ffa02-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="ffa02-105">Event values</span></span>

<span data-ttu-id="ffa02-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="ffa02-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="ffa02-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ffa02-107">VARTYPE</span></span>              | <span data-ttu-id="ffa02-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ffa02-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="ffa02-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="ffa02-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="ffa02-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="ffa02-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="ffa02-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ffa02-111">Remarks</span></span>

<span data-ttu-id="ffa02-112">Jeder aktive Stream in der Präsentation sendet dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ffa02-112">Each active stream in the presentation sends this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffa02-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ffa02-113">Requirements</span></span>



| <span data-ttu-id="ffa02-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ffa02-114">Requirement</span></span> | <span data-ttu-id="ffa02-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ffa02-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffa02-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ffa02-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ffa02-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ffa02-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ffa02-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ffa02-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ffa02-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ffa02-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ffa02-120">Header</span><span class="sxs-lookup"><span data-stu-id="ffa02-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffa02-121"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ffa02-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffa02-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ffa02-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffa02-123">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ffa02-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




