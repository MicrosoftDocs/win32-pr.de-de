---
title: Ivmharddisk-Schnittstelle (vpccominterfaces. h)
description: Ermöglicht den Zugriff auf ein Festplatten Abbild. Der Zugriff ist über die Eigenschaft "ivmharddiskconnection Harddisk" oder die Methode "ivmvirtualpc getharddisk" möglich.
ms.assetid: 0c536906-91be-428a-8199-c452abef423d
keywords:
- Ivmharddisk Interface Virtual PC
- Virtueller Computer für ivmharddisk Interface, beschrieben
topic_type:
- apiref
api_name:
- IVMHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24d6df46e7c698676e3873dd17a854fd0b7d7933
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475039"
---
# <a name="ivmharddisk-interface"></a><span data-ttu-id="82c9f-106">Ivmharddisk-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="82c9f-106">IVMHardDisk interface</span></span>

<span data-ttu-id="82c9f-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="82c9f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="82c9f-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="82c9f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="82c9f-109">Ermöglicht den Zugriff auf ein Festplatten Abbild.</span><span class="sxs-lookup"><span data-stu-id="82c9f-109">Provides access to a hard disk image.</span></span> <span data-ttu-id="82c9f-110">Sie können über die [**ivmharddiskconnection:: Harddisk**](ivmharddiskconnection-harddisk.md) -Eigenschaft oder die [**ivmvirtualpc:: getharddisk**](ivmvirtualpc-getharddisk.md) -Methode darauf zugreifen.</span><span class="sxs-lookup"><span data-stu-id="82c9f-110">It can be accessed through the [**IVMHardDiskConnection::HardDisk**](ivmharddiskconnection-harddisk.md) property or the [**IVMVirtualPC::GetHardDisk**](ivmvirtualpc-getharddisk.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="82c9f-111">Member</span><span class="sxs-lookup"><span data-stu-id="82c9f-111">Members</span></span>

<span data-ttu-id="82c9f-112">Die **ivmharddisk** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="82c9f-112">The **IVMHardDisk** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="82c9f-113">**Ivmharddisk** verfügt auch über die folgenden Typen von Mitgliedern:</span><span class="sxs-lookup"><span data-stu-id="82c9f-113">**IVMHardDisk** also has these types of members:</span></span>

-   [<span data-ttu-id="82c9f-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="82c9f-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="82c9f-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="82c9f-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="82c9f-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="82c9f-116">Methods</span></span>

<span data-ttu-id="82c9f-117">Die **ivmharddisk** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="82c9f-117">The **IVMHardDisk** interface has these methods.</span></span>



| <span data-ttu-id="82c9f-118">Methode</span><span class="sxs-lookup"><span data-stu-id="82c9f-118">Method</span></span>                                 | <span data-ttu-id="82c9f-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="82c9f-119">Description</span></span>                                                                                                                                                 |
|:---------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82c9f-120">**Kompakt**</span><span class="sxs-lookup"><span data-stu-id="82c9f-120">**Compact**</span></span>](ivmharddisk-compact.md) | <span data-ttu-id="82c9f-121">Komprimiert eine dynamisch erweiterbare virtuelle Festplatten Abbild.</span><span class="sxs-lookup"><span data-stu-id="82c9f-121">Compacts a dynamically expanding virtual hard disk image.</span></span><br/>                                                                                        |
| [<span data-ttu-id="82c9f-122">**Umgebaut**</span><span class="sxs-lookup"><span data-stu-id="82c9f-122">**Convert**</span></span>](ivmharddisk-convert.md) | <span data-ttu-id="82c9f-123">Konvertiert eine virtuelle Festplatte entweder in eine dynamisch erweiterbare virtuelle Festplatte oder eine virtuelle Festplatte mit fester Größe.</span><span class="sxs-lookup"><span data-stu-id="82c9f-123">Converts any virtual hard disk to either a dynamically expanding virtual hard disk or a fixed-size virtual hard disk.</span></span><br/>                            |
| [<span data-ttu-id="82c9f-124">**Merge**</span><span class="sxs-lookup"><span data-stu-id="82c9f-124">**Merge**</span></span>](ivmharddisk-merge.md)     | <span data-ttu-id="82c9f-125">Führt eine differenzierende virtuelle Festplatte mit dem übergeordneten Datenträger Image zusammen.</span><span class="sxs-lookup"><span data-stu-id="82c9f-125">Merges a differencing virtual hard disk with its parent disk image.</span></span><br/>                                                                              |
| [<span data-ttu-id="82c9f-126">**Mergeto**</span><span class="sxs-lookup"><span data-stu-id="82c9f-126">**MergeTo**</span></span>](ivmharddisk-mergeto.md) | <span data-ttu-id="82c9f-127">Führt eine differenzierende virtuelle Festplatte mit allen übergeordneten Elementen (bis einschließlich der übergeordneten virtuellen Festplatte) einer neuen Festplatten Datei zusammen.</span><span class="sxs-lookup"><span data-stu-id="82c9f-127">Merges a differencing virtual hard disk with all of its parents (up to and including the root parent virtual hard disk) to a new hard disk file.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="82c9f-128">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="82c9f-128">Properties</span></span>

<span data-ttu-id="82c9f-129">Die **ivmharddisk** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="82c9f-129">The **IVMHardDisk** interface has these properties.</span></span>



| <span data-ttu-id="82c9f-130">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="82c9f-130">Property</span></span>                                                              | <span data-ttu-id="82c9f-131">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="82c9f-131">Access type</span></span>           | <span data-ttu-id="82c9f-132">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="82c9f-132">Description</span></span>                                                                                    |
|:----------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82c9f-133">**Datei**</span><span class="sxs-lookup"><span data-stu-id="82c9f-133">**File**</span></span>](ivmharddisk-file.md)<br/>                           | <span data-ttu-id="82c9f-134">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82c9f-134">Read-only</span></span><br/>  | <span data-ttu-id="82c9f-135">Der vollständige Pfadname der virtuellen Festplatten Datei.</span><span class="sxs-lookup"><span data-stu-id="82c9f-135">The full path name of the virtual hard disk file.</span></span><br/>                                   |
| [<span data-ttu-id="82c9f-136">**Hostfrediskspace**</span><span class="sxs-lookup"><span data-stu-id="82c9f-136">**HostFreeDiskSpace**</span></span>](ivmharddisk-hostfreediskspace.md)<br/> | <span data-ttu-id="82c9f-137">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82c9f-137">Read-only</span></span><br/>  | <span data-ttu-id="82c9f-138">Die Menge des verbleibenden Speicherplatzes, der auf dem Host für die virtuelle Festplatte verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="82c9f-138">The amount of remaining disk space available on the host for the virtual hard disk.</span></span><br/> |
| [<span data-ttu-id="82c9f-139">**Parent**</span><span class="sxs-lookup"><span data-stu-id="82c9f-139">**Parent**</span></span>](ivmharddisk-parent.md)<br/>                       | <span data-ttu-id="82c9f-140">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="82c9f-140">Read/write</span></span><br/> | <span data-ttu-id="82c9f-141">Das übergeordnete Element der differenzierenden virtuellen Festplatte.</span><span class="sxs-lookup"><span data-stu-id="82c9f-141">The parent of the differencing virtual hard disk.</span></span><br/>                                   |
| [<span data-ttu-id="82c9f-142">**Sizeingeguest**</span><span class="sxs-lookup"><span data-stu-id="82c9f-142">**SizeInGuest**</span></span>](ivmharddisk-sizeinguest.md)<br/>             | <span data-ttu-id="82c9f-143">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82c9f-143">Read-only</span></span><br/>  | <span data-ttu-id="82c9f-144">Die Größe der virtuellen Festplatte im Gast Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="82c9f-144">The size of the virtual hard disk in the guest operating system.</span></span><br/>                    |
| [<span data-ttu-id="82c9f-145">**Sizeonhost**</span><span class="sxs-lookup"><span data-stu-id="82c9f-145">**SizeOnHost**</span></span>](ivmharddisk-sizeonhost.md)<br/>               | <span data-ttu-id="82c9f-146">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82c9f-146">Read-only</span></span><br/>  | <span data-ttu-id="82c9f-147">Die Größe der virtuellen Festplatten Datei auf dem Host Computer.</span><span class="sxs-lookup"><span data-stu-id="82c9f-147">The size of the virtual hard disk file on the host computer.</span></span><br/>                        |
| [<span data-ttu-id="82c9f-148">**type**</span><span class="sxs-lookup"><span data-stu-id="82c9f-148">**Type**</span></span>](ivmharddisk-type.md)<br/>                           | <span data-ttu-id="82c9f-149">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82c9f-149">Read-only</span></span><br/>  | <span data-ttu-id="82c9f-150">Der Typ der virtuellen Festplatte.</span><span class="sxs-lookup"><span data-stu-id="82c9f-150">The type of the virtual hard disk.</span></span><br/>                                                  |



 

## <a name="requirements"></a><span data-ttu-id="82c9f-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="82c9f-151">Requirements</span></span>



| <span data-ttu-id="82c9f-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82c9f-152">Requirement</span></span> | <span data-ttu-id="82c9f-153">Wert</span><span class="sxs-lookup"><span data-stu-id="82c9f-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="82c9f-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="82c9f-154">Minimum supported client</span></span><br/> | <span data-ttu-id="82c9f-155">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="82c9f-155">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="82c9f-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="82c9f-156">Minimum supported server</span></span><br/> | <span data-ttu-id="82c9f-157">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="82c9f-157">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="82c9f-158">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="82c9f-158">End of client support</span></span><br/>    | <span data-ttu-id="82c9f-159">Windows 7</span><span class="sxs-lookup"><span data-stu-id="82c9f-159">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="82c9f-160">Produkt</span><span class="sxs-lookup"><span data-stu-id="82c9f-160">Product</span></span><br/>                  | <span data-ttu-id="82c9f-161">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="82c9f-161">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="82c9f-162">Header</span><span class="sxs-lookup"><span data-stu-id="82c9f-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="82c9f-163"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="82c9f-163"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="82c9f-164">IID</span><span class="sxs-lookup"><span data-stu-id="82c9f-164">IID</span></span><br/>                      | <span data-ttu-id="82c9f-165">IID \_ ivmharddisk ist als ffa14ae6-48f5-42a4-8a22-186f2e5c7db0 definiert.</span><span class="sxs-lookup"><span data-stu-id="82c9f-165">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



 

