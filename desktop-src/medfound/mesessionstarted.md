---
description: 'Wird ausgelöst, wenn die imfmediasession:: Start-Methode asynchron abgeschlossen wird.'
ms.assetid: 28ed32f0-9b23-4da1-9587-15f490da7bf9
title: Mesessionstarted-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9510fb5f5dda3d14b916ed40dcba4ca05800b52b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041964"
---
# <a name="mesessionstarted-event"></a><span data-ttu-id="c5174-103">Mesessionstarted-Ereignis</span><span class="sxs-lookup"><span data-stu-id="c5174-103">MESessionStarted event</span></span>

<span data-ttu-id="c5174-104">Wird ausgelöst, wenn die [**imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) -Methode asynchron abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="c5174-104">Raised when the [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="c5174-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="c5174-105">Event values</span></span>

<span data-ttu-id="c5174-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="c5174-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="c5174-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c5174-107">VARTYPE</span></span>              | <span data-ttu-id="c5174-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c5174-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="c5174-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="c5174-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="c5174-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="c5174-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="c5174-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="c5174-111">Attributes</span></span>

<span data-ttu-id="c5174-112">Für dieses Ereignis sind die folgenden Attribute definiert:</span><span class="sxs-lookup"><span data-stu-id="c5174-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="c5174-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="c5174-113">Attribute</span></span>                                                                                               | <span data-ttu-id="c5174-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c5174-114">Description</span></span>                                                                                     |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5174-115">**Zeit Offset der MF- \_ Ereignis \_ Präsentation \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c5174-115">**MF\_EVENT\_PRESENTATION\_TIME\_OFFSET**</span></span>](mf-event-presentation-time-offset-attribute.md)<br/> | <span data-ttu-id="c5174-116">Offset zwischen der Präsentationszeit und den Zeitstempeln der Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="c5174-116">Offset between the presentation time and the media source's time stamps.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="c5174-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5174-117">Requirements</span></span>



| <span data-ttu-id="c5174-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5174-118">Requirement</span></span> | <span data-ttu-id="c5174-119">Wert</span><span class="sxs-lookup"><span data-stu-id="c5174-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5174-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c5174-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c5174-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5174-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c5174-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c5174-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c5174-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5174-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c5174-124">Header</span><span class="sxs-lookup"><span data-stu-id="c5174-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5174-125"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c5174-125"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5174-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5174-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5174-127">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c5174-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




