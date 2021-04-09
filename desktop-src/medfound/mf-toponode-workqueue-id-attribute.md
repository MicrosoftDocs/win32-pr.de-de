---
description: Gibt eine Arbeits Warteschlange für eine topologieverzweigung an.
ms.assetid: 5bc7e2db-cfd2-4b94-b4d6-fe2b9ea9daf8
title: MF_TOPONODE_WORKQUEUE_ID-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9acda95895a1812f6cebbe64cbf3cd3bcdea4eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130137"
---
# <a name="mf_toponode_workqueue_id-attribute"></a><span data-ttu-id="a5cf6-103">ID-Attribut der MF- \_ toponode- \_ workqueue \_</span><span class="sxs-lookup"><span data-stu-id="a5cf6-103">MF\_TOPONODE\_WORKQUEUE\_ID attribute</span></span>

<span data-ttu-id="a5cf6-104">Gibt eine Arbeits Warteschlange für eine topologieverzweigung an.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-104">Specifies a work queue for a topology branch.</span></span>

## <a name="data-type"></a><span data-ttu-id="a5cf6-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a5cf6-105">Data type</span></span>

<span data-ttu-id="a5cf6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a5cf6-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="a5cf6-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5cf6-107">Remarks</span></span>

<span data-ttu-id="a5cf6-108">Dieses Attribut gilt für Quellknoten (**MF- \_ Topologie \_ sourcestream- \_ Knoten**).</span><span class="sxs-lookup"><span data-stu-id="a5cf6-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="a5cf6-109">Das-Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-109">The attribute is optional.</span></span>

<span data-ttu-id="a5cf6-110">Der Wert des-Attributs ist ein von der Anwendung definierter Bezeichner für die Arbeits Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-110">The value of the attribute is an application-defined identifier for the work queue.</span></span>

<span data-ttu-id="a5cf6-111">Anwendungen können dieses Attribut verwenden, um den branches der Topologie Arbeits Warteschlangen zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-111">Applications can use this attribute to assign work queues to branches of the topology.</span></span> <span data-ttu-id="a5cf6-112">Jeder Quellknoten in der Topologie definiert eine Verzweigung.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-112">Each source node in the topology defines one branch.</span></span> <span data-ttu-id="a5cf6-113">Die Verzweigung schließt jeden topologieknoten ein, der Daten von diesem Knoten empfängt.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-113">The branch includes every topology node that receives data from that node.</span></span>

<span data-ttu-id="a5cf6-114">Wenn Sie dieses Attribut festlegen, müssen Sie die [**imfworkqueueservices:: beginregistertopologyworkqueueswithmmcss**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) -Methode für die aufgelöste Topologie aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-114">If you set this attribute, call the [**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) method on the resolved topology.</span></span> <span data-ttu-id="a5cf6-115">Mehrere Verzweigungen in der Topologie können dieselbe Arbeits Warteschlange gemeinsam verwenden, und Arbeits Warteschlangen können über Topologien hinweg wieder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-115">Multiple branches in the topology can share the same work queue, and work queues can be re-used across topologies.</span></span>

> [!Note]  
> <span data-ttu-id="a5cf6-116">Der Wert dieses Attributs ist nicht mit dem Bezeichner identisch, der von der MF-Funktion der [**MF**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-116">The value of this attribute is not the same as the identifier that is returned by the [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) function.</span></span> <span data-ttu-id="a5cf6-117">Der Wert des-Attributs ist ein von der Anwendung definierter Bezeichner, der zum Zuordnen von topologiebranches zu Arbeits Warteschlangen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-117">The value of the attribute is an application-defined identifier, and is used to associate topology branches with work queues.</span></span> <span data-ttu-id="a5cf6-118">Wenn die Medien Sitzung eine neue Arbeits Warteschlange belegt, speichert Sie den tatsächlichen Bezeichner der Arbeits Warteschlange intern.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-118">When the Media Session allocates a new work queue, it stores the actual work-queue identifier internally.</span></span>

 

<span data-ttu-id="a5cf6-119">Wenn dieses Attribut festgelegt wird, kann die Anwendung die Verzweigung auch einer MMCSS-Aufgabe (Multimedia Class Scheduler Service) zuweisen, indem das Attribut " [**MF \_ toponode \_ workqueue \_ MMCSS \_ Class**](mf-toponode-workqueue-mmcss-class-attribute.md) " festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-119">If this attribute it set, the application can also assign the branch to a Multimedia Class Scheduler Service (MMCSS) task, by setting the [**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**](mf-toponode-workqueue-mmcss-class-attribute.md) attribute.</span></span>

<span data-ttu-id="a5cf6-120">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="a5cf6-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5cf6-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5cf6-121">Requirements</span></span>



| <span data-ttu-id="a5cf6-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5cf6-122">Requirement</span></span> | <span data-ttu-id="a5cf6-123">Wert</span><span class="sxs-lookup"><span data-stu-id="a5cf6-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a5cf6-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a5cf6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a5cf6-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a5cf6-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a5cf6-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a5cf6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a5cf6-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a5cf6-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a5cf6-128">Header</span><span class="sxs-lookup"><span data-stu-id="a5cf6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5cf6-129"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5cf6-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5cf6-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5cf6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5cf6-131">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="a5cf6-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a5cf6-132">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a5cf6-132">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="a5cf6-133">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a5cf6-133">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="a5cf6-134">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="a5cf6-134">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="a5cf6-135">**IMF workqueueservices:: beginregistertopologyworkqueueswithmmcss**</span><span class="sxs-lookup"><span data-stu-id="a5cf6-135">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="a5cf6-136">**MF \_ toponode \_ workqueue \_ MMCSS- \_ Klasse**</span><span class="sxs-lookup"><span data-stu-id="a5cf6-136">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**</span></span>](mf-toponode-workqueue-mmcss-class-attribute.md)
</dt> <dt>

[<span data-ttu-id="a5cf6-137">**MF \_ toponode \_ workqueue \_ MMCSS \_ TaskID**</span><span class="sxs-lookup"><span data-stu-id="a5cf6-137">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID**</span></span>](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> <dt>

[<span data-ttu-id="a5cf6-138">Topologieknotenattribute</span><span class="sxs-lookup"><span data-stu-id="a5cf6-138">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="a5cf6-139">Arbeits Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="a5cf6-139">Work Queues</span></span>](work-queues.md)
</dt> </dl>

 

 




