---
description: Gibt an, wann eine Transformation entladen wird.
ms.assetid: 68332106-d1fe-467b-8baa-1e592b9cc243
title: MF_TOPONODE_DRAIN-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 679b87d626738b82f4504673392bd0fe159e2722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350500"
---
# <a name="mf_toponode_drain-attribute"></a><span data-ttu-id="0176e-103">MF- \_ toponode-Attribut zum Entfernen \_</span><span class="sxs-lookup"><span data-stu-id="0176e-103">MF\_TOPONODE\_DRAIN attribute</span></span>

<span data-ttu-id="0176e-104">Gibt an, wann eine Transformation entladen wird.</span><span class="sxs-lookup"><span data-stu-id="0176e-104">Specifies when a transform is drained.</span></span>

## <a name="data-type"></a><span data-ttu-id="0176e-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0176e-105">Data type</span></span>

<span data-ttu-id="0176e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0176e-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="0176e-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0176e-107">Remarks</span></span>

<span data-ttu-id="0176e-108">Dieses Attribut gilt für Transformations Knoten (**MF- \_ topologietransformations- \_ \_ Knoten**).</span><span class="sxs-lookup"><span data-stu-id="0176e-108">This attribute applies to transform nodes (**MF\_TOPOLOGY\_TRANSFORM\_NODE**).</span></span>

<span data-ttu-id="0176e-109">Der Wert des-Attributs ist ein Member der [**MF- \_ toponode-Ausgleichs \_ \_ Modus**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_drain_mode) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="0176e-109">The value of the attribute is a member of the [**MF\_TOPONODE\_DRAIN\_MODE**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_drain_mode) enumeration.</span></span> <span data-ttu-id="0176e-110">Wenn dieses Attribut nicht festgelegt ist, ist der Standardwert **MF \_ toponode- \_ \_ Standard** Wert.</span><span class="sxs-lookup"><span data-stu-id="0176e-110">If this attribute is not set, the default value is **MF\_TOPONODE\_DRAIN\_DEFAULT**.</span></span>

<span data-ttu-id="0176e-111">Die Ableitung erfolgt durch Aufrufen von [**imftransform::P rocess Message**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) für die Transformation mit der [**MFT- \_ Nachrichten \_ Befehls \_**](mft-message-command-drain.md) Ausgleichs Nachricht.</span><span class="sxs-lookup"><span data-stu-id="0176e-111">Draining is performed by calling [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) on the transform with the [**MFT\_MESSAGE\_COMMAND\_DRAIN**](mft-message-command-drain.md) message.</span></span> <span data-ttu-id="0176e-112">Weitere Informationen finden Sie unter [**MFT \_ Message \_ Type**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type) Enumeration.</span><span class="sxs-lookup"><span data-stu-id="0176e-112">For more information, see [**MFT\_MESSAGE\_TYPE**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type) enumeration.</span></span>

<span data-ttu-id="0176e-113">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="0176e-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0176e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0176e-114">Requirements</span></span>



| <span data-ttu-id="0176e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0176e-115">Requirement</span></span> | <span data-ttu-id="0176e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0176e-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0176e-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0176e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0176e-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0176e-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0176e-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0176e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0176e-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0176e-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0176e-121">Header</span><span class="sxs-lookup"><span data-stu-id="0176e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0176e-122"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0176e-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0176e-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0176e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0176e-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="0176e-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0176e-125">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="0176e-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="0176e-126">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="0176e-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="0176e-127">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="0176e-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="0176e-128">Topologieknotenattribute</span><span class="sxs-lookup"><span data-stu-id="0176e-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




