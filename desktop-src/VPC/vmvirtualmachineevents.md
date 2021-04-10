---
title: Vmvirtualmachineevents-Enumeration (vpccominterfaces. h)
description: Gibt die VM-Ereignisse an.
ms.assetid: 158bdada-6fd3-488c-9ff1-e04df9a79127
keywords:
- Vmvirtualmachineevents-Enumeration virtueller PC
topic_type:
- apiref
api_name:
- VMVirtualMachineEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de1e1d8f4d89c28f63886444537fb9d894fc42e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040906"
---
# <a name="vmvirtualmachineevents-enumeration"></a><span data-ttu-id="7a1e0-104">Vmvirtualmachineevents-Enumeration</span><span class="sxs-lookup"><span data-stu-id="7a1e0-104">VMVirtualMachineEvents enumeration</span></span>

<span data-ttu-id="7a1e0-105">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7a1e0-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7a1e0-106">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7a1e0-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7a1e0-107">Gibt die Ereignisse des virtuellen Computers (Virtual Machine, VM) an.</span><span class="sxs-lookup"><span data-stu-id="7a1e0-107">Specifies the virtual machine (VM) events.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a1e0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a1e0-108">Syntax</span></span>


```C++
typedef enum  { 
  vmVirtualMachineEvent_StateChanged              = 1,
  vmVirtualMachineEvent_RequestShutdown           = 2,
  vmVirtualMachineEvent_Reset                     = 3,
  vmVirtualMachineEvent_TripleFault               = 4,
  vmVirtualMachineEvent_HeartbeatStopped          = 5,
  vmVirtualMachineEvent_ConfigurationChanged      = 6,
  vmVirtualMachineEvent_EnhancedVideoModeChanged  = 7,
  vmVirtualMachineEvent_AdditionsUninstalled      = 8,
  vmVirtualMachineEvent_AdditionsAvailable        = 9,
  vmVirtualMachineEvent_GuestShutdown             = 10,
  vmVirtualMachineEvent_GuestLogoff               = 11,
  vmVirtualMachineEvent_DiskOutOfSpace            = 12
} VMVirtualMachineEvents;
```



## <a name="constants"></a><span data-ttu-id="7a1e0-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="7a1e0-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7a1e0-110"><span id="vmVirtualMachineEvent_StateChanged"></span><span id="vmvirtualmachineevent_statechanged"></span><span id="VMVIRTUALMACHINEEVENT_STATECHANGED"></span>**vmvirtualmachineevent \_ StateChanged**</span><span class="sxs-lookup"><span data-stu-id="7a1e0-110"><span id="vmVirtualMachineEvent_StateChanged"></span><span id="vmvirtualmachineevent_statechanged"></span><span id="VMVIRTUALMACHINEEVENT_STATECHANGED"></span>**vmVirtualMachineEvent\_StateChanged**</span></span>
</dt> <dd>

<span data-ttu-id="7a1e0-111">Der Status eines virtuellen Computers wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="7a1e0-111">A VM's state has changed.</span></span>

</dd> <dt>

<span data-ttu-id="7a1e0-112"><span id="vmVirtualMachineEvent_RequestShutdown"></span><span id="vmvirtualmachineevent_requestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_REQUESTSHUTDOWN"></span>**vmvirtualmachineevent \_ requestshutdown**</span><span class="sxs-lookup"><span data-stu-id="7a1e0-112"><span id="vmVirtualMachineEvent_RequestShutdown"></span><span id="vmvirtualmachineevent_requestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_REQUESTSHUTDOWN"></span>**vmVirtualMachineEvent\_RequestShutdown**</span></span>
</dt> <dd>

<span data-ttu-id="7a1e0-113">Ein Herunterfahren wurde angefordert.</span><span class="sxs-lookup"><span data-stu-id="7a1e0-113">A shutdown has been requested.</span></span>

</dd> <dt>

<span data-ttu-id="7a1e0-114"><span id="vmVirtualMachineEvent_Reset"></span><span id="vmvirtualmachineevent_reset"></span><span id="VMVIRTUALMACHINEEVENT_RESET"></span>**vmvirtualmachineevent \_ Reset**</span><span class="sxs-lookup"><span data-stu-id="7a1e0-114"><span id="vmVirtualMachineEvent_Reset"></span><span id="vmvirtualmachineevent_reset"></span><span id="VMVIRTUALMACHINEEVENT_RESET"></span>**vmVirtualMachineEvent\_Reset**</span></span>
</dt> <dd>

<span data-ttu-id="7a1e0-115">Ein virtueller Computer wurde zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="7a1e0-115">A VM has been reset.</span></span>

</dd> <dt>

<span data-ttu-id="7a1e0-116"><span id="vmVirtualMachineEvent_TripleFault"></span><span id="vmvirtualmachineevent_triplefault"></span><span id="VMVIRTUALMACHINEEVENT_TRIPLEFAULT"></span>**vmvirtualmachineevent-Auswert \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="7a1e0-116"><span id="vmVirtualMachineEvent_TripleFault"></span><span id="vmvirtualmachineevent_triplefault"></span><span id="VMVIRTUALMACHINEEVENT_TRIPLEFAULT"></span>**vmVirtualMachineEvent\_TripleFault**</span></span>
</dt> <dd>

<span data-ttu-id="7a1e0-117">Ein virtueller Computer hat einen dreifachen Fehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="7a1e0-117">A VM has triple-faulted.</span></span>

</dd> <dt>

<span data-ttu-id="7a1e0-118"><span id="vmVirtualMachineEvent_HeartbeatStopped"></span><span id="vmvirtualmachineevent_heartbeatstopped"></span><span id="VMVIRTUALMACHINEEVENT_HEARTBEATSTOPPED"></span>**tabeatbeendete vmvirtualmachineevent \_**</span><span class="sxs-lookup"><span data-stu-id="7a1e0-118"><span id="vmVirtualMachineEvent_HeartbeatStopped"></span><span id="vmvirtualmachineevent_heartbeatstopped"></span><span id="VMVIRTUALMACHINEEVENT_HEARTBEATSTOPPED"></span>**vmVirtualMachineEvent\_HeartbeatStopped**</span></span>
</dt> <dd>

<span data-ttu-id="7a1e0-119">Der Takt einer VM wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="7a1e0-119">A VM's heartbeat has stopped.</span></span> <span data-ttu-id="7a1e0-120">Dies weist normalerweise darauf hin, dass das Gast Betriebssystem abgestürzt ist.</span><span class="sxs-lookup"><span data-stu-id="7a1e0-120">This usually indicates that the guest operating system has crashed.</span></span>

</dd> <dt>

<span data-ttu-id="7a1e0-121"><span id="vmVirtualMachineEvent_ConfigurationChanged"></span><span id="vmvirtualmachineevent_configurationchanged"></span><span id="VMVIRTUALMACHINEEVENT_CONFIGURATIONCHANGED"></span>**vmvirtualmachineevent \_ configurationchanged**</span><span class="sxs-lookup"><span data-stu-id="7a1e0-121"><span id="vmVirtualMachineEvent_ConfigurationChanged"></span><span id="vmvirtualmachineevent_configurationchanged"></span><span id="VMVIRTUALMACHINEEVENT_CONFIGURATIONCHANGED"></span>**vmVirtualMachineEvent\_ConfigurationChanged**</span></span>
</dt> <dd>

<span data-ttu-id="7a1e0-122">Ein Wert in der Konfiguration für diesen virtuellen Computer wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="7a1e0-122">A value in the configuration for this VM has changed</span></span>

</dd> <dt>

<span data-ttu-id="7a1e0-123"><span id="vmVirtualMachineEvent_EnhancedVideoModeChanged"></span><span id="vmvirtualmachineevent_enhancedvideomodechanged"></span><span id="VMVIRTUALMACHINEEVENT_ENHANCEDVIDEOMODECHANGED"></span>**vmvirtualmachineevent \_ enhancedvideomode Changed**</span><span class="sxs-lookup"><span data-stu-id="7a1e0-123"><span id="vmVirtualMachineEvent_EnhancedVideoModeChanged"></span><span id="vmvirtualmachineevent_enhancedvideomodechanged"></span><span id="VMVIRTUALMACHINEEVENT_ENHANCEDVIDEOMODECHANGED"></span>**vmVirtualMachineEvent\_EnhancedVideoModeChanged**</span></span>
</dt> <dd>

<span data-ttu-id="7a1e0-124">Der Videomodus eines virtuellen Computers wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="7a1e0-124">A VM's video mode has changed.</span></span>

</dd> <dt>

<span data-ttu-id="7a1e0-125"><span id="vmVirtualMachineEvent_AdditionsUninstalled"></span><span id="vmvirtualmachineevent_additionsuninstalled"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSUNINSTALLED"></span>**vmvirtualmachineevent \_ additionsuninstalliert**</span><span class="sxs-lookup"><span data-stu-id="7a1e0-125"><span id="vmVirtualMachineEvent_AdditionsUninstalled"></span><span id="vmvirtualmachineevent_additionsuninstalled"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSUNINSTALLED"></span>**vmVirtualMachineEvent\_AdditionsUninstalled**</span></span>
</dt> <dd>

<span data-ttu-id="7a1e0-126">Integrations Komponenten wurden auf der VM deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="7a1e0-126">Integration components have been uninstalled from the VM.</span></span>

</dd> <dt>

<span data-ttu-id="7a1e0-127"><span id="vmVirtualMachineEvent_AdditionsAvailable"></span><span id="vmvirtualmachineevent_additionsavailable"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSAVAILABLE"></span>**vmvirtualmachineevent \_ additionsavailable**</span><span class="sxs-lookup"><span data-stu-id="7a1e0-127"><span id="vmVirtualMachineEvent_AdditionsAvailable"></span><span id="vmvirtualmachineevent_additionsavailable"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSAVAILABLE"></span>**vmVirtualMachineEvent\_AdditionsAvailable**</span></span>
</dt> <dd>

<span data-ttu-id="7a1e0-128">Integration ist im Gast Betriebssystem verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7a1e0-128">Integration are available in the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="7a1e0-129"><span id="vmVirtualMachineEvent_GuestShutdown"></span><span id="vmvirtualmachineevent_guestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_GUESTSHUTDOWN"></span>**vmvirtualmachineevent \_ guestshutdown**</span><span class="sxs-lookup"><span data-stu-id="7a1e0-129"><span id="vmVirtualMachineEvent_GuestShutdown"></span><span id="vmvirtualmachineevent_guestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_GUESTSHUTDOWN"></span>**vmVirtualMachineEvent\_GuestShutdown**</span></span>
</dt> <dd>

<span data-ttu-id="7a1e0-130">Ein Gast Betriebssystem wird heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="7a1e0-130">A guest operating system is shutting down.</span></span>

</dd> <dt>

<span data-ttu-id="7a1e0-131"><span id="vmVirtualMachineEvent_GuestLogoff"></span><span id="vmvirtualmachineevent_guestlogoff"></span><span id="VMVIRTUALMACHINEEVENT_GUESTLOGOFF"></span>**vmvirtualmachineevent \_ guestlogoff**</span><span class="sxs-lookup"><span data-stu-id="7a1e0-131"><span id="vmVirtualMachineEvent_GuestLogoff"></span><span id="vmvirtualmachineevent_guestlogoff"></span><span id="VMVIRTUALMACHINEEVENT_GUESTLOGOFF"></span>**vmVirtualMachineEvent\_GuestLogoff**</span></span>
</dt> <dd>

<span data-ttu-id="7a1e0-132">Ein Benutzer hat sich vom Gast Betriebssystem abgemeldet.</span><span class="sxs-lookup"><span data-stu-id="7a1e0-132">A user logged off from the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="7a1e0-133"><span id="vmVirtualMachineEvent_DiskOutOfSpace"></span><span id="vmvirtualmachineevent_diskoutofspace"></span><span id="VMVIRTUALMACHINEEVENT_DISKOUTOFSPACE"></span>**vmvirtualmachineevent \_ diskouesleerraum**</span><span class="sxs-lookup"><span data-stu-id="7a1e0-133"><span id="vmVirtualMachineEvent_DiskOutOfSpace"></span><span id="vmvirtualmachineevent_diskoutofspace"></span><span id="VMVIRTUALMACHINEEVENT_DISKOUTOFSPACE"></span>**vmVirtualMachineEvent\_DiskOutOfSpace**</span></span>
</dt> <dd>

<span data-ttu-id="7a1e0-134">Für den virtuellen Computer ist wenig Speicherplatz auf dem Datenträger erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7a1e0-134">A disk required by the VM is low on space.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7a1e0-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a1e0-135">Requirements</span></span>



| <span data-ttu-id="7a1e0-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a1e0-136">Requirement</span></span> | <span data-ttu-id="7a1e0-137">Wert</span><span class="sxs-lookup"><span data-stu-id="7a1e0-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a1e0-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7a1e0-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7a1e0-139">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7a1e0-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7a1e0-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7a1e0-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7a1e0-141">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7a1e0-141">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7a1e0-142">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="7a1e0-142">End of client support</span></span><br/>    | <span data-ttu-id="7a1e0-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7a1e0-143">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7a1e0-144">Produkt</span><span class="sxs-lookup"><span data-stu-id="7a1e0-144">Product</span></span><br/>                  | <span data-ttu-id="7a1e0-145">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7a1e0-145">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7a1e0-146">Header</span><span class="sxs-lookup"><span data-stu-id="7a1e0-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a1e0-147"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a1e0-147"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a1e0-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a1e0-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a1e0-149">**Ivmvirtualmachineevents**</span><span class="sxs-lookup"><span data-stu-id="7a1e0-149">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

