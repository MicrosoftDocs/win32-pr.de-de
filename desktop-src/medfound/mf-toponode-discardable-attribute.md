---
description: Gibt an, ob die Pipeline Beispiele von einem topologieknoten ablegen kann.
ms.assetid: 8be20446-4876-4d6f-b0db-2eb1ffaef9aa
title: MF_TOPONODE_DISCARDABLE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d76e00a0f70735211cf06aca0adc00238ae5c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363740"
---
# <a name="mf_toponode_discardable-attribute"></a><span data-ttu-id="99c80-103">Zu \_ verwerfbares MF-toponode- \_ Attribut</span><span class="sxs-lookup"><span data-stu-id="99c80-103">MF\_TOPONODE\_DISCARDABLE attribute</span></span>

<span data-ttu-id="99c80-104">Gibt an, ob die Pipeline Beispiele von einem topologieknoten ablegen kann.</span><span class="sxs-lookup"><span data-stu-id="99c80-104">Specifies whether the pipeline can drop samples from a topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="99c80-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="99c80-105">Data type</span></span>

<span data-ttu-id="99c80-106">Bytearray</span><span class="sxs-lookup"><span data-stu-id="99c80-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="99c80-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="99c80-107">Remarks</span></span>

<span data-ttu-id="99c80-108">Dieses Attribut gilt für alle Knoten Typen.</span><span class="sxs-lookup"><span data-stu-id="99c80-108">This attribute applies to all node types.</span></span> <span data-ttu-id="99c80-109">In der Regel legen Sie dieses Attribut auf Tee-Knoten fest, um anzugeben, dass die sekundären Ausgaben nicht von wesentlicher Bedeutung sind.</span><span class="sxs-lookup"><span data-stu-id="99c80-109">Typically you would set this attribute on tee nodes, to indicate that the secondary outputs are not essential.</span></span>

<span data-ttu-id="99c80-110">Der Wert des-Attributs ist ein Array von Indizes für Ausgabedaten Ströme auf dem Knoten.</span><span class="sxs-lookup"><span data-stu-id="99c80-110">The value of the attribute is an array of indexes to output streams on the node.</span></span>

<span data-ttu-id="99c80-111">Wenn dieses Attribut festgelegt ist, kann die Pipeline Beispiele aus den angegebenen Ausgabestreams ablegen, wenn der Stream ausfällt.</span><span class="sxs-lookup"><span data-stu-id="99c80-111">If this attribute is set, the pipeline might drop samples from the specified output streams, if the stream is falling behind.</span></span>

<span data-ttu-id="99c80-112">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="99c80-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="99c80-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="99c80-113">Requirements</span></span>



| <span data-ttu-id="99c80-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="99c80-114">Requirement</span></span> | <span data-ttu-id="99c80-115">Wert</span><span class="sxs-lookup"><span data-stu-id="99c80-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="99c80-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="99c80-116">Minimum supported client</span></span><br/> | <span data-ttu-id="99c80-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="99c80-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="99c80-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="99c80-118">Minimum supported server</span></span><br/> | <span data-ttu-id="99c80-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="99c80-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="99c80-120">Header</span><span class="sxs-lookup"><span data-stu-id="99c80-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="99c80-121"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="99c80-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99c80-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99c80-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99c80-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="99c80-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="99c80-124">**Imfattributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="99c80-124">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="99c80-125">**Imfattributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="99c80-125">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="99c80-126">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="99c80-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="99c80-127">Topologieknotenattribute</span><span class="sxs-lookup"><span data-stu-id="99c80-127">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




