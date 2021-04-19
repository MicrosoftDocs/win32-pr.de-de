---
description: Gibt an, ob die Pipeline auf diesem Knoten ein Markierungszeichen anwendet.
ms.assetid: 406145e8-e00e-460d-b282-85face457605
title: MF_TOPONODE_MARKIN_HERE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efa355cc070a7371ff2e294b3ca3ad558a4749b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348463"
---
# <a name="mf_toponode_markin_here-attribute"></a><span data-ttu-id="e3ba1-103">Attribut "MF \_ toponode \_ Markin this" \_</span><span class="sxs-lookup"><span data-stu-id="e3ba1-103">MF\_TOPONODE\_MARKIN\_HERE attribute</span></span>

<span data-ttu-id="e3ba1-104">Gibt an, ob die Pipeline auf diesem Knoten ein Markierungszeichen anwendet.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-104">Specifies whether the pipeline applies mark-in at this node.</span></span> <span data-ttu-id="e3ba1-105">Mark-in ist der Punkt, an dem eine Präsentation beginnt.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-105">Mark-in is the point where a presentation starts.</span></span> <span data-ttu-id="e3ba1-106">Wenn Pipeline Komponenten Daten vor dem Markierungs Punkt generieren, werden die Daten nicht gerendert.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-106">If pipeline components generate data before the mark-in point, the data is not rendered.</span></span>

## <a name="data-type"></a><span data-ttu-id="e3ba1-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e3ba1-107">Data type</span></span>

<span data-ttu-id="e3ba1-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e3ba1-108">**UINT32**</span></span>

<span data-ttu-id="e3ba1-109">Als booleschen Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-109">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3ba1-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3ba1-110">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e3ba1-111">Die meisten Anwendungen müssen dieses Attribut nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-111">Most applications do not need to use this attribute.</span></span> <span data-ttu-id="e3ba1-112">Das Attribut wird bei Bedarf automatisch von der [Medien Sitzung](media-session.md) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-112">The [Media Session](media-session.md) automatically sets this attribute if needed.</span></span>

 

<span data-ttu-id="e3ba1-113">Dieses Attribut gilt für alle Knoten Typen.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-113">This attribute applies to all node types.</span></span> <span data-ttu-id="e3ba1-114">Wenn das Attribut **true** ist, schneidet die Media Foundation Pipeline die Ausgabe Beispiele von diesem Knoten ab, sodass Sie mit der Startzeit der Präsentation identisch sind.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-114">If the attribute is **TRUE**, the Media Foundation pipeline trims the output samples from this node to match the start time for the presentation.</span></span> <span data-ttu-id="e3ba1-115">Das topologielader legt dieses Attribut fest, wenn es eine Topologie auflöst.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-115">The topology loader sets this attribute when it resolves a topology.</span></span>

<span data-ttu-id="e3ba1-116">Es wird empfohlen, dass für genau einen Knoten in jeder Verzweigung der Topologie dieses Attribut auf " **true**" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-116">It is recommended that exactly one node in every branch of the topology should have this attribute set to **TRUE**.</span></span> <span data-ttu-id="e3ba1-117">Eine topologieverzweigung ist als Pfad von einem Quellknoten zu einem Ausgabe Knoten definiert.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-117">A topology branch is defined as the path from a source node to an output node.</span></span> <span data-ttu-id="e3ba1-118">Innerhalb einer Verzweigung müssen die Attribute " [MF \_ toponode \_ markout \_ here](mf-toponode-markout-here-attribute.md) " und "MF \_ toponode \_ Markin \_ here" für denselben Knoten in der Verzweigung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-118">Within a branch, the [MF\_TOPONODE\_MARKOUT\_HERE](mf-toponode-markout-here-attribute.md) and MF\_TOPONODE\_MARKIN\_HERE attributes must be set on the same node in the branch.</span></span> <span data-ttu-id="e3ba1-119">Sie können nicht auf verschiedenen Knoten innerhalb desselben branches festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-119">They cannot be set on different nodes within the same branch.</span></span>

<span data-ttu-id="e3ba1-120">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3ba1-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3ba1-121">Requirements</span></span>



| <span data-ttu-id="e3ba1-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3ba1-122">Requirement</span></span> | <span data-ttu-id="e3ba1-123">Wert</span><span class="sxs-lookup"><span data-stu-id="e3ba1-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e3ba1-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e3ba1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e3ba1-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3ba1-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e3ba1-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e3ba1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e3ba1-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3ba1-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e3ba1-128">Header</span><span class="sxs-lookup"><span data-stu-id="e3ba1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3ba1-129"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3ba1-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3ba1-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3ba1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3ba1-131">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="e3ba1-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e3ba1-132">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="e3ba1-132">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="e3ba1-133">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="e3ba1-133">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="e3ba1-134">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="e3ba1-134">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="e3ba1-135">**MF \_ toponode \_ markout \_ hier**</span><span class="sxs-lookup"><span data-stu-id="e3ba1-135">**MF\_TOPONODE\_MARKOUT\_HERE**</span></span>](mf-toponode-markout-here-attribute.md)
</dt> <dt>

[<span data-ttu-id="e3ba1-136">Topologieknotenattribute</span><span class="sxs-lookup"><span data-stu-id="e3ba1-136">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




