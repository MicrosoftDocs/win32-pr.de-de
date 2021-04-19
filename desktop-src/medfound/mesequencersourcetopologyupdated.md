---
description: 'Wird von der Sequencer-Quelle ausgelöst, wenn die IMF sequencersource:: updatetopology-Methode asynchron abgeschlossen wird.'
ms.assetid: f573cbd0-689c-4bfe-846b-6fc8008101c8
title: Mesequendcersourcetopologyaktualisierte-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baaf03119832937a584178b9f5958b066046c633
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353198"
---
# <a name="mesequencersourcetopologyupdated-event"></a><span data-ttu-id="db17a-103">Mesequendcersourcetopologyaktualisierte-Ereignis</span><span class="sxs-lookup"><span data-stu-id="db17a-103">MESequencerSourceTopologyUpdated event</span></span>

<span data-ttu-id="db17a-104">Wird von der Sequencer-Quelle ausgelöst, wenn die [**IMF sequencersource:: updatetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) -Methode asynchron abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="db17a-104">Raised by the sequencer source when the [**IMFSequencerSource::UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="db17a-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="db17a-105">Event values</span></span>

<span data-ttu-id="db17a-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="db17a-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="db17a-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="db17a-107">VARTYPE</span></span>            | <span data-ttu-id="db17a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="db17a-108">Description</span></span>                                                                                                                                                                                                                        |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db17a-109">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="db17a-109">VT\_UI4</span></span><br/> | <span data-ttu-id="db17a-110">Der Sequencer-Element Bezeichner der Topologie, die aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="db17a-110">Sequencer element identifier of the topology that is being updated.</span></span> <span data-ttu-id="db17a-111">Die Anwendung gibt diesen Wert im *dwID* -Parameter der [**updatetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) -Methode an.</span><span class="sxs-lookup"><span data-stu-id="db17a-111">The application specifies this value in the *dwId* parameter of the [**UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) method.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="db17a-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db17a-112">Remarks</span></span>

<span data-ttu-id="db17a-113">Dieses Ereignis signalisiert, dass die Sequencer-Quelle die Topologie aktualisiert hat, bedeutet jedoch nicht, dass die Topologie für die Wiedergabe bereit ist.</span><span class="sxs-lookup"><span data-stu-id="db17a-113">This event signals that the sequencer source has updated the topology, but does not mean that the topology is ready for playback.</span></span> <span data-ttu-id="db17a-114">Die Anwendung sollte auf das Ereignis [mesessiontopologystatus](mesessiontopologystatus.md) warten.</span><span class="sxs-lookup"><span data-stu-id="db17a-114">The application should wait for the [MESessionTopologyStatus](mesessiontopologystatus.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="db17a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db17a-115">Requirements</span></span>



| <span data-ttu-id="db17a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db17a-116">Requirement</span></span> | <span data-ttu-id="db17a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="db17a-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db17a-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="db17a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="db17a-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db17a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="db17a-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="db17a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="db17a-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db17a-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="db17a-122">Header</span><span class="sxs-lookup"><span data-stu-id="db17a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="db17a-123"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="db17a-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db17a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db17a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db17a-125">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="db17a-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="db17a-126">Sequencer-Quelle</span><span class="sxs-lookup"><span data-stu-id="db17a-126">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 




