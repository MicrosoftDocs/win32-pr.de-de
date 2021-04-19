---
title: Ivmusbdevice-Schnittstelle (vpccominterfaces. h)
description: Definiert die Schnittstelle für ein USB-Gerät, das dem Host zugeordnet ist. Sie können ein USB-Gerät an einen virtuellen Computer anfügen, um das Gerät auf dem virtuellen Computer zu verwenden.
ms.assetid: f491fe8f-bc43-4dfa-b9c1-c93b4e5a7df6
keywords:
- Ivmusbdevice Interface Virtual PC
- Virtueller Computer für ivmusbdevice Interface, beschrieben
topic_type:
- apiref
api_name:
- IVMUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a1547bd812ea6d8f117f5910a254334676cafd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338342"
---
# <a name="ivmusbdevice-interface"></a><span data-ttu-id="c0d2f-106">Ivmusbdevice-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="c0d2f-106">IVMUSBDevice interface</span></span>

<span data-ttu-id="c0d2f-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c0d2f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c0d2f-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c0d2f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c0d2f-109">Definiert die Schnittstelle für ein USB-Gerät, das dem Host zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c0d2f-109">Defines the interface for a USB device attached to host.</span></span> <span data-ttu-id="c0d2f-110">Sie können ein USB-Gerät an einen virtuellen Computer anfügen, um das Gerät auf dem virtuellen Computer zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c0d2f-110">You can attach USB device to a virtual machine to use the device inside the virtual machine.</span></span>

## <a name="members"></a><span data-ttu-id="c0d2f-111">Member</span><span class="sxs-lookup"><span data-stu-id="c0d2f-111">Members</span></span>

<span data-ttu-id="c0d2f-112">Die **ivmusbdevice** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c0d2f-112">The **IVMUSBDevice** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="c0d2f-113">**Ivmusbdevice** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c0d2f-113">**IVMUSBDevice** also has these types of members:</span></span>

-   [<span data-ttu-id="c0d2f-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c0d2f-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c0d2f-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c0d2f-115">Properties</span></span>

<span data-ttu-id="c0d2f-116">Die **ivmusbdevice** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c0d2f-116">The **IVMUSBDevice** interface has these properties.</span></span>



| <span data-ttu-id="c0d2f-117">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c0d2f-117">Property</span></span>                                                                 | <span data-ttu-id="c0d2f-118">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="c0d2f-118">Access type</span></span>          | <span data-ttu-id="c0d2f-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c0d2f-119">Description</span></span>                                                                     |
|:-------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="c0d2f-120">**"AttachedTo VM"**</span><span class="sxs-lookup"><span data-stu-id="c0d2f-120">**AttachedToVM**</span></span>](ivmusbdevice-attachedtovm.md)<br/>             | <span data-ttu-id="c0d2f-121">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c0d2f-121">Read-only</span></span><br/> | <span data-ttu-id="c0d2f-122">Der Name des virtuellen Computers, an den das USB-Gerät angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="c0d2f-122">The name of the virtual machine to which the USB device is attached.</span></span><br/> |
| [<span data-ttu-id="c0d2f-123">**DeviceClass**</span><span class="sxs-lookup"><span data-stu-id="c0d2f-123">**DeviceClass**</span></span>](ivmusbdevice-deviceclass.md)<br/>               | <span data-ttu-id="c0d2f-124">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c0d2f-124">Read-only</span></span><br/> | <span data-ttu-id="c0d2f-125">Die Geräteklasse des USB-Geräts.</span><span class="sxs-lookup"><span data-stu-id="c0d2f-125">The device class of the USB device.</span></span><br/>                                  |
| [<span data-ttu-id="c0d2f-126">**Devicestring**</span><span class="sxs-lookup"><span data-stu-id="c0d2f-126">**DeviceString**</span></span>](ivmusbdevice-devicestring.md)<br/>             | <span data-ttu-id="c0d2f-127">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c0d2f-127">Read-only</span></span><br/> | <span data-ttu-id="c0d2f-128">Der Name des USB-Geräts.</span><span class="sxs-lookup"><span data-stu-id="c0d2f-128">The name of the USB device.</span></span><br/>                                          |
| [<span data-ttu-id="c0d2f-129">**Hubid**</span><span class="sxs-lookup"><span data-stu-id="c0d2f-129">**HubID**</span></span>](ivmusbdevice-hubid.md)<br/>                           | <span data-ttu-id="c0d2f-130">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c0d2f-130">Read-only</span></span><br/> | <span data-ttu-id="c0d2f-131">Der Bezeichner des Hubs, mit dem das Gerät verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="c0d2f-131">The identifier of the hub on which the device is connected.</span></span><br/>          |
| [<span data-ttu-id="c0d2f-132">**Manufacturerstring**</span><span class="sxs-lookup"><span data-stu-id="c0d2f-132">**ManufacturerString**</span></span>](ivmusbdevice-manufacturerstring.md)<br/> | <span data-ttu-id="c0d2f-133">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c0d2f-133">Read-only</span></span><br/> | <span data-ttu-id="c0d2f-134">Der Name des Herstellers des USB-Geräts.</span><span class="sxs-lookup"><span data-stu-id="c0d2f-134">The name of the USB device manufacturer.</span></span><br/>                             |
| [<span data-ttu-id="c0d2f-135">**Port**</span><span class="sxs-lookup"><span data-stu-id="c0d2f-135">**Port**</span></span>](ivmusbdevice-port.md)<br/>                             | <span data-ttu-id="c0d2f-136">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c0d2f-136">Read-only</span></span><br/> | <span data-ttu-id="c0d2f-137">Der Bezeichner des Ports, mit dem das Gerät verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="c0d2f-137">The identifier of the port on which the device is connected.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="c0d2f-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0d2f-138">Requirements</span></span>



| <span data-ttu-id="c0d2f-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0d2f-139">Requirement</span></span> | <span data-ttu-id="c0d2f-140">Wert</span><span class="sxs-lookup"><span data-stu-id="c0d2f-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0d2f-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c0d2f-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c0d2f-142">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c0d2f-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c0d2f-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c0d2f-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c0d2f-144">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c0d2f-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c0d2f-145">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c0d2f-145">End of client support</span></span><br/>    | <span data-ttu-id="c0d2f-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0d2f-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c0d2f-147">Produkt</span><span class="sxs-lookup"><span data-stu-id="c0d2f-147">Product</span></span><br/>                  | <span data-ttu-id="c0d2f-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c0d2f-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c0d2f-149">Header</span><span class="sxs-lookup"><span data-stu-id="c0d2f-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0d2f-150"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0d2f-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c0d2f-151">IID</span><span class="sxs-lookup"><span data-stu-id="c0d2f-151">IID</span></span><br/>                      | <span data-ttu-id="c0d2f-152">IID \_ ivmusbdevice ist als 63c1258c-5721-4070-B86B-A6CE2AFEC0B3 definiert.</span><span class="sxs-lookup"><span data-stu-id="c0d2f-152">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



 

