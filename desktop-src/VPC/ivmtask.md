---
title: Ivmtask-Schnittstelle (vpccominterfaces. h)
description: Verwenden Sie die ivmtask-Schnittstelle, um asynchrone Aufgaben für verschiedene com-Methoden zu überwachen und zu steuern.
ms.assetid: 9b593444-80f5-43e9-9b95-1a2150c66efd
keywords:
- Ivmtask Interface Virtual PC
- Virtueller Computer für ivmtask Interface, beschrieben
topic_type:
- apiref
api_name:
- IVMTask
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e1d519471fe5b1fc32cb6365d1139243c85538
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518383"
---
# <a name="ivmtask-interface"></a><span data-ttu-id="14419-105">Ivmtask-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="14419-105">IVMTask interface</span></span>

<span data-ttu-id="14419-106">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="14419-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="14419-107">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="14419-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="14419-108">Verwenden Sie die **ivmtask** -Schnittstelle, um asynchrone Aufgaben für verschiedene com-Methoden zu überwachen und zu steuern.</span><span class="sxs-lookup"><span data-stu-id="14419-108">Use the **IVMTask** interface to monitor and control asynchronous tasks for various COM methods.</span></span>

## <a name="members"></a><span data-ttu-id="14419-109">Member</span><span class="sxs-lookup"><span data-stu-id="14419-109">Members</span></span>

<span data-ttu-id="14419-110">Die **ivmtask** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="14419-110">The **IVMTask** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="14419-111">**Ivmtask** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="14419-111">**IVMTask** also has these types of members:</span></span>

-   [<span data-ttu-id="14419-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="14419-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="14419-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="14419-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="14419-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="14419-114">Methods</span></span>

<span data-ttu-id="14419-115">Die **ivmtask** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="14419-115">The **IVMTask** interface has these methods.</span></span>



| <span data-ttu-id="14419-116">Methode</span><span class="sxs-lookup"><span data-stu-id="14419-116">Method</span></span>                                                 | <span data-ttu-id="14419-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="14419-117">Description</span></span>                                                                                 |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="14419-118">**Abbrechen**</span><span class="sxs-lookup"><span data-stu-id="14419-118">**Cancel**</span></span>](ivmtask-cancel.md)                       | <span data-ttu-id="14419-119">Bricht die Aufgabe ab.</span><span class="sxs-lookup"><span data-stu-id="14419-119">Cancels the task.</span></span><br/>                                                                |
| [<span data-ttu-id="14419-120">**Waitforcompletion**</span><span class="sxs-lookup"><span data-stu-id="14419-120">**WaitForCompletion**</span></span>](ivmtask-waitforcompletion.md) | <span data-ttu-id="14419-121">Wartet, bis die Aufgabe beendet oder das angegebene Timeout Intervall abläuft.</span><span class="sxs-lookup"><span data-stu-id="14419-121">Waits for the task to complete or for the specified time-out interval to elapse.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="14419-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="14419-122">Properties</span></span>

<span data-ttu-id="14419-123">Die **ivmtask** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="14419-123">The **IVMTask** interface has these properties.</span></span>



| <span data-ttu-id="14419-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="14419-124">Property</span></span>                                                        | <span data-ttu-id="14419-125">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="14419-125">Access type</span></span>          | <span data-ttu-id="14419-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="14419-126">Description</span></span>                                                        |
|:----------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="14419-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="14419-127">**Description**</span></span>](ivmtask-description.md)<br/>           | <span data-ttu-id="14419-128">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="14419-128">Read-only</span></span><br/> | <span data-ttu-id="14419-129">Eine Beschreibung des Tasks.</span><span class="sxs-lookup"><span data-stu-id="14419-129">A description of the task.</span></span><br/>                              |
| [<span data-ttu-id="14419-130">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="14419-130">**Error**</span></span>](ivmtask-error.md)<br/>                       | <span data-ttu-id="14419-131">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="14419-131">Read-only</span></span><br/> | <span data-ttu-id="14419-132">Der für diese Aufgabe aufgezeichnete Fehler.</span><span class="sxs-lookup"><span data-stu-id="14419-132">The error recorded for this task.</span></span><br/>                       |
| [<span data-ttu-id="14419-133">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="14419-133">**ErrorDescription**</span></span>](ivmtask-errordescription.md)<br/> | <span data-ttu-id="14419-134">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="14419-134">Read-only</span></span><br/> | <span data-ttu-id="14419-135">Die lokalisierte Fehlerbeschreibung, die für diese Aufgabe aufgezeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="14419-135">The localized error description recorded for this task.</span></span><br/> |
| [<span data-ttu-id="14419-136">**id**</span><span class="sxs-lookup"><span data-stu-id="14419-136">**ID**</span></span>](ivmtask-id.md)<br/>                             | <span data-ttu-id="14419-137">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="14419-137">Read-only</span></span><br/> | <span data-ttu-id="14419-138">Ein eindeutiger Bezeichner für diese Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="14419-138">A unique identifier for this task.</span></span><br/>                      |
| [<span data-ttu-id="14419-139">**IsCancelable**</span><span class="sxs-lookup"><span data-stu-id="14419-139">**IsCancelable**</span></span>](ivmtask-iscancelable.md)<br/>         | <span data-ttu-id="14419-140">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="14419-140">Read-only</span></span><br/> | <span data-ttu-id="14419-141">Gibt an, ob der Task abgebrochen werden kann.</span><span class="sxs-lookup"><span data-stu-id="14419-141">Indicates whether the task can be canceled.</span></span><br/>             |
| [<span data-ttu-id="14419-142">**IsComplete**</span><span class="sxs-lookup"><span data-stu-id="14419-142">**IsComplete**</span></span>](ivmtask-iscomplete.md)<br/>             | <span data-ttu-id="14419-143">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="14419-143">Read-only</span></span><br/> | <span data-ttu-id="14419-144">Gibt an, ob die Aufgabe abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="14419-144">Indicates whether the task has completed.</span></span><br/>               |
| [<span data-ttu-id="14419-145">**Prozentuabgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="14419-145">**PercentCompleted**</span></span>](ivmtask-percentcompleted.md)<br/> | <span data-ttu-id="14419-146">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="14419-146">Read-only</span></span><br/> | <span data-ttu-id="14419-147">Der Abschluss Prozentsatz der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="14419-147">The completion percentage of the task.</span></span><br/>                  |
| [<span data-ttu-id="14419-148">**Dadurch**</span><span class="sxs-lookup"><span data-stu-id="14419-148">**Result**</span></span>](ivmtask-result.md)<br/>                     | <span data-ttu-id="14419-149">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="14419-149">Read-only</span></span><br/> | <span data-ttu-id="14419-150">Das Ergebnis der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="14419-150">The result of the task.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="14419-151">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14419-151">Remarks</span></span>

<span data-ttu-id="14419-152">Ein **ivmtask** -Objekt wird von Methoden zurückgegeben, für die möglicherweise eine beträchtliche Zeitspanne benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="14419-152">An **IVMTask** object is returned by methods that could potentially require a significant amount of time to complete.</span></span> <span data-ttu-id="14419-153">Dies ermöglicht es der Anwendung, den Fortschritt des gewünschten Vorgangs zu überwachen, ohne Sie zu erzwingen, dass eine weitere Ausführung blockiert wird, während auf den Abschluss des Vorgangs gewartet wird.</span><span class="sxs-lookup"><span data-stu-id="14419-153">This allows the application to monitor the progress of the desired operation without forcing it to block further execution while waiting for the completion of the operation.</span></span>

<span data-ttu-id="14419-154">Die folgenden Methoden geben ein **ivmtask** -Objekt zurück, das verwendet werden kann, um den Fortschritt zu verfolgen:</span><span class="sxs-lookup"><span data-stu-id="14419-154">The following methods return an **IVMTask** object that can be used to track progress:</span></span>

-   [<span data-ttu-id="14419-155">**Ivmguestos:: abmelden**</span><span class="sxs-lookup"><span data-stu-id="14419-155">**IVMGuestOS::Logoff**</span></span>](ivmguestos-logoff.md)
-   [<span data-ttu-id="14419-156">**Ivmguestos:: Restart**</span><span class="sxs-lookup"><span data-stu-id="14419-156">**IVMGuestOS::Restart**</span></span>](ivmguestos-restart.md)
-   [<span data-ttu-id="14419-157">**Ivmguestos:: Shutdown**</span><span class="sxs-lookup"><span data-stu-id="14419-157">**IVMGuestOS::Shutdown**</span></span>](ivmguestos-shutdown.md)
-   [<span data-ttu-id="14419-158">**Ivmharddisk:: Compact**</span><span class="sxs-lookup"><span data-stu-id="14419-158">**IVMHardDisk::Compact**</span></span>](ivmharddisk-compact.md)
-   [<span data-ttu-id="14419-159">**Ivmharddisk:: Convert**</span><span class="sxs-lookup"><span data-stu-id="14419-159">**IVMHardDisk::Convert**</span></span>](ivmharddisk-convert.md)
-   [<span data-ttu-id="14419-160">**Ivmharddisk:: Merge**</span><span class="sxs-lookup"><span data-stu-id="14419-160">**IVMHardDisk::Merge**</span></span>](ivmharddisk-merge.md)
-   [<span data-ttu-id="14419-161">**Ivmharddisk:: mergeto**</span><span class="sxs-lookup"><span data-stu-id="14419-161">**IVMHardDisk::MergeTo**</span></span>](ivmharddisk-mergeto.md)
-   [<span data-ttu-id="14419-162">**Ivmvirtualmachine:: mergeundodisks**</span><span class="sxs-lookup"><span data-stu-id="14419-162">**IVMVirtualMachine::MergeUndoDisks**</span></span>](ivmvirtualmachine-mergeundodisks.md)
-   [<span data-ttu-id="14419-163">**Ivmvirtualmachine:: Reset**</span><span class="sxs-lookup"><span data-stu-id="14419-163">**IVMVirtualMachine::Reset**</span></span>](ivmvirtualmachine-reset.md)
-   [<span data-ttu-id="14419-164">**Ivmvirtualmachine:: Save**</span><span class="sxs-lookup"><span data-stu-id="14419-164">**IVMVirtualMachine::Save**</span></span>](ivmvirtualmachine-save.md)
-   [<span data-ttu-id="14419-165">**Ivmvirtualmachine:: Startup**</span><span class="sxs-lookup"><span data-stu-id="14419-165">**IVMVirtualMachine::Startup**</span></span>](ivmvirtualmachine-startup.md)
-   [<span data-ttu-id="14419-166">**Ivmvirtualmachine:: Startup2**</span><span class="sxs-lookup"><span data-stu-id="14419-166">**IVMVirtualMachine::Startup2**</span></span>](ivmvirtualmachine-startup2.md)
-   [<span data-ttu-id="14419-167">**Ivmvirtualmachine:: Turnoff**</span><span class="sxs-lookup"><span data-stu-id="14419-167">**IVMVirtualMachine::TurnOff**</span></span>](ivmvirtualmachine-turnoff.md)
-   [<span data-ttu-id="14419-168">**Ivmvirtualpc:: kreatedifferencingvirtualharddisk**</span><span class="sxs-lookup"><span data-stu-id="14419-168">**IVMVirtualPC::CreateDifferencingVirtualHardDisk**</span></span>](ivmvirtualpc-createdifferencingvirtualharddisk.md)
-   [<span data-ttu-id="14419-169">**Ivmvirtualpc:: kreatedynamicvirtualharddisk**</span><span class="sxs-lookup"><span data-stu-id="14419-169">**IVMVirtualPC::CreateDynamicVirtualHardDisk**</span></span>](ivmvirtualpc-createdynamicvirtualharddisk.md)
-   [<span data-ttu-id="14419-170">**Ivmvirtualpc:: kreatefixedvirtualharddisk**</span><span class="sxs-lookup"><span data-stu-id="14419-170">**IVMVirtualPC::CreateFixedVirtualHardDisk**</span></span>](ivmvirtualpc-createfixedvirtualharddisk.md)

## <a name="requirements"></a><span data-ttu-id="14419-171">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14419-171">Requirements</span></span>



| <span data-ttu-id="14419-172">Anforderung</span><span class="sxs-lookup"><span data-stu-id="14419-172">Requirement</span></span> | <span data-ttu-id="14419-173">Wert</span><span class="sxs-lookup"><span data-stu-id="14419-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="14419-174">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="14419-174">Minimum supported client</span></span><br/> | <span data-ttu-id="14419-175">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="14419-175">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="14419-176">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="14419-176">Minimum supported server</span></span><br/> | <span data-ttu-id="14419-177">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="14419-177">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="14419-178">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="14419-178">End of client support</span></span><br/>    | <span data-ttu-id="14419-179">Windows 7</span><span class="sxs-lookup"><span data-stu-id="14419-179">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="14419-180">Produkt</span><span class="sxs-lookup"><span data-stu-id="14419-180">Product</span></span><br/>                  | <span data-ttu-id="14419-181">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="14419-181">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="14419-182">Header</span><span class="sxs-lookup"><span data-stu-id="14419-182">Header</span></span><br/>                   | <dl> <span data-ttu-id="14419-183"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="14419-183"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="14419-184">IID</span><span class="sxs-lookup"><span data-stu-id="14419-184">IID</span></span><br/>                      | <span data-ttu-id="14419-185">IID \_ ivmtask ist als ab72b222-6e9c-48ae-AA54-85e3e635767c definiert.</span><span class="sxs-lookup"><span data-stu-id="14419-185">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



 

