---
description: Fügt eine virtuelle Festplatten Datei im Loopback Modus an.
ms.assetid: 54bd8e67-e309-4bf3-94bd-e29bc3300a3d
title: Attachvirtualharddisk-Methode der Msvm_ImageManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.AttachVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0f8a22ac377eb96fdc01fa54877cdc6c12619c41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865220"
---
# <a name="attachvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="75a6e-103">Attachvirtualharddisk-Methode der MSVM \_ imagemanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="75a6e-103">AttachVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="75a6e-104">Fügt eine virtuelle Festplatten Datei im Loopback Modus an.</span><span class="sxs-lookup"><span data-stu-id="75a6e-104">Attaches a virtual hard disk file in loopback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="75a6e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="75a6e-105">Syntax</span></span>


```mof
uint32 AttachVirtualHardDisk(
  [in]  string              Path,
  [in]  boolean             AssignDriveLetter,
  [in]  boolean             ReadOnly,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="75a6e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="75a6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75a6e-107">*Pfad* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75a6e-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75a6e-108">Ein voll qualifizierter Pfad, der den Speicherort der anzufügenden virtuellen Festplatten Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="75a6e-108">A fully qualified path that specifies the location of the virtual hard disk file to attach.</span></span>

</dd> <dt>

<span data-ttu-id="75a6e-109">Zuder zuder *Zuordnung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75a6e-109">*AssignDriveLetter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75a6e-110">Gibt an, ob den Volumes des Datenträgers Laufwerk Buchstaben zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="75a6e-110">Indicates if drive letters are assigned to the disk's volumes.</span></span>

</dd> <dt>

<span data-ttu-id="75a6e-111">Schreibgeschützt  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75a6e-111">*ReadOnly* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75a6e-112">Gibt an, ob die angefügte Festplatte schreibgeschützt sein soll.</span><span class="sxs-lookup"><span data-stu-id="75a6e-112">Indicates if the attached hard disk should be read-only.</span></span>

</dd> <dt>

<span data-ttu-id="75a6e-113">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="75a6e-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75a6e-114">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="75a6e-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75a6e-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="75a6e-115">Return value</span></span>

<span data-ttu-id="75a6e-116">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="75a6e-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="75a6e-117">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="75a6e-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="75a6e-118">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="75a6e-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="75a6e-119">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="75a6e-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="75a6e-120">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="75a6e-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="75a6e-121">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="75a6e-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="75a6e-122">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="75a6e-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="75a6e-123">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="75a6e-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="75a6e-124">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="75a6e-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="75a6e-125">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="75a6e-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="75a6e-126">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="75a6e-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="75a6e-127">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="75a6e-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="75a6e-128">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="75a6e-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="75a6e-129">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="75a6e-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="75a6e-130">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="75a6e-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="75a6e-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75a6e-131">Remarks</span></span>

<span data-ttu-id="75a6e-132">Verwenden Sie zum Trennen der virtuellen Festplatte die Methode [**MSVM \_ mountedstorageimage. detachvirtualharddisk**](detachvirtualharddisk-msvm-mountedstorageimage.md) .</span><span class="sxs-lookup"><span data-stu-id="75a6e-132">To detach the virtual hard disk, use the [**Msvm\_MountedStorageImage.DetachVirtualHardDisk**](detachvirtualharddisk-msvm-mountedstorageimage.md) method.</span></span>

<span data-ttu-id="75a6e-133">Der Zugriff auf die [**MSVM \_ imagemanagementservice**](msvm-imagemanagementservice.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="75a6e-133">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="75a6e-134">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="75a6e-134">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="75a6e-135">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75a6e-135">Examples</span></span>

<span data-ttu-id="75a6e-136">Im folgenden c#-Beispiel wird gezeigt, wie Sie eine virtuelle Festplatten Datei anfügen.</span><span class="sxs-lookup"><span data-stu-id="75a6e-136">The following C# example shows how to attach a virtual hard disk file.</span></span> <span data-ttu-id="75a6e-137">Die Dienstprogramme, auf die verwiesen wird, finden Sie unter [Allgemeine Hilfsprogramme für die Virtualisierungsbeispiele (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="75a6e-137">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public static void AttachVirtualHardDisk(string path)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("AttachVirtualHardDisk");
    inParams["Path"] = path;
    inParams["AssignDriveLetter"] = true;
    inParams["ReadOnly"] = false;
    ManagementBaseObject outParams = imageService.InvokeMethod("AttachVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was attached successfully.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to attach {0}", inParams["Path"]);
        }
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="75a6e-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75a6e-138">Requirements</span></span>



| <span data-ttu-id="75a6e-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75a6e-139">Requirement</span></span> | <span data-ttu-id="75a6e-140">Wert</span><span class="sxs-lookup"><span data-stu-id="75a6e-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75a6e-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="75a6e-141">Minimum supported client</span></span><br/> | <span data-ttu-id="75a6e-142">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="75a6e-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="75a6e-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="75a6e-143">Minimum supported server</span></span><br/> | <span data-ttu-id="75a6e-144">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="75a6e-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="75a6e-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="75a6e-145">Namespace</span></span><br/>                | <span data-ttu-id="75a6e-146">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="75a6e-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="75a6e-147">MOF</span><span class="sxs-lookup"><span data-stu-id="75a6e-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75a6e-148"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="75a6e-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="75a6e-149">DLL</span><span class="sxs-lookup"><span data-stu-id="75a6e-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75a6e-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="75a6e-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="75a6e-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75a6e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75a6e-152">**MSVM \_ mountedstorageimage. detachvirtualharddisk**</span><span class="sxs-lookup"><span data-stu-id="75a6e-152">**Msvm\_MountedStorageImage.DetachVirtualHardDisk**</span></span>](detachvirtualharddisk-msvm-mountedstorageimage.md)
</dt> <dt>

[<span data-ttu-id="75a6e-153">**Einbinden (v1)**</span><span class="sxs-lookup"><span data-stu-id="75a6e-153">**Mount (V1)**</span></span>](/previous-versions/windows/desktop/virtual/mount-msvm-imagemanagementservice)
</dt> <dt>

[<span data-ttu-id="75a6e-154">**MSVM \_ imagemanagementservice**</span><span class="sxs-lookup"><span data-stu-id="75a6e-154">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

