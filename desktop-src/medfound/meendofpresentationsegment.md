---
description: Wird von der Sequencer-Quelle ausgelöst, wenn ein Segment abgeschlossen wird, gefolgt von einem anderen Segment. Wenn das abschließende Segment abgeschlossen ist, löst die Sequencer-Quelle ein meendof Presentation-Ereignis aus.
ms.assetid: 1be13c9a-d454-4642-b26b-556f2461b705
title: Meendofpresentationsegment-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d3608f51f3ff66e21261cc40d1f8cf690c92c4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863620"
---
# <a name="meendofpresentationsegment-event"></a><span data-ttu-id="96751-104">Meendof presentationsegment-Ereignis</span><span class="sxs-lookup"><span data-stu-id="96751-104">MEEndOfPresentationSegment event</span></span>

<span data-ttu-id="96751-105">Wird von der Sequencer-Quelle ausgelöst, wenn ein Segment abgeschlossen wird, gefolgt von einem anderen Segment.</span><span class="sxs-lookup"><span data-stu-id="96751-105">Raised by the sequencer source when a segment is completed and is followed by another segment.</span></span> <span data-ttu-id="96751-106">Wenn das abschließende Segment abgeschlossen ist, löst die Sequencer-Quelle ein [meendof Presentation](meendofpresentation.md) -Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="96751-106">When the final segment is completed, the sequencer source raises an [MEEndOfPresentation](meendofpresentation.md) event.</span></span>

<span data-ttu-id="96751-107">Die Medien Sitzung leitet dieses Ereignis an die Anwendung weiter.</span><span class="sxs-lookup"><span data-stu-id="96751-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="96751-108">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="96751-108">Event values</span></span>

<span data-ttu-id="96751-109">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="96751-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="96751-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="96751-110">VARTYPE</span></span>              | <span data-ttu-id="96751-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="96751-111">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="96751-112">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="96751-112">VT\_EMPTY</span></span><br/> | <span data-ttu-id="96751-113">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="96751-113">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="96751-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="96751-114">Attributes</span></span>

<span data-ttu-id="96751-115">Für dieses Ereignis sind die folgenden Attribute definiert:</span><span class="sxs-lookup"><span data-stu-id="96751-115">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="96751-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="96751-116">Attribute</span></span>                                                                                               | <span data-ttu-id="96751-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="96751-117">Description</span></span>                                                                          |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="96751-118">**die MF- \_ Ereignis \_ Quell \_ Topologie wurde \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="96751-118">**MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED**</span></span>](mf-event-source-topology-canceled-attribute.md)<br/> | <span data-ttu-id="96751-119">Gibt an, ob die Sequencer-Quelle dieses Segment abgebrochen hat.</span><span class="sxs-lookup"><span data-stu-id="96751-119">Specifies whether the sequencer source canceled this segment.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="96751-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96751-120">Requirements</span></span>



| <span data-ttu-id="96751-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96751-121">Requirement</span></span> | <span data-ttu-id="96751-122">Wert</span><span class="sxs-lookup"><span data-stu-id="96751-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96751-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="96751-123">Minimum supported client</span></span><br/> | <span data-ttu-id="96751-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="96751-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="96751-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="96751-125">Minimum supported server</span></span><br/> | <span data-ttu-id="96751-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="96751-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="96751-127">Header</span><span class="sxs-lookup"><span data-stu-id="96751-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="96751-128"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="96751-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96751-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96751-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96751-130">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="96751-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="96751-131">Informationen über die Sequencer-Quelle</span><span class="sxs-lookup"><span data-stu-id="96751-131">About the Sequencer Source</span></span>](about-the-sequencer-source.md)
</dt> <dt>

[<span data-ttu-id="96751-132">Sequencer-Quell Ereignisse</span><span class="sxs-lookup"><span data-stu-id="96751-132">Sequencer Source Events</span></span>](sequencer-source-events.md)
</dt> </dl>

 

 




