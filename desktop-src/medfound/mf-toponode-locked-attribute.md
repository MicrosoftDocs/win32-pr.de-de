---
description: Gibt an, ob die Medientypen für diesen topologieknoten geändert werden können.
ms.assetid: 8805ed63-1408-40bc-bb82-f3c51576dfa4
title: MF_TOPONODE_LOCKED-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70776b1a5ba9c5c35cd2a2d97618de4b3a65abb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753168"
---
# <a name="mf_toponode_locked-attribute"></a><span data-ttu-id="4286f-103">MF- \_ Attribut "toponode \_ gesperrt"</span><span class="sxs-lookup"><span data-stu-id="4286f-103">MF\_TOPONODE\_LOCKED attribute</span></span>

<span data-ttu-id="4286f-104">Gibt an, ob die Medientypen für diesen topologieknoten geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="4286f-104">Specifies whether the media types can be changed on this topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="4286f-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4286f-105">Data type</span></span>

<span data-ttu-id="4286f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4286f-106">**UINT32**</span></span>

<span data-ttu-id="4286f-107">Als booleschen Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="4286f-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4286f-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4286f-108">Remarks</span></span>

<span data-ttu-id="4286f-109">Dieses Attribut gilt für alle Knoten Typen.</span><span class="sxs-lookup"><span data-stu-id="4286f-109">This attribute applies to all node types.</span></span>

<span data-ttu-id="4286f-110">Wenn der Wert dieses Attributs ungleich 0 (null) ist, werden die Medientypen vom topologielader nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="4286f-110">If value of this attribute is nonzero, the topology loader will not change the media types.</span></span> <span data-ttu-id="4286f-111">Dieses Attribut wird auf " **true** " festgelegt, wenn der Knoten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4286f-111">This attribute is set to **TRUE** when the node is in use.</span></span>

<span data-ttu-id="4286f-112">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="4286f-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4286f-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4286f-113">Requirements</span></span>



| <span data-ttu-id="4286f-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4286f-114">Requirement</span></span> | <span data-ttu-id="4286f-115">Wert</span><span class="sxs-lookup"><span data-stu-id="4286f-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4286f-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4286f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4286f-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4286f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4286f-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4286f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4286f-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4286f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4286f-120">Header</span><span class="sxs-lookup"><span data-stu-id="4286f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4286f-121"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4286f-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4286f-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4286f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4286f-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="4286f-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4286f-124">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="4286f-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="4286f-125">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="4286f-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="4286f-126">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="4286f-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="4286f-127">Topologieknotenattribute</span><span class="sxs-lookup"><span data-stu-id="4286f-127">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




