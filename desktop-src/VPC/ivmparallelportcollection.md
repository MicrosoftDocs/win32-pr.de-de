---
title: Ivmparallelportcollection-Schnittstelle (vpccominterfaces. h)
description: Definiert die Sammlung paralleler Ports innerhalb des virtuellen Computers. Zum Abrufen eines ivmparallelportcollection-Objekts verwenden Sie die ivmvirtualmachine Parallelports-Eigenschaft.
ms.assetid: 038a5c08-cd92-426f-a059-9a4c2110548d
keywords:
- Ivmparallelportcollection-Schnittstelle virtueller PC
- Ivmparallelportcollection-Schnittstelle virtueller PC, beschrieben
topic_type:
- apiref
api_name:
- IVMParallelPortCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8284b3720e0272147c932cfbfd70448babf5606f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106052"
---
# <a name="ivmparallelportcollection-interface"></a><span data-ttu-id="28fa8-106">Ivmparallelportcollection-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="28fa8-106">IVMParallelPortCollection interface</span></span>

<span data-ttu-id="28fa8-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="28fa8-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="28fa8-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="28fa8-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="28fa8-109">Definiert die Sammlung paralleler Ports innerhalb des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="28fa8-109">Defines the collection of parallel ports within the virtual machine.</span></span> <span data-ttu-id="28fa8-110">Verwenden Sie zum Abrufen eines **ivmparallelportcollection** -Objekts die [**ivmvirtualmachine::P arallelports**](ivmvirtualmachine-parallelports.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="28fa8-110">To obtain an **IVMParallelPortCollection** object, use the [**IVMVirtualMachine::ParallelPorts**](ivmvirtualmachine-parallelports.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="28fa8-111">Member</span><span class="sxs-lookup"><span data-stu-id="28fa8-111">Members</span></span>

<span data-ttu-id="28fa8-112">Die **ivmparallelportcollection** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="28fa8-112">The **IVMParallelPortCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="28fa8-113">**Ivmparallelportcollection** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="28fa8-113">**IVMParallelPortCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="28fa8-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="28fa8-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="28fa8-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="28fa8-115">Properties</span></span>

<span data-ttu-id="28fa8-116">Die **ivmparallelportcollection** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="28fa8-116">The **IVMParallelPortCollection** interface has these properties.</span></span>



| <span data-ttu-id="28fa8-117">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="28fa8-117">Property</span></span>                                                           | <span data-ttu-id="28fa8-118">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="28fa8-118">Access type</span></span>          | <span data-ttu-id="28fa8-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="28fa8-119">Description</span></span>                                                                  |
|:-------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="28fa8-120">**\_"Netwenum"**</span><span class="sxs-lookup"><span data-stu-id="28fa8-120">**\_NewEnum**</span></span>](ivmparallelportcollection--newenum.md)<br/> | <span data-ttu-id="28fa8-121">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="28fa8-121">Read-only</span></span><br/> | <span data-ttu-id="28fa8-122">Ein Enumerator für die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="28fa8-122">An enumerator for the collection.</span></span><br/>                                 |
| [<span data-ttu-id="28fa8-123">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="28fa8-123">**Count**</span></span>](ivmparallelportcollection-count.md)<br/>        | <span data-ttu-id="28fa8-124">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="28fa8-124">Read-only</span></span><br/> | <span data-ttu-id="28fa8-125">Die Anzahl paralleler Ports in dieser Auflistung.</span><span class="sxs-lookup"><span data-stu-id="28fa8-125">The number of parallel ports in this collection.</span></span><br/>                  |
| [<span data-ttu-id="28fa8-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="28fa8-126">**Item**</span></span>](ivmparallelportcollection-item.md)<br/>          | <span data-ttu-id="28fa8-127">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="28fa8-127">Read-only</span></span><br/> | <span data-ttu-id="28fa8-128">Das parallele Port Objekt, das dem angegebenen Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="28fa8-128">The parallel port object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="28fa8-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28fa8-129">Requirements</span></span>



| <span data-ttu-id="28fa8-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28fa8-130">Requirement</span></span> | <span data-ttu-id="28fa8-131">Wert</span><span class="sxs-lookup"><span data-stu-id="28fa8-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="28fa8-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="28fa8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="28fa8-133">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="28fa8-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="28fa8-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="28fa8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="28fa8-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="28fa8-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="28fa8-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="28fa8-136">End of client support</span></span><br/>    | <span data-ttu-id="28fa8-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="28fa8-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="28fa8-138">Produkt</span><span class="sxs-lookup"><span data-stu-id="28fa8-138">Product</span></span><br/>                  | <span data-ttu-id="28fa8-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="28fa8-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="28fa8-140">Header</span><span class="sxs-lookup"><span data-stu-id="28fa8-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="28fa8-141"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="28fa8-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="28fa8-142">IID</span><span class="sxs-lookup"><span data-stu-id="28fa8-142">IID</span></span><br/>                      | <span data-ttu-id="28fa8-143">IID \_ ivmparallelportcollection ist als 27c3e036-198l-430c-8735-6e652f 7203fd definiert.</span><span class="sxs-lookup"><span data-stu-id="28fa8-143">IID\_IVMParallelPortCollection is defined as 27c3e036-198f-430c-8735-6e652f7203fd</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="28fa8-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28fa8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28fa8-145">**Ivmparallelport**</span><span class="sxs-lookup"><span data-stu-id="28fa8-145">**IVMParallelPort**</span></span>](ivmparallelport.md)
</dt> <dt>

[<span data-ttu-id="28fa8-146">**Ivmvirtualmachine::P arallelports**</span><span class="sxs-lookup"><span data-stu-id="28fa8-146">**IVMVirtualMachine::ParallelPorts**</span></span>](ivmvirtualmachine-parallelports.md)
</dt> </dl>

 

