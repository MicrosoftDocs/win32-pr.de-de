---
description: Erstellt eine Momentaufnahme einer virtuellen Maschine.
ms.assetid: 2de12fe7-5ec2-49d0-87ff-cd48c34fec46
title: Kreatesnapshot-Methode der Msvm_VirtualSystemSnapshotService-Klasse (dbdaoint. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c62b4abf60e367da1c4ac4b176e5f5d70f547c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346368"
---
# <a name="createsnapshot-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="4a2d4-103">Die Methode "kreatesnapshot" der MSVM- \_ Klasse "virtualsystemsnapshotservice"</span><span class="sxs-lookup"><span data-stu-id="4a2d4-103">CreateSnapshot method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="4a2d4-104">Erstellt eine Momentaufnahme einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="4a2d4-104">Creates a snapshot of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a2d4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a2d4-105">Syntax</span></span>


```mof
uint32 CreateSnapshot(
  [in]      CIM_ComputerSystem           REF AffectedSystem,
  [in]      string                           SnapshotSettings,
  [in]      uint16                           SnapshotType,
  [in, out] CIM_VirtualSystemSettingData REF ResultingSnapshot,
  [out]     CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="4a2d4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a2d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a2d4-107">*Affectedsystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a2d4-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a2d4-108">Ein Verweis auf eine [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Klasse, die den virtuellen Computer zum Erstellen einer Momentaufnahme von darstellt.</span><span class="sxs-lookup"><span data-stu-id="4a2d4-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the virtual machine to create a snapshot of.</span></span>

</dd> <dt>

<span data-ttu-id="4a2d4-109">*Snapshotsettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a2d4-109">*SnapshotSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a2d4-110">Eine Zeichenfolge, die eine eingebettete Instanz einer [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) -Klasse enthält, die die Parametereinstellungen für die Momentaufnahme enthält.</span><span class="sxs-lookup"><span data-stu-id="4a2d4-110">A string that contains an embedded instance of a [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) class that contains the parameter settings for the snapshot.</span></span> <span data-ttu-id="4a2d4-111">Dieser Parameter ist optional und kann eine leere Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="4a2d4-111">This parameter is optional and may be an empty string.</span></span>

</dd> <dt>

<span data-ttu-id="4a2d4-112">*Snapshottype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a2d4-112">*SnapshotType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a2d4-113">Gibt den Typ der angeforderten Momentaufnahme an.</span><span class="sxs-lookup"><span data-stu-id="4a2d4-113">Specifies the type of snapshot requested.</span></span> <span data-ttu-id="4a2d4-114">Dabei muss es sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="4a2d4-114">This must be one of the following values.</span></span>

<dt>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>

<span data-ttu-id="4a2d4-115"><span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Vollständige Momentaufnahme** (2)</span><span class="sxs-lookup"><span data-stu-id="4a2d4-115"><span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Full Snapshot** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4a2d4-116">Vervollständigen Sie die Momentaufnahme des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="4a2d4-116">Complete snapshot of the virtual machine.</span></span>

</dd> <dt>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>

<span data-ttu-id="4a2d4-117"><span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>Datenträger **Momentaufnahme** (3)</span><span class="sxs-lookup"><span data-stu-id="4a2d4-117"><span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**Disk Snapshot** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4a2d4-118">Momentaufnahme der Datenträger virtueller Computer.</span><span class="sxs-lookup"><span data-stu-id="4a2d4-118">Snapshot of virtual machine disks.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="4a2d4-119"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="4a2d4-119"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="4a2d4-120"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="4a2d4-120"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="4a2d4-121">*Resultingsnapshot* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4a2d4-121">*ResultingSnapshot* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a2d4-122">Ein Verweis auf ein [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85)) -Objekt, das die resultierende Momentaufnahme des virtuellen Computers darstellt.</span><span class="sxs-lookup"><span data-stu-id="4a2d4-122">A reference to a [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) object that represents the resulting virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="4a2d4-123">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4a2d4-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a2d4-124">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="4a2d4-124">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a2d4-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4a2d4-125">Return value</span></span>

<span data-ttu-id="4a2d4-126">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="4a2d4-126">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="4a2d4-127">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="4a2d4-127">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4a2d4-128">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="4a2d4-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4a2d4-129">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="4a2d4-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4a2d4-130">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="4a2d4-130">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4a2d4-131">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="4a2d4-131">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4a2d4-132">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="4a2d4-132">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4a2d4-133">**Ungültiger Typ** (6)</span><span class="sxs-lookup"><span data-stu-id="4a2d4-133">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="4a2d4-134">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="4a2d4-134">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4a2d4-135">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="4a2d4-135">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="4a2d4-136">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="4a2d4-136">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="4a2d4-137">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="4a2d4-137">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="4a2d4-138">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4a2d4-138">Examples</span></span>

<span data-ttu-id="4a2d4-139">Mit dem folgenden c#-Beispielcode wird ein virtueller Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="4a2d4-139">The following C# example code creates a virtual machine.</span></span> <span data-ttu-id="4a2d4-140">Die Dienstprogramme, auf die verwiesen wird, finden Sie unter [Allgemeine Hilfsprogramme für die Virtualisierungsbeispiele (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="4a2d4-140">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4a2d4-141">Der folgende Code muss auf dem Host Server für virtuelle Maschinen ausgeführt werden, und er muss mit Administrator Rechten ausgeführt werden, damit er ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="4a2d4-141">To function correctly, the following code must be run on the virtual machine host server, and it must be run with Administrator privileges.</span></span>

 


```CSharp
public static void CreateSnapshot(string vmName)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemSnapshotService");

    ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("CreateSnapshot");

    // Set the AffectedSystem property.
    ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
    if (null == vm)
    {
        throw new ArgumentException(string.Format("The virtual machine \"{0}\" could not be found.", vmName));
    }

    inParams["AffectedSystem"] = vm.Path.Path;

    // Set the SnapshotSettings property.
#if(true)
    inParams["SnapshotSettings"] = "";
#else
    ManagementObject snapshotSettings = Utility.GetServiceObject(scope, "CIM_SettingData"); 
    inParams["SnapshotSettings"] = snapshotSettings.ToString();
#endif       
    // Set the SnapshotType property.
    inParams["SnapshotType"] = 2; // Full snapshot.

    ManagementBaseObject outParams = virtualSystemService.InvokeMethod("CreateSnapshot", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("Snapshot was created successfully.");

            MiscClass.GetAffectedElement(outParams, scope);
        }
        else
        {
            Console.WriteLine("Failed to create snapshot VM");
        }
    }
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        Console.WriteLine("Snapshot was created successfully.");
    }
    else
    {
        Console.WriteLine("Create virtual system snapshot failed with error {0}", outParams["ReturnValue"]);
    }

    inParams.Dispose();
    outParams.Dispose();
    vm.Dispose();
    virtualSystemService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="4a2d4-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a2d4-142">Requirements</span></span>



| <span data-ttu-id="4a2d4-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a2d4-143">Requirement</span></span> | <span data-ttu-id="4a2d4-144">Wert</span><span class="sxs-lookup"><span data-stu-id="4a2d4-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a2d4-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4a2d4-145">Minimum supported client</span></span><br/> | <span data-ttu-id="4a2d4-146">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a2d4-146">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4a2d4-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4a2d4-147">Minimum supported server</span></span><br/> | <span data-ttu-id="4a2d4-148">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a2d4-148">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4a2d4-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="4a2d4-149">Namespace</span></span><br/>                | <span data-ttu-id="4a2d4-150">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="4a2d4-150">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4a2d4-151">Header</span><span class="sxs-lookup"><span data-stu-id="4a2d4-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a2d4-152"><dt>Dbdaoint. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a2d4-152"><dt>Dbdaoint.h</dt></span></span> </dl>                   |
| <span data-ttu-id="4a2d4-153">MOF</span><span class="sxs-lookup"><span data-stu-id="4a2d4-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4a2d4-154"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4a2d4-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4a2d4-155">DLL</span><span class="sxs-lookup"><span data-stu-id="4a2d4-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a2d4-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4a2d4-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4a2d4-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a2d4-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a2d4-158">**MSVM \_ virtualsystemsnapshotservice**</span><span class="sxs-lookup"><span data-stu-id="4a2d4-158">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[<span data-ttu-id="4a2d4-159">**"Kreatevirtualsystemsnapshot" (v1)**</span><span class="sxs-lookup"><span data-stu-id="4a2d4-159">**CreateVirtualSystemSnapshot (V1)**</span></span>](/previous-versions/windows/desktop/virtual/createvirtualsystemsnapshot-msvm-virtualsystemmanagementservice)
</dt> </dl>

 

