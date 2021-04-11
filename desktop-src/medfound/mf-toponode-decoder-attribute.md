---
description: Gibt an, ob ein dem Objekt zugrunde liegendes topologieknoten ein Decoder ist.
ms.assetid: b6d576dc-b12f-49bf-b938-db2c629df400
title: MF_TOPONODE_DECODER-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ab16d14a91608fb6b21c901e3fb055ce5e4dfbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218115"
---
# <a name="mf_toponode_decoder-attribute"></a><span data-ttu-id="ee128-103">MF- \_ toponode- \_ decoderattribut</span><span class="sxs-lookup"><span data-stu-id="ee128-103">MF\_TOPONODE\_DECODER attribute</span></span>

<span data-ttu-id="ee128-104">Gibt an, ob das zugrunde liegende Objekt eines topologieknotens ein Decoder ist.</span><span class="sxs-lookup"><span data-stu-id="ee128-104">Specifies whether a topology node's underlying object is a decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="ee128-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ee128-105">Data type</span></span>

<span data-ttu-id="ee128-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ee128-106">**UINT32**</span></span>

<span data-ttu-id="ee128-107">Als booleschen Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="ee128-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee128-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ee128-108">Remarks</span></span>

<span data-ttu-id="ee128-109">Dieses Attribut gilt für alle Knoten Typen.</span><span class="sxs-lookup"><span data-stu-id="ee128-109">This attribute applies to all node types.</span></span>

<span data-ttu-id="ee128-110">Wenn der Wert dieses Attributs ungleich 0 (null) ist, ist das zugrunde liegende Objekt des Knotens ein Decoder.</span><span class="sxs-lookup"><span data-stu-id="ee128-110">If the value of this attribute is nonzero, the node's underlying object is a decoder.</span></span>

<span data-ttu-id="ee128-111">Das topologielader legt dieses Attribut fest, wenn es einen decoderknoten erstellt.</span><span class="sxs-lookup"><span data-stu-id="ee128-111">The topology loader sets this attribute when it creates a decoder node.</span></span> <span data-ttu-id="ee128-112">Eine Anwendung sollte dieses Attribut festlegen, wenn die Anwendung der Topologie manuell einen Decoder hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="ee128-112">An application should set this attribute if the application manually adds a decoder to the topology.</span></span>

<span data-ttu-id="ee128-113">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="ee128-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee128-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee128-114">Requirements</span></span>



| <span data-ttu-id="ee128-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee128-115">Requirement</span></span> | <span data-ttu-id="ee128-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ee128-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ee128-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ee128-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ee128-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee128-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ee128-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ee128-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ee128-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee128-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ee128-121">Header</span><span class="sxs-lookup"><span data-stu-id="ee128-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee128-122"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee128-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee128-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee128-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee128-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="ee128-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ee128-125">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ee128-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="ee128-126">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ee128-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="ee128-127">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="ee128-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="ee128-128">Topologieknotenattribute</span><span class="sxs-lookup"><span data-stu-id="ee128-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




