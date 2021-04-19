---
description: Erstellt eine Momentaufnahme eines virtuellen Systems.
ms.assetid: cad4cb4f-523f-4fda-ac88-8cece7abc227
title: Kreatesnapshot-Methode der CIM_VirtualSystemSnapshotService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ee96098477501123cffc1fd59a52734bbbea35d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356930"
---
# <a name="createsnapshot-method-of-the-cim_virtualsystemsnapshotservice-class"></a><span data-ttu-id="3ceea-103">Kreatesnapshot-Methode der CIM \_ virtualsystemsnapshotservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="3ceea-103">CreateSnapshot method of the CIM\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="3ceea-104">Erstellt eine Momentaufnahme eines virtuellen Systems.</span><span class="sxs-lookup"><span data-stu-id="3ceea-104">Creates a snapshot of a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ceea-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ceea-105">Syntax</span></span>


```mof
uint32 CreateSnapshot(
  [in]      CIM_ComputerSystem           REF AffectedSystem,
  [in]      string                           SnapshotSettings,
  [in]      uint16                           SnapshotType,
  [in, out] CIM_VirtualSystemSettingData REF ResultingSnapshot,
  [out]     CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3ceea-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ceea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ceea-107">*Affectedsystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ceea-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ceea-108">Ein [**CIM \_ Computersystem**](cim-computersystem.md) -Verweis auf das betroffene virtuelle System.</span><span class="sxs-lookup"><span data-stu-id="3ceea-108">A [**CIM\_ComputerSystem**](cim-computersystem.md) reference to the affected virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="3ceea-109">*Snapshotsettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ceea-109">*SnapshotSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ceea-110">Parameter Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="3ceea-110">Parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="3ceea-111">*Snapshottype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ceea-111">*SnapshotType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ceea-112">Angeforderter snapshottyp:</span><span class="sxs-lookup"><span data-stu-id="3ceea-112">Requested snapshot type:</span></span>

<dt>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>

<span data-ttu-id="3ceea-113"><span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Vollständige Momentaufnahme** (2)</span><span class="sxs-lookup"><span data-stu-id="3ceea-113"><span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Full Snapshot** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3ceea-114">Vervollständigen Sie die Momentaufnahme des virtuellen Systems.</span><span class="sxs-lookup"><span data-stu-id="3ceea-114">Complete snapshot of the virtual system.</span></span>

</dd> <dt>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>

<span data-ttu-id="3ceea-115"><span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>Datenträger **Momentaufnahme** (3)</span><span class="sxs-lookup"><span data-stu-id="3ceea-115"><span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**Disk Snapshot** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3ceea-116">Momentaufnahme von virtuellen System Datenträgern.</span><span class="sxs-lookup"><span data-stu-id="3ceea-116">Snapshot of virtual system disks.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3ceea-117"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="3ceea-117"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="3ceea-118"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="3ceea-118"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="3ceea-119">*Resultingsnapshot* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3ceea-119">*ResultingSnapshot* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ceea-120">Ein [**CIM \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md) -Verweis auf die resultierende virtuelle System Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="3ceea-120">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) reference to the resulting virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="3ceea-121">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3ceea-121">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ceea-122">Wenn der Vorgang lange ausgeführt wird, kann optional ein Auftrag zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3ceea-122">If the operation is long running, then optionally a job may be returned.</span></span> <span data-ttu-id="3ceea-123">In diesem Fall gilt: die Instanz der [**CIM \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md) -Klasse, die die neue Momentaufnahme des virtuellen Systems darstellt, wird über die [**CIM \_ affectedjobelate**](cim-affectedjobelement.md) -Zuordnung mit dem Wert der **affectedelta** -Eigenschaft präsentiert, die auf die neue Instanz der **CIM \_ virtualsystemsettingdata** -Klasse verweist, die  die Momentaufnahme des virtuellen Systems darstellt</span><span class="sxs-lookup"><span data-stu-id="3ceea-123">In this case, the instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing the new virtual system snapshot is presented via the [**CIM\_AffectedJobElement**](cim-affectedjobelement.md) association with the value of the **AffectedElement** property referring to the new instance of the **CIM\_VirtualSystemSettingData** class representing the virtual system snapshot and the value of the **ElementEffects** set to 5 (Create).</span></span>

> [!Note]  
> <span data-ttu-id="3ceea-124">Dieser Parameter war in Windows 8.1 mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="3ceea-124">This parameter was read/write in Windows 8.1.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ceea-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3ceea-125">Return value</span></span>

<span data-ttu-id="3ceea-126">Bei Erfolg wird 0 zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3ceea-126">On success, returns 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="3ceea-127">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="3ceea-127">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3ceea-128">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="3ceea-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3ceea-129">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="3ceea-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3ceea-130">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="3ceea-130">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3ceea-131">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="3ceea-131">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3ceea-132">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="3ceea-132">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3ceea-133">**Ungültiger Typ** (6)</span><span class="sxs-lookup"><span data-stu-id="3ceea-133">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3ceea-134">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="3ceea-134">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3ceea-135">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="3ceea-135">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3ceea-136">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="3ceea-136">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="3ceea-137">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="3ceea-137">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3ceea-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3ceea-138">Requirements</span></span>



| <span data-ttu-id="3ceea-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3ceea-139">Requirement</span></span> | <span data-ttu-id="3ceea-140">Wert</span><span class="sxs-lookup"><span data-stu-id="3ceea-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ceea-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3ceea-141">Minimum supported client</span></span><br/> | <span data-ttu-id="3ceea-142">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="3ceea-142">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="3ceea-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3ceea-143">Minimum supported server</span></span><br/> | <span data-ttu-id="3ceea-144">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3ceea-144">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="3ceea-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="3ceea-145">Namespace</span></span><br/>                | <span data-ttu-id="3ceea-146">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="3ceea-146">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3ceea-147">MOF</span><span class="sxs-lookup"><span data-stu-id="3ceea-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ceea-148"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3ceea-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ceea-149">DLL</span><span class="sxs-lookup"><span data-stu-id="3ceea-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ceea-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3ceea-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3ceea-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ceea-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ceea-152">**CIM \_ virtualsystemsnapshotservice**</span><span class="sxs-lookup"><span data-stu-id="3ceea-152">**CIM\_VirtualSystemSnapshotService**</span></span>](cim-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




