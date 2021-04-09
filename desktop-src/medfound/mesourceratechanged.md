---
description: 'Wird von einer Medienquelle ausgelöst, wenn sich die Wiedergabe Rate ändert. Dieses Ereignis wird gesendet, nachdem die imfratecontrol:: abtrate-Methode asynchron abgeschlossen wurde.'
ms.assetid: 68a7fe64-e28a-4c20-830c-9402e1fb57f8
title: Mesourceratechanged-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2af1ca671e09fc8a236ba79b36c1610635989ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129809"
---
# <a name="mesourceratechanged-event"></a><span data-ttu-id="36942-104">Mesourceratechanged-Ereignis</span><span class="sxs-lookup"><span data-stu-id="36942-104">MESourceRateChanged event</span></span>

<span data-ttu-id="36942-105">Wird von einer Medienquelle ausgelöst, wenn sich die Wiedergabe Rate ändert.</span><span class="sxs-lookup"><span data-stu-id="36942-105">Raised by a media source when the playback rate changes.</span></span> <span data-ttu-id="36942-106">Dieses Ereignis wird gesendet, nachdem die [**imfratecontrol:: abtrate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) -Methode asynchron abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="36942-106">This event is sent after the [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="36942-107">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="36942-107">Event values</span></span>

<span data-ttu-id="36942-108">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="36942-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="36942-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="36942-109">VARTYPE</span></span>           | <span data-ttu-id="36942-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36942-110">Description</span></span>                                   |
|-------------------|-----------------------------------------------|
| <span data-ttu-id="36942-111">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="36942-111">VT\_R4</span></span><br/> | <span data-ttu-id="36942-112">Die neue Wiedergabe Rate.</span><span class="sxs-lookup"><span data-stu-id="36942-112">The new playback rate.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="36942-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="36942-113">Requirements</span></span>



| <span data-ttu-id="36942-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="36942-114">Requirement</span></span> | <span data-ttu-id="36942-115">Wert</span><span class="sxs-lookup"><span data-stu-id="36942-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36942-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="36942-116">Minimum supported client</span></span><br/> | <span data-ttu-id="36942-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36942-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="36942-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="36942-118">Minimum supported server</span></span><br/> | <span data-ttu-id="36942-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36942-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="36942-120">Header</span><span class="sxs-lookup"><span data-stu-id="36942-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="36942-121"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="36942-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36942-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36942-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36942-123">Implementieren der Raten Steuerung</span><span class="sxs-lookup"><span data-stu-id="36942-123">Implementing Rate Control</span></span>](implementing-rate-control.md)
</dt> <dt>

[<span data-ttu-id="36942-124">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="36942-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="36942-125">Raten Steuerung</span><span class="sxs-lookup"><span data-stu-id="36942-125">Rate Control</span></span>](rate-control.md)
</dt> <dt>

[<span data-ttu-id="36942-126">**Imfratecontrol:: abtrate**</span><span class="sxs-lookup"><span data-stu-id="36942-126">**IMFRateControl::SetRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)
</dt> </dl>

 

 




