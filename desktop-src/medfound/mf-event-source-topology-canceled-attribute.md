---
description: Gibt an, ob die Sequencer-Quelle eine Topologie abgebrochen hat.
ms.assetid: b7252336-1612-43fc-8f08-1fdfdbb293eb
title: MF_EVENT_SOURCE_TOPOLOGY_CANCELED-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2a161aec292d834b0418f59f1c26ea2f11a538e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366249"
---
# <a name="mf_event_source_topology_canceled-attribute"></a><span data-ttu-id="3c966-103">Attribut der MF- \_ Ereignis \_ Quell \_ Topologie wurde \_ abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="3c966-103">MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED attribute</span></span>

<span data-ttu-id="3c966-104">Gibt an, ob die [Sequencer-Quelle](sequencer-source.md) eine Topologie abgebrochen hat.</span><span class="sxs-lookup"><span data-stu-id="3c966-104">Specifies whether the [Sequencer Source](sequencer-source.md) canceled a topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="3c966-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="3c966-105">Data type</span></span>

<span data-ttu-id="3c966-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3c966-106">**UINT32**</span></span>

<span data-ttu-id="3c966-107">Als booleschen Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="3c966-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c966-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c966-108">Remarks</span></span>

<span data-ttu-id="3c966-109">Dieses Attribut wird mit den folgenden Ereignissen verwendet:</span><span class="sxs-lookup"><span data-stu-id="3c966-109">This attribute is used with the following events:</span></span>

-   [<span data-ttu-id="3c966-110">Meendof presentationsegment</span><span class="sxs-lookup"><span data-stu-id="3c966-110">MEEndOfPresentationSegment</span></span>](meendofpresentationsegment.md)
-   [<span data-ttu-id="3c966-111">Meendof Presentation</span><span class="sxs-lookup"><span data-stu-id="3c966-111">MEEndOfPresentation</span></span>](meendofpresentation.md)

<span data-ttu-id="3c966-112">Wenn dieses Attribut vorhanden und ungleich NULL ist, bedeutet dies, dass das Präsentations Segment beendet wurde, weil die Sequencer-Quelle die Topologie abgebrochen hat.</span><span class="sxs-lookup"><span data-stu-id="3c966-112">If this attribute is present and nonzero, it means that the presentation segment ended because the sequencer source canceled the topology.</span></span> <span data-ttu-id="3c966-113">Andernfalls wurde das Präsentations Segment normal beendet.</span><span class="sxs-lookup"><span data-stu-id="3c966-113">Otherwise, the presentation segment ended normally.</span></span>

<span data-ttu-id="3c966-114">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="3c966-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c966-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c966-115">Requirements</span></span>



| <span data-ttu-id="3c966-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c966-116">Requirement</span></span> | <span data-ttu-id="3c966-117">Wert</span><span class="sxs-lookup"><span data-stu-id="3c966-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3c966-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3c966-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3c966-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c966-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3c966-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3c966-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3c966-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c966-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3c966-122">Header</span><span class="sxs-lookup"><span data-stu-id="3c966-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c966-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c966-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c966-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c966-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c966-125">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="3c966-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3c966-126">Ereignisattribute</span><span class="sxs-lookup"><span data-stu-id="3c966-126">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="3c966-127">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="3c966-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="3c966-128">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="3c966-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="3c966-129">Sequencer-Quell Ereignisse</span><span class="sxs-lookup"><span data-stu-id="3c966-129">Sequencer Source Events</span></span>](sequencer-source-events.md)
</dt> </dl>

 

 




