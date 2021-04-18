---
description: Wird von imfmediasource gesendet, die das Gerät kapselt, um anzugeben, dass das Gerät entfernt wurde.
ms.assetid: 107AFF19-B444-4B62-9217-46A99AC3632C
title: Mevideocapturedeviceremoved-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e3276f53f86bdce78825b94828577eab9e40954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357912"
---
# <a name="mevideocapturedeviceremoved-event"></a><span data-ttu-id="c7e18-103">Mevideocapturedeviceremoved-Ereignis</span><span class="sxs-lookup"><span data-stu-id="c7e18-103">MEVideoCaptureDeviceRemoved event</span></span>

<span data-ttu-id="c7e18-104">Wird von [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) gesendet, die das Gerät kapselt, um anzugeben, dass das Gerät entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="c7e18-104">Sent by the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) that encapsulates the device to indicate that the device has been removed.</span></span>

## <a name="event-values"></a><span data-ttu-id="c7e18-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="c7e18-105">Event values</span></span>

<span data-ttu-id="c7e18-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="c7e18-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="c7e18-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c7e18-107">VARTYPE</span></span>               | <span data-ttu-id="c7e18-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c7e18-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="c7e18-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="c7e18-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="c7e18-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="c7e18-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="c7e18-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7e18-111">Remarks</span></span>

<span data-ttu-id="c7e18-112">Dieses Ereignis wird von der [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) gesendet, die das Gerät kapselt.</span><span class="sxs-lookup"><span data-stu-id="c7e18-112">This event is sent by the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) that encapsulates the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7e18-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7e18-113">Requirements</span></span>



| <span data-ttu-id="c7e18-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7e18-114">Requirement</span></span> | <span data-ttu-id="c7e18-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c7e18-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7e18-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c7e18-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c7e18-117">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7e18-117">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="c7e18-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c7e18-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c7e18-119">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7e18-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c7e18-120">Header</span><span class="sxs-lookup"><span data-stu-id="c7e18-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7e18-121"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c7e18-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7e18-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7e18-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7e18-123">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c7e18-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




