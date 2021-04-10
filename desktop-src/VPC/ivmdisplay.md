---
title: Ivmdisplay-Schnittstelle (vpccominterfaces. h)
description: Steuert die Anzeigeeinstellungen eines virtuellen Computers. Die ivmdisplay-Schnittstelle für eine virtuelle Maschine kann mithilfe der Anzeige Eigenschaft ivmvirtualmachine abgerufen werden.
ms.assetid: b2eafd86-459c-4807-aa77-8b9125bce53e
keywords:
- Ivmdisplay Interface Virtual PC
- Virtueller Computer für ivmdisplay Interface, beschrieben
topic_type:
- apiref
api_name:
- IVMDisplay
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0f410e49682d2fa9f5f8511d96e3b9ce9a1094
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956847"
---
# <a name="ivmdisplay-interface"></a><span data-ttu-id="9aee6-106">Ivmdisplay-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9aee6-106">IVMDisplay interface</span></span>

<span data-ttu-id="9aee6-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9aee6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9aee6-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="9aee6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9aee6-109">Steuert die Anzeigeeinstellungen eines virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="9aee6-109">Controls the display settings of a virtual machine.</span></span> <span data-ttu-id="9aee6-110">Die **ivmdisplay** -Schnittstelle für eine virtuelle Maschine kann mithilfe der [**ivmvirtualmachine::D isplay**](ivmvirtualmachine-display.md) -Eigenschaft abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="9aee6-110">The **IVMDisplay** interface for a virtual machine can be retrieved using the [**IVMVirtualMachine::Display**](ivmvirtualmachine-display.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="9aee6-111">Member</span><span class="sxs-lookup"><span data-stu-id="9aee6-111">Members</span></span>

<span data-ttu-id="9aee6-112">Die **ivmdisplay** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9aee6-112">The **IVMDisplay** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="9aee6-113">**Ivmdisplay** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9aee6-113">**IVMDisplay** also has these types of members:</span></span>

-   [<span data-ttu-id="9aee6-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="9aee6-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="9aee6-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9aee6-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9aee6-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="9aee6-116">Methods</span></span>

<span data-ttu-id="9aee6-117">Die **ivmdisplay** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="9aee6-117">The **IVMDisplay** interface has these methods.</span></span>



| <span data-ttu-id="9aee6-118">Methode</span><span class="sxs-lookup"><span data-stu-id="9aee6-118">Method</span></span>                                                       | <span data-ttu-id="9aee6-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9aee6-119">Description</span></span>                                                                                             |
|:-------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9aee6-120">**\_GenerateThumbnail**</span><span class="sxs-lookup"><span data-stu-id="9aee6-120">**\_GenerateThumbnail**</span></span>](ivmdisplay--generatethumbnail.md) | <span data-ttu-id="9aee6-121">Ruft ein Array von Pixeln ab, das ein Miniaturbild des Bildschirms der virtuellen Maschine darstellt.</span><span class="sxs-lookup"><span data-stu-id="9aee6-121">Retrieves an array of pixels representing a thumbnail image of the virtual machine's screen.</span></span><br/> |
| [<span data-ttu-id="9aee6-122">**Setdimensions**</span><span class="sxs-lookup"><span data-stu-id="9aee6-122">**SetDimensions**</span></span>](ivmdisplay-setdimensions.md)            | <span data-ttu-id="9aee6-123">Legt die Höhe und Breite der Anzeige des virtuellen Computers in Pixel fest.</span><span class="sxs-lookup"><span data-stu-id="9aee6-123">Sets the height and width of the virtual machine's display, in pixels.</span></span><br/>                       |



 

### <a name="properties"></a><span data-ttu-id="9aee6-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9aee6-124">Properties</span></span>

<span data-ttu-id="9aee6-125">Die **ivmdisplay** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9aee6-125">The **IVMDisplay** interface has these properties.</span></span>



| <span data-ttu-id="9aee6-126">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9aee6-126">Property</span></span>                                             | <span data-ttu-id="9aee6-127">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="9aee6-127">Access type</span></span>          | <span data-ttu-id="9aee6-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9aee6-128">Description</span></span>                                                                                   |
|:-----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9aee6-129">**CanResize**</span><span class="sxs-lookup"><span data-stu-id="9aee6-129">**CanResize**</span></span>](ivmdisplay-canresize.md)<br/> | <span data-ttu-id="9aee6-130">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9aee6-130">Read-only</span></span><br/> | <span data-ttu-id="9aee6-131">Gibt an, ob der Gast Auflösungs Änderungen zulässt.</span><span class="sxs-lookup"><span data-stu-id="9aee6-131">Indicates whether the Guest allows resolution changes.</span></span><br/>                             |
| [<span data-ttu-id="9aee6-132">**Höhe**</span><span class="sxs-lookup"><span data-stu-id="9aee6-132">**Height**</span></span>](ivmdisplay-height.md)<br/>       | <span data-ttu-id="9aee6-133">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9aee6-133">Read-only</span></span><br/> | <span data-ttu-id="9aee6-134">Die Höhe der Anzeige des virtuellen Computers in Pixel.</span><span class="sxs-lookup"><span data-stu-id="9aee6-134">The height of the virtual machine's display, in pixels.</span></span><br/>                            |
| [<span data-ttu-id="9aee6-135">**Miniaturansicht**</span><span class="sxs-lookup"><span data-stu-id="9aee6-135">**Thumbnail**</span></span>](ivmdisplay-thumbnail.md)<br/> | <span data-ttu-id="9aee6-136">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9aee6-136">Read-only</span></span><br/> | <span data-ttu-id="9aee6-137">Ein Array von Pixeln, das ein Miniaturbild des Bildschirms der virtuellen Maschine darstellt.</span><span class="sxs-lookup"><span data-stu-id="9aee6-137">An array of pixels representing a thumbnail image of the virtual machine's screen.</span></span><br/> |
| [<span data-ttu-id="9aee6-138">**Videomode**</span><span class="sxs-lookup"><span data-stu-id="9aee6-138">**VideoMode**</span></span>](ivmdisplay-videomode.md)<br/> | <span data-ttu-id="9aee6-139">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9aee6-139">Read-only</span></span><br/> | <span data-ttu-id="9aee6-140">Der aktuelle Videomodus (Text, VGA, SVGA usw.).</span><span class="sxs-lookup"><span data-stu-id="9aee6-140">The current video mode (Text, VGA, SVGA, and so on).</span></span><br/>                               |
| [<span data-ttu-id="9aee6-141">**Breite**</span><span class="sxs-lookup"><span data-stu-id="9aee6-141">**Width**</span></span>](ivmdisplay-width.md)<br/>         | <span data-ttu-id="9aee6-142">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9aee6-142">Read-only</span></span><br/> | <span data-ttu-id="9aee6-143">Die Breite der Anzeige des virtuellen Computers in Pixel.</span><span class="sxs-lookup"><span data-stu-id="9aee6-143">The width of the virtual machine's display, in pixels.</span></span><br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="9aee6-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9aee6-144">Requirements</span></span>



| <span data-ttu-id="9aee6-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9aee6-145">Requirement</span></span> | <span data-ttu-id="9aee6-146">Wert</span><span class="sxs-lookup"><span data-stu-id="9aee6-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9aee6-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9aee6-147">Minimum supported client</span></span><br/> | <span data-ttu-id="9aee6-148">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9aee6-148">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9aee6-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9aee6-149">Minimum supported server</span></span><br/> | <span data-ttu-id="9aee6-150">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9aee6-150">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9aee6-151">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="9aee6-151">End of client support</span></span><br/>    | <span data-ttu-id="9aee6-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9aee6-152">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9aee6-153">Produkt</span><span class="sxs-lookup"><span data-stu-id="9aee6-153">Product</span></span><br/>                  | <span data-ttu-id="9aee6-154">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9aee6-154">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9aee6-155">Header</span><span class="sxs-lookup"><span data-stu-id="9aee6-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="9aee6-156"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="9aee6-156"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="9aee6-157">IID</span><span class="sxs-lookup"><span data-stu-id="9aee6-157">IID</span></span><br/>                      | <span data-ttu-id="9aee6-158">IID \_ ivmdisplay ist als 960895e9-f 743-4498-96aa-261f 867e7fc5 definiert.</span><span class="sxs-lookup"><span data-stu-id="9aee6-158">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



 

