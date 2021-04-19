---
description: Gibt an, wie die Medien Sitzung ein Objekt in der Topologie herunterfährt.
ms.assetid: 53b4faba-860f-4d6c-a145-09ea4ae63b8b
title: MF_TOPONODE_NOSHUTDOWN_ON_REMOVE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bec06d2190491167d978250270503e5e6506d58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345786"
---
# <a name="mf_toponode_noshutdown_on_remove-attribute"></a><span data-ttu-id="229c8-103">MF \_ toponode \_ noshutdown \_ beim \_ Remove-Attribut</span><span class="sxs-lookup"><span data-stu-id="229c8-103">MF\_TOPONODE\_NOSHUTDOWN\_ON\_REMOVE attribute</span></span>

<span data-ttu-id="229c8-104">Gibt an, wie die Medien Sitzung ein Objekt in der Topologie herunterfährt.</span><span class="sxs-lookup"><span data-stu-id="229c8-104">Specifies how the Media Session shuts down an object in the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="229c8-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="229c8-105">Data type</span></span>

<span data-ttu-id="229c8-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="229c8-106">**UINT32**</span></span>

<span data-ttu-id="229c8-107">Als booleschen Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="229c8-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="229c8-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="229c8-108">Remarks</span></span>

<span data-ttu-id="229c8-109">Dieses Attribut gilt für die folgenden Typen von topologietknoten:</span><span class="sxs-lookup"><span data-stu-id="229c8-109">This attribute applies to the following types of toplogy node:</span></span>

-   <span data-ttu-id="229c8-110">Ausgabe Knoten</span><span class="sxs-lookup"><span data-stu-id="229c8-110">Output nodes</span></span>
-   <span data-ttu-id="229c8-111">Ein beliebiger Transformations Knoten, der eine *asynchrone* Media Foundation Transformation (MFT) enthält.</span><span class="sxs-lookup"><span data-stu-id="229c8-111">Any transform node that contains an *asynchronous* Media Foundation transform (MFT).</span></span>

<span data-ttu-id="229c8-112">Das-Attribut kann die folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="229c8-112">The attribute can have the following values:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="229c8-113">Wert</span><span class="sxs-lookup"><span data-stu-id="229c8-113">Value</span></span></th>
<th><span data-ttu-id="229c8-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="229c8-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="229c8-115"><strong>TRUE</strong></span><span class="sxs-lookup"><span data-stu-id="229c8-115"><strong>TRUE</strong></span></span></td>
<td><span data-ttu-id="229c8-116">Wenn die Medien Sitzung zu einer neuen Topologie wechselt oder die aktuelle Topologie löscht, wird das Objekt, das zu diesem topologieknoten gehört, nicht heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="229c8-116">When the Media Session switches to a new topology or clears the current topology, it does not shut down the object that belongs to this topology node.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="229c8-117"><strong>FALSE</strong></span><span class="sxs-lookup"><span data-stu-id="229c8-117"><strong>FALSE</strong></span></span></td>
<td><span data-ttu-id="229c8-118">Wenn die Medien Sitzung zu einer neuen Topologie wechselt oder die aktuelle Topologie löscht, wird das Knoten Objekt wie folgt heruntergefahren:</span><span class="sxs-lookup"><span data-stu-id="229c8-118">When the Media Session switches to a new topology or clears the current topology, it shuts down the node object, as follows:</span></span>
<ul>
<li><span data-ttu-id="229c8-119">Ausgabe Knoten: die Sitzung ruft <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown"><strong>imfmediasink:: Shutdown</strong></a> für die Medien Senke auf.</span><span class="sxs-lookup"><span data-stu-id="229c8-119">Output nodes: The session calls <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown"><strong>IMFMediaSink::Shutdown</strong></a> on the media sink.</span></span></li>
<li><span data-ttu-id="229c8-120">Transformations Knoten: die Sitzung ruft <a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown"><strong>imfshutdown:: Shutdown</strong></a> für die MFT auf.</span><span class="sxs-lookup"><span data-stu-id="229c8-120">Transform nodes: The session calls <a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown"><strong>IMFShutdown::Shutdown</strong></a> on the MFT.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="229c8-121">Der Standardwert ist " **true**".</span><span class="sxs-lookup"><span data-stu-id="229c8-121">The default value is **TRUE**.</span></span>

<span data-ttu-id="229c8-122">Wenn Ihre Anwendung mehrere Topologien in die Warteschlange stellt, empfiehlt es sich, dieses Attribut auf " **false**" festzulegen.</span><span class="sxs-lookup"><span data-stu-id="229c8-122">If your application queues multiple topologies, it is a good idea to set this attribute to **FALSE**.</span></span> <span data-ttu-id="229c8-123">Andernfalls werden Objekte in der Topologie möglicherweise nicht ordnungsgemäß heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="229c8-123">Otherwise, objects in the topology might not be shut down correctly.</span></span>

<span data-ttu-id="229c8-124">Dieses Attribut gilt nicht, wenn die Anwendung die Medien Sitzung durch Aufrufen von [**imfmediasession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown)herunterfährt.</span><span class="sxs-lookup"><span data-stu-id="229c8-124">This attribute does not apply when the application shuts down the Media Session by calling [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span> <span data-ttu-id="229c8-125">Wenn die Medien Sitzung heruntergefahren wird, werden die Medien senken und asynchrone MFTs in der aktuellen Topologie immer heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="229c8-125">When the Media Session shuts down, it always shuts down the media sinks and asynchronous MFTs in the current topology.</span></span>

<span data-ttu-id="229c8-126">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="229c8-126">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="229c8-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="229c8-127">Requirements</span></span>



| <span data-ttu-id="229c8-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="229c8-128">Requirement</span></span> | <span data-ttu-id="229c8-129">Wert</span><span class="sxs-lookup"><span data-stu-id="229c8-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="229c8-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="229c8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="229c8-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="229c8-131">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="229c8-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="229c8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="229c8-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="229c8-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="229c8-134">Header</span><span class="sxs-lookup"><span data-stu-id="229c8-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="229c8-135"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="229c8-135"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="229c8-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="229c8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="229c8-137">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="229c8-137">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="229c8-138">Asynchrone MFTs</span><span class="sxs-lookup"><span data-stu-id="229c8-138">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="229c8-139">Topologieknotenattribute</span><span class="sxs-lookup"><span data-stu-id="229c8-139">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="229c8-140">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="229c8-140">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="229c8-141">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="229c8-141">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="229c8-142">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="229c8-142">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 




