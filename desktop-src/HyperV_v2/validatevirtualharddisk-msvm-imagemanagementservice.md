---
description: Bestimmt, ob eine virtuelle Festplatten Datei gültig ist.
ms.assetid: 5F7C99DB-0C81-46D5-A965-B6D87647ABF6
title: Validatevirtualharddisk-Methode der Msvm_ImageManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ValidateVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 50c00dc4336e3e85b7db8ffd334de8868054c997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349635"
---
# <a name="validatevirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="b8636-103">Validatevirtualharddisk-Methode der MSVM \_ imagemanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="b8636-103">ValidateVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="b8636-104">Bestimmt, ob eine virtuelle Festplatten Datei gültig ist.</span><span class="sxs-lookup"><span data-stu-id="b8636-104">Determines whether a virtual hard disk file is valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8636-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8636-105">Syntax</span></span>


```mof
uint32 ValidateVirtualHardDisk(
  [in]  string              Path,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="b8636-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8636-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8636-107">*Pfad* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8636-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8636-108">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b8636-108">Type: **string**</span></span>

<span data-ttu-id="b8636-109">Ein voll qualifizierter Pfad, der den Speicherort der virtuellen Festplatten Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="b8636-109">A fully qualified path that specifies the location of the virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="b8636-110">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b8636-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8636-111">Typ: **[ **CIM \_ bettejob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="b8636-111">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="b8636-112">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="b8636-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8636-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b8636-113">Return value</span></span>

<span data-ttu-id="b8636-114">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b8636-114">Type: **uint32**</span></span>

<span data-ttu-id="b8636-115">Diese Methode kann einen der folgenden Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b8636-115">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b8636-116">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="b8636-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b8636-117">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="b8636-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b8636-118">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="b8636-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="b8636-119">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="b8636-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="b8636-120">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="b8636-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="b8636-121">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="b8636-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="b8636-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="b8636-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="b8636-123">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="b8636-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="b8636-124">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="b8636-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="b8636-125">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="b8636-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="b8636-126">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="b8636-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="b8636-127">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="b8636-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="b8636-128">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="b8636-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="b8636-129">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="b8636-129">**File not found** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="b8636-130">Der **VHD-Differenzierungs Ketten-Cycle wurde erkannt** (32787).</span><span class="sxs-lookup"><span data-stu-id="b8636-130">**Vhd differencing chain cycle detected** (32787)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="b8636-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8636-131">Remarks</span></span>

<span data-ttu-id="b8636-132">Wenn die virtuelle Festplatte ein differenzierender Datenträger ist, wird die gesamte virtuelle Datenträger Kette geöffnet.</span><span class="sxs-lookup"><span data-stu-id="b8636-132">If the virtual hard disk is a differencing disk, the entire virtual disk chain is opened.</span></span> <span data-ttu-id="b8636-133">Wenn der Link in der Datenträger Kette beschädigt ist, wird ein Auftrags Objekt mit dem entsprechenden Fehler initialisiert zurückgegeben, und die untergeordneten und übergeordneten Eigenschaften werden mit dem Speicherort initialisiert, an dem der Link getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="b8636-133">If the link is broken in the disk chain, a job object is returned with the appropriate error initialized and the child and parent properties are initialized to the location where the link is broken.</span></span>

<span data-ttu-id="b8636-134">Der Zugriff auf die [**MSVM \_ imagemanagementservice**](msvm-imagemanagementservice.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="b8636-134">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b8636-135">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="b8636-135">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="b8636-136">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b8636-136">Examples</span></span>

<span data-ttu-id="b8636-137">Im folgenden c#-Beispiel wird ein virtuelles Festplatten Abbild überprüft.</span><span class="sxs-lookup"><span data-stu-id="b8636-137">The following C# example validates a virtual hard disk image.</span></span> <span data-ttu-id="b8636-138">Die Dienstprogramme, auf die verwiesen wird, finden Sie unter [Allgemeine Hilfsprogramme für die Virtualisierungsbeispiele (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="b8636-138">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public static void ValidateVirtualHardDisk(string vhdPath)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("ValidateVirtualHardDisk");
    inParams["Path"] = vhdPath;
    ManagementBaseObject outParams = imageService.InvokeMethod("ValidateVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} is a valid virtual hard disk.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to validate {0}", inParams["Path"]);
        }
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="b8636-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8636-139">Requirements</span></span>



| <span data-ttu-id="b8636-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8636-140">Requirement</span></span> | <span data-ttu-id="b8636-141">Wert</span><span class="sxs-lookup"><span data-stu-id="b8636-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8636-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b8636-142">Minimum supported client</span></span><br/> | <span data-ttu-id="b8636-143">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b8636-143">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b8636-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b8636-144">Minimum supported server</span></span><br/> | <span data-ttu-id="b8636-145">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b8636-145">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b8636-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="b8636-146">Namespace</span></span><br/>                | <span data-ttu-id="b8636-147">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="b8636-147">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b8636-148">MOF</span><span class="sxs-lookup"><span data-stu-id="b8636-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8636-149"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b8636-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8636-150">DLL</span><span class="sxs-lookup"><span data-stu-id="b8636-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8636-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b8636-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b8636-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8636-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8636-153">**Validatevirtualharddisk (v1)**</span><span class="sxs-lookup"><span data-stu-id="b8636-153">**ValidateVirtualHardDisk (V1)**</span></span>](/previous-versions/windows/desktop/virtual/validatevirtualharddisk-msvm-imagemanagementservice)
</dt> <dt>

<span data-ttu-id="b8636-154">[**CIM- \_ concretejob**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b8636-154">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b8636-155">**MSVM \_ imagemanagementservice**</span><span class="sxs-lookup"><span data-stu-id="b8636-155">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

