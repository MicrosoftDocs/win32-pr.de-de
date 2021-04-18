---
description: Konvertiert eine vorhandene virtuelle Festplatte in einen anderen Typ oder ein anderes Format.
ms.assetid: D4F3A030-D860-4569-B6CD-31661BD40D54
title: Convertvirtualharddisk-Methode der Msvm_ImageManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ConvertVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 766b117b69ecfebd13986d02ca21df3725981bb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358571"
---
# <a name="convertvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="ae012-103">Convertvirtualharddisk-Methode der MSVM \_ imagemanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="ae012-103">ConvertVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="ae012-104">Konvertiert eine vorhandene virtuelle Festplatte in einen anderen Typ oder ein anderes Format.</span><span class="sxs-lookup"><span data-stu-id="ae012-104">Converts an existing virtual hard disk to a different type or format.</span></span> <span data-ttu-id="ae012-105">Diese Methode erstellt eine neue virtuelle Festplatte und konvertiert die virtuelle Quell Festplatte nicht direkt.</span><span class="sxs-lookup"><span data-stu-id="ae012-105">This method creates a new virtual hard disk and does not convert the source virtual hard disk in place.</span></span> <span data-ttu-id="ae012-106">Weitere Informationen zu Nutzungseinschränkungen für diese Methode finden Sie unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ae012-106">See Remarks for usage restrictions for this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae012-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae012-107">Syntax</span></span>


```mof
uint32 ConvertVirtualHardDisk(
  [in]  string              SourcePath,
  [in]  string              VirtualDiskSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ae012-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae012-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae012-109">*SourcePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae012-109">*SourcePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae012-110">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ae012-110">Type: **string**</span></span>

<span data-ttu-id="ae012-111">Der voll qualifizierte Pfad der zu konvertierenden Quelldatei für die virtuelle Festplatte.</span><span class="sxs-lookup"><span data-stu-id="ae012-111">The fully qualified path of the source virtual hard disk file to convert.</span></span> <span data-ttu-id="ae012-112">Diese Datei wird nicht als Ergebnis dieses Vorgangs geändert.</span><span class="sxs-lookup"><span data-stu-id="ae012-112">This file will not be modified as a result of this operation.</span></span>

</dd> <dt>

<span data-ttu-id="ae012-113">*Virtualdisksettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae012-113">*VirtualDiskSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae012-114">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ae012-114">Type: **string**</span></span>

<span data-ttu-id="ae012-115">Eine Zeichen folgen Darstellung der [**MSVM \_ virtualharddisksettingdata**](msvm-virtualharddisksettingdata.md) -Klasse, die die Attribute der neuen virtuellen Festplatte angibt.</span><span class="sxs-lookup"><span data-stu-id="ae012-115">A string representation of the [**Msvm\_VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) class that specifies the attributes of the new virtual hard disk.</span></span> <span data-ttu-id="ae012-116">Der **Pfad**, der **Typ**, das **Format**, die Eigenschaften **Pfad**-, **BLOCKSIZE**-und **logicalsecorsize** -Eigenschaften müssen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ae012-116">The **Path**, **Type**, **Format**, **ParentPath**, **BlockSize**, and **LogicalSectorSize** properties must be set.</span></span> <span data-ttu-id="ae012-117">Die **Eigenschaft** "Eigenschaft" kann **null** sein, wenn Sie nicht benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="ae012-117">The **ParentPath** property can be **Null** if it is not needed.</span></span> <span data-ttu-id="ae012-118">Legen Sie die **BLOCKSIZE** -Eigenschaft und die **logicalsector size** -Eigenschaft auf 0 fest, um die Standardwerte zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ae012-118">Set the **BlockSize** and **LogicalSectorSize** properties to 0 to use the default values.</span></span>

<span data-ttu-id="ae012-119">Um das Format (VHD oder vhdx) der neuen virtuellen Festplatte anzugeben, legen Sie die Erweiterung des **Pfads** auf den entsprechenden Wert (". VHD" oder ". vhdx") fest.</span><span class="sxs-lookup"><span data-stu-id="ae012-119">To specify the format (VHD or VHDX) of the new virtual hard disk, set the extension of the **Path** to the appropriate value (".vhd" or ".vhdx").</span></span> <span data-ttu-id="ae012-120">Die **Format** -Eigenschaft muss mit der Dateinamenerweiterung im **Pfad** identisch sein.</span><span class="sxs-lookup"><span data-stu-id="ae012-120">The **Format** property must match the file name extension in the **Path**.</span></span>

<span data-ttu-id="ae012-121">Die **logicalsector size** -Eigenschaft wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ae012-121">The **LogicalSectorSize** property will be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="ae012-122">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ae012-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae012-123">Typ: **[ **CIM \_ bettejob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="ae012-123">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="ae012-124">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="ae012-124">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae012-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ae012-125">Return value</span></span>

<span data-ttu-id="ae012-126">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ae012-126">Type: **uint32**</span></span>

<span data-ttu-id="ae012-127">Diese Methode kann einen der folgenden Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ae012-127">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ae012-128">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="ae012-128">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ae012-129">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="ae012-129">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ae012-130">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="ae012-130">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ae012-131">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="ae012-131">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ae012-132">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="ae012-132">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ae012-133">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="ae012-133">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ae012-134">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="ae012-134">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ae012-135">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="ae012-135">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ae012-136">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="ae012-136">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ae012-137">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="ae012-137">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ae012-138">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="ae012-138">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ae012-139">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="ae012-139">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ae012-140">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="ae012-140">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="ae012-141">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="ae012-141">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="ae012-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ae012-142">Remarks</span></span>

<span data-ttu-id="ae012-143">Mit dieser Methode können nur die folgenden Typen von virtuellen Festplatten verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="ae012-143">Only the following types of virtual hard disks can be used with this method:</span></span>

-   <span data-ttu-id="ae012-144">Festgelegte VHD</span><span class="sxs-lookup"><span data-stu-id="ae012-144">Fixed VHD</span></span>
-   <span data-ttu-id="ae012-145">Festes vhdx</span><span class="sxs-lookup"><span data-stu-id="ae012-145">Fixed VHDX</span></span>
-   <span data-ttu-id="ae012-146">Dynamische VHD</span><span class="sxs-lookup"><span data-stu-id="ae012-146">Dynamic VHD</span></span>
-   <span data-ttu-id="ae012-147">Dynamische vhdx-Datei</span><span class="sxs-lookup"><span data-stu-id="ae012-147">Dynamic VHDX</span></span>
-   <span data-ttu-id="ae012-148">Differenzierende VHD</span><span class="sxs-lookup"><span data-stu-id="ae012-148">Differencing VHD</span></span>
-   <span data-ttu-id="ae012-149">Differenzierende vhdx</span><span class="sxs-lookup"><span data-stu-id="ae012-149">Differencing VHDX</span></span>

<span data-ttu-id="ae012-150">Der Zugriff auf die [**MSVM \_ imagemanagementservice**](msvm-imagemanagementservice.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="ae012-150">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ae012-151">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="ae012-151">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="ae012-152">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ae012-152">Examples</span></span>

<span data-ttu-id="ae012-153">Im folgenden c#-Beispiel wird eine virtuelle Festplatte konvertiert.</span><span class="sxs-lookup"><span data-stu-id="ae012-153">The following C# example converts a virtual hard disk.</span></span> <span data-ttu-id="ae012-154">Die Dienstprogramme, auf die verwiesen wird, finden Sie unter [Allgemeine Hilfsprogramme für die Virtualisierungsbeispiele (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="ae012-154">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public enum VirtualHardDiskType
{
    Fixed = 2,
    Dynamic = 3,
    Differencing = 4
}

public enum VirtualHardDiskFormat
{
    Unknown = 0,
    Vhd = 2,
    Vhdx = 3
}

public static void ConvertVirtualHardDisk(string sourcePath, string destinationPath, VirtualHardDiskType diskType, VirtualHardDiskFormat diskFormat)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementPath path = new ManagementPath()
    {
        Server = null,
        NamespacePath = imageService.Path.Path,
        ClassName = "Msvm_VirtualHardDiskSettingData"
    };

    ManagementClass settingsClass = new ManagementClass(path);
    ManagementObject settingsInstance = settingsClass.CreateInstance();
    settingsInstance["Path"] = destinationPath;
    settingsInstance["Type"] = diskType;
    settingsInstance["Format"] = diskFormat;
    settingsInstance["ParentPath"] = null;
    settingsInstance["MaxInternalSize"] = 0;
    settingsInstance["BlockSize"] = 0;
    settingsInstance["LogicalSectorSize"] = 0;
    settingsInstance["PhysicalSectorSize"] = 0;

    ManagementBaseObject inParams = imageService.GetMethodParameters("ConvertVirtualHardDisk");

    inParams["SourcePath"] = sourcePath;
    inParams["VirtualDiskSettingData"] = settingsInstance.GetText(TextFormat.WmiDtd20);

    ManagementBaseObject outParams = imageService.InvokeMethod("ConvertVirtualHardDisk", inParams, null);
    UInt32 result = (UInt32)outParams["ReturnValue"];
    if (ReturnCode.Completed == result)
    {
        Console.WriteLine("{0} was converted successfully.", inParams["SourcePath"]);
    }
    else if (ReturnCode.Started == result)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was converted successfully.", inParams["SourcePath"]);
        }
        else
        {
            Console.WriteLine("Unable to convert {0}", inParams["SourcePath"]);
        }
    }
    else
    {
        // The method failed.
        Console.WriteLine("ConvertVirtualHardDisk failed with error code {0}.", result);
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="ae012-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae012-155">Requirements</span></span>



| <span data-ttu-id="ae012-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae012-156">Requirement</span></span> | <span data-ttu-id="ae012-157">Wert</span><span class="sxs-lookup"><span data-stu-id="ae012-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae012-158">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ae012-158">Minimum supported client</span></span><br/> | <span data-ttu-id="ae012-159">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ae012-159">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ae012-160">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ae012-160">Minimum supported server</span></span><br/> | <span data-ttu-id="ae012-161">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ae012-161">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ae012-162">Namespace</span><span class="sxs-lookup"><span data-stu-id="ae012-162">Namespace</span></span><br/>                | <span data-ttu-id="ae012-163">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="ae012-163">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ae012-164">MOF</span><span class="sxs-lookup"><span data-stu-id="ae012-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae012-165"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ae012-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae012-166">DLL</span><span class="sxs-lookup"><span data-stu-id="ae012-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae012-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ae012-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ae012-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae012-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae012-169">**Convertvirtualharddisk (v1)**</span><span class="sxs-lookup"><span data-stu-id="ae012-169">**ConvertVirtualHardDisk (V1)**</span></span>](/previous-versions/windows/desktop/virtual/convertvirtualharddisk-msvm-imagemanagementservice)
</dt> <dt>

<span data-ttu-id="ae012-170">[**CIM- \_ concretejob**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ae012-170">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ae012-171">**MSVM \_ imagemanagementservice**</span><span class="sxs-lookup"><span data-stu-id="ae012-171">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

