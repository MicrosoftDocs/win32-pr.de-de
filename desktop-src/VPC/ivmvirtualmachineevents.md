---
title: Ivmvirtualmachineevents-Schnittstelle (vpccominterfaces. h)
description: Definiert die ausgehende Ereignis Schnittstelle für die ivmvirtualmachine-Schnittstelle.
ms.assetid: 52901a95-0f4f-4503-97c5-1459179feeb8
keywords:
- Ivmvirtualmachineevents Interface Virtual PC
- Ivmvirtualmachineevents Interface Virtual PC, beschrieben
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fddcc2ded96f5a39a520d3b5a712e63fbb0a65d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478669"
---
# <a name="ivmvirtualmachineevents-interface"></a><span data-ttu-id="5a670-105">Ivmvirtualmachineevents-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5a670-105">IVMVirtualMachineEvents interface</span></span>

<span data-ttu-id="5a670-106">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5a670-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5a670-107">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5a670-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5a670-108">Definiert die ausgehende Ereignis Schnittstelle für die [**ivmvirtualmachine**](ivmvirtualmachine.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5a670-108">Defines the outgoing event interface for the [**IVMVirtualMachine**](ivmvirtualmachine.md) interface.</span></span> <span data-ttu-id="5a670-109">Der Client implementiert diese Methoden, um von [**ivmvirtualmachine**](ivmvirtualmachine.md)gesendete Ereignisse zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="5a670-109">The client implements these methods to receive events sent from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="members"></a><span data-ttu-id="5a670-110">Member</span><span class="sxs-lookup"><span data-stu-id="5a670-110">Members</span></span>

<span data-ttu-id="5a670-111">Die **ivmvirtualmachineevents** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5a670-111">The **IVMVirtualMachineEvents** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="5a670-112">**Ivmvirtualmachineevents** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5a670-112">**IVMVirtualMachineEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="5a670-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="5a670-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5a670-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="5a670-114">Methods</span></span>

<span data-ttu-id="5a670-115">Die **ivmvirtualmachineevents** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="5a670-115">The **IVMVirtualMachineEvents** interface has these methods.</span></span>



| <span data-ttu-id="5a670-116">Methode</span><span class="sxs-lookup"><span data-stu-id="5a670-116">Method</span></span>                                                                                   | <span data-ttu-id="5a670-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5a670-117">Description</span></span>                                                                                                                                     |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5a670-118">**Onadditionsavailable**</span><span class="sxs-lookup"><span data-stu-id="5a670-118">**OnAdditionsAvailable**</span></span>](ivmvirtualmachineevents-onadditionsavailable.md)             | <span data-ttu-id="5a670-119">Empfängt eine Benachrichtigung, dass Integrations Komponenten auf einem virtuellen Computer verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="5a670-119">Receives notification that integration components are available in a virtual machine.</span></span><br/>                                                |
| [<span data-ttu-id="5a670-120">**Onadditionsuninstalliert**</span><span class="sxs-lookup"><span data-stu-id="5a670-120">**OnAdditionsUninstalled**</span></span>](ivmvirtualmachineevents-onadditionsuninstalled.md)         | <span data-ttu-id="5a670-121">Empfängt eine Benachrichtigung, dass Integrations Komponenten auf einem virtuellen Computer deinstalliert werden.</span><span class="sxs-lookup"><span data-stu-id="5a670-121">Receives notification that integration components are uninstalled in a virtual machine.</span></span><br/>                                              |
| [<span data-ttu-id="5a670-122">**Onconfigurationchanged**</span><span class="sxs-lookup"><span data-stu-id="5a670-122">**OnConfigurationChanged**</span></span>](ivmvirtualmachineevents-onconfigurationchanged.md)         | <span data-ttu-id="5a670-123">Empfängt eine Benachrichtigung, dass sich ein Wert in der Konfiguration für diesen virtuellen Computer geändert hat.</span><span class="sxs-lookup"><span data-stu-id="5a670-123">Receives notification that a value in the configuration for this virtual machine has changed.</span></span><br/>                                        |
| [<span data-ttu-id="5a670-124">**Ondiskouesleerraum**</span><span class="sxs-lookup"><span data-stu-id="5a670-124">**OnDiskOutOfSpace**</span></span>](ivmvirtualmachineevents-ondiskoutofspace.md)                     | <span data-ttu-id="5a670-125">Empfängt eine Benachrichtigung, dass ein für eine virtuelle Maschine erforderlicher Datenträger nicht über genügend Speicherplatz verfügt und die virtuelle Maschine nicht ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5a670-125">Receives notification that a disk required for a virtual machine is out of space and the virtual machine is unable to run.</span></span><br/>           |
| [<span data-ttu-id="5a670-126">**Onenhancedvideomode Changed**</span><span class="sxs-lookup"><span data-stu-id="5a670-126">**OnEnhancedVideoModeChanged**</span></span>](ivmvirtualmachineevents-onenhancedvideomodechanged.md) | <span data-ttu-id="5a670-127">Empfängt eine Benachrichtigung, dass die Unterstützung einer virtuellen Maschine für den erweiterten Videomodus geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="5a670-127">Receives notification that a virtual machine's support for enhanced video mode has changed.</span></span><br/>                                          |
| [<span data-ttu-id="5a670-128">**Onguestlogoff**</span><span class="sxs-lookup"><span data-stu-id="5a670-128">**OnGuestLogoff**</span></span>](ivmvirtualmachineevents-onguestlogoff.md)                           | <span data-ttu-id="5a670-129">Empfängt eine Benachrichtigung, dass sich ein Benutzer vom Gast Betriebssystem abgemeldet hat.</span><span class="sxs-lookup"><span data-stu-id="5a670-129">Receives notification that a user has logged off from the guest operating system.</span></span><br/>                                                    |
| [<span data-ttu-id="5a670-130">**Onguestshutdown**</span><span class="sxs-lookup"><span data-stu-id="5a670-130">**OnGuestShutdown**</span></span>](ivmvirtualmachineevents-onguestshutdown.md)                       | <span data-ttu-id="5a670-131">Empfängt eine Benachrichtigung, dass das Gast Betriebssystem heruntergefahren wurde.</span><span class="sxs-lookup"><span data-stu-id="5a670-131">Receives notification that guest operating system has shut down.</span></span><br/>                                                                     |
| [<span data-ttu-id="5a670-132">**Onheartbeatbeendet**</span><span class="sxs-lookup"><span data-stu-id="5a670-132">**OnHeartbeatStopped**</span></span>](ivmvirtualmachineevents-onheartbeatstopped.md)                 | <span data-ttu-id="5a670-133">Empfängt eine Benachrichtigung, dass der Takt einer virtuellen Maschine beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="5a670-133">Receives notification that a virtual machine's heartbeat has stopped.</span></span> <span data-ttu-id="5a670-134">Dies weist normalerweise darauf hin, dass das Gast Betriebssystem abgestürzt ist.</span><span class="sxs-lookup"><span data-stu-id="5a670-134">This usually indicates the guest operating system has crashed.</span></span><br/> |
| [<span data-ttu-id="5a670-135">**Onrequestshutdown**</span><span class="sxs-lookup"><span data-stu-id="5a670-135">**OnRequestShutdown**</span></span>](ivmvirtualmachineevents-onrequestshutdown.md)                   | <span data-ttu-id="5a670-136">Empfängt eine Benachrichtigung, dass eine Anforderung zum Herunterfahren durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="5a670-136">Receives notification that a shutdown request has been made.</span></span><br/>                                                                         |
| [<span data-ttu-id="5a670-137">**OnReset**</span><span class="sxs-lookup"><span data-stu-id="5a670-137">**OnReset**</span></span>](ivmvirtualmachineevents-onreset.md)                                       | <span data-ttu-id="5a670-138">Empfängt eine Benachrichtigung, dass ein virtueller Computer zurückgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="5a670-138">Receives notification that a virtual machine has been reset.</span></span><br/>                                                                         |
| [<span data-ttu-id="5a670-139">**OnStateChange**</span><span class="sxs-lookup"><span data-stu-id="5a670-139">**OnStateChange**</span></span>](ivmvirtualmachineevents-onstatechange.md)                           | <span data-ttu-id="5a670-140">Empfängt eine Benachrichtigung, dass sich der Zustand einer virtuellen Maschine geändert hat.</span><span class="sxs-lookup"><span data-stu-id="5a670-140">Receives notification that a virtual machine's state has changed.</span></span><br/>                                                                    |
| [<span data-ttu-id="5a670-141">**Ontrplefault**</span><span class="sxs-lookup"><span data-stu-id="5a670-141">**OnTripleFault**</span></span>](ivmvirtualmachineevents-ontriplefault.md)                           | <span data-ttu-id="5a670-142">Empfängt eine Benachrichtigung, dass ein virtueller Computer einen dreifachen Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="5a670-142">Receives notification that a virtual machine has triple-faulted.</span></span><br/>                                                                     |



 

## <a name="requirements"></a><span data-ttu-id="5a670-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a670-143">Requirements</span></span>



| <span data-ttu-id="5a670-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5a670-144">Requirement</span></span> | <span data-ttu-id="5a670-145">Wert</span><span class="sxs-lookup"><span data-stu-id="5a670-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a670-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5a670-146">Minimum supported client</span></span><br/> | <span data-ttu-id="5a670-147">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5a670-147">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5a670-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5a670-148">Minimum supported server</span></span><br/> | <span data-ttu-id="5a670-149">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5a670-149">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5a670-150">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="5a670-150">End of client support</span></span><br/>    | <span data-ttu-id="5a670-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5a670-151">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5a670-152">Produkt</span><span class="sxs-lookup"><span data-stu-id="5a670-152">Product</span></span><br/>                  | <span data-ttu-id="5a670-153">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5a670-153">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5a670-154">Header</span><span class="sxs-lookup"><span data-stu-id="5a670-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a670-155"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a670-155"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5a670-156">IID</span><span class="sxs-lookup"><span data-stu-id="5a670-156">IID</span></span><br/>                      | <span data-ttu-id="5a670-157">Diid \_ ivmvirtualmachineevents ist als 9d84f560-bb67-4961-BD12-a4da780c67e4 definiert.</span><span class="sxs-lookup"><span data-stu-id="5a670-157">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



 

