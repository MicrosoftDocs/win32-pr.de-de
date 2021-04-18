---
description: Gibt an, ob die Medien Senke, die diesem topologieknoten zugeordnet ist, ratlos ist.
ms.assetid: 81ef7005-a9ab-4f26-bc39-68b27c4f92aa
title: MF_TOPONODE_RATELESS-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5c5ded4d8d09e8d45f766b03737954329c9202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345785"
---
# <a name="mf_toponode_rateless-attribute"></a><span data-ttu-id="b1abb-103">Attribut "MF- \_ toponode- \_ Attribut"</span><span class="sxs-lookup"><span data-stu-id="b1abb-103">MF\_TOPONODE\_RATELESS attribute</span></span>

<span data-ttu-id="b1abb-104">Gibt an, ob die Medien Senke, die diesem topologieknoten zugeordnet ist, ratlos ist.</span><span class="sxs-lookup"><span data-stu-id="b1abb-104">Specifies whether the media sink associated with this topology node is rateless.</span></span>

## <a name="data-type"></a><span data-ttu-id="b1abb-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b1abb-105">Data type</span></span>

<span data-ttu-id="b1abb-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b1abb-106">**UINT32**</span></span>

<span data-ttu-id="b1abb-107">Als booleschen Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="b1abb-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1abb-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1abb-108">Remarks</span></span>

<span data-ttu-id="b1abb-109">Dieses Attribut gilt für Ausgabe Knoten (**MF- \_ topologieausgabe- \_ \_ Knoten**).</span><span class="sxs-lookup"><span data-stu-id="b1abb-109">This attribute applies to output nodes (**MF\_TOPOLOGY\_OUTPUT\_NODE**).</span></span>

<span data-ttu-id="b1abb-110">Wenn der Wert dieses Attributs ungleich 0 (null) ist, behandelt die Medien Sitzung die Medien Senke als ratlose Senke, unabhängig davon, ob die Medien Senke das **mediasink \_** -Attribut zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b1abb-110">If the value of this attribute is nonzero, the Media Session treats the media sink as a rateless sink, regardless of whether the media sink returns the **MEDIASINK\_RATELESS** characteristic.</span></span> <span data-ttu-id="b1abb-111">Wenn dieses Attribut nicht festgelegt ist, wird davon ausgegangen, dass die Medien Senke nicht ratlos ist.</span><span class="sxs-lookup"><span data-stu-id="b1abb-111">If this attribute is not set, the media sink is assumed not to be rateless.</span></span>

<span data-ttu-id="b1abb-112">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="b1abb-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1abb-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1abb-113">Requirements</span></span>



| <span data-ttu-id="b1abb-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1abb-114">Requirement</span></span> | <span data-ttu-id="b1abb-115">Wert</span><span class="sxs-lookup"><span data-stu-id="b1abb-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b1abb-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b1abb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b1abb-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1abb-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b1abb-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b1abb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b1abb-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1abb-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b1abb-120">Header</span><span class="sxs-lookup"><span data-stu-id="b1abb-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1abb-121"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1abb-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1abb-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1abb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1abb-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="b1abb-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b1abb-124">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="b1abb-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="b1abb-125">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="b1abb-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="b1abb-126">**Imfmediasink:: getcharacteristics**</span><span class="sxs-lookup"><span data-stu-id="b1abb-126">**IMFMediaSink::GetCharacteristics**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics)
</dt> <dt>

[<span data-ttu-id="b1abb-127">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="b1abb-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="b1abb-128">Topologieknotenattribute</span><span class="sxs-lookup"><span data-stu-id="b1abb-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




