---
description: Diese Klasse stellt einen Auftrag für den Export Vorgang eines virtuellen System-Referenz Punkts dar.
ms.assetid: 3d8e117c-4863-441a-9264-c33f05fbc5ef
title: Msvm_VirtualSystemReferencePointExportJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob
- Msvm_VirtualSystemReferencePointExportJob.Cancellable
- Msvm_VirtualSystemReferencePointExportJob.ErrorSummaryDescription
- Msvm_VirtualSystemReferencePointExportJob.ExportDirectory
- Msvm_VirtualSystemReferencePointExportJob.VirtualMachineId
- Msvm_VirtualSystemReferencePointExportJob.ReferencePointId
- Msvm_VirtualSystemReferencePointExportJob.BaseReferencePointId
- Msvm_VirtualSystemReferencePointExportJob.ExportedDisks
- Msvm_VirtualSystemReferencePointExportJob.ExportedLogFilePaths
- Msvm_VirtualSystemReferencePointExportJob.ExportedConfigFilePath
- Msvm_VirtualSystemReferencePointExportJob.ExportedRuntimeFilePath
- Msvm_VirtualSystemReferencePointExportJob.ExportedGuestStateFilePath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 04b5d8f27efae4817062917541af9bb488cec32c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530452"
---
# <a name="msvm_virtualsystemreferencepointexportjob-class"></a><span data-ttu-id="6ac78-103">MSVM \_ virtualsystemreferencepointexportjob-Klasse</span><span class="sxs-lookup"><span data-stu-id="6ac78-103">Msvm\_VirtualSystemReferencePointExportJob class</span></span>

<span data-ttu-id="6ac78-104">Diese Klasse stellt einen Auftrag für den Export Vorgang eines virtuellen System-Referenz Punkts dar.</span><span class="sxs-lookup"><span data-stu-id="6ac78-104">This class represents a virtual system reference point export operation job.</span></span>

<span data-ttu-id="6ac78-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6ac78-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ac78-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ac78-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePointExportJob : CIM_ConcreteJob
{
  boolean Cancellable;
  string  ErrorSummaryDescription;
  string  ExportDirectory;
  string  VirtualMachineId;
  string  ReferencePointId;
  string  BaseReferencePointId;
  string  ExportedDisks[];
  string  ExportedLogFilePaths[];
  string  ExportedConfigFilePath;
  string  ExportedRuntimeFilePath;
  string  ExportedGuestStateFilePath;
};
```

## <a name="members"></a><span data-ttu-id="6ac78-107">Member</span><span class="sxs-lookup"><span data-stu-id="6ac78-107">Members</span></span>

<span data-ttu-id="6ac78-108">Die **MSVM \_ virtualsystemreferencepointexportjob** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6ac78-108">The **Msvm\_VirtualSystemReferencePointExportJob** class has these types of members:</span></span>

-   [<span data-ttu-id="6ac78-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="6ac78-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="6ac78-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6ac78-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6ac78-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="6ac78-111">Methods</span></span>

<span data-ttu-id="6ac78-112">Die **MSVM \_ virtualsystemreferencepointexportjob** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="6ac78-112">The **Msvm\_VirtualSystemReferencePointExportJob** class has these methods.</span></span>



| <span data-ttu-id="6ac78-113">Methode</span><span class="sxs-lookup"><span data-stu-id="6ac78-113">Method</span></span>                                                                                     | <span data-ttu-id="6ac78-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ac78-114">Description</span></span>                                        |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------|
| [<span data-ttu-id="6ac78-115">**GetError**</span><span class="sxs-lookup"><span data-stu-id="6ac78-115">**GetError**</span></span>](msvm-virtualsystemreferencepointexportjob-geterror.md)                     | <span data-ttu-id="6ac78-116">Ruft den Fehler ab.</span><span class="sxs-lookup"><span data-stu-id="6ac78-116">Retrieves the error.</span></span><br/>                    |
| [<span data-ttu-id="6ac78-117">**Geterrorex**</span><span class="sxs-lookup"><span data-stu-id="6ac78-117">**GetErrorEx**</span></span>](msvm-virtualsystemreferencepointexportjob-geterrorex.md)                 | <span data-ttu-id="6ac78-118">Ruft zusätzliche Fehlerinformationen ab.</span><span class="sxs-lookup"><span data-stu-id="6ac78-118">Retrieves additional error information.</span></span><br/> |
| [<span data-ttu-id="6ac78-119">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="6ac78-119">**RequestStateChange**</span></span>](msvm-virtualsystemreferencepointexportjob-requeststatechange.md) | <span data-ttu-id="6ac78-120">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="6ac78-120">Requests a state change.</span></span><br/>                |



 

### <a name="properties"></a><span data-ttu-id="6ac78-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6ac78-121">Properties</span></span>

<span data-ttu-id="6ac78-122">Die **MSVM \_ virtualsystemreferencepointexportjob** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6ac78-122">The **Msvm\_VirtualSystemReferencePointExportJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6ac78-123">**Basereferencepointid**</span><span class="sxs-lookup"><span data-stu-id="6ac78-123">**BaseReferencePointId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ac78-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6ac78-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ac78-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6ac78-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ac78-126">GUID des Bezugspunkts, der als Basis im Export Vorgang verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ac78-126">GUID of the reference point which is used as the base in the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="6ac78-127">**Abbrechbar**</span><span class="sxs-lookup"><span data-stu-id="6ac78-127">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ac78-128">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="6ac78-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6ac78-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6ac78-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ac78-130">Gibt an, ob der Auftrag abgebrochen werden kann.</span><span class="sxs-lookup"><span data-stu-id="6ac78-130">Indicates whether the job can be cancelled.</span></span> <span data-ttu-id="6ac78-131">Der Wert dieser Eigenschaft garantiert nicht, dass eine Anforderung zum Abbrechen des Auftrags erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="6ac78-131">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="6ac78-132">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="6ac78-132">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ac78-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6ac78-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ac78-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6ac78-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ac78-135">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ Auftrag**](cim-job.md)".**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="6ac78-135">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="6ac78-136">Enthält eine Beschreibung der Fehler Zusammenfassung.</span><span class="sxs-lookup"><span data-stu-id="6ac78-136">Contains an error summary description.</span></span>

</dd> <dt>

<span data-ttu-id="6ac78-137">**Exportdirectory**</span><span class="sxs-lookup"><span data-stu-id="6ac78-137">**ExportDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ac78-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6ac78-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ac78-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6ac78-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ac78-140">Der Export Speicherort.</span><span class="sxs-lookup"><span data-stu-id="6ac78-140">The export location.</span></span>

</dd> <dt>

<span data-ttu-id="6ac78-141">**Exportedconfigfilepath**</span><span class="sxs-lookup"><span data-stu-id="6ac78-141">**ExportedConfigFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ac78-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6ac78-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ac78-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6ac78-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ac78-144">Der Pfad der exportierten Konfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="6ac78-144">Path of the exported config file.</span></span>

</dd> <dt>

<span data-ttu-id="6ac78-145">**Exporteddisks**</span><span class="sxs-lookup"><span data-stu-id="6ac78-145">**ExportedDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ac78-146">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="6ac78-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6ac78-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6ac78-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ac78-148">Instanz-IDs von virtuellen Datenträgern, für die Protokolldateien exportiert wurden.</span><span class="sxs-lookup"><span data-stu-id="6ac78-148">Instance IDs of virtual disks for which log files were exported.</span></span>

</dd> <dt>

<span data-ttu-id="6ac78-149">**Exportedgueststatefilepath**</span><span class="sxs-lookup"><span data-stu-id="6ac78-149">**ExportedGuestStateFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ac78-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6ac78-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ac78-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6ac78-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ac78-152">Der Pfad der exportierten Gast Zustands Datei.</span><span class="sxs-lookup"><span data-stu-id="6ac78-152">Path of the exported guest state file.</span></span>

> [!Note]  
> <span data-ttu-id="6ac78-153">Hinzugefügt in Windows 10, Version 1709.</span><span class="sxs-lookup"><span data-stu-id="6ac78-153">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="6ac78-154">**Exportedlogfilepath**</span><span class="sxs-lookup"><span data-stu-id="6ac78-154">**ExportedLogFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ac78-155">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="6ac78-155">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6ac78-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6ac78-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ac78-157">Pfade der Protokolldateien, die exportiert wurden.</span><span class="sxs-lookup"><span data-stu-id="6ac78-157">Paths of the log files which were exported.</span></span>

</dd> <dt>

<span data-ttu-id="6ac78-158">**Exportedruntimefilepath**</span><span class="sxs-lookup"><span data-stu-id="6ac78-158">**ExportedRuntimeFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ac78-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6ac78-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ac78-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6ac78-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ac78-161">Der Pfad der exportierten Lauf Zeit Zustands Datei.</span><span class="sxs-lookup"><span data-stu-id="6ac78-161">Path of the exported runtime state file.</span></span>

</dd> <dt>

<span data-ttu-id="6ac78-162">**Referencepointid**</span><span class="sxs-lookup"><span data-stu-id="6ac78-162">**ReferencePointId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ac78-163">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6ac78-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ac78-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6ac78-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ac78-165">GUID des Verweis Punkts, der exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="6ac78-165">GUID of the reference point which is exported.</span></span>

</dd> <dt>

<span data-ttu-id="6ac78-166">**Virtualmachineid**</span><span class="sxs-lookup"><span data-stu-id="6ac78-166">**VirtualMachineId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ac78-167">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6ac78-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ac78-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6ac78-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ac78-169">GUID des virtuellen Computers, für den Protokolldateien exportiert wurden.</span><span class="sxs-lookup"><span data-stu-id="6ac78-169">GUID of the virtual machine for which log files were exported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6ac78-170">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ac78-170">Requirements</span></span>



| <span data-ttu-id="6ac78-171">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ac78-171">Requirement</span></span> | <span data-ttu-id="6ac78-172">Wert</span><span class="sxs-lookup"><span data-stu-id="6ac78-172">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ac78-173">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6ac78-173">Minimum supported client</span></span><br/> | <span data-ttu-id="6ac78-174">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ac78-174">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6ac78-175">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6ac78-175">Minimum supported server</span></span><br/> | <span data-ttu-id="6ac78-176">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6ac78-176">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="6ac78-177">Namespace</span><span class="sxs-lookup"><span data-stu-id="6ac78-177">Namespace</span></span><br/>                | <span data-ttu-id="6ac78-178">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="6ac78-178">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6ac78-179">MOF</span><span class="sxs-lookup"><span data-stu-id="6ac78-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ac78-180"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6ac78-180"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ac78-181">DLL</span><span class="sxs-lookup"><span data-stu-id="6ac78-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ac78-182"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6ac78-182"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6ac78-183">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ac78-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ac78-184">**CIM- \_ concretejob**</span><span class="sxs-lookup"><span data-stu-id="6ac78-184">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> </dl>

 

