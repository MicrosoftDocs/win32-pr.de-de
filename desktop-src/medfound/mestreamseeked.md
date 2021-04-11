---
description: 'Wird von einem Mediendaten Strom nach einem imfmediasource:: Start-Rückruf ausgelöst und bewirkt eine Suche im Stream. Ein Mediendaten Strom löst dieses Ereignis aus, wenn die Medienquelle das mesourceseeked-Ereignis auslöst.'
ms.assetid: df06df16-711d-4262-b049-fb29f25934de
title: Mestreamseeked-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7b66e2176b08c04b01fc487aac4b8218536b615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215159"
---
# <a name="mestreamseeked-event"></a><span data-ttu-id="b6b81-104">Mestreamseeked-Ereignis</span><span class="sxs-lookup"><span data-stu-id="b6b81-104">MEStreamSeeked event</span></span>

<span data-ttu-id="b6b81-105">Wird von einem Mediendaten Strom nach einem [**imfmediasource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) -Rückruf ausgelöst und bewirkt eine Suche im Stream.</span><span class="sxs-lookup"><span data-stu-id="b6b81-105">Raised by a media stream after a call to [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) causes a seek in the stream.</span></span> <span data-ttu-id="b6b81-106">Ein Mediendaten Strom löst dieses Ereignis aus, wenn die Medienquelle das [mesourceseeked](mesourceseeked.md) -Ereignis auslöst.</span><span class="sxs-lookup"><span data-stu-id="b6b81-106">A media stream raises this event when the media source raises the [MESourceSeeked](mesourceseeked.md) event.</span></span>

## <a name="event-values"></a><span data-ttu-id="b6b81-107">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="b6b81-107">Event values</span></span>

<span data-ttu-id="b6b81-108">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="b6b81-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="b6b81-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="b6b81-109">VARTYPE</span></span>           | <span data-ttu-id="b6b81-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b6b81-110">Description</span></span>                                                        |
|-------------------|--------------------------------------------------------------------|
| <span data-ttu-id="b6b81-111">VT \_ I8</span><span class="sxs-lookup"><span data-stu-id="b6b81-111">VT\_I8</span></span><br/> | <span data-ttu-id="b6b81-112">Neue Startzeit in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="b6b81-112">New starting time, in 100-nanosecond units.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="b6b81-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6b81-113">Requirements</span></span>



| <span data-ttu-id="b6b81-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6b81-114">Requirement</span></span> | <span data-ttu-id="b6b81-115">Wert</span><span class="sxs-lookup"><span data-stu-id="b6b81-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6b81-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b6b81-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b6b81-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6b81-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b6b81-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b6b81-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b6b81-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6b81-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b6b81-120">Header</span><span class="sxs-lookup"><span data-stu-id="b6b81-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6b81-121"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6b81-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6b81-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6b81-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6b81-123">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b6b81-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




