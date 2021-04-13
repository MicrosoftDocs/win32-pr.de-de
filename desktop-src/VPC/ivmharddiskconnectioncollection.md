---
title: Ivmharddiskconnectioncollection-Schnittstelle (vpccominterfaces. h)
description: Definiert die Sammlung von Festplatten Verbindungen innerhalb des virtuellen Computers. Verwenden Sie zum Abrufen eines ivmharddiskconnectioncollection-Objekts die ivmvirtualmachine harddiskconnections-Eigenschaft.
ms.assetid: 3440318c-45f4-4d24-9609-dbe5ca59b005
keywords:
- Ivmharddiskconnectioncollection-Schnittstelle virtueller PC
- Ivmharddiskconnectioncollection-Schnittstelle virtueller PC, beschrieben
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbde67f226c5b2d8cb86a8764c6dd61c24c2a468
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475033"
---
# <a name="ivmharddiskconnectioncollection-interface"></a><span data-ttu-id="7d880-106">Ivmharddiskconnectioncollection-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="7d880-106">IVMHardDiskConnectionCollection interface</span></span>

<span data-ttu-id="7d880-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7d880-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7d880-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7d880-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7d880-109">Definiert die Sammlung von Festplatten Verbindungen innerhalb des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="7d880-109">Defines the collection of hard disk connections within the virtual machine.</span></span> <span data-ttu-id="7d880-110">Verwenden Sie zum Abrufen eines **ivmharddiskconnectioncollection** -Objekts die [**ivmvirtualmachine:: harddiskconnections**](ivmvirtualmachine-harddiskconnections.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="7d880-110">To obtain an **IVMHardDiskConnectionCollection** object, use the [**IVMVirtualMachine::HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="7d880-111">Member</span><span class="sxs-lookup"><span data-stu-id="7d880-111">Members</span></span>

<span data-ttu-id="7d880-112">Die **ivmharddiskconnectioncollection** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7d880-112">The **IVMHardDiskConnectionCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="7d880-113">**Ivmharddiskconnectioncollection** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7d880-113">**IVMHardDiskConnectionCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="7d880-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7d880-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7d880-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7d880-115">Properties</span></span>

<span data-ttu-id="7d880-116">Die **ivmharddiskconnectioncollection** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7d880-116">The **IVMHardDiskConnectionCollection** interface has these properties.</span></span>



| <span data-ttu-id="7d880-117">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7d880-117">Property</span></span>                                                                 | <span data-ttu-id="7d880-118">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="7d880-118">Access type</span></span>          | <span data-ttu-id="7d880-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7d880-119">Description</span></span>                                                                         |
|:-------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="7d880-120">**\_"Netwenum"**</span><span class="sxs-lookup"><span data-stu-id="7d880-120">**\_NewEnum**</span></span>](ivmharddiskconnectioncollection--newenum.md)<br/> | <span data-ttu-id="7d880-121">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7d880-121">Read-only</span></span><br/> | <span data-ttu-id="7d880-122">Ein Enumerator für die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="7d880-122">An enumerator for the collection.</span></span><br/>                                        |
| [<span data-ttu-id="7d880-123">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="7d880-123">**Count**</span></span>](ivmharddiskconnectioncollection-count.md)<br/>        | <span data-ttu-id="7d880-124">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7d880-124">Read-only</span></span><br/> | <span data-ttu-id="7d880-125">Die Anzahl der Festplatten Verbindungen in dieser Sammlung.</span><span class="sxs-lookup"><span data-stu-id="7d880-125">The number of hard disk connections in this collection.</span></span><br/>                  |
| [<span data-ttu-id="7d880-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="7d880-126">**Item**</span></span>](ivmharddiskconnectioncollection-item.md)<br/>          | <span data-ttu-id="7d880-127">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7d880-127">Read-only</span></span><br/> | <span data-ttu-id="7d880-128">Das Festplatten Verbindungs Objekt, das dem angegebenen Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="7d880-128">The hard disk connection object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7d880-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d880-129">Requirements</span></span>



| <span data-ttu-id="7d880-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d880-130">Requirement</span></span> | <span data-ttu-id="7d880-131">Wert</span><span class="sxs-lookup"><span data-stu-id="7d880-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d880-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7d880-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7d880-133">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7d880-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="7d880-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7d880-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7d880-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7d880-135">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="7d880-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="7d880-136">End of client support</span></span><br/>    | <span data-ttu-id="7d880-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7d880-137">Windows 7</span></span><br/>                                                                               |
| <span data-ttu-id="7d880-138">Produkt</span><span class="sxs-lookup"><span data-stu-id="7d880-138">Product</span></span><br/>                  | <span data-ttu-id="7d880-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7d880-139">Windows Virtual PC</span></span><br/>                                                                      |
| <span data-ttu-id="7d880-140">Header</span><span class="sxs-lookup"><span data-stu-id="7d880-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d880-141"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d880-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>      |
| <span data-ttu-id="7d880-142">IID</span><span class="sxs-lookup"><span data-stu-id="7d880-142">IID</span></span><br/>                      | <span data-ttu-id="7d880-143">IID \_ ivmharddiskconnectioncollection ist definiert als b9f2caf4-0aeb-4085-B105-ceddb90dbf62</span><span class="sxs-lookup"><span data-stu-id="7d880-143">IID\_IVMHardDiskconnectionCollection is defined as b9f2caf4-0aeb-4085-b105-ceddb90dbf62</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7d880-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d880-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d880-145">**Ivmharddiskconnection**</span><span class="sxs-lookup"><span data-stu-id="7d880-145">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> <dt>

[<span data-ttu-id="7d880-146">**Ivmvirtualmachine:: harddiskconnections**</span><span class="sxs-lookup"><span data-stu-id="7d880-146">**IVMVirtualMachine::HardDiskConnections**</span></span>](ivmvirtualmachine-harddiskconnections.md)
</dt> </dl>

 

