---
description: Wird von einer Medienquelle ausgelöst, die Topologien über die imfmediasourcetopologyprovider-Schnittstelle bereitstellt, z. b. die Sequencer-Quelle. Die Quelle löst das-Ereignis aus, wenn es eine neue Präsentation enthält. Die Medien Sitzung leitet dieses Ereignis an die Anwendung weiter.
ms.assetid: c669b2c9-5ece-4045-b691-8a71bbf491e1
title: Menewpresentation-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70265a84cc7724fc6f5b6a77be2181149bd82176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215168"
---
# <a name="menewpresentation-event"></a><span data-ttu-id="90b20-105">Menewpresentation-Ereignis</span><span class="sxs-lookup"><span data-stu-id="90b20-105">MENewPresentation event</span></span>

<span data-ttu-id="90b20-106">Wird von einer Medienquelle ausgelöst, die Topologien über die [**imfmediasourcetopologyprovider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) -Schnittstelle bereitstellt, z. b. die Sequencer-Quelle.</span><span class="sxs-lookup"><span data-stu-id="90b20-106">Raised by a media source that provides topologies through the [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) interface, such as the sequencer source.</span></span> <span data-ttu-id="90b20-107">Die Quelle löst das-Ereignis aus, wenn es eine neue Präsentation enthält.</span><span class="sxs-lookup"><span data-stu-id="90b20-107">The source raises the event when it has a new presentation.</span></span> <span data-ttu-id="90b20-108">Die Medien Sitzung leitet dieses Ereignis an die Anwendung weiter.</span><span class="sxs-lookup"><span data-stu-id="90b20-108">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="90b20-109">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="90b20-109">Event values</span></span>

<span data-ttu-id="90b20-110">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="90b20-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="90b20-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="90b20-111">VARTYPE</span></span>                | <span data-ttu-id="90b20-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="90b20-112">Description</span></span>                                                                                                                                                             |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90b20-113">VT \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="90b20-113">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="90b20-114">Ein Zeiger auf die [**imfpresentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) -Schnittstelle des Präsentations Deskriptors für die neue Präsentation.</span><span class="sxs-lookup"><span data-stu-id="90b20-114">Pointer to the [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface of the presentation descriptor for the new presentation.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="90b20-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90b20-115">Remarks</span></span>

<span data-ttu-id="90b20-116">Die Anwendung kann die Topologie abrufen, die dem Präsentations Deskriptor entspricht, indem [**imfmediasourcetopologyprovider:: getmediasourcetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) in der Medienquelle aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="90b20-116">The application can get the topology that corresponds to the presentation descriptor by calling [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) on the media source.</span></span> <span data-ttu-id="90b20-117">Die Anwendung kann dann die neue Topologie in der Medien Sitzung durch Aufrufen von [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)in eine Warteschlange stellen.</span><span class="sxs-lookup"><span data-stu-id="90b20-117">The application can then queue the new topology on the Media Session by calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span>

## <a name="requirements"></a><span data-ttu-id="90b20-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90b20-118">Requirements</span></span>



| <span data-ttu-id="90b20-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90b20-119">Requirement</span></span> | <span data-ttu-id="90b20-120">Wert</span><span class="sxs-lookup"><span data-stu-id="90b20-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90b20-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="90b20-121">Minimum supported client</span></span><br/> | <span data-ttu-id="90b20-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90b20-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="90b20-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="90b20-123">Minimum supported server</span></span><br/> | <span data-ttu-id="90b20-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90b20-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="90b20-125">Header</span><span class="sxs-lookup"><span data-stu-id="90b20-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="90b20-126"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="90b20-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90b20-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90b20-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90b20-128">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="90b20-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="90b20-129">Sequencer-Quelle</span><span class="sxs-lookup"><span data-stu-id="90b20-129">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 




