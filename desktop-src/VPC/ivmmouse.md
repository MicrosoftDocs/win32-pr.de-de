---
title: Ivmmouse-Schnittstelle (vpccominterfaces. h)
description: Steuert das Mausgerät innerhalb einer VM.
ms.assetid: 13bbf980-aafd-4c63-b1cb-60f00b738d1f
keywords:
- Ivmmouse Interface Virtual PC
- Virtueller Computer für ivmmouse Interface, beschrieben
topic_type:
- apiref
api_name:
- IVMMouse
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7041b8a28b924ffedc8ff23edd2b04afdaa78be2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859182"
---
# <a name="ivmmouse-interface"></a><span data-ttu-id="694b6-105">Ivmmouse-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="694b6-105">IVMMouse interface</span></span>

<span data-ttu-id="694b6-106">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="694b6-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="694b6-107">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="694b6-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="694b6-108">Steuert das Mausgerät innerhalb eines virtuellen Computers (VM).</span><span class="sxs-lookup"><span data-stu-id="694b6-108">Controls the mouse device within a virtual machine (VM).</span></span> <span data-ttu-id="694b6-109">Das **ivmmouse** für eine virtuelle Maschine kann mithilfe der [**ivmvirtualmachine:: Mouse**](ivmvirtualmachine-mouse.md) -Eigenschaft abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="694b6-109">The **IVMMouse** for a virtual machine can be retrieved using the [**IVMVirtualMachine::Mouse**](ivmvirtualmachine-mouse.md) property.</span></span> <span data-ttu-id="694b6-110">Koordinaten für das Mausgerät können entweder in absoluten Koordinaten oder in Delta Koordinaten dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="694b6-110">Coordinates for the mouse device can be represented either in absolute coordinates or in delta coordinates.</span></span> <span data-ttu-id="694b6-111">Verwenden Sie die [**usingabsolutekoordinaten**](ivmmouse-usingabsolutecoordinates.md) -Eigenschaft, um zwischen den beiden Methoden der Koordinaten Darstellung zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="694b6-111">Use the [**UsingAbsoluteCoordinates**](ivmmouse-usingabsolutecoordinates.md) property to distinguish between the two methods of coordinate representation.</span></span> <span data-ttu-id="694b6-112">Beachten Sie, dass das Abrufen der aktuellen Cursorposition und der Verwendung absoluter Koordinaten nur unterstützt wird, wenn auf dem Gast Betriebssystem die-Integrations Komponenten installiert sind.</span><span class="sxs-lookup"><span data-stu-id="694b6-112">Note that retrieving the current cursor position and the use of absolute coordinates are only supported if the guest operating system has the integration components installed.</span></span>

## <a name="members"></a><span data-ttu-id="694b6-113">Member</span><span class="sxs-lookup"><span data-stu-id="694b6-113">Members</span></span>

<span data-ttu-id="694b6-114">Die **ivmmouse** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="694b6-114">The **IVMMouse** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="694b6-115">**Ivmmouse** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="694b6-115">**IVMMouse** also has these types of members:</span></span>

-   [<span data-ttu-id="694b6-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="694b6-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="694b6-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="694b6-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="694b6-118">Methoden</span><span class="sxs-lookup"><span data-stu-id="694b6-118">Methods</span></span>

<span data-ttu-id="694b6-119">Die **ivmmouse** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="694b6-119">The **IVMMouse** interface has these methods.</span></span>



| <span data-ttu-id="694b6-120">Methode</span><span class="sxs-lookup"><span data-stu-id="694b6-120">Method</span></span>                                  | <span data-ttu-id="694b6-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="694b6-121">Description</span></span>                                                                        |
|:----------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="694b6-122">**Sie**</span><span class="sxs-lookup"><span data-stu-id="694b6-122">**Click**</span></span>](ivmmouse-click.md)         | <span data-ttu-id="694b6-123">Simuliert das Klicken auf die Maustaste.</span><span class="sxs-lookup"><span data-stu-id="694b6-123">Simulates a mouse button click.</span></span><br/>                                         |
| [<span data-ttu-id="694b6-124">**Getbutton**</span><span class="sxs-lookup"><span data-stu-id="694b6-124">**GetButton**</span></span>](ivmmouse-getbutton.md) | <span data-ttu-id="694b6-125">Ruft den aktuellen Zustand (nach oben oder unten) der angegebenen Maustaste ab.</span><span class="sxs-lookup"><span data-stu-id="694b6-125">Retrieves the current state (up or down) of the specified mouse button.</span></span><br/> |
| [<span data-ttu-id="694b6-126">**Setbutton**</span><span class="sxs-lookup"><span data-stu-id="694b6-126">**SetButton**</span></span>](ivmmouse-setbutton.md) | <span data-ttu-id="694b6-127">Legt den aktuellen Zustand (nach oben oder unten) der angegebenen Maustaste fest.</span><span class="sxs-lookup"><span data-stu-id="694b6-127">Sets the current state (up or down) of the specified mouse button.</span></span><br/>      |



 

### <a name="properties"></a><span data-ttu-id="694b6-128">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="694b6-128">Properties</span></span>

<span data-ttu-id="694b6-129">Die **ivmmouse** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="694b6-129">The **IVMMouse** interface has these properties.</span></span>



| <span data-ttu-id="694b6-130">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="694b6-130">Property</span></span>                                                                         | <span data-ttu-id="694b6-131">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="694b6-131">Access type</span></span>           | <span data-ttu-id="694b6-132">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="694b6-132">Description</span></span>                                                                                |
|:---------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="694b6-133">**HorizontalPosition**</span><span class="sxs-lookup"><span data-stu-id="694b6-133">**HorizontalPosition**</span></span>](ivmmouse-horizontalposition.md)<br/>             | <span data-ttu-id="694b6-134">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="694b6-134">Read/write</span></span><br/> | <span data-ttu-id="694b6-135">Die absolute x-Koordinate der Maus.</span><span class="sxs-lookup"><span data-stu-id="694b6-135">The absolute x-coordinate of the mouse.</span></span><br/>                                         |
| [<span data-ttu-id="694b6-136">**Scrollwheelposition**</span><span class="sxs-lookup"><span data-stu-id="694b6-136">**ScrollWheelPosition**</span></span>](ivmmouse-scrollwheelposition.md)<br/>           | <span data-ttu-id="694b6-137">Lesegeschützt</span><span class="sxs-lookup"><span data-stu-id="694b6-137">Write-only</span></span><br/> | <span data-ttu-id="694b6-138">Die z-Koordinate der Maus (nur relativ).</span><span class="sxs-lookup"><span data-stu-id="694b6-138">The z-coordinate of the mouse (relative only).</span></span><br/>                                  |
| [<span data-ttu-id="694b6-139">**Usingabsolutekoordinaten**</span><span class="sxs-lookup"><span data-stu-id="694b6-139">**UsingAbsoluteCoordinates**</span></span>](ivmmouse-usingabsolutecoordinates.md)<br/> | <span data-ttu-id="694b6-140">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="694b6-140">Read/write</span></span><br/> | <span data-ttu-id="694b6-141">Gibt an, ob Maus Koordinaten absolute oder relative Koordinaten darstellen.</span><span class="sxs-lookup"><span data-stu-id="694b6-141">Indicates whether mouse coordinates represent absolute or relative coordinates.</span></span><br/> |
| [<span data-ttu-id="694b6-142">**VerticalPosition**</span><span class="sxs-lookup"><span data-stu-id="694b6-142">**VerticalPosition**</span></span>](ivmmouse-verticalposition.md)<br/>                 | <span data-ttu-id="694b6-143">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="694b6-143">Read/write</span></span><br/> | <span data-ttu-id="694b6-144">Die absolute y-Koordinate der Maus.</span><span class="sxs-lookup"><span data-stu-id="694b6-144">The absolute y-coordinate of the mouse.</span></span><br/>                                         |



 

## <a name="requirements"></a><span data-ttu-id="694b6-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="694b6-145">Requirements</span></span>



| <span data-ttu-id="694b6-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="694b6-146">Requirement</span></span> | <span data-ttu-id="694b6-147">Wert</span><span class="sxs-lookup"><span data-stu-id="694b6-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="694b6-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="694b6-148">Minimum supported client</span></span><br/> | <span data-ttu-id="694b6-149">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="694b6-149">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="694b6-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="694b6-150">Minimum supported server</span></span><br/> | <span data-ttu-id="694b6-151">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="694b6-151">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="694b6-152">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="694b6-152">End of client support</span></span><br/>    | <span data-ttu-id="694b6-153">Windows 7</span><span class="sxs-lookup"><span data-stu-id="694b6-153">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="694b6-154">Produkt</span><span class="sxs-lookup"><span data-stu-id="694b6-154">Product</span></span><br/>                  | <span data-ttu-id="694b6-155">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="694b6-155">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="694b6-156">Header</span><span class="sxs-lookup"><span data-stu-id="694b6-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="694b6-157"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="694b6-157"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="694b6-158">IID</span><span class="sxs-lookup"><span data-stu-id="694b6-158">IID</span></span><br/>                      | <span data-ttu-id="694b6-159">IID \_ ivmmouse ist als ac903f6d-6346-4f29-8875-5d511a13895e definiert.</span><span class="sxs-lookup"><span data-stu-id="694b6-159">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



 

