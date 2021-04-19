---
description: Gibt an, wann eine Transformation geleert wird.
ms.assetid: 1e87f58f-546f-4dd4-b218-1458ff17db53
title: MF_TOPONODE_FLUSH-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cea241227d70d967f6f41ccd994176e9ddbbacbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356544"
---
# <a name="mf_toponode_flush-attribute"></a><span data-ttu-id="0f828-103">MF- \_ Attribut "toponode \_ Flush"</span><span class="sxs-lookup"><span data-stu-id="0f828-103">MF\_TOPONODE\_FLUSH attribute</span></span>

<span data-ttu-id="0f828-104">Gibt an, wann eine Transformation geleert wird.</span><span class="sxs-lookup"><span data-stu-id="0f828-104">Specifies when a transform is flushed.</span></span>

## <a name="data-type"></a><span data-ttu-id="0f828-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0f828-105">Data type</span></span>

<span data-ttu-id="0f828-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0f828-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="0f828-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0f828-107">Remarks</span></span>

<span data-ttu-id="0f828-108">Dieses Attribut gilt für Transformations Knoten (**MF- \_ topologietransformations- \_ \_ Knoten**).</span><span class="sxs-lookup"><span data-stu-id="0f828-108">This attribute applies to transform nodes (**MF\_TOPOLOGY\_TRANSFORM\_NODE**).</span></span>

<span data-ttu-id="0f828-109">Der Wert des-Attributs ist ein Member der [**MF- \_ toponode \_ \_**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_flush_mode) -Leerungs Modus-Enumeration.</span><span class="sxs-lookup"><span data-stu-id="0f828-109">The value of the attribute is a member of the [**MF\_TOPONODE\_FLUSH\_MODE**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_flush_mode) enumeration.</span></span> <span data-ttu-id="0f828-110">Wenn dieses Attribut nicht festgelegt ist, lautet der Standardwert " **MF \_ toponode \_ Flush \_ Always**".</span><span class="sxs-lookup"><span data-stu-id="0f828-110">If this attribute is not set, the default value is **MF\_TOPONODE\_FLUSH\_ALWAYS**.</span></span>

<span data-ttu-id="0f828-111">Das leeren erfolgt durch Aufrufen von [**imftransform::P rocess Message**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) für die Transformation mit der [**MFT- \_ \_ nachrichtenbefehlsleerungs \_**](mft-message-command-flush.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="0f828-111">Flushing is performed by calling [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) on the transform with the [**MFT\_MESSAGE\_COMMAND\_FLUSH**](mft-message-command-flush.md) message.</span></span> <span data-ttu-id="0f828-112">Weitere Informationen finden Sie unter [**MFT \_ Message \_ Type**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type) Enumeration.</span><span class="sxs-lookup"><span data-stu-id="0f828-112">For more information, see [**MFT\_MESSAGE\_TYPE**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type) enumeration.</span></span>

<span data-ttu-id="0f828-113">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="0f828-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f828-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f828-114">Requirements</span></span>



| <span data-ttu-id="0f828-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f828-115">Requirement</span></span> | <span data-ttu-id="0f828-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0f828-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0f828-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0f828-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0f828-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f828-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0f828-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0f828-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0f828-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f828-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0f828-121">Header</span><span class="sxs-lookup"><span data-stu-id="0f828-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f828-122"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f828-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f828-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f828-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f828-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="0f828-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0f828-125">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="0f828-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="0f828-126">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="0f828-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="0f828-127">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="0f828-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="0f828-128">Topologieknotenattribute</span><span class="sxs-lookup"><span data-stu-id="0f828-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




