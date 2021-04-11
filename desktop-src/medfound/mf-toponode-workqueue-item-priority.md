---
description: Gibt die Arbeits Element Priorität für eine Verzweigung der Topologie an.
ms.assetid: B2FA1151-08D3-46F9-A38D-AC8908EFA6A2
title: MF_TOPONODE_WORKQUEUE_ITEM_PRIORITY-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5f7df6630e41a32eeb069c2a07b8030da79929
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214882"
---
# <a name="mf_toponode_workqueue_item_priority-attribute"></a><span data-ttu-id="b6312-103">\_ \_ \_ Element \_ Prioritäts Attribut für MF-toponode-workqueue</span><span class="sxs-lookup"><span data-stu-id="b6312-103">MF\_TOPONODE\_WORKQUEUE\_ITEM\_PRIORITY attribute</span></span>

<span data-ttu-id="b6312-104">Gibt die Arbeits Element Priorität für eine Verzweigung der Topologie an.</span><span class="sxs-lookup"><span data-stu-id="b6312-104">Specifies the work-item priority for a branch of the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="b6312-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b6312-105">Data type</span></span>

<span data-ttu-id="b6312-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b6312-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="b6312-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6312-107">Remarks</span></span>

<span data-ttu-id="b6312-108">Dieses Attribut gilt für Quellknoten (**MF- \_ Topologie \_ sourcestream- \_ Knoten**).</span><span class="sxs-lookup"><span data-stu-id="b6312-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="b6312-109">Das-Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="b6312-109">The attribute is optional.</span></span>

<span data-ttu-id="b6312-110">Dieses Attribut erfordert das [MF- \_ toponode- \_ workqueue- \_ ID](mf-toponode-workqueue-id-attribute.md) -Attribut auf dem gleichen Knoten.</span><span class="sxs-lookup"><span data-stu-id="b6312-110">This attribute requires the [MF\_TOPONODE\_WORKQUEUE\_ID](mf-toponode-workqueue-id-attribute.md) attribute on the same node.</span></span>

<span data-ttu-id="b6312-111">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="b6312-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6312-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6312-112">Requirements</span></span>



| <span data-ttu-id="b6312-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6312-113">Requirement</span></span> | <span data-ttu-id="b6312-114">Wert</span><span class="sxs-lookup"><span data-stu-id="b6312-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b6312-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b6312-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b6312-116">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6312-116">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b6312-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b6312-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b6312-118">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6312-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b6312-119">Header</span><span class="sxs-lookup"><span data-stu-id="b6312-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6312-120"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6312-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6312-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6312-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6312-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="b6312-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b6312-123">Topologieknotenattribute</span><span class="sxs-lookup"><span data-stu-id="b6312-123">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="b6312-124">Arbeits Warteschlangen und Threading</span><span class="sxs-lookup"><span data-stu-id="b6312-124">Work Queue and Threading Improvements</span></span>](media-foundation-work-queue-and-threading-improvements.md)
</dt> <dt>

[<span data-ttu-id="b6312-125">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="b6312-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="b6312-126">**IMF workqueueservices:: beginregistertopologyworkqueueswithmmcss**</span><span class="sxs-lookup"><span data-stu-id="b6312-126">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="b6312-127">**MF- \_ toponode- \_ workwarteschlangen- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="b6312-127">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)
</dt> </dl>

 

 




