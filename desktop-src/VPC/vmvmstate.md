---
title: Vmvmstate-Enumeration (vpccominterfaces. h)
description: Gibt den Status einer virtuellen Maschine an.
ms.assetid: 952dab9d-3d38-4cc5-ab75-4ee5096f7923
keywords:
- Vmvmstate-Enumeration virtueller PC
topic_type:
- apiref
api_name:
- VMVMState
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45505e4fb4b444b15697afca4576e889f2da9a6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339586"
---
# <a name="vmvmstate-enumeration"></a><span data-ttu-id="30730-104">Vmvmstate-Enumeration</span><span class="sxs-lookup"><span data-stu-id="30730-104">VMVMState enumeration</span></span>

<span data-ttu-id="30730-105">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="30730-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="30730-106">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="30730-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="30730-107">Gibt den Status einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="30730-107">Specifies the state of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="30730-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="30730-108">Syntax</span></span>


```C++
typedef enum  { 
  vmVMState_Invalid        = 0,
  vmVMState_TurnedOff      = 1,
  vmVMState_Saved          = 2,
  vmVMState_TurningOn      = 3,
  vmVMState_Restoring      = 4,
  vmVMState_Running        = 5,
  vmVMState_Paused         = 6,
  vmVMState_Saving         = 7,
  vmVMState_TurningOff     = 8,
  vmVMState_MergingDrives  = 9,
  vmVMState_DeleteMachine  = 10
} VMVMState;
```



## <a name="constants"></a><span data-ttu-id="30730-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="30730-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="30730-110"><span id="vmVMState_Invalid"></span><span id="vmvmstate_invalid"></span><span id="VMVMSTATE_INVALID"></span>**vmvmstate ist \_ ungültig.**</span><span class="sxs-lookup"><span data-stu-id="30730-110"><span id="vmVMState_Invalid"></span><span id="vmvmstate_invalid"></span><span id="VMVMSTATE_INVALID"></span>**vmVMState\_Invalid**</span></span>
</dt> <dd>

<span data-ttu-id="30730-111">Ungültiger Status (sollte nicht auftreten, wenn der virtuelle Computer vorhanden ist).</span><span class="sxs-lookup"><span data-stu-id="30730-111">An invalid state (should not occur if the virtual machine exists).</span></span>

</dd> <dt>

<span data-ttu-id="30730-112"><span id="vmVMState_TurnedOff"></span><span id="vmvmstate_turnedoff"></span><span id="VMVMSTATE_TURNEDOFF"></span>**vmvmstate \_ turnetdoff**</span><span class="sxs-lookup"><span data-stu-id="30730-112"><span id="vmVMState_TurnedOff"></span><span id="vmvmstate_turnedoff"></span><span id="VMVMSTATE_TURNEDOFF"></span>**vmVMState\_TurnedOff**</span></span>
</dt> <dd>

<span data-ttu-id="30730-113">Off und nicht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="30730-113">Off and not saved.</span></span>

</dd> <dt>

<span data-ttu-id="30730-114"><span id="vmVMState_Saved"></span><span id="vmvmstate_saved"></span><span id="VMVMSTATE_SAVED"></span>**vmvmstate wurde \_ gespeichert.**</span><span class="sxs-lookup"><span data-stu-id="30730-114"><span id="vmVMState_Saved"></span><span id="vmvmstate_saved"></span><span id="VMVMSTATE_SAVED"></span>**vmVMState\_Saved**</span></span>
</dt> <dd>

<span data-ttu-id="30730-115">Aus, aber der Gast wird gespeichert.</span><span class="sxs-lookup"><span data-stu-id="30730-115">Off but the guest is saved.</span></span>

</dd> <dt>

<span data-ttu-id="30730-116"><span id="vmVMState_TurningOn"></span><span id="vmvmstate_turningon"></span><span id="VMVMSTATE_TURNINGON"></span>**vmvmstate- \_ turningon**</span><span class="sxs-lookup"><span data-stu-id="30730-116"><span id="vmVMState_TurningOn"></span><span id="vmvmstate_turningon"></span><span id="VMVMSTATE_TURNINGON"></span>**vmVMState\_TurningOn**</span></span>
</dt> <dd>

<span data-ttu-id="30730-117">Beim Einschalten.</span><span class="sxs-lookup"><span data-stu-id="30730-117">In the process of turning on.</span></span>

</dd> <dt>

<span data-ttu-id="30730-118"><span id="vmVMState_Restoring"></span><span id="vmvmstate_restoring"></span><span id="VMVMSTATE_RESTORING"></span>**vmvmstate- \_ Wiederherstellung**</span><span class="sxs-lookup"><span data-stu-id="30730-118"><span id="vmVMState_Restoring"></span><span id="vmvmstate_restoring"></span><span id="VMVMSTATE_RESTORING"></span>**vmVMState\_Restoring**</span></span>
</dt> <dd>

<span data-ttu-id="30730-119">Der Zustand wird wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="30730-119">Restoring the state.</span></span>

</dd> <dt>

<span data-ttu-id="30730-120"><span id="vmVMState_Running"></span><span id="vmvmstate_running"></span><span id="VMVMSTATE_RUNNING"></span>**vmvmstate wird \_ ausgeführt**</span><span class="sxs-lookup"><span data-stu-id="30730-120"><span id="vmVMState_Running"></span><span id="vmvmstate_running"></span><span id="VMVMSTATE_RUNNING"></span>**vmVMState\_Running**</span></span>
</dt> <dd>

<span data-ttu-id="30730-121">Wird ausgeführt und nicht angehalten.</span><span class="sxs-lookup"><span data-stu-id="30730-121">Running and not paused.</span></span>

</dd> <dt>

<span data-ttu-id="30730-122"><span id="vmVMState_Paused"></span><span id="vmvmstate_paused"></span><span id="VMVMSTATE_PAUSED"></span>**vmvmstate \_ angehalten**</span><span class="sxs-lookup"><span data-stu-id="30730-122"><span id="vmVMState_Paused"></span><span id="vmvmstate_paused"></span><span id="VMVMSTATE_PAUSED"></span>**vmVMState\_Paused**</span></span>
</dt> <dd>

<span data-ttu-id="30730-123">Wird ausgeführt und angehalten.</span><span class="sxs-lookup"><span data-stu-id="30730-123">Running and paused.</span></span>

</dd> <dt>

<span data-ttu-id="30730-124"><span id="vmVMState_Saving"></span><span id="vmvmstate_saving"></span><span id="VMVMSTATE_SAVING"></span>**Speichern von vmvmstate \_**</span><span class="sxs-lookup"><span data-stu-id="30730-124"><span id="vmVMState_Saving"></span><span id="vmvmstate_saving"></span><span id="VMVMSTATE_SAVING"></span>**vmVMState\_Saving**</span></span>
</dt> <dd>

<span data-ttu-id="30730-125">Der Zustand wird gespeichert.</span><span class="sxs-lookup"><span data-stu-id="30730-125">Saving the state.</span></span>

</dd> <dt>

<span data-ttu-id="30730-126"><span id="vmVMState_TurningOff"></span><span id="vmvmstate_turningoff"></span><span id="VMVMSTATE_TURNINGOFF"></span>**vmvmstate ( \_ turningoff)**</span><span class="sxs-lookup"><span data-stu-id="30730-126"><span id="vmVMState_TurningOff"></span><span id="vmvmstate_turningoff"></span><span id="VMVMSTATE_TURNINGOFF"></span>**vmVMState\_TurningOff**</span></span>
</dt> <dd>

<span data-ttu-id="30730-127">Beim Ausschalten.</span><span class="sxs-lookup"><span data-stu-id="30730-127">In the process of turning off.</span></span>

</dd> <dt>

<span data-ttu-id="30730-128"><span id="vmVMState_MergingDrives"></span><span id="vmvmstate_mergingdrives"></span><span id="VMVMSTATE_MERGINGDRIVES"></span>**vmvmstate- \_ mergingdrives**</span><span class="sxs-lookup"><span data-stu-id="30730-128"><span id="vmVMState_MergingDrives"></span><span id="vmvmstate_mergingdrives"></span><span id="VMVMSTATE_MERGINGDRIVES"></span>**vmVMState\_MergingDrives**</span></span>
</dt> <dd>

<span data-ttu-id="30730-129">Beim Zusammenführen von rückgängig-Laufwerken.</span><span class="sxs-lookup"><span data-stu-id="30730-129">In the process of merging undo drives.</span></span>

</dd> <dt>

<span data-ttu-id="30730-130"><span id="vmVMState_DeleteMachine"></span><span id="vmvmstate_deletemachine"></span><span id="VMVMSTATE_DELETEMACHINE"></span>**vmvmstate \_ deletemachine**</span><span class="sxs-lookup"><span data-stu-id="30730-130"><span id="vmVMState_DeleteMachine"></span><span id="vmvmstate_deletemachine"></span><span id="VMVMSTATE_DELETEMACHINE"></span>**vmVMState\_DeleteMachine**</span></span>
</dt> <dd>

<span data-ttu-id="30730-131">Der virtuelle Computer wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="30730-131">Deleting the virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="30730-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30730-132">Requirements</span></span>



| <span data-ttu-id="30730-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30730-133">Requirement</span></span> | <span data-ttu-id="30730-134">Wert</span><span class="sxs-lookup"><span data-stu-id="30730-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="30730-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="30730-135">Minimum supported client</span></span><br/> | <span data-ttu-id="30730-136">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30730-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="30730-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="30730-137">Minimum supported server</span></span><br/> | <span data-ttu-id="30730-138">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="30730-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="30730-139">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="30730-139">End of client support</span></span><br/>    | <span data-ttu-id="30730-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="30730-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="30730-141">Produkt</span><span class="sxs-lookup"><span data-stu-id="30730-141">Product</span></span><br/>                  | <span data-ttu-id="30730-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="30730-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="30730-143">Header</span><span class="sxs-lookup"><span data-stu-id="30730-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="30730-144"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="30730-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30730-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30730-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30730-146">**Ivmvirtualmachine:: State**</span><span class="sxs-lookup"><span data-stu-id="30730-146">**IVMVirtualMachine::State**</span></span>](ivmvirtualmachine-state.md)
</dt> <dt>

[<span data-ttu-id="30730-147">**Ivmvirtualmachineevents:: OnStateChange**</span><span class="sxs-lookup"><span data-stu-id="30730-147">**IVMVirtualMachineEvents::OnStateChange**</span></span>](ivmvirtualmachineevents-onstatechange.md)
</dt> <dt>

[<span data-ttu-id="30730-148">**Ivmvirtualpcevents:: onvmstatechange**</span><span class="sxs-lookup"><span data-stu-id="30730-148">**IVMVirtualPCEvents::OnVMStateChange**</span></span>](ivmvirtualpcevents-onvmstatechange.md)
</dt> </dl>

 

