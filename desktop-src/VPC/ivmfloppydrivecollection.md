---
title: Ivmfloppydrivecollection-Schnittstelle (vpccominterfaces. h)
description: Definiert eine Sammlung von Diskettenlaufwerken innerhalb des virtuellen Computers.
ms.assetid: ba05fa84-81c3-4e70-98f5-404a9bc517ad
keywords:
- Ivmfloppydrivecollection Interface Virtual PC
- Ivmfloppydrivecollection Interface Virtual PC, beschrieben
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 664937a08bf7576c35b94a162fb5b6f4a7400f15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392202"
---
# <a name="ivmfloppydrivecollection-interface"></a><span data-ttu-id="1a852-105">Ivmfloppydrivecollection-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="1a852-105">IVMFloppyDriveCollection interface</span></span>

<span data-ttu-id="1a852-106">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1a852-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1a852-107">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1a852-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1a852-108">Definiert eine Sammlung von Diskettenlaufwerken innerhalb des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="1a852-108">Defines a collection of floppy drives within the virtual machine.</span></span> <span data-ttu-id="1a852-109">Zum Abrufen eines **ivmfloppydrivecollection** -Objekts verwenden Sie die [**ivmvirtualmachine:: floppydrives**](ivmvirtualmachine-floppydrives.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1a852-109">To obtain an **IVMFloppyDriveCollection** object, use the [**IVMVirtualMachine::FloppyDrives**](ivmvirtualmachine-floppydrives.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="1a852-110">Member</span><span class="sxs-lookup"><span data-stu-id="1a852-110">Members</span></span>

<span data-ttu-id="1a852-111">Die **ivmfloppydrivecollection** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="1a852-111">The **IVMFloppyDriveCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="1a852-112">**Ivmfloppydrivecollection** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1a852-112">**IVMFloppyDriveCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="1a852-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1a852-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1a852-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1a852-114">Properties</span></span>

<span data-ttu-id="1a852-115">Die **ivmfloppydrivecollection** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1a852-115">The **IVMFloppyDriveCollection** interface has these properties.</span></span>



| <span data-ttu-id="1a852-116">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1a852-116">Property</span></span>                                                          | <span data-ttu-id="1a852-117">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="1a852-117">Access type</span></span>          | <span data-ttu-id="1a852-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a852-118">Description</span></span>                                                                 |
|:------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="1a852-119">**\_"Netwenum"**</span><span class="sxs-lookup"><span data-stu-id="1a852-119">**\_NewEnum**</span></span>](ivmfloppydrivecollection--newenum.md)<br/> | <span data-ttu-id="1a852-120">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1a852-120">Read-only</span></span><br/> | <span data-ttu-id="1a852-121">Ein Enumerator für die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="1a852-121">An enumerator for the collection.</span></span><br/>                                |
| [<span data-ttu-id="1a852-122">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="1a852-122">**Count**</span></span>](ivmfloppydrivecollection-count.md)<br/>        | <span data-ttu-id="1a852-123">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1a852-123">Read-only</span></span><br/> | <span data-ttu-id="1a852-124">Die Anzahl der Diskettenlaufwerke in dieser Auflistung.</span><span class="sxs-lookup"><span data-stu-id="1a852-124">The number of floppy drives in this collection.</span></span><br/>                  |
| [<span data-ttu-id="1a852-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="1a852-125">**Item**</span></span>](ivmfloppydrivecollection-item.md)<br/>          | <span data-ttu-id="1a852-126">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1a852-126">Read-only</span></span><br/> | <span data-ttu-id="1a852-127">Das Disketten Laufwerks Objekt, das dem angegebenen Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="1a852-127">The floppy drive object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1a852-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a852-128">Requirements</span></span>



| <span data-ttu-id="1a852-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1a852-129">Requirement</span></span> | <span data-ttu-id="1a852-130">Wert</span><span class="sxs-lookup"><span data-stu-id="1a852-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a852-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1a852-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1a852-132">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1a852-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1a852-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1a852-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1a852-134">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1a852-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1a852-135">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="1a852-135">End of client support</span></span><br/>    | <span data-ttu-id="1a852-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1a852-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1a852-137">Produkt</span><span class="sxs-lookup"><span data-stu-id="1a852-137">Product</span></span><br/>                  | <span data-ttu-id="1a852-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1a852-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1a852-139">Header</span><span class="sxs-lookup"><span data-stu-id="1a852-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a852-140"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a852-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1a852-141">IID</span><span class="sxs-lookup"><span data-stu-id="1a852-141">IID</span></span><br/>                      | <span data-ttu-id="1a852-142">IID \_ ivmfloppydrivecollection ist als 8ba70a25-s698-4ee5-85ce-3cc93a925516 definiert.</span><span class="sxs-lookup"><span data-stu-id="1a852-142">IID\_IVMFloppyDriveCollection is defined as 8ba70a25-f698-4ee5-85ce-3cc93a925516</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="1a852-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a852-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a852-144">**Ivmfloppydrive**</span><span class="sxs-lookup"><span data-stu-id="1a852-144">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> <dt>

[<span data-ttu-id="1a852-145">**Ivmvirtualmachine:: floppydrives**</span><span class="sxs-lookup"><span data-stu-id="1a852-145">**IVMVirtualMachine::FloppyDrives**</span></span>](ivmvirtualmachine-floppydrives.md)
</dt> </dl>

 

