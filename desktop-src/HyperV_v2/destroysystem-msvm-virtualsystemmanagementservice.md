---
description: Entfernt den zuvor definierten virtuellen Computer aus dem Verwaltungsbereich des Host Systems.
ms.assetid: 16E6EEB0-CB29-4FFC-AEFF-872E099337FA
title: Destroysystem-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DestroySystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1caf4e4a590bdbfe2f7543e23d5ca00018300fb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867075"
---
# <a name="destroysystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="57b18-103">Destroysystem-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="57b18-103">DestroySystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="57b18-104">Entfernt den zuvor definierten virtuellen Computer aus dem Verwaltungsbereich des Host Systems.</span><span class="sxs-lookup"><span data-stu-id="57b18-104">Removes the previously defined virtual machine from the management scope of the host system.</span></span> <span data-ttu-id="57b18-105">Alle zugehörigen Ressourcen Definitionen werden ebenfalls entfernt.</span><span class="sxs-lookup"><span data-stu-id="57b18-105">Any associated resource definitions will also be removed.</span></span> <span data-ttu-id="57b18-106">Der virtuelle Computer muss sich im ausgeschalteten oder gespeicherten Zustand befinden, bevor diese Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="57b18-106">The virtual machine must be in the powered off or saved state prior to calling this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="57b18-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="57b18-107">Syntax</span></span>


```mof
uint32 DestroySystem(
  [in]  CIM_ComputerSystem REF AffectedSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="57b18-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="57b18-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57b18-109">*Affectedsystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57b18-109">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57b18-110">Typ: **CIM \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="57b18-110">Type: **CIM\_ComputerSystem**</span></span>

<span data-ttu-id="57b18-111">Ein Verweis auf eine Instanz des [**CIM- \_ Computer Systems**](/windows/desktop/CIMWin32Prov/cim-computersystem) , die die zu zerstörende Instanz des virtuellen Computers darstellt.</span><span class="sxs-lookup"><span data-stu-id="57b18-111">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) that represents the virtual machine instance to be destroyed.</span></span>

</dd> <dt>

<span data-ttu-id="57b18-112">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="57b18-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57b18-113">Typ: **CIM \_ bettejob**</span><span class="sxs-lookup"><span data-stu-id="57b18-113">Type: **CIM\_ConcreteJob**</span></span>

<span data-ttu-id="57b18-114">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="57b18-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57b18-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="57b18-115">Return value</span></span>

<span data-ttu-id="57b18-116">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57b18-116">Type: **uint32**</span></span>

<span data-ttu-id="57b18-117">Wenn diese Methode synchron ausgeführt wird, wird 0 zurückgegeben, wenn Sie erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="57b18-117">If this method is executed synchronously, it returns 0 if it succeeds.</span></span> <span data-ttu-id="57b18-118">Wenn diese Methode asynchron ausgeführt wird, wird 4096 zurückgegeben, und der *Auftrags* Ausgabeparameter kann verwendet werden, um den Fortschritt des asynchronen Vorgangs zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="57b18-118">If this method is executed asynchronously, it returns 4096 and the *Job* output parameter can be used to track the progress of the asynchronous operation.</span></span> <span data-ttu-id="57b18-119">Jeder andere Rückgabewert gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="57b18-119">Any other return value indicates an error.</span></span>

<dl> <dt>

<span data-ttu-id="57b18-120">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="57b18-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="57b18-121">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="57b18-121">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="57b18-122">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="57b18-122">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="57b18-123">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="57b18-123">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="57b18-124">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="57b18-124">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="57b18-125">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="57b18-125">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="57b18-126">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="57b18-126">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="57b18-127">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="57b18-127">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="57b18-128">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="57b18-128">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="57b18-129">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="57b18-129">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="57b18-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="57b18-130">Remarks</span></span>

<span data-ttu-id="57b18-131">Der Zugriff auf die [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="57b18-131">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="57b18-132">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="57b18-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="57b18-133">Beispiele</span><span class="sxs-lookup"><span data-stu-id="57b18-133">Examples</span></span>

<span data-ttu-id="57b18-134">Im folgenden c#-Beispiel wird die **destroysystem** -Methode verwendet, um einen geplanten virtuellen Computer zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="57b18-134">The following C# sample uses the **DestroySystem** method to remove a planned virtual machine.</span></span> <span data-ttu-id="57b18-135">Dieser Code stammt aus dem Beispiel zu den von [Hyper-V geplanten virtuellen](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm)Computern.</span><span class="sxs-lookup"><span data-stu-id="57b18-135">This code is taken from the [Hyper-V planned virtual machines sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span></span> <span data-ttu-id="57b18-136">Die Dienstprogramme, auf die verwiesen wird, finden Sie unter [Allgemeine Hilfsprogramme für die Virtualisierungsbeispiele (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="57b18-136">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="57b18-137">Der folgende Code muss auf dem Host Server des virtuellen Computers ausgeführt werden, und er muss mit Administrator Rechten ausgeführt werden, um ordnungsgemäß zu funktionieren.</span><span class="sxs-lookup"><span data-stu-id="57b18-137">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
/// <summary>
/// Finds the first Planned VM matching pvmName and removes it.
/// </summary>
/// <param name="pvmName">The name of the PVM to be removed.</param>
internal static void
RemovePvm(
    string pvmName
    )
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2");

    using (ManagementObject pvm = WmiUtilities.GetPlannedVirtualMachine(pvmName, scope))
    using (ManagementObject managementService = WmiUtilities.GetVirtualMachineManagementService(scope))
    using (ManagementBaseObject inParams =
        managementService.GetMethodParameters("DestroySystem"))
    {
        inParams["AffectedSystem"] = pvm.Path;

        Console.WriteLine("Removing Planned Virtual Machine \"{0}\" ({1})...",
                pvm["ElementName"], pvm["Name"]);

        using (ManagementBaseObject outParams =
            managementService.InvokeMethod("DestroySystem", inParams, null))
        {
            WmiUtilities.ValidateOutput(outParams, scope);
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="57b18-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="57b18-138">Requirements</span></span>



| <span data-ttu-id="57b18-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="57b18-139">Requirement</span></span> | <span data-ttu-id="57b18-140">Wert</span><span class="sxs-lookup"><span data-stu-id="57b18-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57b18-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="57b18-141">Minimum supported client</span></span><br/> | <span data-ttu-id="57b18-142">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57b18-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="57b18-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="57b18-143">Minimum supported server</span></span><br/> | <span data-ttu-id="57b18-144">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57b18-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="57b18-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="57b18-145">Namespace</span></span><br/>                | <span data-ttu-id="57b18-146">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="57b18-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="57b18-147">MOF</span><span class="sxs-lookup"><span data-stu-id="57b18-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="57b18-148"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="57b18-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="57b18-149">DLL</span><span class="sxs-lookup"><span data-stu-id="57b18-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57b18-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="57b18-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="57b18-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57b18-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57b18-152">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="57b18-152">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

