---
description: Gibt das Element an, das diesen Quellknoten enthält.
ms.assetid: f5fa5c10-8f30-43bd-8054-a39996f807a3
title: MF_TOPONODE_SEQUENCE_ELEMENTID-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3cd2c66c40a0bc3776d2fd2b7d78535cf24b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345172"
---
# <a name="mf_toponode_sequence_elementid-attribute"></a><span data-ttu-id="85e0a-103">\_ \_ \_ ElementId-Attribut der MF-toponode-Sequenz</span><span class="sxs-lookup"><span data-stu-id="85e0a-103">MF\_TOPONODE\_SEQUENCE\_ELEMENTID attribute</span></span>

<span data-ttu-id="85e0a-104">Gibt das Element an, das diesen Quellknoten enthält.</span><span class="sxs-lookup"><span data-stu-id="85e0a-104">Specifies the element that contains this source node.</span></span>

## <a name="data-type"></a><span data-ttu-id="85e0a-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="85e0a-105">Data type</span></span>

<span data-ttu-id="85e0a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="85e0a-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="85e0a-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85e0a-107">Remarks</span></span>

<span data-ttu-id="85e0a-108">Dieses Attribut gilt für Quellknoten (**MF- \_ Topologie \_ sourcestream- \_ Knoten**).</span><span class="sxs-lookup"><span data-stu-id="85e0a-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span>

<span data-ttu-id="85e0a-109">Die Medien Pipeline verwendet dieses Attribut, um zu ermitteln, wann Medienquellen Teil desselben Elements sind.</span><span class="sxs-lookup"><span data-stu-id="85e0a-109">The media pipeline uses this attribute to discover when media sources are part of the same element.</span></span> <span data-ttu-id="85e0a-110">Die Pipeline behandelt alle Quellknoten, die Teil desselben Elements sind, mit derselben Uhr.</span><span class="sxs-lookup"><span data-stu-id="85e0a-110">The pipeline treats all source nodes that are part of the same element as having the same clock.</span></span>

<span data-ttu-id="85e0a-111">Wenn die Pipeline eine neue Topologie in die Warteschlange stellt, die Quellknoten enthält, die Teil eines in der vorherigen Topologie vorhandenen Elements sind, behandelt die Pipeline diese Quellknoten als dieselbe Uhr wie die Quellknoten von diesem Element in der vorherigen Topologie.</span><span class="sxs-lookup"><span data-stu-id="85e0a-111">When the pipeline queues up a new topology that contains source nodes that are part of an element that is present in the previous topology, the pipeline treats these source nodes as having the same clock as the source nodes from that element in the previous topology.</span></span>

> [!Note]  
> <span data-ttu-id="85e0a-112">Die Medien Pipeline korrigiert Zeitstempel für Quellknoten mit unterschiedlichen Takt Raten nicht.</span><span class="sxs-lookup"><span data-stu-id="85e0a-112">The media pipeline does not correct time stamps for source nodes with different clock rates.</span></span>

 

<span data-ttu-id="85e0a-113">Eine Medienquelle, die Topologien bereitstellen kann, sollte die [**imfmediasourcetopologyprovider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) -Schnittstelle oder die [**imfsequencersource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="85e0a-113">A media source that can provide topologies should implement the [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) interface or the [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) interface.</span></span> <span data-ttu-id="85e0a-114">Eine Medienquelle, die Topologien bereitstellt, sollte das **Element "MF \_ toponode \_ Sequence \_ elementId** " für jeden Quellknoten festlegen, den Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="85e0a-114">A media source that provides topologies should set the **MF\_TOPONODE\_SEQUENCE\_ELEMENTID** attribute on every source node that it creates.</span></span>

<span data-ttu-id="85e0a-115">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="85e0a-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="85e0a-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85e0a-116">Requirements</span></span>



| <span data-ttu-id="85e0a-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85e0a-117">Requirement</span></span> | <span data-ttu-id="85e0a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="85e0a-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="85e0a-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="85e0a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="85e0a-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85e0a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="85e0a-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="85e0a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="85e0a-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85e0a-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="85e0a-123">Header</span><span class="sxs-lookup"><span data-stu-id="85e0a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="85e0a-124"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="85e0a-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85e0a-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85e0a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85e0a-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="85e0a-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="85e0a-127">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="85e0a-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="85e0a-128">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="85e0a-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="85e0a-129">**Imfmediasourcetopologyprovider**</span><span class="sxs-lookup"><span data-stu-id="85e0a-129">**IMFMediaSourceTopologyProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
</dt> <dt>

[<span data-ttu-id="85e0a-130">**IMF sequencersource**</span><span class="sxs-lookup"><span data-stu-id="85e0a-130">**IMFSequencerSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)
</dt> <dt>

[<span data-ttu-id="85e0a-131">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="85e0a-131">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="85e0a-132">Topologieknotenattribute</span><span class="sxs-lookup"><span data-stu-id="85e0a-132">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="85e0a-133">Sequencer-Quelle</span><span class="sxs-lookup"><span data-stu-id="85e0a-133">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 




