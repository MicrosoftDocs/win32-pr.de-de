---
description: Wird von imfmediasource gesendet, die das Gerät kapselt, um anzugeben, dass das Gerät vorzeitig entfernt wurde.
ms.assetid: 85EE663C-94B7-47EA-ABBA-A8371342EEB2
title: Mevideocapturedevicepreempted-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3968c0641d954741474b1d5ec7ffaa11dcad5f15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348515"
---
# <a name="mevideocapturedevicepreempted-event"></a><span data-ttu-id="6ebd7-103">Mevideocapturedevicepreempted-Ereignis</span><span class="sxs-lookup"><span data-stu-id="6ebd7-103">MEVideoCaptureDevicePreempted event</span></span>

<span data-ttu-id="6ebd7-104">Wird von [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) gesendet, die das Gerät kapselt, um anzugeben, dass das Gerät vorzeitig entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ebd7-104">Sent by the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) that encapsulates the device to indicate that the device has been preempted.</span></span>

## <a name="event-values"></a><span data-ttu-id="6ebd7-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="6ebd7-105">Event values</span></span>

<span data-ttu-id="6ebd7-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="6ebd7-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="6ebd7-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="6ebd7-107">VARTYPE</span></span>               | <span data-ttu-id="6ebd7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ebd7-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="6ebd7-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="6ebd7-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="6ebd7-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="6ebd7-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="6ebd7-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ebd7-111">Remarks</span></span>

<span data-ttu-id="6ebd7-112">Dieses Ereignis wird von der [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) gesendet, die das Gerät kapselt.</span><span class="sxs-lookup"><span data-stu-id="6ebd7-112">This event is sent by the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) that encapsulates the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ebd7-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ebd7-113">Requirements</span></span>



| <span data-ttu-id="6ebd7-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ebd7-114">Requirement</span></span> | <span data-ttu-id="6ebd7-115">Wert</span><span class="sxs-lookup"><span data-stu-id="6ebd7-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ebd7-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6ebd7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6ebd7-117">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ebd7-117">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="6ebd7-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6ebd7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6ebd7-119">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ebd7-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6ebd7-120">Header</span><span class="sxs-lookup"><span data-stu-id="6ebd7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ebd7-121"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ebd7-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ebd7-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ebd7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ebd7-123">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6ebd7-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




