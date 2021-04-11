---
description: Gibt an, ob die Pipeline nur Stichproben Abtastungen
ms.assetid: 4ba66d18-3854-4994-9509-967303dc7d98
title: MF_TOPOLOGY_NO_MARKIN_MARKOUT-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03d7b0152798379406887619a3e691cc528a6993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215138"
---
# <a name="mf_topology_no_markin_markout-attribute"></a><span data-ttu-id="8fcda-103">MF- \_ Topologie \_ kein \_ Markin \_ markout-Attribut</span><span class="sxs-lookup"><span data-stu-id="8fcda-103">MF\_TOPOLOGY\_NO\_MARKIN\_MARKOUT attribute</span></span>

<span data-ttu-id="8fcda-104">Gibt an, ob die Pipeline nur Stichproben Abtastungen</span><span class="sxs-lookup"><span data-stu-id="8fcda-104">Specifies whether the pipeline trims samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="8fcda-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8fcda-105">Data type</span></span>

<span data-ttu-id="8fcda-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="8fcda-106">**UINT32**</span></span>

<span data-ttu-id="8fcda-107">Als booleschen Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="8fcda-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fcda-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8fcda-108">Remarks</span></span>

<span data-ttu-id="8fcda-109">Standardmäßig werden die Beispiele für die Pipeline mit den richtigen Präsentations Zeiten getestet.</span><span class="sxs-lookup"><span data-stu-id="8fcda-109">By default, the pipeline trims samples to match the correct presentation times.</span></span> <span data-ttu-id="8fcda-110">Die Kürzung erfolgt auf den topologieknoten, die über das [**MF- \_ toponode- \_ Markin \_ hier**](mf-toponode-markin-here-attribute.md) und die [**MF- \_ toponode- \_ markout \_**](mf-toponode-markout-here-attribute.md) -Attribute verfügen.</span><span class="sxs-lookup"><span data-stu-id="8fcda-110">Trimming is done at the topology nodes that have the [**MF\_TOPONODE\_MARKIN\_HERE**](mf-toponode-markin-here-attribute.md) and [**MF\_TOPONODE\_MARKOUT\_HERE**](mf-toponode-markout-here-attribute.md) attributes.</span></span> <span data-ttu-id="8fcda-111">Wenn die **MF- \_ Topologie \_ kein \_ Markin \_ markout** -Attribut für die Topologie auf **true** festgelegt ist, werden die Beispiele von der Pipeline nicht beschnitten, und die hier aufgeführten Attribute " **MF \_ toponode \_ Markin \_ here** " und " **MF \_ toponode \_ markout \_** " werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="8fcda-111">If the **MF\_TOPOLOGY\_NO\_MARKIN\_MARKOUT** attribute is set to **TRUE** on the topology, the pipeline does not trim samples, and the **MF\_TOPONODE\_MARKIN\_HERE** and **MF\_TOPONODE\_MARKOUT\_HERE** attributes are ignored.</span></span> <span data-ttu-id="8fcda-112">Wenn das Attribut nicht festgelegt ist oder den Wert **false** aufweist, werden die Beispiele für die Pipeline getestet.</span><span class="sxs-lookup"><span data-stu-id="8fcda-112">If the attribute is not set, or has the value **FALSE**, the pipeline trims samples.</span></span>

<span data-ttu-id="8fcda-113">Eine Anwendung kann die **MF- \_ Topologie \_ kein \_ Markin \_ markout** -Attribut auf " **true** " festlegen, wenn die Anwendung komprimierte Beispiele von der Pipeline empfängt und alle Keyframes erhalten muss, die andernfalls gekürzt werden.</span><span class="sxs-lookup"><span data-stu-id="8fcda-113">An application might set the **MF\_TOPOLOGY\_NO\_MARKIN\_MARKOUT** attribute to **TRUE** if the application receives compressed samples from the pipeline and needs to get all of the key frames, which might otherwise be trimmed.</span></span>

<span data-ttu-id="8fcda-114">Der Standardwert dieses Attributs ist **false**.</span><span class="sxs-lookup"><span data-stu-id="8fcda-114">The default value of this attribute is **FALSE**.</span></span>

<span data-ttu-id="8fcda-115">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="8fcda-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fcda-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8fcda-116">Requirements</span></span>



| <span data-ttu-id="8fcda-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8fcda-117">Requirement</span></span> | <span data-ttu-id="8fcda-118">Wert</span><span class="sxs-lookup"><span data-stu-id="8fcda-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8fcda-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8fcda-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8fcda-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8fcda-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8fcda-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8fcda-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8fcda-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8fcda-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8fcda-123">Header</span><span class="sxs-lookup"><span data-stu-id="8fcda-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fcda-124"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fcda-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fcda-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8fcda-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fcda-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="8fcda-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8fcda-127">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="8fcda-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="8fcda-128">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="8fcda-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="8fcda-129">**Hier finden Sie ein MF- \_ toponode- \_ Markin \_**</span><span class="sxs-lookup"><span data-stu-id="8fcda-129">**MF\_TOPONODE\_MARKIN\_HERE**</span></span>](mf-toponode-markin-here-attribute.md)
</dt> <dt>

[<span data-ttu-id="8fcda-130">**MF \_ toponode \_ markout \_ hier**</span><span class="sxs-lookup"><span data-stu-id="8fcda-130">**MF\_TOPONODE\_MARKOUT\_HERE**</span></span>](mf-toponode-markout-here-attribute.md)
</dt> <dt>

[<span data-ttu-id="8fcda-131">Topologieattribute</span><span class="sxs-lookup"><span data-stu-id="8fcda-131">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




