---
title: Ivmharddiskconnection-Schnittstelle (vpccominterfaces. h)
description: Definiert die Verbindung für eine Festplatte innerhalb des virtuellen Computers.
ms.assetid: 7ba1ace5-a3af-4b97-b329-f12a0ecbf7d3
keywords:
- Virtuelle Computer der ivmharddiskconnection-Schnittstelle
- Virtueller Computer für die ivmharddiskconnection-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IVMHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e53a092bdca26eee0c46db1d75f7fc040d5ce7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342023"
---
# <a name="ivmharddiskconnection-interface"></a><span data-ttu-id="d7ee1-105">Ivmharddiskconnection-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d7ee1-105">IVMHardDiskConnection interface</span></span>

<span data-ttu-id="d7ee1-106">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d7ee1-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d7ee1-107">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d7ee1-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d7ee1-108">Definiert die Verbindung für eine Festplatte innerhalb des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="d7ee1-108">Defines the connection for a hard disk within the virtual machine.</span></span> <span data-ttu-id="d7ee1-109">Ein **ivmharddiskconnection** -Objekt wird von der [**ivmvirtualmachine:: AddHardDiskConnection**](ivmvirtualmachine-addharddiskconnection.md) -Methode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d7ee1-109">An **IVMHardDiskConnection** object is returned from the [**IVMVirtualMachine::AddHardDiskConnection**](ivmvirtualmachine-addharddiskconnection.md) method.</span></span> <span data-ttu-id="d7ee1-110">Sie können auch ein **ivmharddiskconnection** -Objekt aus dem [**ivmharddiskconnectioncollection**](ivmharddiskconnectioncollection.md) -Objekt abrufen, das von der [**ivmvirtualmachine:: harddiskconnections**](ivmvirtualmachine-harddiskconnections.md) -Eigenschaft zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d7ee1-110">You can also retrieve an **IVMHardDiskConnection** object from the [**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md) object returned from the [**IVMVirtualMachine::HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="d7ee1-111">Member</span><span class="sxs-lookup"><span data-stu-id="d7ee1-111">Members</span></span>

<span data-ttu-id="d7ee1-112">Die **ivmharddiskconnection** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d7ee1-112">The **IVMHardDiskConnection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="d7ee1-113">**Ivmharddiskconnection** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d7ee1-113">**IVMHardDiskConnection** also has these types of members:</span></span>

-   [<span data-ttu-id="d7ee1-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="d7ee1-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="d7ee1-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d7ee1-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d7ee1-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="d7ee1-116">Methods</span></span>

<span data-ttu-id="d7ee1-117">Die **ivmharddiskconnection** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="d7ee1-117">The **IVMHardDiskConnection** interface has these methods.</span></span>



| <span data-ttu-id="d7ee1-118">Methode</span><span class="sxs-lookup"><span data-stu-id="d7ee1-118">Method</span></span>                                                         | <span data-ttu-id="d7ee1-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d7ee1-119">Description</span></span>                                                           |
|:---------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="d7ee1-120">**Setbuslokation**</span><span class="sxs-lookup"><span data-stu-id="d7ee1-120">**SetBusLocation**</span></span>](ivmharddiskconnection-setbuslocation.md) | <span data-ttu-id="d7ee1-121">Legt den Busspeicherort fest, an den diese Festplatte angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="d7ee1-121">Sets the bus location to which this hard disk is attached.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d7ee1-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d7ee1-122">Properties</span></span>

<span data-ttu-id="d7ee1-123">Die **ivmharddiskconnection** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d7ee1-123">The **IVMHardDiskConnection** interface has these properties.</span></span>



| <span data-ttu-id="d7ee1-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d7ee1-124">Property</span></span>                                                              | <span data-ttu-id="d7ee1-125">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="d7ee1-125">Access type</span></span>          | <span data-ttu-id="d7ee1-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d7ee1-126">Description</span></span>                                                                       |
|:----------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="d7ee1-127">**Busnummer**</span><span class="sxs-lookup"><span data-stu-id="d7ee1-127">**BusNumber**</span></span>](ivmharddiskconnection-busnumber.md)<br/>       | <span data-ttu-id="d7ee1-128">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d7ee1-128">Read-only</span></span><br/> | <span data-ttu-id="d7ee1-129">Die Busnummer, an die das Laufwerks Bild angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="d7ee1-129">The bus number to which the drive image is attached.</span></span><br/>                   |
| [<span data-ttu-id="d7ee1-130">**Devicengegen ber**</span><span class="sxs-lookup"><span data-stu-id="d7ee1-130">**DeviceNumber**</span></span>](ivmharddiskconnection-devicenumber.md)<br/> | <span data-ttu-id="d7ee1-131">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d7ee1-131">Read-only</span></span><br/> | <span data-ttu-id="d7ee1-132">Die Gerätenummer, an die das Laufwerks Image angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="d7ee1-132">The device number to which the drive image is attached.</span></span><br/>                |
| [<span data-ttu-id="d7ee1-133">**Festplatten**</span><span class="sxs-lookup"><span data-stu-id="d7ee1-133">**HardDisk**</span></span>](ivmharddiskconnection-harddisk.md)<br/>         | <span data-ttu-id="d7ee1-134">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d7ee1-134">Read-only</span></span><br/> | <span data-ttu-id="d7ee1-135">Ein Festplatten Objekt, das dieser Verbindung entspricht.</span><span class="sxs-lookup"><span data-stu-id="d7ee1-135">A hard disk object corresponding to this connection.</span></span><br/>                   |
| [<span data-ttu-id="d7ee1-136">**Undoharddisk**</span><span class="sxs-lookup"><span data-stu-id="d7ee1-136">**UndoHardDisk**</span></span>](ivmharddiskconnection-undoharddisk.md)<br/> | <span data-ttu-id="d7ee1-137">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d7ee1-137">Read-only</span></span><br/> | <span data-ttu-id="d7ee1-138">Ein Festplatten Objekt, das dem Rückgängig-Datenträger Image dieser Verbindung entspricht.</span><span class="sxs-lookup"><span data-stu-id="d7ee1-138">A hard disk object corresponding to this connection's undo disk image.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d7ee1-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d7ee1-139">Requirements</span></span>



| <span data-ttu-id="d7ee1-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d7ee1-140">Requirement</span></span> | <span data-ttu-id="d7ee1-141">Wert</span><span class="sxs-lookup"><span data-stu-id="d7ee1-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7ee1-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d7ee1-142">Minimum supported client</span></span><br/> | <span data-ttu-id="d7ee1-143">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7ee1-143">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d7ee1-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d7ee1-144">Minimum supported server</span></span><br/> | <span data-ttu-id="d7ee1-145">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d7ee1-145">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d7ee1-146">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="d7ee1-146">End of client support</span></span><br/>    | <span data-ttu-id="d7ee1-147">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d7ee1-147">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d7ee1-148">Produkt</span><span class="sxs-lookup"><span data-stu-id="d7ee1-148">Product</span></span><br/>                  | <span data-ttu-id="d7ee1-149">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d7ee1-149">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d7ee1-150">Header</span><span class="sxs-lookup"><span data-stu-id="d7ee1-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7ee1-151"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7ee1-151"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d7ee1-152">IID</span><span class="sxs-lookup"><span data-stu-id="d7ee1-152">IID</span></span><br/>                      | <span data-ttu-id="d7ee1-153">IID \_ ivmharddiskconnection ist als aefa36a5-463a-46AE-9e6c-a1fb4e12e671 definiert.</span><span class="sxs-lookup"><span data-stu-id="d7ee1-153">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



 

