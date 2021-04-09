---
title: Ivmfloppydrive-Schnittstelle (vpccominterfaces. h)
description: Steuert ein Diskettenlaufwerk innerhalb eines virtuellen Computers.
ms.assetid: b652182a-27ae-4390-81b1-b644a82924df
keywords:
- Ivmfloppydrive Interface Virtual PC
- Virtueller Computer für ivmfloppydrive Interface, beschrieben
topic_type:
- apiref
api_name:
- IVMFloppyDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bab1034bc56c5fe10bb12941bd99309e13e22dca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957021"
---
# <a name="ivmfloppydrive-interface"></a><span data-ttu-id="ba447-105">Ivmfloppydrive-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ba447-105">IVMFloppyDrive interface</span></span>

<span data-ttu-id="ba447-106">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ba447-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ba447-107">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ba447-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ba447-108">Steuert ein Diskettenlaufwerk innerhalb eines virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="ba447-108">Controls a floppy drive within a virtual machine.</span></span> <span data-ttu-id="ba447-109">**Ivmfloppydrive** kann Clients über Ereignisse über die ausgehende Schnittstelle [**ivmfloppydriveevents**](ivmfloppydriveevents.md) benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="ba447-109">**IVMFloppyDrive** can notify clients about events using the [**IVMFloppyDriveEvents**](ivmfloppydriveevents.md) outgoing interface.</span></span> <span data-ttu-id="ba447-110">Sie können ein **ivmfloppydrive** -Objekt aus dem [**ivmfloppydrivecollection**](ivmfloppydrivecollection.md) -Objekt abrufen, das von der [**ivmvirtualmachine:: floppydrives**](ivmvirtualmachine-floppydrives.md) -Eigenschaft zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ba447-110">You can retrieve an **IVMFloppyDrive** object from the [**IVMFloppyDriveCollection**](ivmfloppydrivecollection.md) object returned from the [**IVMVirtualMachine::FloppyDrives**](ivmvirtualmachine-floppydrives.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="ba447-111">Member</span><span class="sxs-lookup"><span data-stu-id="ba447-111">Members</span></span>

<span data-ttu-id="ba447-112">Die **ivmfloppydrive** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ba447-112">The **IVMFloppyDrive** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="ba447-113">**Ivmfloppydrive** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ba447-113">**IVMFloppyDrive** also has these types of members:</span></span>

-   [<span data-ttu-id="ba447-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="ba447-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="ba447-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ba447-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ba447-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="ba447-116">Methods</span></span>

<span data-ttu-id="ba447-117">Die **ivmfloppydrive** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="ba447-117">The **IVMFloppyDrive** interface has these methods.</span></span>



| <span data-ttu-id="ba447-118">Methode</span><span class="sxs-lookup"><span data-stu-id="ba447-118">Method</span></span>                                                      | <span data-ttu-id="ba447-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ba447-119">Description</span></span>                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ba447-120">**AttachHostDrive**</span><span class="sxs-lookup"><span data-stu-id="ba447-120">**AttachHostDrive**</span></span>](ivmfloppydrive-attachhostdrive.md)   | <span data-ttu-id="ba447-121">Fügt ein physisches Laufwerk auf dem Host an das Diskettenlaufwerk auf dem virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="ba447-121">Attaches a physical drive on the host to the floppy drive in the virtual machine.</span></span><br/> |
| [<span data-ttu-id="ba447-122">**Attachimage**</span><span class="sxs-lookup"><span data-stu-id="ba447-122">**AttachImage**</span></span>](ivmfloppydrive-attachimage.md)           | <span data-ttu-id="ba447-123">Fügt ein Disketten Medienbild auf dem Host an das Diskettenlaufwerk an.</span><span class="sxs-lookup"><span data-stu-id="ba447-123">Attaches a floppy media image on the host to the floppy drive.</span></span><br/>                    |
| [<span data-ttu-id="ba447-124">**Releasehostlaufwerk**</span><span class="sxs-lookup"><span data-stu-id="ba447-124">**ReleaseHostDrive**</span></span>](ivmfloppydrive-releasehostdrive.md) | <span data-ttu-id="ba447-125">Gibt ein physisches Laufwerk auf dem Host vom Diskettenlaufwerk frei.</span><span class="sxs-lookup"><span data-stu-id="ba447-125">Releases a physical drive on the host from the floppy drive.</span></span><br/>                      |
| [<span data-ttu-id="ba447-126">**ReleaseImage**</span><span class="sxs-lookup"><span data-stu-id="ba447-126">**ReleaseImage**</span></span>](ivmfloppydrive-releaseimage.md)         | <span data-ttu-id="ba447-127">Gibt ein Disketten Medienbild auf dem Host vom Diskettenlaufwerk aus.</span><span class="sxs-lookup"><span data-stu-id="ba447-127">Releases a floppy media image on the host from the floppy drive.</span></span><br/>                  |



 

### <a name="properties"></a><span data-ttu-id="ba447-128">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ba447-128">Properties</span></span>

<span data-ttu-id="ba447-129">Die **ivmfloppydrive** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ba447-129">The **IVMFloppyDrive** interface has these properties.</span></span>



| <span data-ttu-id="ba447-130">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ba447-130">Property</span></span>                                                             | <span data-ttu-id="ba447-131">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="ba447-131">Access type</span></span>          | <span data-ttu-id="ba447-132">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ba447-132">Description</span></span>                                                                               |
|:---------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ba447-133">**Attachment**</span><span class="sxs-lookup"><span data-stu-id="ba447-133">**Attachment**</span></span>](ivmfloppydrive-attachment.md)<br/>           | <span data-ttu-id="ba447-134">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ba447-134">Read-only</span></span><br/> | <span data-ttu-id="ba447-135">Der Medientyp, der mit dem Diskettenlaufwerk innerhalb des virtuellen Computers verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="ba447-135">The type of media attached to the floppy drive within the virtual machine.</span></span><br/>     |
| [<span data-ttu-id="ba447-136">**Drivenreiber**</span><span class="sxs-lookup"><span data-stu-id="ba447-136">**DriveNumber**</span></span>](ivmfloppydrive-drivenumber.md)<br/>         | <span data-ttu-id="ba447-137">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ba447-137">Read-only</span></span><br/> | <span data-ttu-id="ba447-138">Der null basierte Index des Controllers, an den dieses Diskettenlaufwerk angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="ba447-138">The zero-based index of the controller to which this floppy drive is attached.</span></span><br/> |
| [<span data-ttu-id="ba447-139">**Hostdriveletter**</span><span class="sxs-lookup"><span data-stu-id="ba447-139">**HostDriveLetter**</span></span>](ivmfloppydrive-hostdriveletter.md)<br/> | <span data-ttu-id="ba447-140">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ba447-140">Read-only</span></span><br/> | <span data-ttu-id="ba447-141">Der Buchstabe des Host Laufwerks, an das das Diskettenlaufwerk angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="ba447-141">The letter of the host drive to which the floppy drive is attached.</span></span><br/>            |
| [<span data-ttu-id="ba447-142">**ImageFile**</span><span class="sxs-lookup"><span data-stu-id="ba447-142">**ImageFile**</span></span>](ivmfloppydrive-imagefile.md)<br/>             | <span data-ttu-id="ba447-143">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ba447-143">Read-only</span></span><br/> | <span data-ttu-id="ba447-144">Der vollständige Pfad der Bilddatei, an die das Diskettenlaufwerk angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="ba447-144">The full path of the image file to which the floppy drive is attached.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="ba447-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba447-145">Requirements</span></span>



| <span data-ttu-id="ba447-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ba447-146">Requirement</span></span> | <span data-ttu-id="ba447-147">Wert</span><span class="sxs-lookup"><span data-stu-id="ba447-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba447-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ba447-148">Minimum supported client</span></span><br/> | <span data-ttu-id="ba447-149">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ba447-149">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ba447-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ba447-150">Minimum supported server</span></span><br/> | <span data-ttu-id="ba447-151">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ba447-151">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ba447-152">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="ba447-152">End of client support</span></span><br/>    | <span data-ttu-id="ba447-153">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ba447-153">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ba447-154">Produkt</span><span class="sxs-lookup"><span data-stu-id="ba447-154">Product</span></span><br/>                  | <span data-ttu-id="ba447-155">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ba447-155">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ba447-156">Header</span><span class="sxs-lookup"><span data-stu-id="ba447-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba447-157"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba447-157"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ba447-158">IID</span><span class="sxs-lookup"><span data-stu-id="ba447-158">IID</span></span><br/>                      | <span data-ttu-id="ba447-159">IID \_ ivmfloppydrive ist als 661abee6-112a-4ed9-BABF -3c874969s10e definiert.</span><span class="sxs-lookup"><span data-stu-id="ba447-159">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



 

