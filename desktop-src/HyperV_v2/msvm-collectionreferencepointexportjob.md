---
description: Diese Klasse stellt einen Sammlungs Referenz-Export Vorgangs Auftrag dar.
ms.assetid: c752ff1d-163c-4aa9-b29e-76478a18a08c
title: Msvm_CollectionReferencePointExportJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob
- Msvm_CollectionReferencePointExportJob.Cancellable
- Msvm_CollectionReferencePointExportJob.ErrorSummaryDescription
- Msvm_CollectionReferencePointExportJob.CollectionId
- Msvm_CollectionReferencePointExportJob.ReferencePointGroupId
- Msvm_CollectionReferencePointExportJob.BaseReferencePointGroupId
- Msvm_CollectionReferencePointExportJob.VirtualMachineId
- Msvm_CollectionReferencePointExportJob.ExportDirectory
- Msvm_CollectionReferencePointExportJob.ExportedDisks
- Msvm_CollectionReferencePointExportJob.ExportedLogFilePaths
- Msvm_CollectionReferencePointExportJob.ExportedConfigFilePaths
- Msvm_CollectionReferencePointExportJob.ExportedRuntimeFilePaths
- Msvm_CollectionReferencePointExportJob.ExportedGuestStateFilePaths
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d21fab1519664471bdc2bb5d7102d94cbe3dde1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349718"
---
# <a name="msvm_collectionreferencepointexportjob-class"></a><span data-ttu-id="8d16f-103">MSVM \_ collectionreferencepointexportjob-Klasse</span><span class="sxs-lookup"><span data-stu-id="8d16f-103">Msvm\_CollectionReferencePointExportJob class</span></span>

<span data-ttu-id="8d16f-104">Diese Klasse stellt einen Sammlungs Referenz-Export Vorgangs Auftrag dar.</span><span class="sxs-lookup"><span data-stu-id="8d16f-104">This class represents a collection reference point export operation job.</span></span>

<span data-ttu-id="8d16f-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8d16f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d16f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d16f-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionReferencePointExportJob : CIM_ConcreteJob
{
  boolean Cancellable;
  string  ErrorSummaryDescription;
  string  CollectionId;
  string  ReferencePointGroupId;
  string  BaseReferencePointGroupId;
  string  VirtualMachineId[];
  string  ExportDirectory;
  string  ExportedDisks[];
  string  ExportedLogFilePaths[];
  string  ExportedConfigFilePaths[];
  string  ExportedRuntimeFilePaths[];
  string  ExportedGuestStateFilePaths[];
};
```

## <a name="members"></a><span data-ttu-id="8d16f-107">Member</span><span class="sxs-lookup"><span data-stu-id="8d16f-107">Members</span></span>

<span data-ttu-id="8d16f-108">Die **MSVM \_ collectionreferencepointexportjob** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8d16f-108">The **Msvm\_CollectionReferencePointExportJob** class has these types of members:</span></span>

-   [<span data-ttu-id="8d16f-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="8d16f-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="8d16f-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8d16f-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8d16f-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="8d16f-111">Methods</span></span>

<span data-ttu-id="8d16f-112">Die **MSVM \_ collectionreferencepointexportjob** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="8d16f-112">The **Msvm\_CollectionReferencePointExportJob** class has these methods.</span></span>



| <span data-ttu-id="8d16f-113">Methode</span><span class="sxs-lookup"><span data-stu-id="8d16f-113">Method</span></span>                                                                                  | <span data-ttu-id="8d16f-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8d16f-114">Description</span></span>                                        |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------|
| [<span data-ttu-id="8d16f-115">**GetError**</span><span class="sxs-lookup"><span data-stu-id="8d16f-115">**GetError**</span></span>](msvm-collectionreferencepointexportjob-geterror.md)                     | <span data-ttu-id="8d16f-116">Ruft einen Fehler ab.</span><span class="sxs-lookup"><span data-stu-id="8d16f-116">Retrieves an error.</span></span><br/>                     |
| [<span data-ttu-id="8d16f-117">**Geterrorex**</span><span class="sxs-lookup"><span data-stu-id="8d16f-117">**GetErrorEx**</span></span>](msvm-collectionreferencepointexportjob-geterrorex.md)                 | <span data-ttu-id="8d16f-118">Ruft zusätzliche Fehlerinformationen ab.</span><span class="sxs-lookup"><span data-stu-id="8d16f-118">Retrieves additional error information.</span></span><br/> |
| [<span data-ttu-id="8d16f-119">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="8d16f-119">**RequestStateChange**</span></span>](msvm-collectionreferencepointexportjob-requeststatechange.md) | <span data-ttu-id="8d16f-120">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="8d16f-120">Requests a state change.</span></span><br/>                |



 

### <a name="properties"></a><span data-ttu-id="8d16f-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8d16f-121">Properties</span></span>

<span data-ttu-id="8d16f-122">Die **MSVM \_ collectionreferencepointexportjob** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8d16f-122">The **Msvm\_CollectionReferencePointExportJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8d16f-123">**Basereferencepointgroupid**</span><span class="sxs-lookup"><span data-stu-id="8d16f-123">**BaseReferencePointGroupId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d16f-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8d16f-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d16f-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8d16f-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d16f-126">GUID des Auflistungs Verweis Punkts, der als Basis in "Exportoperation" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8d16f-126">GUID of the collection reference point which is used as the base in the exportoperation.</span></span>

</dd> <dt>

<span data-ttu-id="8d16f-127">**Abbrechbar**</span><span class="sxs-lookup"><span data-stu-id="8d16f-127">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d16f-128">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8d16f-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8d16f-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8d16f-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d16f-130">Gibt an, ob der Auftrag abgebrochen werden kann.</span><span class="sxs-lookup"><span data-stu-id="8d16f-130">Indicates whether the job can be cancelled.</span></span> <span data-ttu-id="8d16f-131">Der Wert dieser Eigenschaft garantiert nicht, dass eine Anforderung zum Abbrechen des Auftrags erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="8d16f-131">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="8d16f-132">**Sammlungs**</span><span class="sxs-lookup"><span data-stu-id="8d16f-132">**CollectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d16f-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8d16f-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d16f-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8d16f-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d16f-135">GUID der virtuellen Computergruppe, für die Protokolldateien wereexportiert werden.</span><span class="sxs-lookup"><span data-stu-id="8d16f-135">GUID of the virtual machine group for which log files wereexported.</span></span>

</dd> <dt>

<span data-ttu-id="8d16f-136">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="8d16f-136">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d16f-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8d16f-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d16f-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8d16f-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d16f-139">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ Auftrag**](cim-job.md)".**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="8d16f-139">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="8d16f-140">Enthält eine Beschreibung der Fehler Zusammenfassung.</span><span class="sxs-lookup"><span data-stu-id="8d16f-140">Contains an error summary description.</span></span>

</dd> <dt>

<span data-ttu-id="8d16f-141">**Exportdirectory**</span><span class="sxs-lookup"><span data-stu-id="8d16f-141">**ExportDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d16f-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8d16f-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d16f-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8d16f-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d16f-144">Export Speicherort.</span><span class="sxs-lookup"><span data-stu-id="8d16f-144">Export Location.</span></span>

</dd> <dt>

<span data-ttu-id="8d16f-145">**Exportedconfigfilepath**</span><span class="sxs-lookup"><span data-stu-id="8d16f-145">**ExportedConfigFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d16f-146">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="8d16f-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8d16f-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8d16f-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d16f-148">Pfad der exportierten Konfigurationsdatei des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="8d16f-148">Path of the exported virtual machine config file.</span></span>

</dd> <dt>

<span data-ttu-id="8d16f-149">**Exporteddisks**</span><span class="sxs-lookup"><span data-stu-id="8d16f-149">**ExportedDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d16f-150">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="8d16f-150">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8d16f-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8d16f-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d16f-152">Instanz-IDs von virtuellen Datenträgern, für die Protokolldateien exportiert wurden.</span><span class="sxs-lookup"><span data-stu-id="8d16f-152">Instance IDs of virtual disks for which log files were exported.</span></span>

</dd> <dt>

<span data-ttu-id="8d16f-153">**Exportedgueststatefilepath**</span><span class="sxs-lookup"><span data-stu-id="8d16f-153">**ExportedGuestStateFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d16f-154">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="8d16f-154">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8d16f-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8d16f-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d16f-156">Pfad der exportierten Gast Zustands Datei der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="8d16f-156">Path of the exported virtual machine guest state file.</span></span>

> [!Note]  
> <span data-ttu-id="8d16f-157">Hinzugefügt in Windows 10, Version 1709.</span><span class="sxs-lookup"><span data-stu-id="8d16f-157">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="8d16f-158">**Exportedlogfilepath**</span><span class="sxs-lookup"><span data-stu-id="8d16f-158">**ExportedLogFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d16f-159">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="8d16f-159">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8d16f-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8d16f-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d16f-161">Pfade der Protokolldateien, die exportiert wurden.</span><span class="sxs-lookup"><span data-stu-id="8d16f-161">Paths of the log files which were exported.</span></span>

</dd> <dt>

<span data-ttu-id="8d16f-162">**Exportedruntimefilepath**</span><span class="sxs-lookup"><span data-stu-id="8d16f-162">**ExportedRuntimeFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d16f-163">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="8d16f-163">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8d16f-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8d16f-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d16f-165">Pfad der exportierten Lauf Zeit Zustands Datei des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="8d16f-165">Path of the exported virtual machine runtime state file.</span></span>

</dd> <dt>

<span data-ttu-id="8d16f-166">**Referencepointgroupid**</span><span class="sxs-lookup"><span data-stu-id="8d16f-166">**ReferencePointGroupId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d16f-167">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8d16f-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d16f-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8d16f-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d16f-169">GUID des Sammlungs Verweis Punkts, der exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="8d16f-169">GUID of the collection reference point which is exported.</span></span>

</dd> <dt>

<span data-ttu-id="8d16f-170">**Virtualmachineid**</span><span class="sxs-lookup"><span data-stu-id="8d16f-170">**VirtualMachineId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d16f-171">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="8d16f-171">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8d16f-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8d16f-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d16f-173">GUID der virtuellen Computer, für die der Export Vorgang durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="8d16f-173">GUID of the virtual machines for which export operation has been performed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8d16f-174">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8d16f-174">Requirements</span></span>



| <span data-ttu-id="8d16f-175">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8d16f-175">Requirement</span></span> | <span data-ttu-id="8d16f-176">Wert</span><span class="sxs-lookup"><span data-stu-id="8d16f-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d16f-177">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8d16f-177">Minimum supported client</span></span><br/> | <span data-ttu-id="8d16f-178">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8d16f-178">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8d16f-179">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8d16f-179">Minimum supported server</span></span><br/> | <span data-ttu-id="8d16f-180">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8d16f-180">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="8d16f-181">Namespace</span><span class="sxs-lookup"><span data-stu-id="8d16f-181">Namespace</span></span><br/>                | <span data-ttu-id="8d16f-182">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="8d16f-182">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8d16f-183">MOF</span><span class="sxs-lookup"><span data-stu-id="8d16f-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d16f-184"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8d16f-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8d16f-185">DLL</span><span class="sxs-lookup"><span data-stu-id="8d16f-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d16f-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8d16f-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8d16f-187">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d16f-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d16f-188">**CIM- \_ concretejob**</span><span class="sxs-lookup"><span data-stu-id="8d16f-188">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> </dl>

 

