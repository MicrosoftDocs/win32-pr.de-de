---
description: Wird von der Medien Sitzung ausgelöst, wenn eine neue Präsentation gestartet wird. Dieses Ereignis zeigt an, wann die Präsentation gestartet wird und der Offset zwischen der Präsentationszeit und der Quell Zeit liegt.
ms.assetid: 67c7d5f3-ffaf-4359-a59c-bb26b992b6cd
title: Mesessionnotifypresentationtime-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7b0cd8811d98094ab58ddcf844ec73e1470d120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349108"
---
# <a name="mesessionnotifypresentationtime-event"></a><span data-ttu-id="cc840-104">Mesessionnotifypresentationtime-Ereignis</span><span class="sxs-lookup"><span data-stu-id="cc840-104">MESessionNotifyPresentationTime event</span></span>

<span data-ttu-id="cc840-105">Wird von der Medien Sitzung ausgelöst, wenn eine neue Präsentation gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="cc840-105">Raised by the Media Session when a new presentation starts.</span></span> <span data-ttu-id="cc840-106">Dieses Ereignis zeigt an, wann die Präsentation gestartet wird und der Offset zwischen der Präsentationszeit und der Quell Zeit liegt.</span><span class="sxs-lookup"><span data-stu-id="cc840-106">This event indicates when the presentation will start and the offset between the presentation time and the source time.</span></span>

## <a name="event-values"></a><span data-ttu-id="cc840-107">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="cc840-107">Event values</span></span>

<span data-ttu-id="cc840-108">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="cc840-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="cc840-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cc840-109">VARTYPE</span></span>              | <span data-ttu-id="cc840-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cc840-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="cc840-111">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="cc840-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="cc840-112">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="cc840-112">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="cc840-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="cc840-113">Attributes</span></span>

<span data-ttu-id="cc840-114">Für dieses Ereignis sind die folgenden Attribute definiert:</span><span class="sxs-lookup"><span data-stu-id="cc840-114">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="cc840-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="cc840-115">Attribute</span></span>                                                                                                                   | <span data-ttu-id="cc840-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cc840-116">Description</span></span>                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc840-117">**\_ \_ Start \_ Präsentations \_ Zeit für MF-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="cc840-117">**MF\_EVENT\_START\_PRESENTATION\_TIME**</span></span>](mf-event-start-presentation-time-attribute.md)<br/>                       | <span data-ttu-id="cc840-118">Startzeit der Präsentation.</span><span class="sxs-lookup"><span data-stu-id="cc840-118">Starting time for the presentation.</span></span><br/> <br/>                                                      |
| [<span data-ttu-id="cc840-119">**Zeit Offset der MF- \_ Ereignis \_ Präsentation \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cc840-119">**MF\_EVENT\_PRESENTATION\_TIME\_OFFSET**</span></span>](mf-event-presentation-time-offset-attribute.md)<br/>                     | <span data-ttu-id="cc840-120">Offset zwischen der Präsentationszeit und den Zeitstempeln der Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="cc840-120">Offset between the presentation time and the media source's time stamps.</span></span><br/> <br/>                 |
| [<span data-ttu-id="cc840-121">**\_ \_ \_ \_ Zeitpunkt der Ausgabe Präsentation des MF-Ereignisses \_ bei der \_ Ausgabe**</span><span class="sxs-lookup"><span data-stu-id="cc840-121">**MF\_EVENT\_START\_PRESENTATION\_TIME\_AT\_OUTPUT**</span></span>](mf-event-start-presentation-time-at-output-attribute.md)<br/> | <span data-ttu-id="cc840-122">Präsentationszeit, in der die Medien senken das erste Beispiel der neuen Topologie Rendering.</span><span class="sxs-lookup"><span data-stu-id="cc840-122">Presentation time when the media sinks will render the first sample of the new topology.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="cc840-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc840-123">Requirements</span></span>



| <span data-ttu-id="cc840-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc840-124">Requirement</span></span> | <span data-ttu-id="cc840-125">Wert</span><span class="sxs-lookup"><span data-stu-id="cc840-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc840-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cc840-126">Minimum supported client</span></span><br/> | <span data-ttu-id="cc840-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc840-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cc840-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cc840-128">Minimum supported server</span></span><br/> | <span data-ttu-id="cc840-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc840-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cc840-130">Header</span><span class="sxs-lookup"><span data-stu-id="cc840-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc840-131"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cc840-131"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc840-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc840-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc840-133">**Imfmediasession**</span><span class="sxs-lookup"><span data-stu-id="cc840-133">**IMFMediaSession**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
</dt> <dt>

[<span data-ttu-id="cc840-134">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cc840-134">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




