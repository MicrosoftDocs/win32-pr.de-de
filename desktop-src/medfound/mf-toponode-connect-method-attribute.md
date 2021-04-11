---
description: Gibt an, wie der topologielader diesen topologieknoten verbindet und ob dieser Knoten optional ist.
ms.assetid: 8d70e1af-607b-47c3-9808-091c95fd05b7
title: MF_TOPONODE_CONNECT_METHOD-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3db5fef529ef451fa02ac4a29e62002b0a1996a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217843"
---
# <a name="mf_toponode_connect_method-attribute"></a><span data-ttu-id="9d001-103">MF \_ toponode \_ Connect- \_ Methoden Attribut</span><span class="sxs-lookup"><span data-stu-id="9d001-103">MF\_TOPONODE\_CONNECT\_METHOD attribute</span></span>

<span data-ttu-id="9d001-104">Gibt an, wie der topologielader diesen topologieknoten verbindet und ob dieser Knoten optional ist.</span><span class="sxs-lookup"><span data-stu-id="9d001-104">Specifies how the topology loader connects this topology node, and whether this node is optional.</span></span>

## <a name="data-type"></a><span data-ttu-id="9d001-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9d001-105">Data type</span></span>

<span data-ttu-id="9d001-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9d001-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="9d001-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d001-107">Remarks</span></span>

<span data-ttu-id="9d001-108">Dieses Attribut gilt für alle Knoten Typen.</span><span class="sxs-lookup"><span data-stu-id="9d001-108">This attribute applies to all node types.</span></span>

<span data-ttu-id="9d001-109">Der Attribut Wert ist ein bitweises **or** von-Flags aus der [**MF \_ Connect- \_ Methoden**](/windows/desktop/api/mfidl/ne-mfidl-mf_connect_method) Enumeration.</span><span class="sxs-lookup"><span data-stu-id="9d001-109">The attribute value is a bitwise **OR** of flags from the [**MF\_CONNECT\_METHOD**](/windows/desktop/api/mfidl/ne-mfidl-mf_connect_method) enumeration.</span></span> <span data-ttu-id="9d001-110">Wenn dieses Attribut nicht festgelegt ist, ist der Standardwert **MF \_ Connect \_ Allow \_ Decoder**.</span><span class="sxs-lookup"><span data-stu-id="9d001-110">If this attribute is not set, the default value is **MF\_CONNECT\_ALLOW\_DECODER**.</span></span>

<span data-ttu-id="9d001-111">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="9d001-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d001-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d001-112">Requirements</span></span>



| <span data-ttu-id="9d001-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d001-113">Requirement</span></span> | <span data-ttu-id="9d001-114">Wert</span><span class="sxs-lookup"><span data-stu-id="9d001-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9d001-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9d001-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9d001-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d001-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9d001-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9d001-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9d001-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d001-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9d001-119">Header</span><span class="sxs-lookup"><span data-stu-id="9d001-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d001-120"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d001-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d001-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d001-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d001-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="9d001-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9d001-123">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="9d001-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="9d001-124">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="9d001-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="9d001-125">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="9d001-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="9d001-126">Topologieknotenattribute</span><span class="sxs-lookup"><span data-stu-id="9d001-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




