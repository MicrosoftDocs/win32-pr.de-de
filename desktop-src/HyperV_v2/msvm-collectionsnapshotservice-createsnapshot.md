---
description: Erstellt eine Momentaufnahme einer virtuellen System Sammlung.
ms.assetid: 2512d82f-06b9-4613-b920-d3a9be884a75
title: Kreatesnapshot-Methode der Msvm_CollectionSnapshotService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 653dae65cc5fe50416b069da6a66e8c678c1b512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755153"
---
# <a name="createsnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="76694-103">Die Methode "kreatesnapshot" der Klasse "MSVM \_ collectionsnapshotservice"</span><span class="sxs-lookup"><span data-stu-id="76694-103">CreateSnapshot method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="76694-104">Erstellt eine Momentaufnahme einer virtuellen System Sammlung.</span><span class="sxs-lookup"><span data-stu-id="76694-104">Creates a snapshot of a virtual system collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="76694-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="76694-105">Syntax</span></span>


```mof
uint32 CreateSnapshot(
  [in]      CIM_CollectionOfMSEs REF Collection,
  [in]      string                   SnapshotSettings,
  [in]      uint16                   SnapshotType,
  [in, out] CIM_Collection       REF ResultingSnapshotCollection,
  [out]     CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="76694-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="76694-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76694-107">*Sammlung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76694-107">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76694-108">Verweis auf einen [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) , der die betroffene Sammlung virtueller Systeme beschreibt.</span><span class="sxs-lookup"><span data-stu-id="76694-108">Reference to a [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) that describes the affected virtual system collection.</span></span>

</dd> <dt>

<span data-ttu-id="76694-109">*Snapshotsettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76694-109">*SnapshotSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76694-110">Enthält die Parametereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="76694-110">Contains the parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="76694-111">*Snapshottype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76694-111">*SnapshotType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76694-112">Angeforderter snapshottyp:</span><span class="sxs-lookup"><span data-stu-id="76694-112">Requested snapshot type:</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="76694-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="76694-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>

<span data-ttu-id="76694-114"><span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>**Standard Momentaufnahme** (1)</span><span class="sxs-lookup"><span data-stu-id="76694-114"><span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>**Standard Snapshot** (1)</span></span>


</dt> <dd>

<span data-ttu-id="76694-115">Standard Momentaufnahme des virtuellen Systems.</span><span class="sxs-lookup"><span data-stu-id="76694-115">Standard snapshot of the virtual system.</span></span>

</dd> <dt>

<span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>

<span data-ttu-id="76694-116"><span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>**Wiederherstellungs Momentaufnahme** (2)</span><span class="sxs-lookup"><span data-stu-id="76694-116"><span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>**Recovery Snapshot** (2)</span></span>


</dt> <dd>

<span data-ttu-id="76694-117">Momentaufnahme für Wiederherstellungs Szenarien, einschließlich failoverreplikation und Sicherung.</span><span class="sxs-lookup"><span data-stu-id="76694-117">Snapshot for recovery scenarios including failover replication and backup.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="76694-118"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="76694-118"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="76694-119"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="76694-119"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="76694-120">*Resultingsnapshotcollection* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="76694-120">*ResultingSnapshotCollection* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="76694-121">Bei Erfolg wird ein [**CIM- \_ Sammlungs**](cim-collection.md) Verweis mit der Momentaufnahme des virtuellen Systems zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="76694-121">On success, returns a [**CIM\_Collection**](cim-collection.md) reference containing the virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="76694-122">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="76694-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76694-123">Ein optionaler Verweis, der zurückgegeben wird, wenn der Vorgang asynchron ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76694-123">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="76694-124">Falls vorhanden, kann der zurückgegebene Verweis auf eine Instanz von [**CIM \_ concretejob**](cim-concretejob.md) verwendet werden, um den Fortschritt zu überwachen und das Ergebnis der Methode abzurufen.</span><span class="sxs-lookup"><span data-stu-id="76694-124">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76694-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="76694-125">Return value</span></span>

<span data-ttu-id="76694-126">Bei Erfolg wird entweder 0 (abgeschlossen) oder 4096 (Auftrag gestartet) zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="76694-126">On success, returns either 0 (Complete) or 4096 (Job Started); otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="76694-127">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="76694-127">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="76694-128">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="76694-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="76694-129">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="76694-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="76694-130">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="76694-130">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="76694-131">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="76694-131">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="76694-132">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="76694-132">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="76694-133">**Ungültiger Typ** (6)</span><span class="sxs-lookup"><span data-stu-id="76694-133">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="76694-134">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="76694-134">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="76694-135">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="76694-135">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="76694-136">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="76694-136">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="76694-137">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="76694-137">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="76694-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76694-138">Requirements</span></span>



| <span data-ttu-id="76694-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76694-139">Requirement</span></span> | <span data-ttu-id="76694-140">Wert</span><span class="sxs-lookup"><span data-stu-id="76694-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76694-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="76694-141">Minimum supported client</span></span><br/> | <span data-ttu-id="76694-142">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76694-142">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="76694-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="76694-143">Minimum supported server</span></span><br/> | <span data-ttu-id="76694-144">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="76694-144">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="76694-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="76694-145">Namespace</span></span><br/>                | <span data-ttu-id="76694-146">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="76694-146">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="76694-147">MOF</span><span class="sxs-lookup"><span data-stu-id="76694-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="76694-148"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="76694-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="76694-149">DLL</span><span class="sxs-lookup"><span data-stu-id="76694-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76694-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="76694-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="76694-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76694-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76694-152">**MSVM \_ collectionsnapshotservice**</span><span class="sxs-lookup"><span data-stu-id="76694-152">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




