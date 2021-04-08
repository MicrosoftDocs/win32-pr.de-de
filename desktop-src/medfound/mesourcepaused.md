---
description: Wird von einer Medienquelle ausgelöst, wenn die imfmediasource::P ause-Methode asynchron abgeschlossen wird.
ms.assetid: cca03d60-47ae-4a11-b29d-81d749e24df9
title: Mesourcepaused-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ac346e679eb3a82ca707a14f772f1a79e2a1e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863604"
---
# <a name="mesourcepaused-event"></a><span data-ttu-id="5f8f3-103">Mesourcepaused-Ereignis</span><span class="sxs-lookup"><span data-stu-id="5f8f3-103">MESourcePaused event</span></span>

<span data-ttu-id="5f8f3-104">Wird von einer Medienquelle ausgelöst, wenn die [**imfmediasource::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) -Methode asynchron abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="5f8f3-104">Raised by a media source when the [**IMFMediaSource::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="5f8f3-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="5f8f3-105">Event values</span></span>

<span data-ttu-id="5f8f3-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="5f8f3-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="5f8f3-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5f8f3-107">VARTYPE</span></span>              | <span data-ttu-id="5f8f3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5f8f3-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="5f8f3-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="5f8f3-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="5f8f3-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="5f8f3-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="5f8f3-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f8f3-111">Requirements</span></span>



| <span data-ttu-id="5f8f3-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f8f3-112">Requirement</span></span> | <span data-ttu-id="5f8f3-113">Wert</span><span class="sxs-lookup"><span data-stu-id="5f8f3-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f8f3-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5f8f3-114">Minimum supported client</span></span><br/> | <span data-ttu-id="5f8f3-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f8f3-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5f8f3-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5f8f3-116">Minimum supported server</span></span><br/> | <span data-ttu-id="5f8f3-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f8f3-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5f8f3-118">Header</span><span class="sxs-lookup"><span data-stu-id="5f8f3-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f8f3-119"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5f8f3-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f8f3-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f8f3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f8f3-121">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5f8f3-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




