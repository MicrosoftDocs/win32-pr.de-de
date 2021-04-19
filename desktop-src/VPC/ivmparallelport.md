---
title: Ivmparallelport-Schnittstelle (vpccominterfaces. h)
description: Definiert einen parallelen Port innerhalb einer virtuellen Maschine.
ms.assetid: da8daf16-5d22-49be-8fe9-72d5018c0622
keywords:
- Ivmparallelport Interface Virtual PC
- Virtueller Computer für ivmparallelport Interface, beschrieben
topic_type:
- apiref
api_name:
- IVMParallelPort
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71b76b23f48e728104a3826afa80a8f272cd7e66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339596"
---
# <a name="ivmparallelport-interface"></a><span data-ttu-id="e92a8-105">Ivmparallelport-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="e92a8-105">IVMParallelPort interface</span></span>

<span data-ttu-id="e92a8-106">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e92a8-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e92a8-107">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e92a8-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e92a8-108">Definiert einen parallelen Port innerhalb einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="e92a8-108">Defines a parallel port inside a virtual machine.</span></span> <span data-ttu-id="e92a8-109">Mit dieser Schnittstelle können Sie parallele Ports in einem virtuellen Computer konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e92a8-109">This interface allows you to configure parallel ports inside a virtual machine.</span></span> <span data-ttu-id="e92a8-110">Sie können ein **ivmparallelport** -Objekt aus dem [**ivmparallelportcollection**](ivmparallelportcollection.md) -Objekt abrufen, das von der [**ivmvirtualmachine::P arallelports**](ivmvirtualmachine-parallelports.md) -Eigenschaft zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e92a8-110">You can retrieve an **IVMParallelPort** object from the [**IVMParallelPortCollection**](ivmparallelportcollection.md) object returned from the [**IVMVirtualMachine::ParallelPorts**](ivmvirtualmachine-parallelports.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="e92a8-111">Member</span><span class="sxs-lookup"><span data-stu-id="e92a8-111">Members</span></span>

<span data-ttu-id="e92a8-112">Die **ivmparallelport** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e92a8-112">The **IVMParallelPort** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="e92a8-113">**Ivmparallelport** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e92a8-113">**IVMParallelPort** also has these types of members:</span></span>

-   [<span data-ttu-id="e92a8-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="e92a8-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="e92a8-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e92a8-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e92a8-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="e92a8-116">Methods</span></span>

<span data-ttu-id="e92a8-117">Die **ivmparallelport** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="e92a8-117">The **IVMParallelPort** interface has these methods.</span></span>



| <span data-ttu-id="e92a8-118">Methode</span><span class="sxs-lookup"><span data-stu-id="e92a8-118">Method</span></span>                              | <span data-ttu-id="e92a8-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e92a8-119">Description</span></span>                                                        |
|:------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="e92a8-120">**\_id**</span><span class="sxs-lookup"><span data-stu-id="e92a8-120">**\_ID**</span></span>](ivmparallelport--id.md) | <span data-ttu-id="e92a8-121">Ruft den internen Bezeichner des parallelen Ports ab.</span><span class="sxs-lookup"><span data-stu-id="e92a8-121">Retrieves the internal identifier of the parallel port.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e92a8-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e92a8-122">Properties</span></span>

<span data-ttu-id="e92a8-123">Die **ivmparallelport** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e92a8-123">The **IVMParallelPort** interface has these properties.</span></span>



| <span data-ttu-id="e92a8-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e92a8-124">Property</span></span>                                        | <span data-ttu-id="e92a8-125">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="e92a8-125">Access type</span></span>           | <span data-ttu-id="e92a8-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e92a8-126">Description</span></span>                               |
|:------------------------------------------------|:----------------------|:------------------------------------------|
| [<span data-ttu-id="e92a8-127">**Name**</span><span class="sxs-lookup"><span data-stu-id="e92a8-127">**Name**</span></span>](ivmparallelport-name.md)<br/> | <span data-ttu-id="e92a8-128">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e92a8-128">Read/write</span></span><br/> | <span data-ttu-id="e92a8-129">Der Name des parallelen Anschlusses.</span><span class="sxs-lookup"><span data-stu-id="e92a8-129">The name of the parallel port.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e92a8-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e92a8-130">Requirements</span></span>



| <span data-ttu-id="e92a8-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e92a8-131">Requirement</span></span> | <span data-ttu-id="e92a8-132">Wert</span><span class="sxs-lookup"><span data-stu-id="e92a8-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e92a8-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e92a8-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e92a8-134">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e92a8-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e92a8-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e92a8-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e92a8-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e92a8-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e92a8-137">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="e92a8-137">End of client support</span></span><br/>    | <span data-ttu-id="e92a8-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e92a8-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e92a8-139">Produkt</span><span class="sxs-lookup"><span data-stu-id="e92a8-139">Product</span></span><br/>                  | <span data-ttu-id="e92a8-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e92a8-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e92a8-141">Header</span><span class="sxs-lookup"><span data-stu-id="e92a8-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="e92a8-142"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e92a8-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e92a8-143">IID</span><span class="sxs-lookup"><span data-stu-id="e92a8-143">IID</span></span><br/>                      | <span data-ttu-id="e92a8-144">IID \_ ivmparallelport ist als 097beecb-0a02-474b-abd6-298b22293fc6 definiert.</span><span class="sxs-lookup"><span data-stu-id="e92a8-144">IID\_IVMParallelPort is defined as 097beecb-0a02-474f-abd6-298b22293fc6</span></span><br/>            |



 

