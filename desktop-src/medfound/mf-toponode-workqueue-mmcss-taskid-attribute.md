---
description: Gibt einen MMCSS-Task Bezeichner (Multimedia Class Scheduler Service) für eine topologieverzweigung an.
ms.assetid: ccecc1e6-2d30-4e89-849f-c3acad97f312
title: MF_TOPONODE_WORKQUEUE_MMCSS_TASKID-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53af119c58d725d42ec5737ffd9bf96286a65ac1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527410"
---
# <a name="mf_toponode_workqueue_mmcss_taskid-attribute"></a><span data-ttu-id="f974e-103">MF \_ toponode \_ workqueue \_ MMCSS \_ TaskID-Attribut</span><span class="sxs-lookup"><span data-stu-id="f974e-103">MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID attribute</span></span>

<span data-ttu-id="f974e-104">Gibt einen MMCSS-Task Bezeichner (Multimedia Class Scheduler Service) für eine topologieverzweigung an.</span><span class="sxs-lookup"><span data-stu-id="f974e-104">Specifies a Multimedia Class Scheduler Service (MMCSS) task identifier for a topology branch.</span></span>

## <a name="data-type"></a><span data-ttu-id="f974e-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f974e-105">Data type</span></span>

<span data-ttu-id="f974e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f974e-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f974e-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f974e-107">Remarks</span></span>

<span data-ttu-id="f974e-108">Dieses Attribut gilt für Quellknoten (**MF- \_ Topologie \_ sourcestream- \_ Knoten**).</span><span class="sxs-lookup"><span data-stu-id="f974e-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="f974e-109">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="f974e-109">This attribute is optional.</span></span>

<span data-ttu-id="f974e-110">Dieses Attribut wird ignoriert, es sei denn, die folgenden Attribute werden ebenfalls festgelegt:</span><span class="sxs-lookup"><span data-stu-id="f974e-110">This attribute is ignored unless the following attributes are also set:</span></span>

-   [<span data-ttu-id="f974e-111">**MF- \_ toponode- \_ workwarteschlangen- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="f974e-111">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)
-   [<span data-ttu-id="f974e-112">**MF \_ toponode \_ workqueue \_ MMCSS- \_ Klasse**</span><span class="sxs-lookup"><span data-stu-id="f974e-112">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**</span></span>](mf-toponode-workqueue-mmcss-class-attribute.md)

<span data-ttu-id="f974e-113">Wenn die Anwendung einen ihrer eigenen Threads mit MMCSS registriert, können Sie dieses Attribut verwenden, um die topologiearbeitswarteschlange der MMCSS-Gruppe der Anwendung zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="f974e-113">If the application registers one of its own threads with MMCSS, you can use this attribute to associate the topology work queue with the application's MMCSS group.</span></span> <span data-ttu-id="f974e-114">Legen Sie den Attribut Wert auf den Task Bezeichner fest, den die Anwendung bei der Registrierung bei MMCSS erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="f974e-114">Set the attribute value equal to the task identifier that the application received when it registered with MMCSS.</span></span> <span data-ttu-id="f974e-115">(Der Task Bezeichner wird im *Taskindex* -Parameter der [**avsetmmthreadcharacteristics**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa) -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f974e-115">(The task identifier is returned in the *TaskIndex* parameter of the [**AvSetMmThreadCharacteristics**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa) function.</span></span> <span data-ttu-id="f974e-116">Weitere Informationen finden Sie im Thema [Prozess-und Thread Funktionen](../procthread/process-and-thread-functions.md).)</span><span class="sxs-lookup"><span data-stu-id="f974e-116">For more information, see the topic [Process and Thread Functions](../procthread/process-and-thread-functions.md).)</span></span>

<span data-ttu-id="f974e-117">Wenn MMCSS einen neuen Task Bezeichner für die Topologie zuweisen soll, legen Sie das Attribut [**MF \_ toponode \_ workqueue \_ MMCSS \_ Class**](mf-toponode-workqueue-mmcss-class-attribute.md) fest, aber legen Sie das Attribut **MF \_ toponode \_ workqueue \_ MMCSS \_ TaskID** nicht fest.</span><span class="sxs-lookup"><span data-stu-id="f974e-117">If you want MMCSS to assign a new task identifier for the topology, set the [**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**](mf-toponode-workqueue-mmcss-class-attribute.md) attribute, but do not set the **MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID** attribute.</span></span>

<span data-ttu-id="f974e-118">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="f974e-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f974e-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f974e-119">Requirements</span></span>



| <span data-ttu-id="f974e-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f974e-120">Requirement</span></span> | <span data-ttu-id="f974e-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f974e-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f974e-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f974e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f974e-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f974e-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f974e-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f974e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f974e-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f974e-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f974e-126">Header</span><span class="sxs-lookup"><span data-stu-id="f974e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f974e-127"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f974e-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f974e-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f974e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f974e-129">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="f974e-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f974e-130">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f974e-130">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="f974e-131">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f974e-131">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="f974e-132">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="f974e-132">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="f974e-133">**IMF workqueueservices:: beginregistertopologyworkqueueswithmmcss**</span><span class="sxs-lookup"><span data-stu-id="f974e-133">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="f974e-134">Topologieknotenattribute</span><span class="sxs-lookup"><span data-stu-id="f974e-134">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="f974e-135">Arbeits Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="f974e-135">Work Queues</span></span>](work-queues.md)
</dt> </dl>

 

 
