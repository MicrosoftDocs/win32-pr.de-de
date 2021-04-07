---
description: Überprüft das angegebene geplante System.
ms.assetid: cb969b38-f36d-4c70-b234-590f1c219d22
title: Validateplannedsystem-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ValidatePlannedSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 96137c3774291e06bfffdea3843658a427e36950
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759048"
---
# <a name="validateplannedsystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="a539d-103">Validateplannedsystem-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="a539d-103">ValidatePlannedSystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="a539d-104">Überprüft das angegebene geplante System.</span><span class="sxs-lookup"><span data-stu-id="a539d-104">Validates the specified planned system.</span></span> <span data-ttu-id="a539d-105">Dies umfasst das Überprüfen der Konfiguration des virtuellen Computers, der Geräte, der momentaufnahmenkonfiguration, von Momentaufnahme Geräten, gespeicherter Zustands Dateien und Speicherdateien</span><span class="sxs-lookup"><span data-stu-id="a539d-105">This involves checks of the virtual machine configuration, devices, snapshot configuration, snapshot devices, saved state files and storage files.</span></span>

## <a name="syntax"></a><span data-ttu-id="a539d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a539d-106">Syntax</span></span>


```mof
uint32 ValidatePlannedSystem(
  [in]  Msvm_PlannedComputerSystem REF PlannedSystem,
  [out] CIM_ConcreteJob            REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a539d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a539d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a539d-108">*Plannedsystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a539d-108">*PlannedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a539d-109">Ein Verweis auf ein [**MSVM- \_ plannedcomputersystem**](msvm-plannedcomputersystem.md) -Objekt, das das geplante System darstellt, das überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="a539d-109">A reference to an [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) object that represents the planned system to be validated.</span></span>

</dd> <dt>

<span data-ttu-id="a539d-110">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a539d-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a539d-111">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="a539d-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a539d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a539d-112">Return value</span></span>

<span data-ttu-id="a539d-113">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="a539d-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a539d-114">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="a539d-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a539d-115">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="a539d-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a539d-116">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="a539d-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="a539d-117">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="a539d-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="a539d-118">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="a539d-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="a539d-119">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="a539d-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="a539d-120">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="a539d-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="a539d-121">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="a539d-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="a539d-122">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="a539d-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="a539d-123">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="a539d-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="a539d-124">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="a539d-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="a539d-125">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="a539d-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="a539d-126">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="a539d-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="a539d-127">**Verwendete Datei** (32779)</span><span class="sxs-lookup"><span data-stu-id="a539d-127">**File in Use** (32779)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="a539d-128">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a539d-128">Examples</span></span>

<span data-ttu-id="a539d-129">Im folgenden c#-Beispiel wird die **validateplannedsystem** -Methode verwendet, um einen geplanten virtuellen Computer zu validieren.</span><span class="sxs-lookup"><span data-stu-id="a539d-129">The following C# sample uses the **ValidatePlannedSystem** method to validate a planned virtual machine.</span></span> <span data-ttu-id="a539d-130">Dieser Code stammt aus dem Beispiel zu den von [Hyper-V geplanten virtuellen](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm)Computern.</span><span class="sxs-lookup"><span data-stu-id="a539d-130">This code is taken from the [Hyper-V planned virtual machines sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span></span> <span data-ttu-id="a539d-131">Die Dienstprogramme, auf die verwiesen wird, finden Sie unter [Allgemeine Hilfsprogramme für die Virtualisierungsbeispiele (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="a539d-131">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a539d-132">Der folgende Code muss auf dem Host Server des virtuellen Computers ausgeführt werden, und er muss mit Administrator Rechten ausgeführt werden, um ordnungsgemäß zu funktionieren.</span><span class="sxs-lookup"><span data-stu-id="a539d-132">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
/// <summary>
/// Finds the first Planned VM matching pvmName and validates it, displaying
/// any warnings produced.
/// </summary>
/// <param name="pvmName">The name of the PVM to be validated.</param>
internal static void
ValidatePvm(
    string pvmName
    )
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2");

    using (ManagementObject pvm = WmiUtilities.GetPlannedVirtualMachine(pvmName, scope))
    using (ManagementObject managementService = WmiUtilities.GetVirtualMachineManagementService(scope))
    using (ManagementBaseObject inParams = 
        managementService.GetMethodParameters("ValidatePlannedSystem"))
    {
        inParams["PlannedSystem"] = pvm.Path;

        Console.WriteLine("Validating Planned Virtual Machine \"{0}\" ({1})...",
                pvm["ElementName"], pvm["Name"]);

        using (ManagementBaseObject outParams = 
            managementService.InvokeMethod("ValidatePlannedSystem", inParams, null))
        {
            if (WmiUtilities.ValidateOutput(outParams, scope))
            {
                using (ManagementObject job = 
                    new ManagementObject((string)outParams["Job"]))
                {
                    WmiUtilities.PrintMsvmErrors(job);
                }
            }
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="a539d-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a539d-133">Requirements</span></span>



| <span data-ttu-id="a539d-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a539d-134">Requirement</span></span> | <span data-ttu-id="a539d-135">Wert</span><span class="sxs-lookup"><span data-stu-id="a539d-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a539d-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a539d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a539d-137">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a539d-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a539d-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a539d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a539d-139">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a539d-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a539d-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="a539d-140">Namespace</span></span><br/>                | <span data-ttu-id="a539d-141">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="a539d-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a539d-142">MOF</span><span class="sxs-lookup"><span data-stu-id="a539d-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a539d-143"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a539d-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a539d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="a539d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a539d-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a539d-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a539d-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a539d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a539d-147">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="a539d-147">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

