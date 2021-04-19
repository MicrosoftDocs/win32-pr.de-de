---
description: Ändert die Größe einer vorhandenen virtuellen Festplatte.
ms.assetid: 54FDCA3B-E12B-4E68-B7EE-893C9CD97E1A
title: Resizevirtualharddisk-Methode der Msvm_ImageManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ResizeVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5fcd88a9063dcbe4e19705245b36af33672dfc5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348207"
---
# <a name="resizevirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="62a67-103">Resizevirtualharddisk-Methode der MSVM \_ imagemanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="62a67-103">ResizeVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="62a67-104">Ändert die Größe einer vorhandenen virtuellen Festplatte.</span><span class="sxs-lookup"><span data-stu-id="62a67-104">Resizes an existing virtual hard disk.</span></span> <span data-ttu-id="62a67-105">Die virtuelle Festplatte muss offline sein.</span><span class="sxs-lookup"><span data-stu-id="62a67-105">The virtual hard disk must be offline.</span></span> <span data-ttu-id="62a67-106">Weitere Informationen zu Nutzungseinschränkungen für diese Methode finden Sie unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="62a67-106">See Remarks for usage restrictions for this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="62a67-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="62a67-107">Syntax</span></span>


```mof
uint32 ResizeVirtualHardDisk(
  [in]  string              Path,
  [in]  uint64              MaxInternalSize,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="62a67-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="62a67-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62a67-109">*Pfad* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62a67-109">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62a67-110">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62a67-110">Type: **string**</span></span>

<span data-ttu-id="62a67-111">Der voll qualifizierte Pfad der virtuellen Festplatten Datei.</span><span class="sxs-lookup"><span data-stu-id="62a67-111">The fully qualified path of the virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="62a67-112">*Maxinternalsize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62a67-112">*MaxInternalSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62a67-113">Typ: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="62a67-113">Type: **uint64**</span></span>

<span data-ttu-id="62a67-114">Die maximale Größe der virtuellen Festplatte, die vom virtuellen Computer angezeigt werden kann (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="62a67-114">The maximum size of the virtual hard disk as viewable by the virtual machine, in bytes.</span></span> <span data-ttu-id="62a67-115">Der minimale *maxinternalsize* -Wert ist *disksize* + 512-(*disksize* mod 512).</span><span class="sxs-lookup"><span data-stu-id="62a67-115">*MaxInternalSize* minimum value is *DiskSize* + 512 - (*DiskSize* mod 512).</span></span> <span data-ttu-id="62a67-116">*Disksize* ist die Größe der virtuellen Festplatten Datei (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="62a67-116">*DiskSize* is the size of the virtual hard disk file, in bytes.</span></span> <span data-ttu-id="62a67-117">Der invalidparameter-Fehler (32773) wird zurückgegeben, wenn der angegebene *maxinternalsize* -Wert kleiner als der minimale Wert ist.</span><span class="sxs-lookup"><span data-stu-id="62a67-117">The InvalidParameter error (32773) is returned if the *MaxInternalSize* value specified is less than the minimum value.</span></span>

</dd> <dt>

<span data-ttu-id="62a67-118">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="62a67-118">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62a67-119">Typ: **[ **CIM \_ bettejob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="62a67-119">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="62a67-120">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="62a67-120">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62a67-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="62a67-121">Return value</span></span>

<span data-ttu-id="62a67-122">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="62a67-122">Type: **uint32**</span></span>

<span data-ttu-id="62a67-123">Diese Methode kann einen der folgenden Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="62a67-123">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="62a67-124">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="62a67-124">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="62a67-125">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="62a67-125">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="62a67-126">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="62a67-126">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="62a67-127">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="62a67-127">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="62a67-128">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="62a67-128">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="62a67-129">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="62a67-129">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="62a67-130">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="62a67-130">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="62a67-131">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="62a67-131">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="62a67-132">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="62a67-132">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="62a67-133">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="62a67-133">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="62a67-134">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="62a67-134">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="62a67-135">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="62a67-135">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="62a67-136">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="62a67-136">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="62a67-137">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="62a67-137">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="62a67-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62a67-138">Remarks</span></span>

<span data-ttu-id="62a67-139">Bei dieser Methode können nur die folgenden Typen von virtuellen Festplatten verwendet werden, wenn die Größe der virtuellen Festplatte zunimmt:</span><span class="sxs-lookup"><span data-stu-id="62a67-139">Only the following types of virtual hard disks can be used with this method when the size of the virtual hard disk is being increased:</span></span>

-   <span data-ttu-id="62a67-140">Festgelegte VHD</span><span class="sxs-lookup"><span data-stu-id="62a67-140">Fixed VHD</span></span>
-   <span data-ttu-id="62a67-141">Festes vhdx</span><span class="sxs-lookup"><span data-stu-id="62a67-141">Fixed VHDX</span></span>
-   <span data-ttu-id="62a67-142">Dynamische VHD</span><span class="sxs-lookup"><span data-stu-id="62a67-142">Dynamic VHD</span></span>
-   <span data-ttu-id="62a67-143">Dynamische vhdx-Datei</span><span class="sxs-lookup"><span data-stu-id="62a67-143">Dynamic VHDX</span></span>
-   <span data-ttu-id="62a67-144">Differenzierende vhdx</span><span class="sxs-lookup"><span data-stu-id="62a67-144">Differencing VHDX</span></span>

<span data-ttu-id="62a67-145">Mit dieser Methode können nur die folgenden Typen von virtuellen Festplatten verwendet werden, wenn die Größe der virtuellen Festplatte verringert wird:</span><span class="sxs-lookup"><span data-stu-id="62a67-145">Only the following types of virtual hard disks can be used with this method when the size of the virtual hard disk is being decreased:</span></span>

-   <span data-ttu-id="62a67-146">Festes vhdx</span><span class="sxs-lookup"><span data-stu-id="62a67-146">Fixed VHDX</span></span>
-   <span data-ttu-id="62a67-147">Dynamische vhdx-Datei</span><span class="sxs-lookup"><span data-stu-id="62a67-147">Dynamic VHDX</span></span>
-   <span data-ttu-id="62a67-148">Differenzierende vhdx</span><span class="sxs-lookup"><span data-stu-id="62a67-148">Differencing VHDX</span></span>

<span data-ttu-id="62a67-149">Der Zugriff auf die [**MSVM \_ imagemanagementservice**](msvm-imagemanagementservice.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="62a67-149">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="62a67-150">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="62a67-150">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="62a67-151">Beispiele</span><span class="sxs-lookup"><span data-stu-id="62a67-151">Examples</span></span>

<span data-ttu-id="62a67-152">Im folgenden c#-Beispiel wird eine virtuelle Festplatten Datei erweitert.</span><span class="sxs-lookup"><span data-stu-id="62a67-152">The following C# example expands a virtual hard disk file.</span></span> <span data-ttu-id="62a67-153">Die Dienstprogramme, auf die verwiesen wird, finden Sie unter [Allgemeine Hilfsprogramme für die Virtualisierungsbeispiele (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="62a67-153">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
const UInt64 size1G = 0x40000000;

public static void ResizeVirtualHardDisk(string path, UInt64 maxInternalSize)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("ResizeVirtualHardDisk");
    inParams["Path"] = path;
    inParams["MaxInternalSize"] = maxInternalSize * size1G;
    ManagementBaseObject outParams = imageService.InvokeMethod("ResizeVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was resized successfully.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to resize {0}", inParams["Path"]);
        }
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="62a67-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62a67-154">Requirements</span></span>



| <span data-ttu-id="62a67-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62a67-155">Requirement</span></span> | <span data-ttu-id="62a67-156">Wert</span><span class="sxs-lookup"><span data-stu-id="62a67-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62a67-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="62a67-157">Minimum supported client</span></span><br/> | <span data-ttu-id="62a67-158">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="62a67-158">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="62a67-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="62a67-159">Minimum supported server</span></span><br/> | <span data-ttu-id="62a67-160">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="62a67-160">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="62a67-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="62a67-161">Namespace</span></span><br/>                | <span data-ttu-id="62a67-162">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="62a67-162">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="62a67-163">MOF</span><span class="sxs-lookup"><span data-stu-id="62a67-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62a67-164"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="62a67-164"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="62a67-165">DLL</span><span class="sxs-lookup"><span data-stu-id="62a67-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62a67-166"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="62a67-166"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="62a67-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62a67-167">See also</span></span>

<dl> <dt>

<span data-ttu-id="62a67-168">[**CIM- \_ concretejob**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="62a67-168">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="62a67-169">**MSVM \_ imagemanagementservice**</span><span class="sxs-lookup"><span data-stu-id="62a67-169">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

