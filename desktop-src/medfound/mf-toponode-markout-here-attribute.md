---
description: Gibt an, ob die Pipeline auf diesem Knoten ein Markierungszeichen anwendet. Markierung ist der Punkt, an dem eine Präsentation endet. Wenn Pipeline Komponenten Daten über den Markierungs Punkt hinaus generieren, werden die Daten nicht gerendert.
ms.assetid: adf2361a-90c7-4650-a486-5c450a41ab54
title: MF_TOPONODE_MARKOUT_HERE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c5dc21f39f45aa04860f3374bead54d260f0821
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349063"
---
# <a name="mf_toponode_markout_here-attribute"></a><span data-ttu-id="4a1be-105">MF- \_ Attribut "toponode \_ markout \_ here"</span><span class="sxs-lookup"><span data-stu-id="4a1be-105">MF\_TOPONODE\_MARKOUT\_HERE attribute</span></span>

<span data-ttu-id="4a1be-106">Gibt an, ob die Pipeline auf diesem Knoten ein Markierungszeichen anwendet.</span><span class="sxs-lookup"><span data-stu-id="4a1be-106">Specifies whether the pipeline applies mark-out at this node.</span></span> <span data-ttu-id="4a1be-107">Markierung ist der Punkt, an dem eine Präsentation endet.</span><span class="sxs-lookup"><span data-stu-id="4a1be-107">Mark-out is the point where a presentation ends.</span></span> <span data-ttu-id="4a1be-108">Wenn Pipeline Komponenten Daten über den Markierungs Punkt hinaus generieren, werden die Daten nicht gerendert.</span><span class="sxs-lookup"><span data-stu-id="4a1be-108">If pipeline components generate data past the mark-out point, the data is not rendered.</span></span>

## <a name="data-type"></a><span data-ttu-id="4a1be-109">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4a1be-109">Data type</span></span>

<span data-ttu-id="4a1be-110">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4a1be-110">**UINT32**</span></span>

<span data-ttu-id="4a1be-111">Als booleschen Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="4a1be-111">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a1be-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a1be-112">Remarks</span></span>

<span data-ttu-id="4a1be-113">Dieses Attribut gilt für alle Knoten Typen.</span><span class="sxs-lookup"><span data-stu-id="4a1be-113">This attribute applies to all node types.</span></span>

<span data-ttu-id="4a1be-114">Wenn dieses Attribut **true** ist, schneidet die Media Foundation Pipeline die Ausgabe Beispiele von diesem Knoten ab, sodass Sie mit der Endzeit der Präsentation verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="4a1be-114">If this attribute is **TRUE**, the Media Foundation pipeline trims the output samples from this node to match the stop time for the presentation.</span></span> <span data-ttu-id="4a1be-115">Das topologielader legt dieses Attribut fest, wenn es eine Topologie auflöst.</span><span class="sxs-lookup"><span data-stu-id="4a1be-115">The topology loader sets this attribute when it resolves a topology.</span></span> <span data-ttu-id="4a1be-116">Die meisten Anwendungen müssen dieses Attribut nicht festlegen oder abrufen.</span><span class="sxs-lookup"><span data-stu-id="4a1be-116">Most applications do not need to set or retrieve this attribute.</span></span>

<span data-ttu-id="4a1be-117">Es wird empfohlen, dass für genau einen Knoten in jeder Verzweigung der Topologie dieses Attribut auf " **true**" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4a1be-117">It is recommended that exactly one node in every branch of the topology should have this attribute set to **TRUE**.</span></span> <span data-ttu-id="4a1be-118">Eine topologieverzweigung ist als Pfad von einem Quellknoten zu einem Ausgabe Knoten definiert.</span><span class="sxs-lookup"><span data-stu-id="4a1be-118">A topology branch is defined as the path from a source node to an output node.</span></span> <span data-ttu-id="4a1be-119">Innerhalb einer Verzweigung müssen die \_ Attribute "MF toponode \_ markout \_ here" und " [MF \_ toponode \_ Markin \_ here](mf-toponode-markin-here-attribute.md) " für denselben Knoten in der Verzweigung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4a1be-119">Within a branch, the MF\_TOPONODE\_MARKOUT\_HERE and [MF\_TOPONODE\_MARKIN\_HERE](mf-toponode-markin-here-attribute.md) attributes must be set on the same node in the branch.</span></span> <span data-ttu-id="4a1be-120">Sie können nicht auf verschiedenen Knoten innerhalb desselben branches festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4a1be-120">They cannot be set on different nodes within the same branch.</span></span>

<span data-ttu-id="4a1be-121">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="4a1be-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a1be-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a1be-122">Requirements</span></span>



| <span data-ttu-id="4a1be-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a1be-123">Requirement</span></span> | <span data-ttu-id="4a1be-124">Wert</span><span class="sxs-lookup"><span data-stu-id="4a1be-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4a1be-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4a1be-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4a1be-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a1be-126">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4a1be-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4a1be-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4a1be-128">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a1be-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4a1be-129">Header</span><span class="sxs-lookup"><span data-stu-id="4a1be-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a1be-130"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a1be-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a1be-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a1be-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a1be-132">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="4a1be-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4a1be-133">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="4a1be-133">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="4a1be-134">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="4a1be-134">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="4a1be-135">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="4a1be-135">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="4a1be-136">**Hier finden Sie ein MF- \_ toponode- \_ Markin \_**</span><span class="sxs-lookup"><span data-stu-id="4a1be-136">**MF\_TOPONODE\_MARKIN\_HERE**</span></span>](mf-toponode-markin-here-attribute.md)
</dt> <dt>

[<span data-ttu-id="4a1be-137">Topologieknotenattribute</span><span class="sxs-lookup"><span data-stu-id="4a1be-137">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




