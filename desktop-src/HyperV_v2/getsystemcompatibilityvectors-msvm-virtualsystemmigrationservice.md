---
description: Ruft eine Liste von MSVM- \_ compatibilityvector-Instanzen ab, die verwendet werden können, um die Kompatibilität des virtuellen Computers (VM) zu überprüfen.
ms.assetid: 3881D9A0-07C2-4275-925D-F3C3A36B79B4
title: 'Msvm_VirtualSystemMigrationService:: getsystemcompatibilityvectors-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.GetSystemCompatibilityVectors
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8ef8a374d992468247f6dc8f914d7252e7cd2829
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958750"
---
# <a name="msvm_virtualsystemmigrationservicegetsystemcompatibilityvectors-method"></a><span data-ttu-id="3a2eb-103">MSVM \_ virtualsystemmigrationservice:: getsystemcompatibilityvectors-Methode</span><span class="sxs-lookup"><span data-stu-id="3a2eb-103">Msvm\_VirtualSystemMigrationService::GetSystemCompatibilityVectors method</span></span>

<span data-ttu-id="3a2eb-104">Ruft eine Liste von [**MSVM- \_ compatibilityvector**](msvm-compatibilityvector.md) -Instanzen ab, die verwendet werden können, um die Kompatibilität des virtuellen Computers (VM) zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="3a2eb-104">Gets a list of [**Msvm\_CompatibilityVector**](msvm-compatibilityvector.md) instances that can be used to check for virtual machine (VM) to host compatibility.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a2eb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a2eb-105">Syntax</span></span>


```C++
uint32 GetSystemCompatibilityVectors(
  [in]  CIM_ComputerSystem   ComputerSystem,
  [out] Msvm_CompatibilityVector CompatibilityVectors[]
);
```



## <a name="parameters"></a><span data-ttu-id="3a2eb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a2eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a2eb-107">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a2eb-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a2eb-108">Ein Verweis auf eine [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse, die den virtuellen Computer zum Abrufen von Kompatibilitäts Vektoren darstellt.</span><span class="sxs-lookup"><span data-stu-id="3a2eb-108">A reference to a [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the VM to retrieve compatibility vectors for.</span></span> <span data-ttu-id="3a2eb-109">Wenn sich dieser Parameter auf das hostingcomputersystem bezieht, können die im *compatibilityvectors* -Parameter zurückgegebenen Daten verwendet werden, um zu bestimmen, ob eine der VMS auf dem Host Computersystem schnell zu einem anderen Host Computersystem migriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="3a2eb-109">If this parameter refers to the hosting computer system, the data returned in the *CompatibilityVectors* parameter can be used to determine whether any of the VMs on the hosting computer system can be quickly migrated to another hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="3a2eb-110">*Compatibilityvectors* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3a2eb-110">*CompatibilityVectors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a2eb-111">Ein Array von [**MSVM \_ compatibilityvector**](msvm-compatibilityvector.md) -Instanzen, die die Kompatibilitätsinformationen für die VMs oder das hostingcomputersystem enthalten.</span><span class="sxs-lookup"><span data-stu-id="3a2eb-111">An array of [**Msvm\_CompatibilityVector**](msvm-compatibilityvector.md) instances that contain the compatibility info for the VMs or hosting computer system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a2eb-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3a2eb-112">Return value</span></span>

<span data-ttu-id="3a2eb-113">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="3a2eb-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="3a2eb-114">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="3a2eb-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3a2eb-115">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="3a2eb-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3a2eb-116">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="3a2eb-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="3a2eb-117">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="3a2eb-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="3a2eb-118">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="3a2eb-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="3a2eb-119">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="3a2eb-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="3a2eb-120">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="3a2eb-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="3a2eb-121">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="3a2eb-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="3a2eb-122">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="3a2eb-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="3a2eb-123">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="3a2eb-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="3a2eb-124">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="3a2eb-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="3a2eb-125">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="3a2eb-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="3a2eb-126">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="3a2eb-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="3a2eb-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a2eb-127">Remarks</span></span>

<span data-ttu-id="3a2eb-128">**Getsystemcompatibilityvectors** ruft Kompatibilitätsinformationen für einen virtuellen Computer (VM) (bei Ausführen auf einem VM-Computersystem) oder einen Host (bei Ausführen auf einem Host Computersystem) ab.</span><span class="sxs-lookup"><span data-stu-id="3a2eb-128">**GetSystemCompatibilityVectors** gets compatibility info for a virtual machine (VM) (when run on a VM computer system) or a host (when run on a host computer system).</span></span> <span data-ttu-id="3a2eb-129">Die Kompatibilitätsinformationen bleiben für den Client nicht transparent, während die Informationen eine Möglichkeit bieten, die Host Kompatibilitätsinformationen mit der des virtuellen Computers zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="3a2eb-129">The compatibility info remains opaque to the client while the info provides a way to compare the host compatibility info with that of the VM.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a2eb-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a2eb-130">Requirements</span></span>



| <span data-ttu-id="3a2eb-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a2eb-131">Requirement</span></span> | <span data-ttu-id="3a2eb-132">Wert</span><span class="sxs-lookup"><span data-stu-id="3a2eb-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a2eb-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3a2eb-133">Minimum supported client</span></span><br/> | <span data-ttu-id="3a2eb-134">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="3a2eb-134">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="3a2eb-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3a2eb-135">Minimum supported server</span></span><br/> | <span data-ttu-id="3a2eb-136">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3a2eb-136">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3a2eb-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="3a2eb-137">Namespace</span></span><br/>                | <span data-ttu-id="3a2eb-138">\\\\\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="3a2eb-138">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="3a2eb-139">MOF</span><span class="sxs-lookup"><span data-stu-id="3a2eb-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a2eb-140"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3a2eb-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a2eb-141">DLL</span><span class="sxs-lookup"><span data-stu-id="3a2eb-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a2eb-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3a2eb-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3a2eb-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a2eb-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a2eb-144">**MSVM \_ compatibilityvector**</span><span class="sxs-lookup"><span data-stu-id="3a2eb-144">**Msvm\_CompatibilityVector**</span></span>](msvm-compatibilityvector.md)
</dt> <dt>

[<span data-ttu-id="3a2eb-145">**MSVM \_ virtualsystemmigrationservice**</span><span class="sxs-lookup"><span data-stu-id="3a2eb-145">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




