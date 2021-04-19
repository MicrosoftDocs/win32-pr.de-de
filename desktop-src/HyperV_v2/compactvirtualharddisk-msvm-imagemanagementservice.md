---
description: Komprimiert eine virtuelle Festplatten Datei.
ms.assetid: 1E64BD91-6FE6-4658-9EBF-615FC705B920
title: Compactvirtualharddisk-Methode der Msvm_ImageManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.CompactVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8e8c148e51105d8c78021b58366e2f2df3913f57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368854"
---
# <a name="compactvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="e4203-103">Compactvirtualharddisk-Methode der MSVM \_ imagemanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="e4203-103">CompactVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="e4203-104">Komprimiert eine virtuelle Festplatten Datei.</span><span class="sxs-lookup"><span data-stu-id="e4203-104">Compacts a virtual hard disk file.</span></span> <span data-ttu-id="e4203-105">Die Komprimierung ist der Prozess der Freigabe nicht verwendeter Teile der virtuellen Festplatte.</span><span class="sxs-lookup"><span data-stu-id="e4203-105">Compacting is the process of freeing unused portions of the virtual hard disk.</span></span> <span data-ttu-id="e4203-106">Die virtuelle Festplatte wird nicht automatisch bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="e4203-106">The virtual hard disk is not automatically mounted.</span></span> <span data-ttu-id="e4203-107">Weitere Informationen zu Nutzungseinschränkungen für diese Methode finden Sie unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="e4203-107">See Remarks for usage restrictions for this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4203-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4203-108">Syntax</span></span>


```mof
uint32 CompactVirtualHardDisk(
  [in]  string              Path,
  [in]  uint16              Mode,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="e4203-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4203-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4203-110">*Pfad* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4203-110">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4203-111">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e4203-111">Type: **string**</span></span>

<span data-ttu-id="e4203-112">Ein voll qualifizierter Pfad, der den Speicherort der Zusammenführungs Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="e4203-112">A fully qualified path that specifies the location of the merging file.</span></span>

</dd> <dt>

<span data-ttu-id="e4203-113">*Modus* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4203-113">*Mode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4203-114">Typ: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e4203-114">Type: **uint16**</span></span>

<span data-ttu-id="e4203-115">Gibt den Modus für den Compact-Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="e4203-115">Specifies the mode for the compact operation.</span></span> <span data-ttu-id="e4203-116">Dabei muss es sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="e4203-116">This must be one of the following values.</span></span>

<dt>

<span id="Full"></span><span id="full"></span><span id="FULL"></span>

<span data-ttu-id="e4203-117">**Full** (0)</span><span class="sxs-lookup"><span data-stu-id="e4203-117">**Full** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Quick"></span><span id="quick"></span><span id="QUICK"></span>

<span data-ttu-id="e4203-118">**Schnell** (1)</span><span class="sxs-lookup"><span data-stu-id="e4203-118">**Quick** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Retrim"></span><span id="retrim"></span><span id="RETRIM"></span>

<span data-ttu-id="e4203-119">**Abruf** (2)</span><span class="sxs-lookup"><span data-stu-id="e4203-119">**Retrim** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Pretrimmed"></span><span id="pretrimmed"></span><span id="PRETRIMMED"></span>

<span data-ttu-id="e4203-120">**Vorab abgeschnitten** (3)</span><span class="sxs-lookup"><span data-stu-id="e4203-120">**Pretrimmed** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Prezeroed"></span><span id="prezeroed"></span><span id="PREZEROED"></span>

<span data-ttu-id="e4203-121">**Präzeroed** (4)</span><span class="sxs-lookup"><span data-stu-id="e4203-121">**Prezeroed** (4)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="e4203-122">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e4203-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4203-123">Typ: **[ **CIM \_ bettejob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="e4203-123">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="e4203-124">Ein Verweis auf den Auftrag (kann **null** sein, wenn die Aufgabe abgeschlossen ist).</span><span class="sxs-lookup"><span data-stu-id="e4203-124">A reference to the job (can be **Null** if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4203-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e4203-125">Return value</span></span>

<span data-ttu-id="e4203-126">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e4203-126">Type: **uint32**</span></span>

<span data-ttu-id="e4203-127">Diese Methode kann einen der folgenden Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e4203-127">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e4203-128">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="e4203-128">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e4203-129">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="e4203-129">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e4203-130">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="e4203-130">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e4203-131">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="e4203-131">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e4203-132">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="e4203-132">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e4203-133">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="e4203-133">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e4203-134">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="e4203-134">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e4203-135">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="e4203-135">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e4203-136">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="e4203-136">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e4203-137">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="e4203-137">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e4203-138">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="e4203-138">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e4203-139">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="e4203-139">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e4203-140">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="e4203-140">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="e4203-141">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="e4203-141">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="e4203-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4203-142">Remarks</span></span>

<span data-ttu-id="e4203-143">Mit dieser Methode können nur die folgenden Typen von virtuellen Festplatten verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="e4203-143">Only the following types of virtual hard disks can be used with this method:</span></span>

-   <span data-ttu-id="e4203-144">Festes vhdx</span><span class="sxs-lookup"><span data-stu-id="e4203-144">Fixed VHDX</span></span>
-   <span data-ttu-id="e4203-145">Dynamische VHD</span><span class="sxs-lookup"><span data-stu-id="e4203-145">Dynamic VHD</span></span>
-   <span data-ttu-id="e4203-146">Dynamische vhdx-Datei</span><span class="sxs-lookup"><span data-stu-id="e4203-146">Dynamic VHDX</span></span>
-   <span data-ttu-id="e4203-147">Differenzierende VHD</span><span class="sxs-lookup"><span data-stu-id="e4203-147">Differencing VHD</span></span>
-   <span data-ttu-id="e4203-148">Differenzierende vhdx</span><span class="sxs-lookup"><span data-stu-id="e4203-148">Differencing VHDX</span></span>

<span data-ttu-id="e4203-149">Der Zugriff auf die [**MSVM \_ imagemanagementservice**](msvm-imagemanagementservice.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="e4203-149">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e4203-150">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e4203-150">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="e4203-151">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e4203-151">Examples</span></span>

<span data-ttu-id="e4203-152">Im folgenden c#-Beispiel wird eine virtuelle Festplatte komprimiert.</span><span class="sxs-lookup"><span data-stu-id="e4203-152">The following C# example compacts a virtual hard disk.</span></span> <span data-ttu-id="e4203-153">Die Dienstprogramme, auf die verwiesen wird, finden Sie unter [Allgemeine Hilfsprogramme für die Virtualisierungsbeispiele (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="e4203-153">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public enum VirtualHardDiskCompactMode
{
    Full = 0,
    Quick = 1,
    Retrim = 2,
    Pretrimmed = 3,
    Prezeroed = 4
}

public static void CompactVirtualHardDisk(string vhdPath, VirtualHardDiskCompactMode compactMode)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("CompactVirtualHardDisk");
    inParams["Path"] = vhdPath;
    inParams["Mode"] = compactMode;
    ManagementBaseObject outParams = imageService.InvokeMethod("CompactVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was compacted successfully.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to compact {0}", inParams["Path"]);
        }
    }
    else
    {
        Console.WriteLine("Compact {0} returned error {1}", inParams["Path"], outParams["ReturnValue"]);
    }

    inParams.Dispose();
    outParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="e4203-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4203-154">Requirements</span></span>



| <span data-ttu-id="e4203-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4203-155">Requirement</span></span> | <span data-ttu-id="e4203-156">Wert</span><span class="sxs-lookup"><span data-stu-id="e4203-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4203-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e4203-157">Minimum supported client</span></span><br/> | <span data-ttu-id="e4203-158">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4203-158">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e4203-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e4203-159">Minimum supported server</span></span><br/> | <span data-ttu-id="e4203-160">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4203-160">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e4203-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="e4203-161">Namespace</span></span><br/>                | <span data-ttu-id="e4203-162">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="e4203-162">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e4203-163">MOF</span><span class="sxs-lookup"><span data-stu-id="e4203-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e4203-164"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e4203-164"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e4203-165">DLL</span><span class="sxs-lookup"><span data-stu-id="e4203-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4203-166"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e4203-166"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e4203-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4203-167">See also</span></span>

<dl> <dt>

<span data-ttu-id="e4203-168">[**CIM- \_ concretejob**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e4203-168">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e4203-169">**MSVM \_ imagemanagementservice**</span><span class="sxs-lookup"><span data-stu-id="e4203-169">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

