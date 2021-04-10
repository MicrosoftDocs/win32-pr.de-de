---
title: Ivmnetworkadaptercollection-Schnittstelle (vpccominterfaces. h)
description: Definiert eine Sammlung virtueller Netzwerkschnittstellenkarten. Zum Abrufen eines ivmnetworkadaptercollection-Objekts verwenden Sie die Eigenschaften "ivmvirtualmachine NetworkAdapters", "ivmvirtualnetwork Network Adapters" und "ivmvirtualpc unconnectednetworkadapters".
ms.assetid: cfb03a7c-a568-488c-9284-798b7e21027a
keywords:
- Ivmnetworkadaptercollection-Schnittstelle virtueller PC
- Ivmnetworkadaptercollection Interface Virtual PC, beschrieben
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8005b88cb873f00708829672cdeb6563b606d42b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040706"
---
# <a name="ivmnetworkadaptercollection-interface"></a><span data-ttu-id="f91f3-106">Ivmnetworkadaptercollection-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f91f3-106">IVMNetworkAdapterCollection interface</span></span>

<span data-ttu-id="f91f3-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f91f3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f91f3-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f91f3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f91f3-109">Definiert eine Sammlung virtueller Netzwerkschnittstellenkarten.</span><span class="sxs-lookup"><span data-stu-id="f91f3-109">Defines a collection of virtual network interface cards.</span></span> <span data-ttu-id="f91f3-110">Zum Abrufen eines ivmnetworkadaptercollection-Objekts verwenden Sie die Eigenschaften [**ivmvirtualmachine:: NetworkAdapters**](ivmvirtualmachine-networkadapters.md), [**ivmvirtualnetwork:: NetworkAdapters**](ivmvirtualnetwork-networkadapters.md)und [**ivmvirtualpc:: unconnectednetworkadapters**](ivmvirtualpc-unconnectednetworkadapters.md) .</span><span class="sxs-lookup"><span data-stu-id="f91f3-110">To obtain an IVMNetworkAdapterCollection object, use the [**IVMVirtualMachine::NetworkAdapters**](ivmvirtualmachine-networkadapters.md), [**IVMVirtualNetwork::NetworkAdapters**](ivmvirtualnetwork-networkadapters.md), and [**IVMVirtualPC::UnconnectedNetworkAdapters**](ivmvirtualpc-unconnectednetworkadapters.md) properties.</span></span>

## <a name="members"></a><span data-ttu-id="f91f3-111">Member</span><span class="sxs-lookup"><span data-stu-id="f91f3-111">Members</span></span>

<span data-ttu-id="f91f3-112">Die **ivmnetworkadaptercollection** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f91f3-112">The **IVMNetworkAdapterCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="f91f3-113">**Ivmnetworkadaptercollection** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f91f3-113">**IVMNetworkAdapterCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="f91f3-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f91f3-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f91f3-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f91f3-115">Properties</span></span>

<span data-ttu-id="f91f3-116">Die **ivmnetworkadaptercollection** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f91f3-116">The **IVMNetworkAdapterCollection** interface has these properties.</span></span>



| <span data-ttu-id="f91f3-117">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f91f3-117">Property</span></span>                                                             | <span data-ttu-id="f91f3-118">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="f91f3-118">Access type</span></span>          | <span data-ttu-id="f91f3-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f91f3-119">Description</span></span>                                                                                                   |
|:---------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f91f3-120">**\_"Netwenum"**</span><span class="sxs-lookup"><span data-stu-id="f91f3-120">**\_NewEnum**</span></span>](ivmnetworkadaptercollection--newenum.md)<br/> | <span data-ttu-id="f91f3-121">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f91f3-121">Read-only</span></span><br/> | <span data-ttu-id="f91f3-122">Ein Enumerator für die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="f91f3-122">An enumerator for the collection.</span></span><br/>                                                                  |
| [<span data-ttu-id="f91f3-123">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="f91f3-123">**Count**</span></span>](ivmnetworkadaptercollection-count.md)<br/>        | <span data-ttu-id="f91f3-124">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f91f3-124">Read-only</span></span><br/> | <span data-ttu-id="f91f3-125">Die Anzahl der Netzwerkschnittstellen in dieser Sammlung.</span><span class="sxs-lookup"><span data-stu-id="f91f3-125">The number of network interfaces in this collection.</span></span><br/>                                               |
| [<span data-ttu-id="f91f3-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="f91f3-126">**Item**</span></span>](ivmnetworkadaptercollection-item.md)<br/>          | <span data-ttu-id="f91f3-127">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f91f3-127">Read-only</span></span><br/> | <span data-ttu-id="f91f3-128">Das [**ivmnetworkadapter**](ivmnetworkadapter.md) -Objekt, das dem angegebenen Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="f91f3-128">The [**IVMNetworkAdapter**](ivmnetworkadapter.md) object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f91f3-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f91f3-129">Requirements</span></span>



| <span data-ttu-id="f91f3-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f91f3-130">Requirement</span></span> | <span data-ttu-id="f91f3-131">Wert</span><span class="sxs-lookup"><span data-stu-id="f91f3-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f91f3-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f91f3-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f91f3-133">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f91f3-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f91f3-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f91f3-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f91f3-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f91f3-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f91f3-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f91f3-136">End of client support</span></span><br/>    | <span data-ttu-id="f91f3-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f91f3-137">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="f91f3-138">Produkt</span><span class="sxs-lookup"><span data-stu-id="f91f3-138">Product</span></span><br/>                  | <span data-ttu-id="f91f3-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f91f3-139">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="f91f3-140">Header</span><span class="sxs-lookup"><span data-stu-id="f91f3-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="f91f3-141"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f91f3-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="f91f3-142">IID</span><span class="sxs-lookup"><span data-stu-id="f91f3-142">IID</span></span><br/>                      | <span data-ttu-id="f91f3-143">IID \_ ivmnetworkadaptercollection ist als ebaeafe9-EBCD-47cf-866e-ad87d735e479 definiert.</span><span class="sxs-lookup"><span data-stu-id="f91f3-143">IID\_IVMNetworkAdapterCollection is defined as ebaeafe9-ebcd-47cf-866e-ad87d735e479</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f91f3-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f91f3-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f91f3-145">**Ivmnetworkadapter**</span><span class="sxs-lookup"><span data-stu-id="f91f3-145">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> <dt>

[<span data-ttu-id="f91f3-146">**Ivmvirtualmachine:: NetworkAdapters**</span><span class="sxs-lookup"><span data-stu-id="f91f3-146">**IVMVirtualMachine::NetworkAdapters**</span></span>](ivmvirtualmachine-networkadapters.md)
</dt> <dt>

[<span data-ttu-id="f91f3-147">**Ivmvirtualnetwork:: NetworkAdapters**</span><span class="sxs-lookup"><span data-stu-id="f91f3-147">**IVMVirtualNetwork::NetworkAdapters**</span></span>](ivmvirtualnetwork-networkadapters.md)
</dt> <dt>

[<span data-ttu-id="f91f3-148">**Ivmvirtualpc:: unconnectednetworkadapters**</span><span class="sxs-lookup"><span data-stu-id="f91f3-148">**IVMVirtualPC::UnconnectedNetworkAdapters**</span></span>](ivmvirtualpc-unconnectednetworkadapters.md)
</dt> </dl>

 

