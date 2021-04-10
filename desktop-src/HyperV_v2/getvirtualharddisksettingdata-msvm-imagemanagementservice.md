---
description: Ruft die der virtuellen Festplatten Datei zugeordneten Einstellungsdaten ab.
ms.assetid: b82c018e-8d23-4615-99c1-3b622a8f41da
title: Getvirtualharddisksettingdata-Methode der Msvm_ImageManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVirtualHardDiskSettingData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: cf8f19d3bbdac593dabef0a1ff8e9c9b60027301
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958749"
---
# <a name="getvirtualharddisksettingdata-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="cddab-103">Getvirtualharddisksettingdata-Methode der MSVM \_ imagemanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="cddab-103">GetVirtualHardDiskSettingData method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="cddab-104">Ruft die der virtuellen Festplatten Datei zugeordneten Einstellungsdaten ab.</span><span class="sxs-lookup"><span data-stu-id="cddab-104">Retrieves the setting data associated with a virtual hard disk file.</span></span>

## <a name="syntax"></a><span data-ttu-id="cddab-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cddab-105">Syntax</span></span>


```mof
uint32 GetVirtualHardDiskSettingData(
  [in]  string              Path,
  [out] string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="cddab-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cddab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cddab-107">*Pfad* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cddab-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cddab-108">Der voll qualifizierte Pfad der Datenträger Image Datei.</span><span class="sxs-lookup"><span data-stu-id="cddab-108">The fully qualified path of the disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="cddab-109">*SettingData* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cddab-109">*SettingData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cddab-110">Bei erfolgreicher Ausführung empfängt eine eingebettete Instanz der [**MSVM-Klasse " \_ virtualharddisksettingdata**](msvm-virtualharddisksettingdata.md) ", die die Einstellungsdaten für die virtuelle Festplatte enthält.</span><span class="sxs-lookup"><span data-stu-id="cddab-110">If successful, receives an embedded instance of the [**Msvm\_VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) class that contains the setting data for the virtual hard disk.</span></span>

</dd> <dt>

<span data-ttu-id="cddab-111">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cddab-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cddab-112">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="cddab-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cddab-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cddab-113">Return value</span></span>

<span data-ttu-id="cddab-114">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="cddab-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="cddab-115">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="cddab-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cddab-116">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="cddab-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="cddab-117">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="cddab-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="cddab-118">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="cddab-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="cddab-119">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="cddab-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="cddab-120">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="cddab-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="cddab-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="cddab-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="cddab-122">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="cddab-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="cddab-123">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="cddab-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="cddab-124">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="cddab-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="cddab-125">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="cddab-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="cddab-126">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="cddab-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="cddab-127">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="cddab-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="cddab-128">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="cddab-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="cddab-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cddab-129">Remarks</span></span>

<span data-ttu-id="cddab-130">Der Zugriff auf die [**MSVM \_ imagemanagementservice**](msvm-imagemanagementservice.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="cddab-130">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="cddab-131">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="cddab-131">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="cddab-132">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cddab-132">Examples</span></span>

<span data-ttu-id="cddab-133">Im folgenden c#-Beispiel wird gezeigt, wie die [**getvirtualharddiskstate**](getvirtualharddiskstate-msvm-imagemanagementservice.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="cddab-133">The following C# example shows how to call the [**GetVirtualHardDiskState**](getvirtualharddiskstate-msvm-imagemanagementservice.md) method.</span></span> <span data-ttu-id="cddab-134">Die Dienstprogramme, auf die verwiesen wird, finden Sie unter [Allgemeine Hilfsprogramme für die Virtualisierungsbeispiele (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="cddab-134">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public static void GetVirtualHardDiskSettingData(string vhdPath)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");
    ManagementBaseObject inParams = imageService.GetMethodParameters("GetVirtualHardDiskSettingData");

    inParams["Path"] = vhdPath;

    ManagementBaseObject outParams = imageService.InvokeMethod("GetVirtualHardDiskSettingData", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("GetVirtualHardDiskSettingData was successful.");
        }
        else
        {
            Console.WriteLine("GetVirtualHardDiskSettingData was not successful.");
        }
    }
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        string diskStateString = outParams["SettingData"].ToString();
        Utility.PrintEmbeddedInstance(diskStateString);
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="cddab-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cddab-135">Requirements</span></span>



| <span data-ttu-id="cddab-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cddab-136">Requirement</span></span> | <span data-ttu-id="cddab-137">Wert</span><span class="sxs-lookup"><span data-stu-id="cddab-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cddab-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cddab-138">Minimum supported client</span></span><br/> | <span data-ttu-id="cddab-139">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cddab-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cddab-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cddab-140">Minimum supported server</span></span><br/> | <span data-ttu-id="cddab-141">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cddab-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cddab-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="cddab-142">Namespace</span></span><br/>                | <span data-ttu-id="cddab-143">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="cddab-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cddab-144">MOF</span><span class="sxs-lookup"><span data-stu-id="cddab-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cddab-145"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cddab-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cddab-146">DLL</span><span class="sxs-lookup"><span data-stu-id="cddab-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cddab-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cddab-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cddab-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cddab-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cddab-149">**MSVM \_ imagemanagementservice**</span><span class="sxs-lookup"><span data-stu-id="cddab-149">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

