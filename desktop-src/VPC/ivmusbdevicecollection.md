---
title: Ivmusbdevicecollection-Schnittstelle (vpccominterfaces. h)
description: Definiert die Sammlung von USB-Geräten, die mit dem Host System verbunden sind. Wenn Sie ein ivmusbdebug-Objekt abrufen möchten, verwenden Sie die ivmvirtualpc-Eigenschaft.
ms.assetid: a5cca485-29d3-47fa-9cda-fedcdc379155
keywords:
- Ivmusbdebug-Schnittstelle virtueller PC
- Ivmusbdebug Interface Virtual PC, beschrieben
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e773f006a1d98253a20ad37d5a70db43f487980
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341003"
---
# <a name="ivmusbdevicecollection-interface"></a><span data-ttu-id="eb6cb-106">Ivmusbdebug ecollection-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="eb6cb-106">IVMUSBDeviceCollection interface</span></span>

<span data-ttu-id="eb6cb-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="eb6cb-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="eb6cb-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="eb6cb-109">Definiert die Sammlung von USB-Geräten, die mit dem Host System verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-109">Defines the collection of USB devices attached to the host system.</span></span> <span data-ttu-id="eb6cb-110">Verwenden Sie zum Abrufen eines **ivmusbdebug** -Objekts die [**ivmvirtualpc::**](ivmvirtualpc-usbdevicecollection.md) Start-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-110">To obtain an **IVMUSBDeviceCollection** object, use the [**IVMVirtualPC::USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="eb6cb-111">Member</span><span class="sxs-lookup"><span data-stu-id="eb6cb-111">Members</span></span>

<span data-ttu-id="eb6cb-112">Die **ivmusbdebug** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-112">The **IVMUSBDeviceCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="eb6cb-113">**Ivmusbdebug ecollection** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="eb6cb-113">**IVMUSBDeviceCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="eb6cb-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eb6cb-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eb6cb-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eb6cb-115">Properties</span></span>

<span data-ttu-id="eb6cb-116">Die **ivmusbdecodecollection** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-116">The **IVMUSBDeviceCollection** interface has these properties.</span></span>



| <span data-ttu-id="eb6cb-117">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="eb6cb-117">Property</span></span>                                                        | <span data-ttu-id="eb6cb-118">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="eb6cb-118">Access type</span></span>          | <span data-ttu-id="eb6cb-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eb6cb-119">Description</span></span>                                                                         |
|:----------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="eb6cb-120">**\_"Netwenum"**</span><span class="sxs-lookup"><span data-stu-id="eb6cb-120">**\_NewEnum**</span></span>](ivmusbdevicecollection--newenum.md)<br/> | <span data-ttu-id="eb6cb-121">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6cb-121">Read-only</span></span><br/> | <span data-ttu-id="eb6cb-122">Ein Enumerator für die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-122">An enumerator for the collection.</span></span><br/>                                        |
| [<span data-ttu-id="eb6cb-123">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="eb6cb-123">**Count**</span></span>](ivmusbdevicecollection-count.md)<br/>        | <span data-ttu-id="eb6cb-124">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6cb-124">Read-only</span></span><br/> | <span data-ttu-id="eb6cb-125">Die Anzahl der USB-Geräte in dieser Sammlung.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-125">The number of USB devices in this collection.</span></span><br/>                            |
| [<span data-ttu-id="eb6cb-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="eb6cb-126">**Item**</span></span>](ivmusbdevicecollection-item.md)<br/>          | <span data-ttu-id="eb6cb-127">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6cb-127">Read-only</span></span><br/> | <span data-ttu-id="eb6cb-128">Das USB-Geräte Objekt, das dem angegebenen Index (1-basiert) entspricht.</span><span class="sxs-lookup"><span data-stu-id="eb6cb-128">The USB device object that corresponds to the specified index (1-based).</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="eb6cb-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb6cb-129">Requirements</span></span>



| <span data-ttu-id="eb6cb-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eb6cb-130">Requirement</span></span> | <span data-ttu-id="eb6cb-131">Wert</span><span class="sxs-lookup"><span data-stu-id="eb6cb-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb6cb-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eb6cb-132">Minimum supported client</span></span><br/> | <span data-ttu-id="eb6cb-133">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eb6cb-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="eb6cb-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eb6cb-134">Minimum supported server</span></span><br/> | <span data-ttu-id="eb6cb-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="eb6cb-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="eb6cb-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="eb6cb-136">End of client support</span></span><br/>    | <span data-ttu-id="eb6cb-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="eb6cb-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="eb6cb-138">Produkt</span><span class="sxs-lookup"><span data-stu-id="eb6cb-138">Product</span></span><br/>                  | <span data-ttu-id="eb6cb-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="eb6cb-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="eb6cb-140">Header</span><span class="sxs-lookup"><span data-stu-id="eb6cb-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb6cb-141"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb6cb-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="eb6cb-142">IID</span><span class="sxs-lookup"><span data-stu-id="eb6cb-142">IID</span></span><br/>                      | <span data-ttu-id="eb6cb-143">IID \_ ivmusbdevicecollection ist als 4f-cd6a5--ID definiert. d1c-9s4d-e90abb8b3749</span><span class="sxs-lookup"><span data-stu-id="eb6cb-143">IID\_IVMUSBDeviceCollection is defined as 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="eb6cb-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb6cb-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb6cb-145">**Ivmusbdevice**</span><span class="sxs-lookup"><span data-stu-id="eb6cb-145">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> <dt>

[<span data-ttu-id="eb6cb-146">**Ivmvirtualpc:: Start Message**</span><span class="sxs-lookup"><span data-stu-id="eb6cb-146">**IVMVirtualPC::USBDeviceCollection**</span></span>](ivmvirtualpc-usbdevicecollection.md)
</dt> </dl>

 

