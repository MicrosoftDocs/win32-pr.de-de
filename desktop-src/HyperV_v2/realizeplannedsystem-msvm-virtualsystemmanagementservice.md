---
description: Überprüft die Konfiguration einer geplanten virtuellen Maschine und konvertiert sie in eine erkannte virtuelle Maschine.
ms.assetid: bddbdc35-4603-45c3-96b4-04f445dbb3a6
title: Realizeplannedsystem-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RealizePlannedSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fc69cbc9be9fc72bc7c1184ec30d9e2b58ba2b6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217812"
---
# <a name="realizeplannedsystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="6bf14-103">Realizeplannedsystem-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="6bf14-103">RealizePlannedSystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="6bf14-104">Überprüft die Konfiguration einer geplanten virtuellen Maschine und konvertiert sie in eine erkannte virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="6bf14-104">Validates the configuration of a planned virtual machine and converts it to a realized virtual machine.</span></span> <span data-ttu-id="6bf14-105">Alle Laufzeitdateien oder gespeicherten Zustands Dateien, die dem virtuellen Computer zugeordnet sind, werden ggf. aus dem Import Verzeichnis in den Daten Stamm der virtuellen Maschine kopiert.</span><span class="sxs-lookup"><span data-stu-id="6bf14-105">Any runtime or saved state files associated with the virtual machine will be copied from the import directory to the virtual machine's data root, if applicable.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bf14-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6bf14-106">Syntax</span></span>


```mof
uint32 RealizePlannedSystem(
  [in]  Msvm_PlannedComputerSystem REF PlannedSystem,
  [out] CIM_ComputerSystem         REF ResultingSystem,
  [out] CIM_ConcreteJob            REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6bf14-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6bf14-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bf14-108">*Plannedsystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6bf14-108">*PlannedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bf14-109">Ein Verweis auf die [**MSVM- \_ plannedcomputersystem**](msvm-plannedcomputersystem.md) -Instanz, die in einen erkannten virtuellen Computer konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6bf14-109">A reference to the [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) instance which is to be converted into a realized virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="6bf14-110">*Resultingsystem* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6bf14-110">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6bf14-111">Wenn der Vorgang synchron abgeschlossen wird, ein Verweis auf ein [**CIM \_ Computersystem**](msvm-computersystem.md) -Objekt, das den resultierenden virtuellen Computer darstellt.</span><span class="sxs-lookup"><span data-stu-id="6bf14-111">If the operation is completed synchronously, a reference to a [**CIM\_ComputerSystem**](msvm-computersystem.md) object that represents the resulting realized virtual machine.</span></span>

<span data-ttu-id="6bf14-112">DataType wurde von [**MSVM \_ Computersystem**](msvm-computersystem.md) in Windows 10, Version 1703, aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6bf14-112">Datatype updated from [**Msvm\_ComputerSystem**](msvm-computersystem.md) in Windows 10, version 1703.</span></span>

</dd> <dt>

<span data-ttu-id="6bf14-113">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6bf14-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6bf14-114">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="6bf14-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bf14-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6bf14-115">Return value</span></span>

<span data-ttu-id="6bf14-116">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="6bf14-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="6bf14-117">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="6bf14-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6bf14-118">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="6bf14-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6bf14-119">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="6bf14-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="6bf14-120">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="6bf14-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="6bf14-121">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="6bf14-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="6bf14-122">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="6bf14-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="6bf14-123">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="6bf14-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="6bf14-124">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="6bf14-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="6bf14-125">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="6bf14-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="6bf14-126">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="6bf14-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="6bf14-127">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="6bf14-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="6bf14-128">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="6bf14-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="6bf14-129">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="6bf14-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="6bf14-130">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6bf14-130">Examples</span></span>

<span data-ttu-id="6bf14-131">Im folgenden c#-Beispiel wird die Methode " **realizeplannedsystem** " verwendet, um einen geplanten virtuellen Computer zu realisieren.</span><span class="sxs-lookup"><span data-stu-id="6bf14-131">The following C# sample uses the **RealizePlannedSystem** method to realize a planned virtual machine.</span></span> <span data-ttu-id="6bf14-132">Dieser Code stammt aus dem Beispiel zu den von [Hyper-V geplanten virtuellen](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm)Computern.</span><span class="sxs-lookup"><span data-stu-id="6bf14-132">This code is taken from the [Hyper-V planned virtual machines sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span></span> <span data-ttu-id="6bf14-133">Die Dienstprogramme, auf die verwiesen wird, finden Sie unter [Allgemeine Hilfsprogramme für die Virtualisierungsbeispiele (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="6bf14-133">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6bf14-134">Der folgende Code muss auf dem Host Server des virtuellen Computers ausgeführt werden, und er muss mit Administrator Rechten ausgeführt werden, um ordnungsgemäß zu funktionieren.</span><span class="sxs-lookup"><span data-stu-id="6bf14-134">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
/// <summary>
/// Finds the first Planned VM matching pvmName and realizes it.
/// </summary>
/// <param name="pvmName">The name of the PVM to be realized.</param>
/// <returns>The Realized Virtual Machine.</returns>
internal static ManagementObject
RealizePvm(
    string pvmName
    )
{
    ManagementObject vm = null;
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2");

    using (ManagementObject pvm = WmiUtilities.GetPlannedVirtualMachine(pvmName, scope))
    using (ManagementObject managementService = WmiUtilities.GetVirtualMachineManagementService(scope))
    using (ManagementBaseObject inParams =
        managementService.GetMethodParameters("RealizePlannedSystem"))
    {
        inParams["PlannedSystem"] = pvm.Path;

        Console.WriteLine("Realizing Planned Virtual Machine \"{0}\" ({1})...",
                pvm["ElementName"], pvm["Name"]);

        using (ManagementBaseObject outParams =
            managementService.InvokeMethod("RealizePlannedSystem", inParams, null))
        {
            if (WmiUtilities.ValidateOutput(outParams, scope, true, true))
            {
                using (ManagementObject job =
                    new ManagementObject((string)outParams["Job"]))
                using (ManagementObjectCollection pvmCollection =
                    job.GetRelated("Msvm_ComputerSystem",
                        "Msvm_AffectedJobElement", null, null, null, null, false, null))
                {
                    vm = WmiUtilities.GetFirstObjectFromCollection(pvmCollection);
                }
            }
        }
    }

    return vm;
}
```



## <a name="requirements"></a><span data-ttu-id="6bf14-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6bf14-135">Requirements</span></span>



| <span data-ttu-id="6bf14-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6bf14-136">Requirement</span></span> | <span data-ttu-id="6bf14-137">Wert</span><span class="sxs-lookup"><span data-stu-id="6bf14-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bf14-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6bf14-138">Minimum supported client</span></span><br/> | <span data-ttu-id="6bf14-139">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6bf14-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6bf14-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6bf14-140">Minimum supported server</span></span><br/> | <span data-ttu-id="6bf14-141">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6bf14-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6bf14-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="6bf14-142">Namespace</span></span><br/>                | <span data-ttu-id="6bf14-143">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="6bf14-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6bf14-144">MOF</span><span class="sxs-lookup"><span data-stu-id="6bf14-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6bf14-145"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6bf14-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6bf14-146">DLL</span><span class="sxs-lookup"><span data-stu-id="6bf14-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6bf14-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6bf14-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6bf14-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6bf14-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bf14-149">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="6bf14-149">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

