---
description: Gibt eine MMCSS-Aufgabe (Multimedia Class Scheduler Service) für eine topologieverzweigung an.
ms.assetid: 8668d0f1-9d54-4c56-bb19-09498252bec4
title: MF_TOPONODE_WORKQUEUE_MMCSS_CLASS-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 824c9dbdc9b12bbc8fead9ab6ae722fca1e6643a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353144"
---
# <a name="mf_toponode_workqueue_mmcss_class-attribute"></a><span data-ttu-id="4f4f7-103">\_ \_ \_ MMCSS- \_ Klassen Attribut für MF toponode workqueue</span><span class="sxs-lookup"><span data-stu-id="4f4f7-103">MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS attribute</span></span>

<span data-ttu-id="4f4f7-104">Gibt eine MMCSS-Aufgabe ( [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) ) für eine topologieverzweigung an.</span><span class="sxs-lookup"><span data-stu-id="4f4f7-104">Specifies a [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) (MMCSS) task for a topology branch.</span></span>

## <a name="data-type"></a><span data-ttu-id="4f4f7-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4f4f7-105">Data type</span></span>

<span data-ttu-id="4f4f7-106">Breitzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4f4f7-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="4f4f7-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f4f7-107">Remarks</span></span>

<span data-ttu-id="4f4f7-108">Dieses Attribut gilt für Quellknoten (**MF- \_ Topologie \_ sourcestream- \_ Knoten**).</span><span class="sxs-lookup"><span data-stu-id="4f4f7-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="4f4f7-109">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="4f4f7-109">This attribute is optional.</span></span>

<span data-ttu-id="4f4f7-110">Dieses Attribut erfordert das [MF- \_ toponode- \_ workqueue- \_ ID](mf-toponode-workqueue-id-attribute.md) -Attribut.</span><span class="sxs-lookup"><span data-stu-id="4f4f7-110">This attribute requires the [MF\_TOPONODE\_WORKQUEUE\_ID](mf-toponode-workqueue-id-attribute.md) attribute.</span></span> <span data-ttu-id="4f4f7-111">Wenn Sie dieses Attribut festlegen, legen Sie außerdem fest, dass das **MF- \_ toponode- \_ workqueue- \_ ID** -Attribut auf dem gleichen Knoten festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4f4f7-111">If you set this attribute, also set the **MF\_TOPONODE\_WORKQUEUE\_ID** attribute is set on the same node.</span></span>

<span data-ttu-id="4f4f7-112">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="4f4f7-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f4f7-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f4f7-113">Requirements</span></span>



| <span data-ttu-id="4f4f7-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f4f7-114">Requirement</span></span> | <span data-ttu-id="4f4f7-115">Wert</span><span class="sxs-lookup"><span data-stu-id="4f4f7-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4f4f7-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4f4f7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4f4f7-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f4f7-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4f4f7-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4f4f7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4f4f7-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f4f7-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4f4f7-120">Header</span><span class="sxs-lookup"><span data-stu-id="4f4f7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f4f7-121"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f4f7-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f4f7-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f4f7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f4f7-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="4f4f7-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4f4f7-124">**Imfattributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="4f4f7-124">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="4f4f7-125">**Imfattributes:: SetString**</span><span class="sxs-lookup"><span data-stu-id="4f4f7-125">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="4f4f7-126">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="4f4f7-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="4f4f7-127">**IMF workqueueservices:: beginregistertopologyworkqueueswithmmcss**</span><span class="sxs-lookup"><span data-stu-id="4f4f7-127">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="4f4f7-128">**MF- \_ toponode- \_ workwarteschlangen- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="4f4f7-128">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)
</dt> <dt>

[<span data-ttu-id="4f4f7-129">**MF \_ toponode \_ workqueue \_ MMCSS \_ TaskID**</span><span class="sxs-lookup"><span data-stu-id="4f4f7-129">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID**</span></span>](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> <dt>

[<span data-ttu-id="4f4f7-130">Topologieknotenattribute</span><span class="sxs-lookup"><span data-stu-id="4f4f7-130">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="4f4f7-131">Arbeits Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="4f4f7-131">Work Queues</span></span>](work-queues.md)
</dt> </dl>

 

 
