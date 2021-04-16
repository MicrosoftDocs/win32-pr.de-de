---
description: Führt eine untergeordnete virtuelle Festplatte in einer differenzierenden Kette mit einer oder mehreren übergeordneten virtuellen Festplatten in der Kette zusammen.
ms.assetid: 10633176-F0C3-4CA0-8E7B-2B11FF93B0EA
title: Mergevirtualharddisk-Methode der Msvm_ImageManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.MergeVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 347e11d55357a8b3366aeb09badc53c1afad9e01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529663"
---
# <a name="mergevirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="613a5-103">Mergevirtualharddisk-Methode der MSVM \_ imagemanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="613a5-103">MergeVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="613a5-104">Führt eine untergeordnete virtuelle Festplatte in einer differenzierenden Kette mit einer oder mehreren übergeordneten virtuellen Festplatten in der Kette zusammen.</span><span class="sxs-lookup"><span data-stu-id="613a5-104">Merges a child virtual hard disk in a differencing chain with one or more parent virtual hard disks in the chain.</span></span> <span data-ttu-id="613a5-105">Weitere Informationen zu Nutzungseinschränkungen für diese Methode finden Sie unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="613a5-105">See Remarks for usage restrictions for this method.</span></span>

<span data-ttu-id="613a5-106">Wenn der Benutzer, der diese Funktion ausführt, nicht über die Berechtigung zum Aktualisieren der virtuellen Maschinen verfügt, schlägt diese Funktion fehl.</span><span class="sxs-lookup"><span data-stu-id="613a5-106">If the user executing this function does not have permission to update the virtual machines, then this function will fail.</span></span>

## <a name="syntax"></a><span data-ttu-id="613a5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="613a5-107">Syntax</span></span>


```mof
uint32 MergeVirtualHardDisk(
  [in]  string              SourcePath,
  [in]  string              DestinationPath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="613a5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="613a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="613a5-109">*SourcePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="613a5-109">*SourcePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="613a5-110">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="613a5-110">Type: **string**</span></span>

<span data-ttu-id="613a5-111">Ein voll qualifizierter Pfad, der den Speicherort der virtuellen Festplatten Datei angibt, die zusammengeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="613a5-111">A fully qualified path that specifies the location of the virtual hard disk file to merge.</span></span>

</dd> <dt>

<span data-ttu-id="613a5-112">*DestinationPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="613a5-112">*DestinationPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="613a5-113">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="613a5-113">Type: **string**</span></span>

<span data-ttu-id="613a5-114">Ein voll qualifizierter Pfad, der den Speicherort der übergeordneten virtuellen Festplatten Datei angibt, in der Daten zusammengeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="613a5-114">A fully qualified path that specifies the location of the parent virtual hard disk file into which data is to be merged.</span></span> <span data-ttu-id="613a5-115">Dabei kann es sich um die unmittelbar übergeordnete virtuelle Festplatte der zusammen zufügenden Datei oder das Image des übergeordneten Datenträgers handeln. ein paar Ebenen der differenzierenden Kette.</span><span class="sxs-lookup"><span data-stu-id="613a5-115">This could be the immediate parent virtual hard disk of the merging file or the parent disk image a few levels up the differencing chain.</span></span>

</dd> <dt>

<span data-ttu-id="613a5-116">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="613a5-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="613a5-117">Typ: **[ **CIM \_ bettejob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="613a5-117">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="613a5-118">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="613a5-118">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="613a5-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="613a5-119">Return value</span></span>

<span data-ttu-id="613a5-120">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="613a5-120">Type: **uint32**</span></span>

<span data-ttu-id="613a5-121">Diese Methode kann einen der folgenden Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="613a5-121">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="613a5-122">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="613a5-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="613a5-123">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="613a5-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="613a5-124">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="613a5-124">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="613a5-125">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="613a5-125">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="613a5-126">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="613a5-126">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="613a5-127">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="613a5-127">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="613a5-128">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="613a5-128">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="613a5-129">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="613a5-129">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="613a5-130">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="613a5-130">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="613a5-131">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="613a5-131">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="613a5-132">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="613a5-132">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="613a5-133">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="613a5-133">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="613a5-134">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="613a5-134">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="613a5-135">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="613a5-135">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="613a5-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="613a5-136">Remarks</span></span>

<span data-ttu-id="613a5-137">Die untergeordnete virtuelle Festplatte muss offline sein.</span><span class="sxs-lookup"><span data-stu-id="613a5-137">The child virtual hard disk must be offline.</span></span>

<span data-ttu-id="613a5-138">Mit dieser Methode können nur die folgenden Typen von virtuellen Festplatten verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="613a5-138">Only the following types of virtual hard disks can be used with this method:</span></span>

-   <span data-ttu-id="613a5-139">Differenzierende VHD</span><span class="sxs-lookup"><span data-stu-id="613a5-139">Differencing VHD</span></span>
-   <span data-ttu-id="613a5-140">Differenzierende vhdx</span><span class="sxs-lookup"><span data-stu-id="613a5-140">Differencing VHDX</span></span>

<span data-ttu-id="613a5-141">Der Zugriff auf die [**MSVM \_ imagemanagementservice**](msvm-imagemanagementservice.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="613a5-141">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="613a5-142">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="613a5-142">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="613a5-143">Beispiele</span><span class="sxs-lookup"><span data-stu-id="613a5-143">Examples</span></span>

<span data-ttu-id="613a5-144">Im folgenden c#-Beispiel wird eine virtuelle Festplatten Datei erweitert.</span><span class="sxs-lookup"><span data-stu-id="613a5-144">The following C# example expands a virtual hard disk file.</span></span> <span data-ttu-id="613a5-145">Die Dienstprogramme, auf die verwiesen wird, finden Sie unter [Allgemeine Hilfsprogramme für die Virtualisierungsbeispiele (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="613a5-145">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
// Merges a VHD into a parent VHD.
// ChildPath: The path to the VHD to merge.</param>
// ParentPath: The path to the parent into which to merge.</param>
public static void MergeVirtualHardDisk(string ChildPath, string ParentPath)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("MergeVirtualHardDisk");

    inParams["SourcePath"] = ChildPath;
    inParams["DestinationPath"] = ParentPath;

    ManagementBaseObject outParams = imageService.InvokeMethod("MergeVirtualHardDisk", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("MergeVirtualHardDisk succeeded.");
        }
        else
        {
            Console.WriteLine("MergeVirtualHardDisk failed.");
        }
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="613a5-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="613a5-146">Requirements</span></span>



| <span data-ttu-id="613a5-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="613a5-147">Requirement</span></span> | <span data-ttu-id="613a5-148">Wert</span><span class="sxs-lookup"><span data-stu-id="613a5-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="613a5-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="613a5-149">Minimum supported client</span></span><br/> | <span data-ttu-id="613a5-150">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="613a5-150">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="613a5-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="613a5-151">Minimum supported server</span></span><br/> | <span data-ttu-id="613a5-152">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="613a5-152">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="613a5-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="613a5-153">Namespace</span></span><br/>                | <span data-ttu-id="613a5-154">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="613a5-154">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="613a5-155">MOF</span><span class="sxs-lookup"><span data-stu-id="613a5-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="613a5-156"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="613a5-156"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="613a5-157">DLL</span><span class="sxs-lookup"><span data-stu-id="613a5-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="613a5-158"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="613a5-158"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="613a5-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="613a5-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="613a5-160">[**CIM- \_ concretejob**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="613a5-160">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="613a5-161">**MSVM \_ imagemanagementservice**</span><span class="sxs-lookup"><span data-stu-id="613a5-161">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

