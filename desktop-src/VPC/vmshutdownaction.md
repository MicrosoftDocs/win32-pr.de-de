---
title: Vmshutdownaction-Enumeration (vpccominterfaces. h)
description: Gibt an, wie eine virtuelle Maschine heruntergefahren wird, wenn der Host heruntergefahren oder der vpc.exe Prozess beendet wird.
ms.assetid: 271a685a-cac9-4a15-b363-bf8873fd5324
keywords:
- Vmshutdownaction-Enumeration virtueller PC
topic_type:
- apiref
api_name:
- VMShutdownAction
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b939954042a446f7ad9f128580e804d73e9d29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341381"
---
# <a name="vmshutdownaction-enumeration"></a><span data-ttu-id="8bdc9-104">Vmshutdownaction-Enumeration</span><span class="sxs-lookup"><span data-stu-id="8bdc9-104">VMShutdownAction enumeration</span></span>

<span data-ttu-id="8bdc9-105">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8bdc9-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8bdc9-106">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8bdc9-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8bdc9-107">Gibt an, wie eine virtuelle Maschine (VM) heruntergefahren wird, wenn der Host heruntergefahren oder der vpc.exe Prozess beendet wird.</span><span class="sxs-lookup"><span data-stu-id="8bdc9-107">Specifies how to shut down a virtual machine (VM) when the host shuts down or the vpc.exe process exits.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bdc9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8bdc9-108">Syntax</span></span>


```C++
typedef enum  { 
  vmShutdownAction_Save      = 0,
  vmShutdownAction_TurnOff   = 1,
  vmShutdownAction_Shutdown  = 2
} VMShutdownAction;
```



## <a name="constants"></a><span data-ttu-id="8bdc9-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="8bdc9-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8bdc9-110"><span id="vmShutdownAction_Save"></span><span id="vmshutdownaction_save"></span><span id="VMSHUTDOWNACTION_SAVE"></span>**vmshutdownaction \_ Speichern**</span><span class="sxs-lookup"><span data-stu-id="8bdc9-110"><span id="vmShutdownAction_Save"></span><span id="vmshutdownaction_save"></span><span id="VMSHUTDOWNACTION_SAVE"></span>**vmShutdownAction\_Save**</span></span>
</dt> <dd>

<span data-ttu-id="8bdc9-111">Speichern Sie den VM-Status.</span><span class="sxs-lookup"><span data-stu-id="8bdc9-111">Save the VM state.</span></span>

</dd> <dt>

<span data-ttu-id="8bdc9-112"><span id="vmShutdownAction_TurnOff"></span><span id="vmshutdownaction_turnoff"></span><span id="VMSHUTDOWNACTION_TURNOFF"></span>**vmshutdownaction- \_ Abzweigung**</span><span class="sxs-lookup"><span data-stu-id="8bdc9-112"><span id="vmShutdownAction_TurnOff"></span><span id="vmshutdownaction_turnoff"></span><span id="VMSHUTDOWNACTION_TURNOFF"></span>**vmShutdownAction\_TurnOff**</span></span>
</dt> <dd>

<span data-ttu-id="8bdc9-113">Schalten Sie die VM aus, ohne die Laufwerke abzumachen.</span><span class="sxs-lookup"><span data-stu-id="8bdc9-113">Turn off the VM without undoing the drives.</span></span>

</dd> <dt>

<span data-ttu-id="8bdc9-114"><span id="vmShutdownAction_Shutdown"></span><span id="vmshutdownaction_shutdown"></span><span id="VMSHUTDOWNACTION_SHUTDOWN"></span>**vmshutdownaction wird \_ heruntergefahren**</span><span class="sxs-lookup"><span data-stu-id="8bdc9-114"><span id="vmShutdownAction_Shutdown"></span><span id="vmshutdownaction_shutdown"></span><span id="VMSHUTDOWNACTION_SHUTDOWN"></span>**vmShutdownAction\_Shutdown**</span></span>
</dt> <dd>

<span data-ttu-id="8bdc9-115">Fahren Sie das Gast Betriebssystem auf dem virtuellen Computer herunter, ohne die Laufwerke abzumachen, wenn die Integrations Komponenten verfügbar sind, und speichern Sie andernfalls die VM.</span><span class="sxs-lookup"><span data-stu-id="8bdc9-115">Shut down the guest operating system on the VM without undoing the drives if the integration components are available and will save the VM otherwise.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8bdc9-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8bdc9-116">Requirements</span></span>



| <span data-ttu-id="8bdc9-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8bdc9-117">Requirement</span></span> | <span data-ttu-id="8bdc9-118">Wert</span><span class="sxs-lookup"><span data-stu-id="8bdc9-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bdc9-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8bdc9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8bdc9-120">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8bdc9-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8bdc9-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8bdc9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8bdc9-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8bdc9-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8bdc9-123">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="8bdc9-123">End of client support</span></span><br/>    | <span data-ttu-id="8bdc9-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8bdc9-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8bdc9-125">Produkt</span><span class="sxs-lookup"><span data-stu-id="8bdc9-125">Product</span></span><br/>                  | <span data-ttu-id="8bdc9-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8bdc9-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8bdc9-127">Header</span><span class="sxs-lookup"><span data-stu-id="8bdc9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bdc9-128"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bdc9-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bdc9-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8bdc9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bdc9-130">Windows Virtual PC-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="8bdc9-130">Windows Virtual PC Enumerations</span></span>](virtual-pc-enumerations.md)
</dt> <dt>

[<span data-ttu-id="8bdc9-131">**Ivmvirtualmachine:: shutdownaktiononquit**</span><span class="sxs-lookup"><span data-stu-id="8bdc9-131">**IVMVirtualMachine::ShutdownActionOnQuit**</span></span>](ivmvirtualmachine-shutdownactiononquit.md)
</dt> </dl>

 

