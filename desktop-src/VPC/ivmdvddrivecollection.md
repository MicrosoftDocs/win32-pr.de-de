---
title: Ivmdvddrivecollection-Schnittstelle (vpccominterfaces. h)
description: Definiert die Sammlung von CD-und DVD-Laufwerken innerhalb des virtuellen Computers. Verwenden Sie zum Abrufen eines ivmdvddrivecollection-Objekts die ivmvirtualmachine-dvdromdrives-Eigenschaft.
ms.assetid: 3069f530-9bc7-4f55-bf5a-82d1244d0cc5
keywords:
- Ivmdvddrivecollection Interface Virtual PC
- Virtueller Computer ivmdvddrivecollection Interface, beschrieben
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6afcf14a1ffe53dea0dcd7e21fcde8729e0bd0ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346724"
---
# <a name="ivmdvddrivecollection-interface"></a><span data-ttu-id="ecf5c-106">Ivmdvddrivecollection-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ecf5c-106">IVMDVDDriveCollection interface</span></span>

<span data-ttu-id="ecf5c-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ecf5c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ecf5c-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ecf5c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ecf5c-109">Definiert die Sammlung von CD-und DVD-Laufwerken innerhalb des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="ecf5c-109">Defines the collection of CD and DVD drives within the virtual machine.</span></span> <span data-ttu-id="ecf5c-110">Verwenden Sie zum Abrufen eines **ivmdvddrivecollection** -Objekts die [**ivmvirtualmachine::D vdromdrives**](ivmvirtualmachine-dvdromdrives.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ecf5c-110">To obtain an **IVMDVDDriveCollection** object, use the [**IVMVirtualMachine::DVDROMDrives**](ivmvirtualmachine-dvdromdrives.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="ecf5c-111">Member</span><span class="sxs-lookup"><span data-stu-id="ecf5c-111">Members</span></span>

<span data-ttu-id="ecf5c-112">Die **ivmdvddrivecollection** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ecf5c-112">The **IVMDVDDriveCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="ecf5c-113">**Ivmdvddrivecollection** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ecf5c-113">**IVMDVDDriveCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="ecf5c-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ecf5c-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ecf5c-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ecf5c-115">Properties</span></span>

<span data-ttu-id="ecf5c-116">Die **ivmdvddrivecollection** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ecf5c-116">The **IVMDVDDriveCollection** interface has these properties.</span></span>



| <span data-ttu-id="ecf5c-117">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ecf5c-117">Property</span></span>                                                       | <span data-ttu-id="ecf5c-118">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="ecf5c-118">Access type</span></span>          | <span data-ttu-id="ecf5c-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ecf5c-119">Description</span></span>                                                                    |
|:---------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="ecf5c-120">**\_"Netwenum"**</span><span class="sxs-lookup"><span data-stu-id="ecf5c-120">**\_NewEnum**</span></span>](ivmdvddrivecollection--newenum.md)<br/> | <span data-ttu-id="ecf5c-121">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ecf5c-121">Read-only</span></span><br/> | <span data-ttu-id="ecf5c-122">Ein Enumerator für die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="ecf5c-122">An enumerator for the collection.</span></span><br/>                                   |
| [<span data-ttu-id="ecf5c-123">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="ecf5c-123">**Count**</span></span>](ivmdvddrivecollection-count.md)<br/>        | <span data-ttu-id="ecf5c-124">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ecf5c-124">Read-only</span></span><br/> | <span data-ttu-id="ecf5c-125">Die Anzahl der CD-und DVD-Laufwerke in dieser Sammlung.</span><span class="sxs-lookup"><span data-stu-id="ecf5c-125">The number of CD and DVD drives in this collection.</span></span><br/>                 |
| [<span data-ttu-id="ecf5c-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="ecf5c-126">**Item**</span></span>](ivmdvddrivecollection-item.md)<br/>          | <span data-ttu-id="ecf5c-127">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ecf5c-127">Read-only</span></span><br/> | <span data-ttu-id="ecf5c-128">Das CD-oder DVD-Laufwerks Objekt, das dem angegebenen Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="ecf5c-128">The CD or DVD drive object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ecf5c-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ecf5c-129">Requirements</span></span>



| <span data-ttu-id="ecf5c-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ecf5c-130">Requirement</span></span> | <span data-ttu-id="ecf5c-131">Wert</span><span class="sxs-lookup"><span data-stu-id="ecf5c-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecf5c-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ecf5c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ecf5c-133">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ecf5c-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ecf5c-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ecf5c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ecf5c-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ecf5c-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ecf5c-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="ecf5c-136">End of client support</span></span><br/>    | <span data-ttu-id="ecf5c-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ecf5c-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ecf5c-138">Produkt</span><span class="sxs-lookup"><span data-stu-id="ecf5c-138">Product</span></span><br/>                  | <span data-ttu-id="ecf5c-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ecf5c-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ecf5c-140">Header</span><span class="sxs-lookup"><span data-stu-id="ecf5c-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecf5c-141"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecf5c-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ecf5c-142">IID</span><span class="sxs-lookup"><span data-stu-id="ecf5c-142">IID</span></span><br/>                      | <span data-ttu-id="ecf5c-143">IID \_ ivmdvddrivecollection ist als bc86e297-e55f-4742-9614-ad11d3131f68 definiert.</span><span class="sxs-lookup"><span data-stu-id="ecf5c-143">IID\_IVMDVDDriveCollection is defined as bc86e297-e55f-4742-9614-ad11d3131f68</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="ecf5c-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ecf5c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecf5c-145">**Ivmdvddrive**</span><span class="sxs-lookup"><span data-stu-id="ecf5c-145">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> <dt>

[<span data-ttu-id="ecf5c-146">**Ivmvirtualmachine::D vdromdrives**</span><span class="sxs-lookup"><span data-stu-id="ecf5c-146">**IVMVirtualMachine::DVDROMDrives**</span></span>](ivmvirtualmachine-dvdromdrives.md)
</dt> </dl>

 

