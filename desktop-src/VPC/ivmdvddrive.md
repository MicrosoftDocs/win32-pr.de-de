---
title: Ivmdvddrive-Schnittstelle (vpccominterfaces. h)
description: Steuert ein CD-ROM-oder DVD-ROM-Laufwerk innerhalb einer virtuellen Maschine. Ivmdvddrive kann Clients über Ereignisse über die ausgehende Schnittstelle ivmdvddriveevents benachrichtigen.
ms.assetid: 0900b3a8-ba52-4c26-bd96-b37334d6d03c
keywords:
- Ivmdvddrive Interface Virtual PC
- Virtueller Computer für ivmdvddrive Interface, beschrieben
topic_type:
- apiref
api_name:
- IVMDVDDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 951213923f74f8425fc4d9eaec85e76f7481eeb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040744"
---
# <a name="ivmdvddrive-interface"></a><span data-ttu-id="f909a-106">Ivmdvddrive-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f909a-106">IVMDVDDrive interface</span></span>

<span data-ttu-id="f909a-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f909a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f909a-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f909a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f909a-109">Steuert ein CD-ROM-oder DVD-ROM-Laufwerk innerhalb einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="f909a-109">Controls a CD-ROM or DVD-ROM drive within a virtual machine.</span></span> <span data-ttu-id="f909a-110">**Ivmdvddrive** kann Clients über Ereignisse über die ausgehende Schnittstelle [**ivmdvddriveevents**](ivmdvddriveevents.md) benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="f909a-110">**IVMDVDDrive** can notify clients about events using the [**IVMDVDDriveEvents**](ivmdvddriveevents.md) outgoing interface.</span></span>

<span data-ttu-id="f909a-111">Sie können ein neues CD-ROM-oder DVD-ROM-Laufwerk mithilfe der [**ivmvirtualmachine:: AddDVDROMDrive**](ivmvirtualmachine-adddvdromdrive.md) -Methode zu einem virtuellen Computer hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f909a-111">You can add a new CD-ROM or DVD-ROM drive to a virtual machine using the [**IVMVirtualMachine::AddDVDROMDrive**](ivmvirtualmachine-adddvdromdrive.md) method.</span></span> <span data-ttu-id="f909a-112">Sie können ein vorhandenes CD-ROM-oder DVD-ROM-Laufwerk mithilfe der [**ivmvirtualmachine:: removedvdromdrive**](ivmvirtualmachine-removedvdromdrive.md) -Methode von einem virtuellen Computer entfernen.</span><span class="sxs-lookup"><span data-stu-id="f909a-112">You can remove an existing CD-ROM or DVD-ROM drive from a virtual machine using the [**IVMVirtualMachine::RemoveDVDROMDrive**](ivmvirtualmachine-removedvdromdrive.md) method.</span></span> <span data-ttu-id="f909a-113">Sie können ein **ivmdvddrive** -Objekt aus dem [**ivmdvddrivecollection**](ivmdvddrivecollection.md) -Objekt abrufen, das von der [**ivmvirtualmachine::D vdromdrives**](ivmvirtualmachine-dvdromdrives.md) -Eigenschaft zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f909a-113">You can retrieve an **IVMDVDDrive** object from the [**IVMDVDDriveCollection**](ivmdvddrivecollection.md) object returned from the [**IVMVirtualMachine::DVDROMDrives**](ivmvirtualmachine-dvdromdrives.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="f909a-114">Member</span><span class="sxs-lookup"><span data-stu-id="f909a-114">Members</span></span>

<span data-ttu-id="f909a-115">Die **ivmdvddrive** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f909a-115">The **IVMDVDDrive** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="f909a-116">**Ivmdvddrive** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f909a-116">**IVMDVDDrive** also has these types of members:</span></span>

-   [<span data-ttu-id="f909a-117">Methoden</span><span class="sxs-lookup"><span data-stu-id="f909a-117">Methods</span></span>](#methods)
-   [<span data-ttu-id="f909a-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f909a-118">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f909a-119">Methoden</span><span class="sxs-lookup"><span data-stu-id="f909a-119">Methods</span></span>

<span data-ttu-id="f909a-120">Die **ivmdvddrive** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f909a-120">The **IVMDVDDrive** interface has these methods.</span></span>



| <span data-ttu-id="f909a-121">Methode</span><span class="sxs-lookup"><span data-stu-id="f909a-121">Method</span></span>                                                   | <span data-ttu-id="f909a-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f909a-122">Description</span></span>                                                                             |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="f909a-123">**AttachHostDrive**</span><span class="sxs-lookup"><span data-stu-id="f909a-123">**AttachHostDrive**</span></span>](ivmdvddrive-attachhostdrive.md)   | <span data-ttu-id="f909a-124">Fügt ein Host Laufwerk an das DVD-Laufwerk innerhalb der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="f909a-124">Attaches a host drive to the DVD drive within the virtual machine.</span></span><br/>           |
| [<span data-ttu-id="f909a-125">**Attachimage**</span><span class="sxs-lookup"><span data-stu-id="f909a-125">**AttachImage**</span></span>](ivmdvddrive-attachimage.md)           | <span data-ttu-id="f909a-126">Fügt ein ISO-Abbild an das DVD-Laufwerk innerhalb des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="f909a-126">Attaches an ISO image to the DVD drive within the virtual machine.</span></span><br/>           |
| [<span data-ttu-id="f909a-127">**Releasehostlaufwerk**</span><span class="sxs-lookup"><span data-stu-id="f909a-127">**ReleaseHostDrive**</span></span>](ivmdvddrive-releasehostdrive.md) | <span data-ttu-id="f909a-128">Gibt ein erfasstes Host Laufwerk vom DVD-Laufwerk frei.</span><span class="sxs-lookup"><span data-stu-id="f909a-128">Releases a captured host drive from the DVD drive.</span></span><br/>                           |
| [<span data-ttu-id="f909a-129">**ReleaseImage**</span><span class="sxs-lookup"><span data-stu-id="f909a-129">**ReleaseImage**</span></span>](ivmdvddrive-releaseimage.md)         | <span data-ttu-id="f909a-130">Gibt ein erfasstes ISO-Abbild vom DVD-Laufwerk frei.</span><span class="sxs-lookup"><span data-stu-id="f909a-130">Releases a captured ISO image from the DVD drive.</span></span><br/>                            |
| [<span data-ttu-id="f909a-131">**Setbuslokation**</span><span class="sxs-lookup"><span data-stu-id="f909a-131">**SetBusLocation**</span></span>](ivmdvddrive-setbuslocation.md)     | <span data-ttu-id="f909a-132">Fügt das DVD-Laufwerk an die angegebene busposition auf dem virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="f909a-132">Attaches the DVD drive to the specified bus location in the virtual machine.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f909a-133">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f909a-133">Properties</span></span>

<span data-ttu-id="f909a-134">Die **ivmdvddrive** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f909a-134">The **IVMDVDDrive** interface has these properties.</span></span>



| <span data-ttu-id="f909a-135">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f909a-135">Property</span></span>                                                          | <span data-ttu-id="f909a-136">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="f909a-136">Access type</span></span>          | <span data-ttu-id="f909a-137">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f909a-137">Description</span></span>                                                                        |
|:------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="f909a-138">**Attachment**</span><span class="sxs-lookup"><span data-stu-id="f909a-138">**Attachment**</span></span>](ivmdvddrive-attachment.md)<br/>           | <span data-ttu-id="f909a-139">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f909a-139">Read-only</span></span><br/> | <span data-ttu-id="f909a-140">Der Medientyp, der mit dem DVD-Laufwerk innerhalb des virtuellen Computers verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="f909a-140">The type of media attached to the DVD drive within the virtual machine.</span></span><br/> |
| [<span data-ttu-id="f909a-141">**Busnummer**</span><span class="sxs-lookup"><span data-stu-id="f909a-141">**BusNumber**</span></span>](ivmdvddrive-busnumber.md)<br/>             | <span data-ttu-id="f909a-142">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f909a-142">Read-only</span></span><br/> | <span data-ttu-id="f909a-143">Die Busnummer, an die dieses Gerät angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="f909a-143">The bus number to which this device is attached.</span></span><br/>                        |
| [<span data-ttu-id="f909a-144">**Devicengegen ber**</span><span class="sxs-lookup"><span data-stu-id="f909a-144">**DeviceNumber**</span></span>](ivmdvddrive-devicenumber.md)<br/>       | <span data-ttu-id="f909a-145">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f909a-145">Read-only</span></span><br/> | <span data-ttu-id="f909a-146">Die Gerätenummer, an die dieses Laufwerk angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="f909a-146">The device number to which this drive is attached.</span></span><br/>                      |
| [<span data-ttu-id="f909a-147">**Hostdriveletter**</span><span class="sxs-lookup"><span data-stu-id="f909a-147">**HostDriveLetter**</span></span>](ivmdvddrive-hostdriveletter.md)<br/> | <span data-ttu-id="f909a-148">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f909a-148">Read-only</span></span><br/> | <span data-ttu-id="f909a-149">Der Buchstabe des Host Laufwerks, das für dieses Gerät festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f909a-149">The letter of the host drive set for this device.</span></span><br/>                       |
| [<span data-ttu-id="f909a-150">**ImageFile**</span><span class="sxs-lookup"><span data-stu-id="f909a-150">**ImageFile**</span></span>](ivmdvddrive-imagefile.md)<br/>             | <span data-ttu-id="f909a-151">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f909a-151">Read-only</span></span><br/> | <span data-ttu-id="f909a-152">Der vollständige Pfad der Bilddatei, die für dieses Gerät festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f909a-152">The full path of the image file set for this device.</span></span><br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="f909a-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f909a-153">Requirements</span></span>



| <span data-ttu-id="f909a-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f909a-154">Requirement</span></span> | <span data-ttu-id="f909a-155">Wert</span><span class="sxs-lookup"><span data-stu-id="f909a-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f909a-156">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f909a-156">Minimum supported client</span></span><br/> | <span data-ttu-id="f909a-157">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f909a-157">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f909a-158">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f909a-158">Minimum supported server</span></span><br/> | <span data-ttu-id="f909a-159">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f909a-159">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f909a-160">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f909a-160">End of client support</span></span><br/>    | <span data-ttu-id="f909a-161">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f909a-161">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f909a-162">Produkt</span><span class="sxs-lookup"><span data-stu-id="f909a-162">Product</span></span><br/>                  | <span data-ttu-id="f909a-163">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f909a-163">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f909a-164">Header</span><span class="sxs-lookup"><span data-stu-id="f909a-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="f909a-165"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f909a-165"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f909a-166">IID</span><span class="sxs-lookup"><span data-stu-id="f909a-166">IID</span></span><br/>                      | <span data-ttu-id="f909a-167">IID \_ ivmdvddrive ist als b96328f6-6732-437d-a00d-ffa47e43971c definiert.</span><span class="sxs-lookup"><span data-stu-id="f909a-167">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



 

