---
description: Wird von einer Medienquelle ausgelöst, wenn eine Präsentation endet. Dieses Ereignis signalisiert, dass alle Datenströme in der Präsentation vollständig sind. Die Medien Sitzung leitet dieses Ereignis an die Anwendung weiter.
ms.assetid: 259b00ae-a91b-461b-a12f-f7291ecc04ff
title: Meendofpresentation-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5e3a904725908d83afd54bbd64012420075037a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350558"
---
# <a name="meendofpresentation-event"></a><span data-ttu-id="07d7c-105">Meendof Presentation-Ereignis</span><span class="sxs-lookup"><span data-stu-id="07d7c-105">MEEndOfPresentation event</span></span>

<span data-ttu-id="07d7c-106">Wird von einer Medienquelle ausgelöst, wenn eine Präsentation endet.</span><span class="sxs-lookup"><span data-stu-id="07d7c-106">Raised by a media source when a presentation ends.</span></span> <span data-ttu-id="07d7c-107">Dieses Ereignis signalisiert, dass alle Datenströme in der Präsentation vollständig sind.</span><span class="sxs-lookup"><span data-stu-id="07d7c-107">This event signals that all streams in the presentation are complete.</span></span> <span data-ttu-id="07d7c-108">Die Medien Sitzung leitet dieses Ereignis an die Anwendung weiter.</span><span class="sxs-lookup"><span data-stu-id="07d7c-108">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="07d7c-109">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="07d7c-109">Event values</span></span>

<span data-ttu-id="07d7c-110">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="07d7c-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="07d7c-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="07d7c-111">VARTYPE</span></span>              | <span data-ttu-id="07d7c-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07d7c-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="07d7c-113">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="07d7c-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="07d7c-114">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="07d7c-114">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="07d7c-115">Attribute</span><span class="sxs-lookup"><span data-stu-id="07d7c-115">Attributes</span></span>

<span data-ttu-id="07d7c-116">Für dieses Ereignis sind die folgenden Attribute definiert:</span><span class="sxs-lookup"><span data-stu-id="07d7c-116">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="07d7c-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="07d7c-117">Attribute</span></span>                                                                                               | <span data-ttu-id="07d7c-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07d7c-118">Description</span></span>                                                                               |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="07d7c-119">**die MF- \_ Ereignis \_ Quell \_ Topologie wurde \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="07d7c-119">**MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED**</span></span>](mf-event-source-topology-canceled-attribute.md)<br/> | <span data-ttu-id="07d7c-120">Gibt an, ob die Sequencer-Quelle diese Präsentation abgebrochen hat.</span><span class="sxs-lookup"><span data-stu-id="07d7c-120">Specifies whether the sequencer source canceled this presentation.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="07d7c-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07d7c-121">Requirements</span></span>



| <span data-ttu-id="07d7c-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07d7c-122">Requirement</span></span> | <span data-ttu-id="07d7c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="07d7c-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07d7c-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="07d7c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="07d7c-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="07d7c-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="07d7c-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="07d7c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="07d7c-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="07d7c-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="07d7c-128">Header</span><span class="sxs-lookup"><span data-stu-id="07d7c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="07d7c-129"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="07d7c-129"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07d7c-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07d7c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07d7c-131">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="07d7c-131">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




