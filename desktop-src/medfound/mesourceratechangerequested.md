---
description: 'Wird von einer Medienquelle ausgelöst, um eine neue Wiedergabe Rate anzufordern. Die Anwendung sollte imfratecontrol:: setRate mit der angeforderten Rate abrufen. Eine Medienquelle kann dieses Ereignis auch dann erhöhen, wenn die Wiedergabe mit der aktuellen Rate nicht fortgesetzt werden kann.'
ms.assetid: 705e5a79-836b-417b-a7ed-c733572f6905
title: Mesourceratechangerequjects-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9973a509541f3ec3d4f6a235b8f1277a20f7ed1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215161"
---
# <a name="mesourceratechangerequested-event"></a><span data-ttu-id="e6edc-105">Mesourceratechangerequnost-Ereignis</span><span class="sxs-lookup"><span data-stu-id="e6edc-105">MESourceRateChangeRequested event</span></span>

<span data-ttu-id="e6edc-106">Wird von einer Medienquelle ausgelöst, um eine neue Wiedergabe Rate anzufordern.</span><span class="sxs-lookup"><span data-stu-id="e6edc-106">Raised by a media source to request a new playback rate.</span></span> <span data-ttu-id="e6edc-107">Die Anwendung sollte [**imfratecontrol:: setRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) mit der angeforderten Rate abrufen.</span><span class="sxs-lookup"><span data-stu-id="e6edc-107">The application should call [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) with the requested rate.</span></span> <span data-ttu-id="e6edc-108">Eine Medienquelle kann dieses Ereignis auch dann erhöhen, wenn die Wiedergabe mit der aktuellen Rate nicht fortgesetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e6edc-108">A media source might raise this event if it cannot continue playback at the current rate.</span></span>

## <a name="event-values"></a><span data-ttu-id="e6edc-109">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="e6edc-109">Event values</span></span>

<span data-ttu-id="e6edc-110">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="e6edc-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="e6edc-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e6edc-111">VARTYPE</span></span>           | <span data-ttu-id="e6edc-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e6edc-112">Description</span></span>                                             |
|-------------------|---------------------------------------------------------|
| <span data-ttu-id="e6edc-113">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="e6edc-113">VT\_R4</span></span><br/> | <span data-ttu-id="e6edc-114">Die angeforderte neue Wiedergabe Rate.</span><span class="sxs-lookup"><span data-stu-id="e6edc-114">The requested new playback rate.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="e6edc-115">Attribute</span><span class="sxs-lookup"><span data-stu-id="e6edc-115">Attributes</span></span>

<span data-ttu-id="e6edc-116">Für dieses Ereignis sind die folgenden Attribute definiert:</span><span class="sxs-lookup"><span data-stu-id="e6edc-116">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="e6edc-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="e6edc-117">Attribute</span></span>                                                                    | <span data-ttu-id="e6edc-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e6edc-118">Description</span></span>                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="e6edc-119">**MF- \_ Ereignis wird \_ \_ dünner**</span><span class="sxs-lookup"><span data-stu-id="e6edc-119">**MF\_EVENT\_DO\_THINNING**</span></span>](mf-event-do-thinning-attribute.md)<br/> | <span data-ttu-id="e6edc-120">Gibt an, ob die Medienquelle auch eine Verdünnung anfordert.</span><span class="sxs-lookup"><span data-stu-id="e6edc-120">Specifies whether the media source also requests thinning.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="e6edc-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6edc-121">Requirements</span></span>



| <span data-ttu-id="e6edc-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6edc-122">Requirement</span></span> | <span data-ttu-id="e6edc-123">Wert</span><span class="sxs-lookup"><span data-stu-id="e6edc-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6edc-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e6edc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e6edc-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6edc-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e6edc-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e6edc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e6edc-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6edc-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e6edc-128">Header</span><span class="sxs-lookup"><span data-stu-id="e6edc-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6edc-129"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6edc-129"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6edc-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6edc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6edc-131">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e6edc-131">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




