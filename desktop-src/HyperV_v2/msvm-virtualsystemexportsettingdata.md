---
description: Bietet zusätzliche Informationen, die mit der exportsystemdefinition-Methode der MSVM \_ virtualsystemmanagementservice-Klasse verwendet werden können.
ms.assetid: 86396A76-83EC-476E-86A9-83861A002152
title: Msvm_VirtualSystemExportSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemExportSettingData
- Msvm_VirtualSystemExportSettingData.CaptureLiveState
- Msvm_VirtualSystemExportSettingData.InstanceID
- Msvm_VirtualSystemExportSettingData.Caption
- Msvm_VirtualSystemExportSettingData.Description
- Msvm_VirtualSystemExportSettingData.ElementName
- Msvm_VirtualSystemExportSettingData.CopySnapshotConfiguration
- Msvm_VirtualSystemExportSettingData.CopyVmRuntimeInformation
- Msvm_VirtualSystemExportSettingData.CopyVmStorage
- Msvm_VirtualSystemExportSettingData.CreateVmExportSubdirectory
- Msvm_VirtualSystemExportSettingData.SnapshotVirtualSystem
- Msvm_VirtualSystemExportSettingData.BackupIntent
- Msvm_VirtualSystemExportSettingData.ExportForLiveMigration
- Msvm_VirtualSystemExportSettingData.DisableDifferentialOfIgnoredStorage
- Msvm_VirtualSystemExportSettingData.ExcludedVirtualHardDisks
- Msvm_VirtualSystemExportSettingData.DifferentialBackupBase
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 77bd451912063ec1164abf14247d81e1d258f56f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344407"
---
# <a name="msvm_virtualsystemexportsettingdata-class"></a><span data-ttu-id="5a01d-103">MSVM \_ virtualsystemexportsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="5a01d-103">Msvm\_VirtualSystemExportSettingData class</span></span>

<span data-ttu-id="5a01d-104">Bietet zusätzliche Informationen, die mit der [**exportsystemdefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="5a01d-104">Provides additional information to be used with the [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="5a01d-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5a01d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a01d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a01d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemExportSettingData : CIM_SettingData
{
  uint8   CaptureLiveState;
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  uint8   CopySnapshotConfiguration;
  boolean CopyVmRuntimeInformation;
  boolean CopyVmStorage;
  boolean CreateVmExportSubdirectory;
  string  SnapshotVirtualSystem;
  uint8   BackupIntent;
  boolean ExportForLiveMigration;
  boolean DisableDifferentialOfIgnoredStorage;
  string  ExcludedVirtualHardDisks[];
  string  DifferentialBackupBase;
};
```

## <a name="members"></a><span data-ttu-id="5a01d-107">Member</span><span class="sxs-lookup"><span data-stu-id="5a01d-107">Members</span></span>

<span data-ttu-id="5a01d-108">Die **MSVM \_ virtualsystemexportsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5a01d-108">The **Msvm\_VirtualSystemExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="5a01d-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5a01d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5a01d-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5a01d-110">Properties</span></span>

<span data-ttu-id="5a01d-111">Die **MSVM \_ virtualsystemexportsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5a01d-111">The **Msvm\_VirtualSystemExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5a01d-112">**Backupintent**</span><span class="sxs-lookup"><span data-stu-id="5a01d-112">**BackupIntent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a01d-113">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="5a01d-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="5a01d-114">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5a01d-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5a01d-115">Gibt die Absicht an, wie die exportierten Sicherungs Sätze verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5a01d-115">Indicates the intent on how the exported backup sets would be used.</span></span>

> [!Note]  
> <span data-ttu-id="5a01d-116">Diese Eigenschaft wurde in Windows 10 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5a01d-116">This property was added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>

<span data-ttu-id="5a01d-117"><span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**Backupintentpreservechain** (0)</span><span class="sxs-lookup"><span data-stu-id="5a01d-117"><span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (0)</span></span>


</dt> <dd>

<span data-ttu-id="5a01d-118">Alle exportierten vollständigen und differenziellen Sicherungs Sätze werden unverändert beibehalten.</span><span class="sxs-lookup"><span data-stu-id="5a01d-118">All exported full and differential backup sets would be preserved as they are.</span></span>

</dd> <dt>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>

<span data-ttu-id="5a01d-119"><span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**Backupintentmerge** (1)</span><span class="sxs-lookup"><span data-stu-id="5a01d-119"><span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5a01d-120">Die exportierten vollständigen und differenziellen Sicherungs Sätze werden zusammengeführt, um vollständige Sicherungs Sätze zu synthetisieren.</span><span class="sxs-lookup"><span data-stu-id="5a01d-120">The exported full and differential backup sets would be merged to synthesize full backup sets.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5a01d-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5a01d-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a01d-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5a01d-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a01d-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5a01d-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a01d-124">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="5a01d-124">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="5a01d-125">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="5a01d-125">A short description of the object.</span></span> <span data-ttu-id="5a01d-126">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5a01d-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5a01d-127">**Capturelivestate**</span><span class="sxs-lookup"><span data-stu-id="5a01d-127">**CaptureLiveState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a01d-128">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="5a01d-128">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="5a01d-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5a01d-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5a01d-130">Gibt an, welcher Zustand erfasst werden soll, wenn das Ziel des Exports eine laufende VM ist.</span><span class="sxs-lookup"><span data-stu-id="5a01d-130">Indicates what state to capture if the target of the export is a running VM.</span></span>

<dt>

<span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>

<span data-ttu-id="5a01d-131"><span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>**Capturecrashkonsistentstate** (0)</span><span class="sxs-lookup"><span data-stu-id="5a01d-131"><span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>**CaptureCrashConsistentState** (0)</span></span>


</dt> <dd>

<span data-ttu-id="5a01d-132">Es werden keine gespeicherten Zustands Dateien für die laufende VM exportiert, sodass Sie in einen Absturz konsistenten Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="5a01d-132">No saved state files will be exported for the running VM, placing it in a crash consistent state.</span></span>

</dd> <dt>

<span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>

<span data-ttu-id="5a01d-133"><span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>**Capturesavedstate** (1)</span><span class="sxs-lookup"><span data-stu-id="5a01d-133"><span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>**CaptureSavedState** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5a01d-134">Gespeicherte Zustands Dateien für die laufende VM werden zusammen mit der VM-Konfiguration exportiert.</span><span class="sxs-lookup"><span data-stu-id="5a01d-134">Saved state files for the running VM will be exported along with the VM configuration.</span></span>

</dd> <dt>

<span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>

<span data-ttu-id="5a01d-135"><span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>**Captureappkonsistentstate** (2)</span><span class="sxs-lookup"><span data-stu-id="5a01d-135"><span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>**CaptureAppConsistentState** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5a01d-136">Der Anwendungs konsistente Zustand des laufenden virtuellen Computers wird exportiert.</span><span class="sxs-lookup"><span data-stu-id="5a01d-136">Application-consistent state of the running VM will be exported.</span></span>

> [!Note]  
> <span data-ttu-id="5a01d-137">In Windows 10 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5a01d-137">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5a01d-138">**Copysnapshotconfiguration**</span><span class="sxs-lookup"><span data-stu-id="5a01d-138">**CopySnapshotConfiguration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a01d-139">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="5a01d-139">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="5a01d-140">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5a01d-140">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5a01d-141">Gibt an, welche Momentaufnahmen mit dem virtuellen Computer exportiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5a01d-141">Indicates what snapshots are to be exported with the virtual machine.</span></span>

<dt>

<span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>

<span data-ttu-id="5a01d-142"><span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>**Exportallshots** (0)</span><span class="sxs-lookup"><span data-stu-id="5a01d-142"><span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>**ExportAllSnapshots** (0)</span></span>


</dt> <dd>

<span data-ttu-id="5a01d-143">Alle Momentaufnahmen werden mit dem virtuellen Computer exportiert.</span><span class="sxs-lookup"><span data-stu-id="5a01d-143">All snapshots will be exported with the virtual machine.</span></span>

</dd> <dt>

<span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>

<span data-ttu-id="5a01d-144"><span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>**Exportnomomentaufnahmen** (1)</span><span class="sxs-lookup"><span data-stu-id="5a01d-144"><span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>**ExportNoSnapshots** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5a01d-145">Es werden keine Momentaufnahmen mit dem virtuellen Computer exportiert.</span><span class="sxs-lookup"><span data-stu-id="5a01d-145">No snapshots will be exported with the virtual machine.</span></span>

</dd> <dt>

<span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>

<span data-ttu-id="5a01d-146"><span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>**Exportonesnapshot** (2)</span><span class="sxs-lookup"><span data-stu-id="5a01d-146"><span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>**ExportOneSnapshot** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5a01d-147">Die von der Eigenschaft **snapshotvirtualsystem** identifizierten Momentaufnahmen werden mit der virtuellen Maschine exportiert.</span><span class="sxs-lookup"><span data-stu-id="5a01d-147">The snapshots identified by the **SnapshotVirtualSystem** property will be exported with the virtual machine.</span></span> <span data-ttu-id="5a01d-148">Die Eigenschaften **copyvmstorage** und **copyvmruntimeinformation** werden ignoriert, Speicher-und Laufzeitinformationen werden mit dem virtuellen Computer exportiert, und alle differenzierenden VHD-Datenträger werden in eine neue VHD zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="5a01d-148">The **CopyVmStorage** and **CopyVmRuntimeInformation** properties are ignored, storage and run-time information is exported with the virtual machine, and any VHD differencing disks will be merged into a new VHD.</span></span>

</dd> <dt>

<span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>

<span data-ttu-id="5a01d-149"><span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>**Exportonesnapshotforbackup** (3)</span><span class="sxs-lookup"><span data-stu-id="5a01d-149"><span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>**ExportOneSnapshotForBackup** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5a01d-150">Die von der **snapshotvirtualsystem** -Eigenschaft identifizierte Momentaufnahme wird zum Zweck der Sicherung des virtuellen Computers exportiert.</span><span class="sxs-lookup"><span data-stu-id="5a01d-150">The snapshot identified by the **SnapshotVirtualSystem** property will be exported for the purpose of backing up the VM.</span></span> <span data-ttu-id="5a01d-151">Die exportierte Konfiguration verwendet die ID der VM.</span><span class="sxs-lookup"><span data-stu-id="5a01d-151">The exported configuration will use ID of the VM.</span></span>

> [!Note]  
> <span data-ttu-id="5a01d-152">In Windows 10 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5a01d-152">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5a01d-153">**Copyvmruntimeinformation**</span><span class="sxs-lookup"><span data-stu-id="5a01d-153">**CopyVmRuntimeInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a01d-154">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5a01d-154">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a01d-155">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5a01d-155">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5a01d-156">Gibt an, ob die Laufzeitinformationen des virtuellen Computers beim Exportieren der virtuellen Maschine kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="5a01d-156">Indicates whether the virtual machine run-time information will be copied when the virtual machine is exported.</span></span>



| <span data-ttu-id="5a01d-157">Wert</span><span class="sxs-lookup"><span data-stu-id="5a01d-157">Value</span></span>                                                                                | <span data-ttu-id="5a01d-158">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5a01d-158">Meaning</span></span>                                                                 |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5a01d-159"><dt>**Fall**</dt></span><span class="sxs-lookup"><span data-stu-id="5a01d-159"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="5a01d-160">Die Laufzeitinformationen der virtuellen Maschine werden kopiert.</span><span class="sxs-lookup"><span data-stu-id="5a01d-160">The virtual machine run-time information will be copied.</span></span><br/>     |
| <dl> <span data-ttu-id="5a01d-161"><dt>**False**</dt></span><span class="sxs-lookup"><span data-stu-id="5a01d-161"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="5a01d-162">Die Laufzeitinformationen für den virtuellen Computer werden nicht kopiert.</span><span class="sxs-lookup"><span data-stu-id="5a01d-162">The virtual machine run-time information will not be copied.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5a01d-163">**Copyvmstorage**</span><span class="sxs-lookup"><span data-stu-id="5a01d-163">**CopyVmStorage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a01d-164">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5a01d-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a01d-165">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5a01d-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5a01d-166">Gibt an, ob der Speicher der virtuellen Maschine beim Exportieren der virtuellen Maschine kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="5a01d-166">Indicates whether the virtual machine storage will be copied when the virtual machine is exported.</span></span>



| <span data-ttu-id="5a01d-167">Wert</span><span class="sxs-lookup"><span data-stu-id="5a01d-167">Value</span></span>                                                                                | <span data-ttu-id="5a01d-168">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5a01d-168">Meaning</span></span>                                                    |
|--------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="5a01d-169"><dt>**Fall**</dt></span><span class="sxs-lookup"><span data-stu-id="5a01d-169"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="5a01d-170">Der Speicher der virtuellen Maschine wird kopiert.</span><span class="sxs-lookup"><span data-stu-id="5a01d-170">The virtual machine storage will be copied.</span></span><br/>     |
| <dl> <span data-ttu-id="5a01d-171"><dt>**False**</dt></span><span class="sxs-lookup"><span data-stu-id="5a01d-171"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="5a01d-172">Der Speicher des virtuellen Computers wird nicht kopiert.</span><span class="sxs-lookup"><span data-stu-id="5a01d-172">The virtual machine storage will not be copied.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5a01d-173">**"Kreatevmexportsubdirectory"**</span><span class="sxs-lookup"><span data-stu-id="5a01d-173">**CreateVmExportSubdirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a01d-174">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5a01d-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a01d-175">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5a01d-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5a01d-176">Gibt an, ob beim Exportieren der virtuellen Maschine ein Unterverzeichnis mit dem Namen der virtuellen Maschine erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="5a01d-176">Indicates whether a subdirectory with the name of the virtual machine will be created when the virtual machine is exported.</span></span>



| <span data-ttu-id="5a01d-177">Wert</span><span class="sxs-lookup"><span data-stu-id="5a01d-177">Value</span></span>                                                                                | <span data-ttu-id="5a01d-178">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5a01d-178">Meaning</span></span>                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="5a01d-179"><dt>**Fall**</dt></span><span class="sxs-lookup"><span data-stu-id="5a01d-179"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="5a01d-180">Es wird ein Unterverzeichnis erstellt.</span><span class="sxs-lookup"><span data-stu-id="5a01d-180">A subdirectory will be created.</span></span><br/>     |
| <dl> <span data-ttu-id="5a01d-181"><dt>**False**</dt></span><span class="sxs-lookup"><span data-stu-id="5a01d-181"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="5a01d-182">Ein Unterverzeichnis wird nicht erstellt.</span><span class="sxs-lookup"><span data-stu-id="5a01d-182">A subdirectory will not be created.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5a01d-183">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5a01d-183">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a01d-184">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5a01d-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a01d-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5a01d-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a01d-186">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="5a01d-186">A description of the object.</span></span> <span data-ttu-id="5a01d-187">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5a01d-187">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5a01d-188">**Differenalbackupbase**</span><span class="sxs-lookup"><span data-stu-id="5a01d-188">**DifferentialBackupBase**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a01d-189">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5a01d-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a01d-190">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5a01d-190">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5a01d-191">Basis für differenziellen Export.</span><span class="sxs-lookup"><span data-stu-id="5a01d-191">Base for differential export.</span></span> <span data-ttu-id="5a01d-192">Dabei handelt es sich entweder um einen Pfad zu einer [**MSVM \_ virtualsystemreferencepoint**](msvm-virtualsystemreferencepoint.md) -Instanz, die den Verweis Punkt oder den Pfad zu einer [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) -Instanz darstellt, die die Momentaufnahme darstellt, die als Basis für den differenziellen Export verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a01d-192">This is either path to a [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) instance that represents the reference point or path to a [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) instance that represents the snapshot to be used as a base for differential export.</span></span> <span data-ttu-id="5a01d-193">Wenn die Eigenschaft **copysnapshotconfiguration** nicht auf 3 (**exportonesnapshotforbackup**) festgelegt ist, wird diese Eigenschaft ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5a01d-193">If the **CopySnapshotConfiguration** property is not set to 3(**ExportOneSnapshotForBackup**), this property is ignored.</span></span>

> [!Note]  
> <span data-ttu-id="5a01d-194">In Windows 10 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5a01d-194">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="5a01d-195">**Disabledifferenalofignoredstorage**</span><span class="sxs-lookup"><span data-stu-id="5a01d-195">**DisableDifferentialOfIgnoredStorage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a01d-196">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5a01d-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a01d-197">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5a01d-197">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5a01d-198">Gibt an, ob differenzierende Datenträger erstellt werden oder nicht, wenn der Speicher beim Export ignoriert wird.</span><span class="sxs-lookup"><span data-stu-id="5a01d-198">Indicates whether differencing disks will be created or not for storage ignored during export.</span></span> <span data-ttu-id="5a01d-199">Standardmäßig ist diese Einstellung auf "false" festgelegt. Dies bedeutet, dass differenzierende Datenträger für den Speicher erstellt werden, der nicht in das Exportziel kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="5a01d-199">By default this is set to false, which means that differencing disks are created for the storage that is not going to be copied over to the export destination.</span></span>

> [!Note]  
> <span data-ttu-id="5a01d-200">Hinzugefügt in Windows 10, Version 1709.</span><span class="sxs-lookup"><span data-stu-id="5a01d-200">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="5a01d-201">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5a01d-201">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a01d-202">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5a01d-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a01d-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5a01d-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a01d-204">Der Anzeige Name für diese Instanz.</span><span class="sxs-lookup"><span data-stu-id="5a01d-204">The display name for this instance.</span></span> <span data-ttu-id="5a01d-205">Außerdem kann der Anzeige Name als Index Eigenschaft für eine Suche oder Abfrage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5a01d-205">In addition, the display name can be used as an index property for a search or query.</span></span> <span data-ttu-id="5a01d-206">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="5a01d-206">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5a01d-207">**Excludvirtualharddisks**</span><span class="sxs-lookup"><span data-stu-id="5a01d-207">**ExcludedVirtualHardDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a01d-208">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="5a01d-208">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5a01d-209">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5a01d-209">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5a01d-210">Array von MSVM-Instanzen-IDs der [**\_ storagezuordungssettingdata**](msvm-storageallocationsettingdata.md) (rasd), die die virtuellen Festplatten darstellen, die aus dem Export Vorgang ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5a01d-210">Array of [**Msvm\_StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) (RASD) instance IDs that represent the virtual hard disks that are requested to be excluded from the export operation.</span></span> <span data-ttu-id="5a01d-211">Wenn mindestens eine der angegebenen IDs keine gültige angefügte virtuelle Festplatte ist, tritt bei dem Vorgang ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="5a01d-211">If at least one of the supplied IDs is not a valid attached virtual hard disk, the operation will fail.</span></span>

<span data-ttu-id="5a01d-212">Die virtuellen Festplatten, auf die diese Eigenschaft verweist, können vom virtuellen Computer und/oder von seinen Momentaufnahmen sein.</span><span class="sxs-lookup"><span data-stu-id="5a01d-212">The virtual hard disks referenced by this property may be from the VM and/or from any of its snapshots.</span></span> <span data-ttu-id="5a01d-213">Der Ausschluss virtueller Festplatten wird nicht unterstützt, wenn die Eigenschaft **copysnapshotconfiguration** auf 0 (exportallsnapshot) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5a01d-213">Exclusion of virtual hard disks is not supported when property **CopySnapshotConfiguration** is set to 0(ExportAllSnapshots).</span></span>

<span data-ttu-id="5a01d-214">Beachten Sie, dass die rasd-Instanz-ID für virtuelle Festplatten den Speicherort darstellt, an den Sie angefügt sind. durch das Ausschließen dieser ID werden alle virtuellen Festplatten ausgeschlossen, die an diesem Speicherort in der Momentaufnahme Struktur der virtuellen Maschine angefügt sind, und zwar unabhängig davon, ob es sich um eine gültige</span><span class="sxs-lookup"><span data-stu-id="5a01d-214">Note that the RASD instance ID for virtual hard disks represents the location they are attached to, and excluding through this ID excludes all virtual hard disks attached in that location throughout the virtual machine's snapshot tree, regardless of them really being a valid virtual hard disk chain.</span></span>

> [!Note]  
> <span data-ttu-id="5a01d-215">Hinzugefügt in Windows 10, Version 1709.</span><span class="sxs-lookup"><span data-stu-id="5a01d-215">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="5a01d-216">**Exportforlivemigration**</span><span class="sxs-lookup"><span data-stu-id="5a01d-216">**ExportForLiveMigration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a01d-217">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5a01d-217">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a01d-218">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5a01d-218">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5a01d-219">Gibt an, ob der exportierte virtuelle Computer bei der Live Migration verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a01d-219">Indicates whether the exported VM is intended to be used in live migration.</span></span>

> [!Note]  
> <span data-ttu-id="5a01d-220">In Windows 10, Version 1703 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5a01d-220">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="5a01d-221">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5a01d-221">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a01d-222">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5a01d-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a01d-223">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5a01d-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a01d-224">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="5a01d-224">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5a01d-225">Innerhalb des Gültigkeits Bereichs des instanziierten Namespaces identifiziert verdeckt und eindeutig eine Instanz dieser Klasse.</span><span class="sxs-lookup"><span data-stu-id="5a01d-225">Within the scope of the instantiating Namespace, opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="5a01d-226">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="5a01d-226">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5a01d-227">**Snapshotvirtualsystem**</span><span class="sxs-lookup"><span data-stu-id="5a01d-227">**SnapshotVirtualSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a01d-228">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5a01d-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a01d-229">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5a01d-229">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5a01d-230">Der Pfad zu einer [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) -Instanz, die die Momentaufnahme darstellt, die mit dem virtuellen Computer exportiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a01d-230">Path to a [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) instance that represents the snapshot to be exported with the virtual machine.</span></span> <span data-ttu-id="5a01d-231">Wenn die Eigenschaft **copysnapshotconfiguration** nicht auf 2 (exportonesnapshot) festgelegt ist, wird diese Eigenschaft ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5a01d-231">If the **CopySnapshotConfiguration** property is not set to 2 (ExportOneSnapshot), this property is ignored.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5a01d-232">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a01d-232">Remarks</span></span>

<span data-ttu-id="5a01d-233">Der Zugriff auf die **MSVM \_ virtualsystemexportsettingdata** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="5a01d-233">Access to the **Msvm\_VirtualSystemExportSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="5a01d-234">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="5a01d-234">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a01d-235">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a01d-235">Requirements</span></span>



| <span data-ttu-id="5a01d-236">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5a01d-236">Requirement</span></span> | <span data-ttu-id="5a01d-237">Wert</span><span class="sxs-lookup"><span data-stu-id="5a01d-237">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a01d-238">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5a01d-238">Minimum supported client</span></span><br/> | <span data-ttu-id="5a01d-239">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5a01d-239">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5a01d-240">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5a01d-240">Minimum supported server</span></span><br/> | <span data-ttu-id="5a01d-241">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5a01d-241">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5a01d-242">Namespace</span><span class="sxs-lookup"><span data-stu-id="5a01d-242">Namespace</span></span><br/>                | <span data-ttu-id="5a01d-243">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="5a01d-243">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5a01d-244">MOF</span><span class="sxs-lookup"><span data-stu-id="5a01d-244">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5a01d-245"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5a01d-245"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5a01d-246">DLL</span><span class="sxs-lookup"><span data-stu-id="5a01d-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a01d-247"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5a01d-247"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5a01d-248">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a01d-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a01d-249">**CIM- \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="5a01d-249">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="5a01d-250">Verwaltungs Klassen für virtuelle Systeme</span><span class="sxs-lookup"><span data-stu-id="5a01d-250">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> <dt>

[<span data-ttu-id="5a01d-251">**Exportsystemdefinition**</span><span class="sxs-lookup"><span data-stu-id="5a01d-251">**ExportSystemDefinition**</span></span>](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

