---
title: Ivmvirtualmachinecollection-Schnittstelle (vpccominterfaces. h)
description: Definiert die Sammlung virtueller Computer innerhalb von Windows Virtual PC. Verwenden Sie zum Abrufen eines ivmvirtualmachinecollection-Objekts die ivmvirtualpc-Eigenschaft VirtualMachines.
ms.assetid: 3d34e791-2dba-4529-b489-96a0c6227294
keywords:
- Ivmvirtualmachinecollection Interface Virtual PC
- Ivmvirtualmachinecollection Interface Virtual PC, beschrieben
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e27426f96e409a1e67eb519e7a864ee7461879a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105645"
---
# <a name="ivmvirtualmachinecollection-interface"></a><span data-ttu-id="b724a-106">Ivmvirtualmachinecollection-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b724a-106">IVMVirtualMachineCollection interface</span></span>

<span data-ttu-id="b724a-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b724a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b724a-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b724a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b724a-109">Definiert die Sammlung virtueller Computer innerhalb von Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="b724a-109">Defines the collection of virtual machines within Windows Virtual PC.</span></span> <span data-ttu-id="b724a-110">Verwenden Sie zum Abrufen eines **ivmvirtualmachinecollection** -Objekts die [**ivmvirtualpc:: VirtualMachines**](ivmvirtualpc-virtualmachines.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b724a-110">To obtain an **IVMVirtualMachineCollection** object, use the [**IVMVirtualPC::VirtualMachines**](ivmvirtualpc-virtualmachines.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="b724a-111">Member</span><span class="sxs-lookup"><span data-stu-id="b724a-111">Members</span></span>

<span data-ttu-id="b724a-112">Die **ivmvirtualmachinecollection** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b724a-112">The **IVMVirtualMachineCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="b724a-113">**Ivmvirtualmachinecollection** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b724a-113">**IVMVirtualMachineCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="b724a-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b724a-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b724a-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b724a-115">Properties</span></span>

<span data-ttu-id="b724a-116">Die **ivmvirtualmachinecollection** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b724a-116">The **IVMVirtualMachineCollection** interface has these properties.</span></span>



| <span data-ttu-id="b724a-117">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b724a-117">Property</span></span>                                                             | <span data-ttu-id="b724a-118">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="b724a-118">Access type</span></span>          | <span data-ttu-id="b724a-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b724a-119">Description</span></span>                                                                    |
|:---------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="b724a-120">**\_"Netwenum"**</span><span class="sxs-lookup"><span data-stu-id="b724a-120">**\_NewEnum**</span></span>](ivmvirtualmachinecollection--newenum.md)<br/> | <span data-ttu-id="b724a-121">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b724a-121">Read-only</span></span><br/> | <span data-ttu-id="b724a-122">Ein Enumerator für die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="b724a-122">An enumerator for the collection.</span></span><br/>                                   |
| [<span data-ttu-id="b724a-123">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="b724a-123">**Count**</span></span>](ivmvirtualmachinecollection-count.md)<br/>        | <span data-ttu-id="b724a-124">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b724a-124">Read-only</span></span><br/> | <span data-ttu-id="b724a-125">Die Anzahl der virtuellen Computer in dieser Sammlung.</span><span class="sxs-lookup"><span data-stu-id="b724a-125">The number of virtual machines in this collection.</span></span><br/>                  |
| [<span data-ttu-id="b724a-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="b724a-126">**Item**</span></span>](ivmvirtualmachinecollection-item.md)<br/>          | <span data-ttu-id="b724a-127">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b724a-127">Read-only</span></span><br/> | <span data-ttu-id="b724a-128">Das virtuelle Maschinen Objekt, das dem angegebenen Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="b724a-128">The virtual machine object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b724a-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b724a-129">Requirements</span></span>



| <span data-ttu-id="b724a-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b724a-130">Requirement</span></span> | <span data-ttu-id="b724a-131">Wert</span><span class="sxs-lookup"><span data-stu-id="b724a-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b724a-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b724a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b724a-133">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b724a-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b724a-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b724a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b724a-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b724a-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b724a-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="b724a-136">End of client support</span></span><br/>    | <span data-ttu-id="b724a-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b724a-137">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="b724a-138">Produkt</span><span class="sxs-lookup"><span data-stu-id="b724a-138">Product</span></span><br/>                  | <span data-ttu-id="b724a-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b724a-139">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="b724a-140">Header</span><span class="sxs-lookup"><span data-stu-id="b724a-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="b724a-141"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b724a-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="b724a-142">IID</span><span class="sxs-lookup"><span data-stu-id="b724a-142">IID</span></span><br/>                      | <span data-ttu-id="b724a-143">IID \_ ivmvirtualmachinecollection ist als 59F 31786-2a3d-4sbf-9896-d85338ca0da1 definiert.</span><span class="sxs-lookup"><span data-stu-id="b724a-143">IID\_IVMVirtualMachineCollection is defined as 59f31786-2a3d-4fbf-9896-d85338ca0da1</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b724a-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b724a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b724a-145">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="b724a-145">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="b724a-146">**Ivmvirtualpc:: VirtualMachines**</span><span class="sxs-lookup"><span data-stu-id="b724a-146">**IVMVirtualPC::VirtualMachines**</span></span>](ivmvirtualpc-virtualmachines.md)
</dt> </dl>

 

