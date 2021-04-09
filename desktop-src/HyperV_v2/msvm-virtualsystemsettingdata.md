---
description: Stellt die virtualisierungsspezifischen Einstellungen für einen virtuellen Computer dar.
ms.assetid: BE81405E-E773-41CE-9441-33D60B63550E
title: Msvm_VirtualSystemSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSettingData
- Msvm_VirtualSystemSettingData.InstanceID
- Msvm_VirtualSystemSettingData.Caption
- Msvm_VirtualSystemSettingData.Description
- Msvm_VirtualSystemSettingData.ElementName
- Msvm_VirtualSystemSettingData.VirtualSystemIdentifier
- Msvm_VirtualSystemSettingData.VirtualSystemType
- Msvm_VirtualSystemSettingData.Notes
- Msvm_VirtualSystemSettingData.CreationTime
- Msvm_VirtualSystemSettingData.ConfigurationID
- Msvm_VirtualSystemSettingData.ConfigurationDataRoot
- Msvm_VirtualSystemSettingData.ConfigurationFile
- Msvm_VirtualSystemSettingData.SnapshotDataRoot
- Msvm_VirtualSystemSettingData.SuspendDataRoot
- Msvm_VirtualSystemSettingData.SwapFileDataRoot
- Msvm_VirtualSystemSettingData.LogDataRoot
- Msvm_VirtualSystemSettingData.AutomaticStartupAction
- Msvm_VirtualSystemSettingData.AutomaticStartupActionDelay
- Msvm_VirtualSystemSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualSystemSettingData.AutomaticShutdownAction
- Msvm_VirtualSystemSettingData.AutomaticRecoveryAction
- Msvm_VirtualSystemSettingData.RecoveryFile
- Msvm_VirtualSystemSettingData.BIOSGUID
- Msvm_VirtualSystemSettingData.BIOSSerialNumber
- Msvm_VirtualSystemSettingData.BaseBoardSerialNumber
- Msvm_VirtualSystemSettingData.ChassisSerialNumber
- Msvm_VirtualSystemSettingData.Architecture
- Msvm_VirtualSystemSettingData.ChassisAssetTag
- Msvm_VirtualSystemSettingData.BIOSNumLock
- Msvm_VirtualSystemSettingData.BootOrder
- Msvm_VirtualSystemSettingData.Parent
- Msvm_VirtualSystemSettingData.UserSnapshotType
- Msvm_VirtualSystemSettingData.IsSaved
- Msvm_VirtualSystemSettingData.AdditionalRecoveryInformation
- Msvm_VirtualSystemSettingData.AllowFullSCSICommandSet
- Msvm_VirtualSystemSettingData.DebugChannelId
- Msvm_VirtualSystemSettingData.DebugPortEnabled
- Msvm_VirtualSystemSettingData.DebugPort
- Msvm_VirtualSystemSettingData.Version
- Msvm_VirtualSystemSettingData.IncrementalBackupEnabled
- Msvm_VirtualSystemSettingData.VirtualNumaEnabled
- Msvm_VirtualSystemSettingData.AllowReducedFcRedundancy
- Msvm_VirtualSystemSettingData.VirtualSystemSubType
- Msvm_VirtualSystemSettingData.BootSourceOrder
- Msvm_VirtualSystemSettingData.PauseAfterBootFailure
- Msvm_VirtualSystemSettingData.NetworkBootPreferredProtocol
- Msvm_VirtualSystemSettingData.GuestControlledCacheTypes
- Msvm_VirtualSystemSettingData.AutomaticSnapshotsEnabled
- Msvm_VirtualSystemSettingData.IsAutomaticSnapshot
- Msvm_VirtualSystemSettingData.GuestStateFile
- Msvm_VirtualSystemSettingData.GuestStateDataRoot
- Msvm_VirtualSystemSettingData.LockOnDisconnect
- Msvm_VirtualSystemSettingData.ParentPackage
- Msvm_VirtualSystemSettingData.AutomaticCriticalErrorActionTimeout
- Msvm_VirtualSystemSettingData.AutomaticCriticalErrorAction
- Msvm_VirtualSystemSettingData.ConsoleMode
- Msvm_VirtualSystemSettingData.SecureBootEnabled
- Msvm_VirtualSystemSettingData.SecureBootTemplateId
- Msvm_VirtualSystemSettingData.LowMmioGapSize
- Msvm_VirtualSystemSettingData.HighMmioGapSize
- Msvm_VirtualSystemSettingData.EnhancedSessionTransportType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2787abbacfe4220b135544eecd3aeb7e86596c81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958741"
---
# <a name="msvm_virtualsystemsettingdata-class"></a><span data-ttu-id="727ab-103">MSVM \_ virtualsystemsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="727ab-103">Msvm\_VirtualSystemSettingData class</span></span>

<span data-ttu-id="727ab-104">Stellt die virtualisierungsspezifischen Einstellungen für einen virtuellen Computer dar.</span><span class="sxs-lookup"><span data-stu-id="727ab-104">Represents the virtualization-specific settings for a virtual machine.</span></span>

<span data-ttu-id="727ab-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="727ab-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="727ab-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="727ab-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID;
  string   Caption = "Virtual Machine Settings";
  string   Description;
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
  string   BIOSGUID;
  string   BIOSSerialNumber;
  string   BaseBoardSerialNumber;
  string   ChassisSerialNumber;
  string   Architecture;
  string   ChassisAssetTag;
  boolean  BIOSNumLock;
  uint16   BootOrder[];
  string   Parent;
  uint16   UserSnapshotType;
  boolean  IsSaved;
  string   AdditionalRecoveryInformation;
  boolean  AllowFullSCSICommandSet;
  uint32   DebugChannelId;
  uint16   DebugPortEnabled;
  uint32   DebugPort;
  string   Version;
  boolean  IncrementalBackupEnabled;
  boolean  VirtualNumaEnabled;
  boolean  AllowReducedFcRedundancy = False;
  string   VirtualSystemSubType;
  string   BootSourceOrder[];
  boolean  PauseAfterBootFailure;
  uint16   NetworkBootPreferredProtocol;
  boolean  GuestControlledCacheTypes;
  boolean  AutomaticSnapshotsEnabled;
  boolean  IsAutomaticSnapshot;
  string   GuestStateFile;
  string   GuestStateDataRoot;
  boolean  LockOnDisconnect;
  string   ParentPackage;
  datetime AutomaticCriticalErrorActionTimeout;
  uint16   AutomaticCriticalErrorAction;
  uint16   ConsoleMode;
  boolean  SecureBootEnabled;
  string   SecureBootTemplateId;
  uint64   LowMmioGapSize;
  uint64   HighMmioGapSize;
  uint16   EnhancedSessionTransportType;
};
```

## <a name="members"></a><span data-ttu-id="727ab-107">Member</span><span class="sxs-lookup"><span data-stu-id="727ab-107">Members</span></span>

<span data-ttu-id="727ab-108">Die **MSVM \_ virtualsystemsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="727ab-108">The **Msvm\_VirtualSystemSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="727ab-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="727ab-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="727ab-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="727ab-110">Properties</span></span>

<span data-ttu-id="727ab-111">Die **MSVM \_ virtualsystemsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="727ab-111">The **Msvm\_VirtualSystemSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="727ab-112">**Additionalherstellungsinformationen**</span><span class="sxs-lookup"><span data-stu-id="727ab-112">**AdditionalRecoveryInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="727ab-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-114">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="727ab-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="727ab-115">Alle zusätzlichen Informationen, die für die Wiederherstellungs Aktion bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="727ab-115">Any additional information provided to the recovery action.</span></span> <span data-ttu-id="727ab-116">Die Bedeutung dieser Eigenschaft wird durch die Aktion in **automatikrecoveryaction** definiert.</span><span class="sxs-lookup"><span data-stu-id="727ab-116">The meaning of this property is defined by the action in **AutomaticRecoveryAction**.</span></span> <span data-ttu-id="727ab-117">Wenn **automatikrecoveryaction** den Wert 0 ("None") oder 1 ("Restart") hat, ist dieser Wert **null**.</span><span class="sxs-lookup"><span data-stu-id="727ab-117">If **AutomaticRecoveryAction** is 0 ("None") or 1 ("Restart"), this value is **Null**.</span></span> <span data-ttu-id="727ab-118">Wenn **automatidecoveryaction** den Wert 2 hat ("Momentaufnahme wiederherstellen"), ist dies der Objekt Pfad zu einer Momentaufnahme, die bei einem Fehler des Arbeitsprozesses der virtuellen Maschine angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="727ab-118">If **AutomaticRecoveryAction** is 2 ("Revert to Snapshot"), this is the object path to a snapshot that should be applied on failure of the virtual machine worker process.</span></span>

</dd> <dt>

<span data-ttu-id="727ab-119">**Allowfullscsicommandset**</span><span class="sxs-lookup"><span data-stu-id="727ab-119">**AllowFullSCSICommandSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-120">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="727ab-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="727ab-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="727ab-122">**True** , wenn SCSI-Befehle vom Gast Betriebssystem an Pass-Through-Datenträger übergeben werden. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="727ab-122">**True** if SCSI commands from the guest operating system are passed to pass-through disks; otherwise, **False**.</span></span> <span data-ttu-id="727ab-123">**True** gibt an, dass SCSI-Befehle, die vom Gast Betriebssystem an Pass-Through-Datenträger ausgegeben werden, nicht gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="727ab-123">If **True**, SCSI commands emitted by the guest operating system to pass-through disks are not filtered.</span></span> <span data-ttu-id="727ab-124">Es wird empfohlen, die SCSI-Filterung für Produktions Bereitstellungen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="727ab-124">We recommend that SCSI filtering remain enabled for production deployments.</span></span>

</dd> <dt>

<span data-ttu-id="727ab-125">**Allowreducedf | dundancy**</span><span class="sxs-lookup"><span data-stu-id="727ab-125">**AllowReducedFcRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-126">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="727ab-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="727ab-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="727ab-128">Gibt an, ob die Live Migration eines virtuellen Computers, der mit einem virtuellen Fibre Channel Adapter konfiguriert ist, zu einem Zielcomputer zulässig ist, der möglicherweise über keine oder reduzierten Pfad zum Ziel Fibre Channel Geräten verfügt.</span><span class="sxs-lookup"><span data-stu-id="727ab-128">Specifies whether live migration of a virtual machine that is configured with a virtual Fibre Channel adapter is allowed to a destination computer that may have no or reduced paths to the target Fibre Channel devices.</span></span> <span data-ttu-id="727ab-129">Diese Eigenschaft sollte nach einer Live Migration gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="727ab-129">This property should be cleared after a live migration.</span></span>



| <span data-ttu-id="727ab-130">Wert</span><span class="sxs-lookup"><span data-stu-id="727ab-130">Value</span></span>                                                                            | <span data-ttu-id="727ab-131">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="727ab-131">Meaning</span></span>                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="727ab-132"><dt>False</dt></span><span class="sxs-lookup"><span data-stu-id="727ab-132"><dt>False</dt></span></span> </dl> | <span data-ttu-id="727ab-133">Der virtuelle Computer kann nicht auf einen Zielcomputer migriert werden, der möglicherweise keine oder weniger Pfade zum Ziel Fibre Channel Geräten hat.</span><span class="sxs-lookup"><span data-stu-id="727ab-133">The virtual machine cannot be live migrated to a target computer that may have no or reduced paths to the target Fibre Channel devices.</span></span><br/>                                                                                                     |
| <dl> <span data-ttu-id="727ab-134"><dt>True</dt></span><span class="sxs-lookup"><span data-stu-id="727ab-134"><dt>True</dt></span></span> </dl>  | <span data-ttu-id="727ab-135">Der virtuelle Computer kann Live zu einem Zielcomputer migriert werden, der möglicherweise keine oder weniger Pfade zum Ziel Fibre Channel Geräten hat.</span><span class="sxs-lookup"><span data-stu-id="727ab-135">The virtual machine can be live migrated to a target computer that may have no or reduced paths to the target Fibre Channel devices.</span></span> <span data-ttu-id="727ab-136">Das Gast Betriebssystem verliert möglicherweise die Konnektivität mit dem Speicher und kann sich auf unvorhersehbare Weise Verhalten.</span><span class="sxs-lookup"><span data-stu-id="727ab-136">The guest operating system may lose connectivity to storage and may behave in an unpredictable manner.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="727ab-137">**Architektur**</span><span class="sxs-lookup"><span data-stu-id="727ab-137">**Architecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="727ab-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="727ab-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="727ab-140">Die Architektur dieses Systems.</span><span class="sxs-lookup"><span data-stu-id="727ab-140">The architecture of this system.</span></span>

> [!Note]  
> <span data-ttu-id="727ab-141">Hinzugefügt in Windows 10, Version 1709.</span><span class="sxs-lookup"><span data-stu-id="727ab-141">Added in Windows 10, version 1709.</span></span>

 

<dt>

<span id="x64"></span><span id="X64"></span>

<span data-ttu-id="727ab-142">**x64** ()</span><span class="sxs-lookup"><span data-stu-id="727ab-142">**x64** ()</span></span>


</dt> <dd></dd> <dt>

<span id="arm64"></span><span id="ARM64"></span>

<span data-ttu-id="727ab-143">**arm64** ()</span><span class="sxs-lookup"><span data-stu-id="727ab-143">**arm64** ()</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="727ab-144">**Automaticcriticalerroraction**</span><span class="sxs-lookup"><span data-stu-id="727ab-144">**AutomaticCriticalErrorAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-145">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="727ab-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-146">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="727ab-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="727ab-147">Gibt die Aktion an, die auf dem virtuellen Computer ausgeführt werden soll, wenn ein kritischer Fehler auftritt, z. b. Speicher Trennung.</span><span class="sxs-lookup"><span data-stu-id="727ab-147">Identifies the action to be taken on VM, when a critical error happens, like storage disconnect.</span></span>

> [!Note]  
> <span data-ttu-id="727ab-148">In Windows 10 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="727ab-148">Added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="727ab-149"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Keine** (0)</span><span class="sxs-lookup"><span data-stu-id="727ab-149"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (0)</span></span>


</dt> <dd>

<span data-ttu-id="727ab-150">Für kritische Fehlerbedingungen wird keine spezielle Aktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="727ab-150">No specific action will be taken for critical error conditions.</span></span>

</dd> <dt>

<span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>

<span data-ttu-id="727ab-151"><span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>Fortsetzung **anhalten (1** )</span><span class="sxs-lookup"><span data-stu-id="727ab-151"><span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>**Pause Resume** (1)</span></span>


</dt> <dd>

<span data-ttu-id="727ab-152">Bewirkt, dass der virtuelle Computer angehalten und automatisch fortgesetzt wird, wenn der kritische Fehlerzustand behoben ist.</span><span class="sxs-lookup"><span data-stu-id="727ab-152">Causes the VM to be paused and automatically resumed when the critical error condition is resolved.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="727ab-153">**Automaticcriticalerroraktiontimeout**</span><span class="sxs-lookup"><span data-stu-id="727ab-153">**AutomaticCriticalErrorActionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-154">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="727ab-154">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-155">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="727ab-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="727ab-156">Qualifizierer: [**Untertyp**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Intervall")</span><span class="sxs-lookup"><span data-stu-id="727ab-156">Qualifiers: [**SubType**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("interval")</span></span>
</dt> </dl>

<span data-ttu-id="727ab-157">Gibt die maximale Dauer an, für die die **automaticcriticalerroraction** ausgeführt wird, um den kritischen Fehler zu beheben.</span><span class="sxs-lookup"><span data-stu-id="727ab-157">Identifies the maximum duration for which the **AutomaticCriticalErrorAction** will be performed to resolve the critical error.</span></span> <span data-ttu-id="727ab-158">Dies gilt nur, wenn der Wert der **automaticcriticalerroraction** -Eigenschaft nicht 0 (None) ist.</span><span class="sxs-lookup"><span data-stu-id="727ab-158">This is applicable only when the value of the **AutomaticCriticalErrorAction** property is not 0 (None).</span></span> <span data-ttu-id="727ab-159">Nach Ablauf des Timeouts wird der virtuelle Computer ausgeschaltet.</span><span class="sxs-lookup"><span data-stu-id="727ab-159">Once the timeout expires, the VM will be powered off.</span></span> <span data-ttu-id="727ab-160">Der Wert wird auf die nächste Minute aufgerundet.</span><span class="sxs-lookup"><span data-stu-id="727ab-160">The value will be rounded up to the nearest minute.</span></span> <span data-ttu-id="727ab-161">Der Wert 0 bedeutet, dass der virtuelle Computer sofort ausgeschaltet werden sollte, wenn er auf einen kritischen Fehlerzustand stößt.</span><span class="sxs-lookup"><span data-stu-id="727ab-161">A value of 0 implies that the VM should be powered off immediately when it encounters a critical error condition.</span></span>

> [!Note]  
> <span data-ttu-id="727ab-162">In Windows 10 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="727ab-162">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="727ab-163">**Automatikrecoveryaction**</span><span class="sxs-lookup"><span data-stu-id="727ab-163">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-164">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="727ab-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="727ab-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="727ab-166">Die für den virtuellen Computer auszuführende Aktion, wenn die von der virtuellen Maschine ausgeführte Software ausfällt.</span><span class="sxs-lookup"><span data-stu-id="727ab-166">Action to take for the virtual machine when the software executed by the virtual machine fails.</span></span> <span data-ttu-id="727ab-167">Fehler sind in diesem Fall ein Fehler, der von der Host Plattform erkannt werden kann, z. b. eine nicht unter brechbare Bedingung für den Wartezustand.</span><span class="sxs-lookup"><span data-stu-id="727ab-167">Failures in this case means a failure that is detectable by the host platform, such as a noninterruptible wait state condition.</span></span> <span data-ttu-id="727ab-168">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="727ab-168">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="727ab-169">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="727ab-169">This can be one of the following values.</span></span>



| <span data-ttu-id="727ab-170">Wert</span><span class="sxs-lookup"><span data-stu-id="727ab-170">Value</span></span>                                                                               | <span data-ttu-id="727ab-171">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="727ab-171">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="727ab-172"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="727ab-172"><dt>2</dt></span></span> </dl>        | <span data-ttu-id="727ab-173">Keine.</span><span class="sxs-lookup"><span data-stu-id="727ab-173">None.</span></span><br/>               |
| <dl> <span data-ttu-id="727ab-174"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="727ab-174"><dt>3</dt></span></span> </dl>        | <span data-ttu-id="727ab-175">Neu starten</span><span class="sxs-lookup"><span data-stu-id="727ab-175">Restart.</span></span><br/>            |
| <dl> <span data-ttu-id="727ab-176"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="727ab-176"><dt>4</dt></span></span> </dl>        | <span data-ttu-id="727ab-177">Momentaufnahme wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="727ab-177">Revert to snapshot.</span></span><br/> |
| <dl> <span data-ttu-id="727ab-178"><dt>5.. 32768</dt></span><span class="sxs-lookup"><span data-stu-id="727ab-178"><dt>5..32768</dt></span></span> </dl> | <span data-ttu-id="727ab-179">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="727ab-179">Reserved.</span></span><br/>           |



 

</dd> <dt>

<span data-ttu-id="727ab-180">**Automaticshutdownaction**</span><span class="sxs-lookup"><span data-stu-id="727ab-180">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-181">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="727ab-181">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-182">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="727ab-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="727ab-183">Aktion, die beim Herunterfahren des Hosts für die virtuelle Maschine ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="727ab-183">Action to take for the virtual machine when the host is shut down.</span></span> <span data-ttu-id="727ab-184">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="727ab-184">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="727ab-185">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="727ab-185">This can be one of the following values.</span></span>



| <span data-ttu-id="727ab-186">Wert</span><span class="sxs-lookup"><span data-stu-id="727ab-186">Value</span></span>                                                                               | <span data-ttu-id="727ab-187">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="727ab-187">Meaning</span></span>                |
|-------------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="727ab-188"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="727ab-188"><dt>2</dt></span></span> </dl>        | <span data-ttu-id="727ab-189">Ausschalten.</span><span class="sxs-lookup"><span data-stu-id="727ab-189">Turn off.</span></span><br/>   |
| <dl> <span data-ttu-id="727ab-190"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="727ab-190"><dt>3</dt></span></span> </dl>        | <span data-ttu-id="727ab-191">Speichern Sie den Zustand.</span><span class="sxs-lookup"><span data-stu-id="727ab-191">Save state.</span></span><br/> |
| <dl> <span data-ttu-id="727ab-192"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="727ab-192"><dt>4</dt></span></span> </dl>        | <span data-ttu-id="727ab-193">Herunterfahren</span><span class="sxs-lookup"><span data-stu-id="727ab-193">Shutdown.</span></span><br/>   |
| <dl> <span data-ttu-id="727ab-194"><dt>5.. 32768</dt></span><span class="sxs-lookup"><span data-stu-id="727ab-194"><dt>5..32768</dt></span></span> </dl> | <span data-ttu-id="727ab-195">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="727ab-195">Reserved.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="727ab-196">**Automaticsnapshotsenabled**</span><span class="sxs-lookup"><span data-stu-id="727ab-196">**AutomaticSnapshotsEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-197">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="727ab-197">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-198">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="727ab-198">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="727ab-199">Gibt an, ob für diesen virtuellen Computer automatische Momentaufnahmen aktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="727ab-199">Indicates whether this virtual machine should have automatic snapshots enabled.</span></span>

> [!Note]  
> <span data-ttu-id="727ab-200">Hinzugefügt in Windows 10, Version 1709.</span><span class="sxs-lookup"><span data-stu-id="727ab-200">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="727ab-201">**Automaticstartupaction**</span><span class="sxs-lookup"><span data-stu-id="727ab-201">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-202">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="727ab-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="727ab-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="727ab-204">Aktion, die für den virtuellen Computer ausgeführt werden soll, wenn der Host gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="727ab-204">Action to take for the virtual machine when the host is started.</span></span> <span data-ttu-id="727ab-205">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="727ab-205">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="727ab-206">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="727ab-206">This can be one of the following values.</span></span>



| <span data-ttu-id="727ab-207">Wert</span><span class="sxs-lookup"><span data-stu-id="727ab-207">Value</span></span>                                                                               | <span data-ttu-id="727ab-208">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="727ab-208">Meaning</span></span>                                  |
|-------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="727ab-209"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="727ab-209"><dt>2</dt></span></span> </dl>        | <span data-ttu-id="727ab-210">Keine.</span><span class="sxs-lookup"><span data-stu-id="727ab-210">None.</span></span><br/>                         |
| <dl> <span data-ttu-id="727ab-211"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="727ab-211"><dt>3</dt></span></span> </dl>        | <span data-ttu-id="727ab-212">Neu starten, wenn zuvor aktiv.</span><span class="sxs-lookup"><span data-stu-id="727ab-212">Restart if previously active.</span></span><br/> |
| <dl> <span data-ttu-id="727ab-213"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="727ab-213"><dt>4</dt></span></span> </dl>        | <span data-ttu-id="727ab-214">Immer starten.</span><span class="sxs-lookup"><span data-stu-id="727ab-214">Always start.</span></span><br/>                 |
| <dl> <span data-ttu-id="727ab-215"><dt>5.. 32768</dt></span><span class="sxs-lookup"><span data-stu-id="727ab-215"><dt>5..32768</dt></span></span> </dl> | <span data-ttu-id="727ab-216">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="727ab-216">Reserved.</span></span><br/>                     |



 

</dd> <dt>

<span data-ttu-id="727ab-217">**Automaticstartupactiondelay**</span><span class="sxs-lookup"><span data-stu-id="727ab-217">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-218">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="727ab-218">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-219">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="727ab-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="727ab-220">Die Verzögerungszeit, bevor der virtuelle Computer automatisch gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="727ab-220">The delay time before the virtual machine is automatically started up.</span></span> <span data-ttu-id="727ab-221">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="727ab-221">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="727ab-222">**Automaticstartupactionsequencenumschlag**</span><span class="sxs-lookup"><span data-stu-id="727ab-222">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-223">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="727ab-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="727ab-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="727ab-225">Eine Zahl, die die relative Sequenz der Aktivierung virtueller Maschinen angibt, wenn das Host System gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="727ab-225">A number that indicates the relative sequence of virtual machine activation when the host system is started.</span></span> <span data-ttu-id="727ab-226">Eine niedrigere Zahl deutet auf eine frühere Aktivierung hin.</span><span class="sxs-lookup"><span data-stu-id="727ab-226">A lower number indicates earlier activation.</span></span> <span data-ttu-id="727ab-227">Wenn eine oder mehrere Konfigurationen denselben Wert aufweisen, ist die Sequenz implementierungsabhängig.</span><span class="sxs-lookup"><span data-stu-id="727ab-227">If one or more configurations show the same value, the sequence is implementation dependent.</span></span> <span data-ttu-id="727ab-228">Der Wert 0 gibt an, dass die Sequenz implementierungsabhängig ist.</span><span class="sxs-lookup"><span data-stu-id="727ab-228">A value of 0 indicates that the sequence is implementation dependent.</span></span> <span data-ttu-id="727ab-229">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="727ab-229">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="727ab-230">**Baseboardserialnumber**</span><span class="sxs-lookup"><span data-stu-id="727ab-230">**BaseBoardSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-231">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="727ab-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-232">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="727ab-232">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="727ab-233">Die Seriennummer des Basis Boards für die virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="727ab-233">The serial number of the base board for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="727ab-234">**Biosguid**</span><span class="sxs-lookup"><span data-stu-id="727ab-234">**BIOSGUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-235">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="727ab-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-236">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="727ab-236">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="727ab-237">Der Globally Unique Identifier für das BIOS der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="727ab-237">The globally unique identifier for the BIOS of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="727ab-238">**Biosnumlock**</span><span class="sxs-lookup"><span data-stu-id="727ab-238">**BIOSNumLock**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-239">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="727ab-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-240">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="727ab-240">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="727ab-241">**True** , wenn der NUM-Sperr Schlüssel vom BIOS auf ON festgelegt ist. **False** , wenn der NUM-Sperr Schlüssel vom BIOS auf OFF festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="727ab-241">**True** if the num lock key is set to on by the BIOS; **False** if the num lock key is set to off by the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="727ab-242">**BIOSSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="727ab-242">**BIOSSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-243">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="727ab-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-244">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="727ab-244">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="727ab-245">Die Seriennummer des BIOS für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="727ab-245">The serial number of the BIOS for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="727ab-246">**"Bootorder"**</span><span class="sxs-lookup"><span data-stu-id="727ab-246">**BootOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-247">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="727ab-247">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="727ab-248">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="727ab-248">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="727ab-249">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (4)</span><span class="sxs-lookup"><span data-stu-id="727ab-249">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (4)</span></span>
</dt> </dl>

<span data-ttu-id="727ab-250">Die Start Reihenfolge, die innerhalb des BIOS der virtuellen Maschine festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="727ab-250">The boot order set within the BIOS of the virtual machine.</span></span> <span data-ttu-id="727ab-251">Diese Eigenschaft ist ein Array von Werten, **booterder** \[ 0 \] bis **bootor** \[ 3 ( \] inklusiv), wobei jeder Wert ein Gerät angibt, von dem aus gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="727ab-251">This property is an array of values, **BootOrder**\[0\] through **BootOrder**\[3\], inclusive, where each value indicates a device to boot from.</span></span> <span data-ttu-id="727ab-252">Jeder der vier Werte im Array muss festgelegt werden und darf nicht mit einem anderen Wert im Array identisch sein.</span><span class="sxs-lookup"><span data-stu-id="727ab-252">Each of the 4 values in the array must be set and must not be the same as another value in the array.</span></span> <span data-ttu-id="727ab-253">Der virtuelle Computer versucht zunächst, über das Gerät zu starten, das durch den ersten Wert im Array angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="727ab-253">The virtual machine will first attempt to boot from the device indicated by the first value within the array.</span></span> <span data-ttu-id="727ab-254">Wenn dieses Gerät keinen Startsektor enthält, versucht die virtuelle Maschine, vom nächsten Gerät zu starten, das von der **bootorder** -Eigenschaft angegeben wird, und so weiter.</span><span class="sxs-lookup"><span data-stu-id="727ab-254">If that device does not contain a boot sector, the virtual machine will attempt to boot from the next device specified by the **BootOrder** property and so on.</span></span> <span data-ttu-id="727ab-255">Wenn kein im **bootor** angegebener Gerät einen Startsektor enthält, kann der virtuelle Computer nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="727ab-255">If no device specified within the **BootOrder** contains a boot sector the virtual machine will fail to boot.</span></span> <span data-ttu-id="727ab-256">Der Standardwert für eine virtuelle Maschine ist \[ 0, 1, 2, 3 \] .</span><span class="sxs-lookup"><span data-stu-id="727ab-256">The default value for a virtual machine is \[0, 1, 2, 3\].</span></span>

<dt>

<span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>

<span data-ttu-id="727ab-257"><span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>**Diskette** (0)</span><span class="sxs-lookup"><span data-stu-id="727ab-257"><span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>**Floppy** (0)</span></span>


</dt> <dd>

<span data-ttu-id="727ab-258">Der virtuelle Computer wird versuchen, von der Diskette innerhalb des Disketten Laufwerks zu starten.</span><span class="sxs-lookup"><span data-stu-id="727ab-258">The virtual machine will attempt to boot from the floppy disk within the floppy drive.</span></span>

</dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span data-ttu-id="727ab-259"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (1)</span><span class="sxs-lookup"><span data-stu-id="727ab-259"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (1)</span></span>


</dt> <dd>

<span data-ttu-id="727ab-260">Der virtuelle Computer versucht, von der ersten CD oder DVD-Festplatte zu starten, die mit einem Startsektor gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="727ab-260">The virtual machine will attempt to boot from the first CD or DVD disk found with a boot sector.</span></span>

</dd> <dt>

<span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>

<span data-ttu-id="727ab-261"><span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>**IDE-Festplatte** (2)</span><span class="sxs-lookup"><span data-stu-id="727ab-261"><span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>**IDE Hard Drive** (2)</span></span>


</dt> <dd>

<span data-ttu-id="727ab-262">Der virtuelle Computer versucht, vom ersten Festplattenlaufwerk aus zu starten, das sich in einem Startsektor befand.</span><span class="sxs-lookup"><span data-stu-id="727ab-262">The virtual machine will attempt to boot from the first hard disk drive found with a boot sector.</span></span>

</dd> <dt>

<span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>

<span data-ttu-id="727ab-263"><span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>**PXE-Start** (3)</span><span class="sxs-lookup"><span data-stu-id="727ab-263"><span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>**PXE Boot** (3)</span></span>


</dt> <dd>

<span data-ttu-id="727ab-264">Der virtuelle Computer versucht, PXE aus dem Netzwerk zu starten.</span><span class="sxs-lookup"><span data-stu-id="727ab-264">The virtual machine will attempt to PXE boot from the network.</span></span>

</dd> <dt>

<span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>

<span data-ttu-id="727ab-265"><span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>**SCSI-Festplatte** (4)</span><span class="sxs-lookup"><span data-stu-id="727ab-265"><span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>**SCSI Hard Drive** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="727ab-266"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserviert** (5.. 65535)</span><span class="sxs-lookup"><span data-stu-id="727ab-266"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (5..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="727ab-267">**Bootsourceorder**</span><span class="sxs-lookup"><span data-stu-id="727ab-267">**BootSourceOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-268">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="727ab-268">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="727ab-269">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="727ab-269">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="727ab-270">Die Start Quell Reihenfolge für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="727ab-270">The boot source order for the virtual machine.</span></span>

<span data-ttu-id="727ab-271">**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="727ab-271">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="727ab-272">**Caption**</span><span class="sxs-lookup"><span data-stu-id="727ab-272">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-273">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="727ab-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-274">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="727ab-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="727ab-275">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="727ab-275">A short description of the object.</span></span> <span data-ttu-id="727ab-276">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="727ab-276">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="727ab-277">**Chassisassettag**</span><span class="sxs-lookup"><span data-stu-id="727ab-277">**ChassisAssetTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-278">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="727ab-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-279">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="727ab-279">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="727ab-280">Das Bestands Kennzeichen des Chassis für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="727ab-280">The asset tag of the chassis for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="727ab-281">**Chassisserialnumber**</span><span class="sxs-lookup"><span data-stu-id="727ab-281">**ChassisSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-282">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="727ab-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-283">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="727ab-283">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="727ab-284">Die Seriennummer des Chassis für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="727ab-284">The serial number of the chassis for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="727ab-285">**Configurationdataroot**</span><span class="sxs-lookup"><span data-stu-id="727ab-285">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-286">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="727ab-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-287">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="727ab-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="727ab-288">Der Pfad eines Verzeichnisses, in dem Informationen zur Konfiguration der virtuellen Maschine gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="727ab-288">The path of a directory where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="727ab-289">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="727ab-289">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="727ab-290">**ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="727ab-290">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-291">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="727ab-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-292">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="727ab-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="727ab-293">Der relative Pfad und der Dateiname einer Datei, in der Informationen zur Konfiguration der virtuellen Maschine gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="727ab-293">The relative path and file name of a file where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="727ab-294">Dieser Pfad ist relativ zur **configurationdataroot** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="727ab-294">This path is relative to the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="727ab-295">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="727ab-295">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="727ab-296">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="727ab-296">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-297">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="727ab-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-298">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="727ab-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="727ab-299">Der eindeutige Bezeichner der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="727ab-299">The unique identifier of the virtual machine configuration.</span></span> <span data-ttu-id="727ab-300">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="727ab-300">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="727ab-301">**Consolemode**</span><span class="sxs-lookup"><span data-stu-id="727ab-301">**ConsoleMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-302">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="727ab-302">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-303">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="727ab-303">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="727ab-304">Identifiziert den Konsolenmodus für die VM.</span><span class="sxs-lookup"><span data-stu-id="727ab-304">Identifies the Console Mode for the VM.</span></span>

> [!Note]  
> <span data-ttu-id="727ab-305">Diese Eigenschaft wurde in Windows 10 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="727ab-305">This property was added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="727ab-306">**Standard** (0)</span><span class="sxs-lookup"><span data-stu-id="727ab-306">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="COM1"></span><span id="com1"></span>

<span data-ttu-id="727ab-307">**COM1** (1)</span><span class="sxs-lookup"><span data-stu-id="727ab-307">**COM1** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="COM2"></span><span id="com2"></span>

<span data-ttu-id="727ab-308">**COM2** (2)</span><span class="sxs-lookup"><span data-stu-id="727ab-308">**COM2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="727ab-309">**Keine** (3)</span><span class="sxs-lookup"><span data-stu-id="727ab-309">**None** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="727ab-310">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="727ab-310">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-311">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="727ab-311">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-312">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="727ab-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="727ab-313">Das Datum und die Uhrzeit der Erstellung der Einstellungen für die virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="727ab-313">The date and time at which the settings for the virtual machine were created.</span></span> <span data-ttu-id="727ab-314">Wenn dieses-Objekt die aktuellen Einstellungen für die virtuelle Maschine darstellt, ist dieser Wert die Zeit, zu der das System erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="727ab-314">If this object represents the current settings for the virtual machine, this value would be the time at which the system was created.</span></span> <span data-ttu-id="727ab-315">Wenn dieses-Objekt die Momentaufnahme Einstellungen für die virtuelle Maschine darstellt, ist dieser Wert die Zeit, zu der die Momentaufnahme erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="727ab-315">If this object represents the snapshot settings for the virtual machine, this value would be the time at which the snapshot was taken.</span></span> <span data-ttu-id="727ab-316">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="727ab-316">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="727ab-317">**"Debug-channelid"**</span><span class="sxs-lookup"><span data-stu-id="727ab-317">**DebugChannelId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-318">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="727ab-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-319">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="727ab-319">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="727ab-320">Der Kanal Bezeichner, der zum Debuggen des virtuellen Computers mit dem Unified Debugger verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="727ab-320">The channel identifier used to debug the virtual machine using the unified debugger.</span></span>

</dd> <dt>

<span data-ttu-id="727ab-321">**Debugport**</span><span class="sxs-lookup"><span data-stu-id="727ab-321">**DebugPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-322">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="727ab-322">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-323">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="727ab-323">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="727ab-324">Der TCP/IP-Port, der zum Debuggen des virtuellen Computers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="727ab-324">The TCP/IP port used to debug the virtual machine using synthetic debugging.</span></span>

</dd> <dt>

<span data-ttu-id="727ab-325">**"Debug-portenabled"**</span><span class="sxs-lookup"><span data-stu-id="727ab-325">**DebugPortEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-326">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="727ab-326">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-327">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="727ab-327">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="727ab-328">Gibt an, ob der virtuelle Computer synthetisches Debuggen verwendet.</span><span class="sxs-lookup"><span data-stu-id="727ab-328">Specifies whether the virtual machine is using synthetic debugging.</span></span> <span data-ttu-id="727ab-329">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="727ab-329">This can be one of the following values.</span></span>

<dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="727ab-330"><span id="Off"></span><span id="off"></span><span id="OFF"></span>**Aus** (0)</span><span class="sxs-lookup"><span data-stu-id="727ab-330"><span id="Off"></span><span id="off"></span><span id="OFF"></span>**Off** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="On"></span><span id="on"></span><span id="ON"></span>

<span data-ttu-id="727ab-331"><span id="On"></span><span id="on"></span><span id="ON"></span>Ein **(1** )</span><span class="sxs-lookup"><span data-stu-id="727ab-331"><span id="On"></span><span id="on"></span><span id="ON"></span>**On** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>

<span data-ttu-id="727ab-332"><span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>**Onautoassigned** (2)</span><span class="sxs-lookup"><span data-stu-id="727ab-332"><span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>**OnAutoAssigned** (2)</span></span>


</dt> <dd>

<span data-ttu-id="727ab-333">Automatisch zugewiesen</span><span class="sxs-lookup"><span data-stu-id="727ab-333">Auto-assigned</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="727ab-334">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="727ab-334">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-335">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="727ab-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-336">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="727ab-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="727ab-337">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="727ab-337">A description of the object.</span></span> <span data-ttu-id="727ab-338">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf einen der folgenden Werte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="727ab-338">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to one of the following values.</span></span>



| <span data-ttu-id="727ab-339">Wert</span><span class="sxs-lookup"><span data-stu-id="727ab-339">Value</span></span>                                                                                                                  | <span data-ttu-id="727ab-340">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="727ab-340">Meaning</span></span>                                               |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="727ab-341"><dt>"Aktive Einstellungen für den virtuellen Computer"</dt></span><span class="sxs-lookup"><span data-stu-id="727ab-341"><dt>"Active settings for the virtual machine"</dt></span></span> </dl>   | <span data-ttu-id="727ab-342">Diese Instanz verweist auf einen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="727ab-342">This instance refers to a virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="727ab-343"><dt>"Momentaufnahme Einstellungen für den virtuellen Computer"</dt></span><span class="sxs-lookup"><span data-stu-id="727ab-343"><dt>"Snapshot settings for the virtual machine"</dt></span></span> </dl> | <span data-ttu-id="727ab-344">Diese Instanz verweist auf eine Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="727ab-344">This instance refers to a snapshot.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="727ab-345">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="727ab-345">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-346">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="727ab-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-347">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="727ab-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="727ab-348">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="727ab-348">A display name for the object.</span></span> <span data-ttu-id="727ab-349">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt und wird immer auf den anzeigen Amen für den Computer festgelegt.</span><span class="sxs-lookup"><span data-stu-id="727ab-349">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and it is always set to the display name for the machine.</span></span> <span data-ttu-id="727ab-350">Dieser Name darf nicht länger als 100 Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="727ab-350">This name may not exceed 100 characters in length.</span></span>

</dd> <dt>

<span data-ttu-id="727ab-351">**Enhancedsessiontransporttype**</span><span class="sxs-lookup"><span data-stu-id="727ab-351">**EnhancedSessionTransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-352">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="727ab-352">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-353">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="727ab-353">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="727ab-354">Gibt den Transporttyp an, der beim Herstellen einer Verbindung mit einer erweiterten Sitzung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="727ab-354">Indicates the transport type to use when connecting to an enhanced session.</span></span>

> [!Note]  
> <span data-ttu-id="727ab-355">Diese Eigenschaft wurde in Windows 10, Version 1803, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="727ab-355">This property was added in Windows 10, version 1803.</span></span>

 

<dt>

<span id="VMBus_Pipe"></span><span id="vmbus_pipe"></span><span id="VMBUS_PIPE"></span>

<span data-ttu-id="727ab-356">**VMBus-Pipe** (0)</span><span class="sxs-lookup"><span data-stu-id="727ab-356">**VMBus Pipe** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Hyper-V_Socket"></span><span id="hyper-v_socket"></span><span id="HYPER-V_SOCKET"></span>

<span data-ttu-id="727ab-357">**Hyper-V-Socket** (1)</span><span class="sxs-lookup"><span data-stu-id="727ab-357">**Hyper-V Socket** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="727ab-358">**Guestcontrolledcachetypes**</span><span class="sxs-lookup"><span data-stu-id="727ab-358">**GuestControlledCacheTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-359">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="727ab-359">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-360">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="727ab-360">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="727ab-361">Gibt an, ob der Gast Cache Typen steuern kann.</span><span class="sxs-lookup"><span data-stu-id="727ab-361">Indicates whether the guest can control cache types.</span></span>

> [!Note]  
> <span data-ttu-id="727ab-362">In Windows 10 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="727ab-362">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="727ab-363">**Gueststatedataroot**</span><span class="sxs-lookup"><span data-stu-id="727ab-363">**GuestStateDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-364">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="727ab-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-365">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="727ab-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="727ab-366">Dateipfad eines Verzeichnisses, in dem Informationen über den Gast Lauf Zeit Zustand gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="727ab-366">Filepath of a directory where information about the guest runtime state is stored.</span></span>

> [!Note]  
> <span data-ttu-id="727ab-367">Hinzugefügt in Windows 10, Version 1709.</span><span class="sxs-lookup"><span data-stu-id="727ab-367">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="727ab-368">**Gueststatefile**</span><span class="sxs-lookup"><span data-stu-id="727ab-368">**GuestStateFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-369">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="727ab-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-370">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="727ab-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="727ab-371">Dateipfad einer Datei, in der Informationen über den Gast Lauf Zeit Zustand gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="727ab-371">Filepath of a file where information about the guest runtime state is stored.</span></span> <span data-ttu-id="727ab-372">Ein relativer Pfad wird an den Wert der **gueststatedataroot** -Eigenschaft angefügt.</span><span class="sxs-lookup"><span data-stu-id="727ab-372">A relative path appends to the value of the **GuestStateDataRoot** property.</span></span>

> [!Note]  
> <span data-ttu-id="727ab-373">Hinzugefügt in Windows 10, Version 1709.</span><span class="sxs-lookup"><span data-stu-id="727ab-373">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="727ab-374">**Highmmiogapsize**</span><span class="sxs-lookup"><span data-stu-id="727ab-374">**HighMmioGapSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-375">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="727ab-375">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-376">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="727ab-376">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="727ab-377">Die Größe des oberen (über 4 GB) Memory-Mapped e/a-GAP in MB</span><span class="sxs-lookup"><span data-stu-id="727ab-377">The size of the High (above 4GB) Memory-Mapped IO Gap in MB</span></span>

> [!Note]  
> <span data-ttu-id="727ab-378">Diese Eigenschaft wurde in Windows 10, Version 1703, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="727ab-378">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="727ab-379">**Incrementalbackupabled**</span><span class="sxs-lookup"><span data-stu-id="727ab-379">**IncrementalBackupEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-380">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="727ab-380">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-381">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="727ab-381">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="727ab-382">Gibt an, ob die Hyper-V-VSS Writer die das inkrementelle sichern dieser virtuellen Maschine unterstützt.</span><span class="sxs-lookup"><span data-stu-id="727ab-382">Indicates whether the Hyper-V VSS writer supports taking incremental backups of this virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="727ab-383">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="727ab-383">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-384">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="727ab-384">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-385">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="727ab-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="727ab-386">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="727ab-386">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="727ab-387">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="727ab-387">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="727ab-388">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="727ab-388">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="727ab-389">**Isautomaticsnapshot**</span><span class="sxs-lookup"><span data-stu-id="727ab-389">**IsAutomaticSnapshot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-390">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="727ab-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-391">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="727ab-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="727ab-392">Gibt an, ob es sich um eine für den Benutzer automatisch erstellte Momentaufnahme handelt.</span><span class="sxs-lookup"><span data-stu-id="727ab-392">Indicates whether this is a snapshot created automatically for the user.</span></span>

> [!Note]  
> <span data-ttu-id="727ab-393">Hinzugefügt in Windows 10, Version 1709.</span><span class="sxs-lookup"><span data-stu-id="727ab-393">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="727ab-394">**IsSaved**</span><span class="sxs-lookup"><span data-stu-id="727ab-394">**IsSaved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-395">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="727ab-395">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-396">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="727ab-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="727ab-397">**True** , wenn die Konfiguration einen Verweis auf eine gespeicherte Zustands Datei enthält. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="727ab-397">**True** if the configuration has a reference to a saved state file; otherwise, **False**.</span></span> <span data-ttu-id="727ab-398">Dies deutet nicht darauf hin, dass eine solche Datei vorhanden ist, sondern nur, dass die Konfiguration eine Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="727ab-398">This does not indicate the presence of such a file, only that the configuration specifies one.</span></span>

</dd> <dt>

<span data-ttu-id="727ab-399">**Lockondisconnect**</span><span class="sxs-lookup"><span data-stu-id="727ab-399">**LockOnDisconnect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-400">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="727ab-400">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-401">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="727ab-401">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="727ab-402">Sperren Sie die Konsole, wenn Sie die Verbindung mit VMConnect trennen.</span><span class="sxs-lookup"><span data-stu-id="727ab-402">Lock the console when disconnecting from vmconnect.</span></span>

> [!Note]  
> <span data-ttu-id="727ab-403">In Windows 10 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="727ab-403">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="727ab-404">**Logdataroot**</span><span class="sxs-lookup"><span data-stu-id="727ab-404">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-405">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="727ab-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-406">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="727ab-406">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="727ab-407">Der Pfad eines Verzeichnisses, in dem Protokollinformationen für den virtuellen Computer gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="727ab-407">The path of a directory where log information for the virtual machine is stored.</span></span> <span data-ttu-id="727ab-408">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="727ab-408">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="727ab-409">**Lowmmiogapsize**</span><span class="sxs-lookup"><span data-stu-id="727ab-409">**LowMmioGapSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-410">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="727ab-410">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-411">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="727ab-411">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="727ab-412">Hiermit wird die Größe der ersten MMIO-Lücke für einen virtuellen Computer (VM) in Megabyte konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="727ab-412">Configures the size, in megabytes, of the first MMIO gap for a virtual machine (VM).</span></span>

<span data-ttu-id="727ab-413">**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="727ab-413">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<span data-ttu-id="727ab-414">Bereich: 128 3584</span><span class="sxs-lookup"><span data-stu-id="727ab-414">Range: 128 3584</span></span>

</dd> <dt>

<span data-ttu-id="727ab-415">**Network bootpreferredprotocol**</span><span class="sxs-lookup"><span data-stu-id="727ab-415">**NetworkBootPreferredProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-416">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="727ab-416">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-417">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="727ab-417">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="727ab-418">Bestimmt, ob das bevorzugte Protokoll für den PXE-Start IPv4 oder IPv6 ist.</span><span class="sxs-lookup"><span data-stu-id="727ab-418">Determines if the preferred protocol for PXE boot is IPv4 or IPv6.</span></span>

<span data-ttu-id="727ab-419">**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="727ab-419">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="727ab-420">**IPv4** (4096)</span><span class="sxs-lookup"><span data-stu-id="727ab-420">**IPv4** (4096)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="727ab-421">**IPv6** (4097)</span><span class="sxs-lookup"><span data-stu-id="727ab-421">**IPv6** (4097)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="727ab-422">**Hinweise**</span><span class="sxs-lookup"><span data-stu-id="727ab-422">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-423">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="727ab-423">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="727ab-424">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="727ab-424">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="727ab-425">Vom Benutzer bereitgestellte Hinweise zum virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="727ab-425">User supplied notes that are related to the virtual machine.</span></span> <span data-ttu-id="727ab-426">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="727ab-426">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="727ab-427">**Parent**</span><span class="sxs-lookup"><span data-stu-id="727ab-427">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-428">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="727ab-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-429">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="727ab-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="727ab-430">Wenn diese Instanz kein System darstellt, das auf einer Momentaufnahme einer virtuellen Maschine basiert, ist diese Eigenschaft **null**.</span><span class="sxs-lookup"><span data-stu-id="727ab-430">If this instance does not represent a system based on a snapshot of a virtual machine, this property is **Null**.</span></span> <span data-ttu-id="727ab-431">Andernfalls enthält die Eigenschaft den Objekt Pfad des **MSVM \_ virtualsystemsettingdata** -Objekts, auf dem diese Instanz basiert.</span><span class="sxs-lookup"><span data-stu-id="727ab-431">Otherwise, the property holds the object path of the **Msvm\_VirtualSystemSettingData** object on which this instance is based.</span></span> <span data-ttu-id="727ab-432">Beim Erstellen einer Momentaufnahme Struktur Hierarchie für den virtuellen Computer verweist diese Eigenschaft auf das Objekt, von dem die aktuelle Instanz abgeleitet wird (die aktuelle Instanz ist der untergeordnete Knoten, und das Objekt, auf das in dieser Eigenschaft verwiesen wird, ist der übergeordnete Knoten.)</span><span class="sxs-lookup"><span data-stu-id="727ab-432">When building a snapshot tree hierarchy for the virtual machine, this property references the object from which the current instance is derived (the current instance is the child node and the object referenced in this property is the parent node.)</span></span>

</dd> <dt>

<span data-ttu-id="727ab-433">**Paket Paket**</span><span class="sxs-lookup"><span data-stu-id="727ab-433">**ParentPackage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-434">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="727ab-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-435">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="727ab-435">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="727ab-436">Wenn es sich um einen Container handelt, ist dies der Pfad zum MSVM- \_ containerpackage, auf dem dieses System basiert.</span><span class="sxs-lookup"><span data-stu-id="727ab-436">If this system is a container, the path to the Msvm\_ContainerPackage from which this system is based.</span></span>

> [!Note]  
> <span data-ttu-id="727ab-437">In Windows 10 hinzugefügt entfernt in Windows 10, Version 1703.</span><span class="sxs-lookup"><span data-stu-id="727ab-437">Added in Windows 10; removed in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="727ab-438">**Pauseafterbootfailure**</span><span class="sxs-lookup"><span data-stu-id="727ab-438">**PauseAfterBootFailure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-439">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="727ab-439">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-440">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="727ab-440">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="727ab-441">Gibt an, ob das BIOS nach jedem Fehler beim Start Eintrag angehalten wird, wenn der Benutzer eine Taste drückt.</span><span class="sxs-lookup"><span data-stu-id="727ab-441">Indicates whether the BIOS pauses after every boot entry failure waiting for the user to press a key.</span></span> <span data-ttu-id="727ab-442">**True** , wenn das BIOS angehalten wird. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="727ab-442">**True** if the BIOS pauses; otherwise, **False**.</span></span>

<span data-ttu-id="727ab-443">**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="727ab-443">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="727ab-444">**Wiederherstellbare Datei**</span><span class="sxs-lookup"><span data-stu-id="727ab-444">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-445">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="727ab-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-446">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="727ab-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="727ab-447">Der vollständige Pfad einer Datei, in der Wiederherstellungs bezogene Informationen für den virtuellen Computer gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="727ab-447">The full path of a file where recovery related information for the virtual machine is stored.</span></span> <span data-ttu-id="727ab-448">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="727ab-448">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="727ab-449">**"Securebootenabled"**</span><span class="sxs-lookup"><span data-stu-id="727ab-449">**SecureBootEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-450">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="727ab-450">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-451">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="727ab-451">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="727ab-452">Gibt an, ob der sichere Start für den virtuellen Computer (VM) aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="727ab-452">Indicates whether secure boot is enabled for the virtual machine (VM).</span></span> <span data-ttu-id="727ab-453">**True** , wenn aktiviert; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="727ab-453">**True** if enabled; otherwise, **False**.</span></span>

> [!Note]  
> <span data-ttu-id="727ab-454">Der sichere Start kann nur für VMS der Generation 2 aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="727ab-454">Secure boot can only be enabled for generation 2 VMs.</span></span>

 

<span data-ttu-id="727ab-455">**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="727ab-455">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="727ab-456">**Secureboottemplateid**</span><span class="sxs-lookup"><span data-stu-id="727ab-456">**SecureBootTemplateId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-457">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="727ab-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-458">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="727ab-458">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="727ab-459">Der Global eindeutige Bezeichner der Vorlage mit den Anfangs-Werten von UEFI-Variablen für den sicheren Start.</span><span class="sxs-lookup"><span data-stu-id="727ab-459">The globally-unique identifier of the template of intial values of UEFI Secure Boot related variables.</span></span>

<span data-ttu-id="727ab-460">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyvirtualsystem**](https://www.bing.com/search?q=**ModifyVirtualSystem**) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="727ab-460">This is a read-only property, but it can be changed using the [**ModifyVirtualSystem**](https://www.bing.com/search?q=**ModifyVirtualSystem**) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="727ab-461">In Windows 10 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="727ab-461">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="727ab-462">**Snapshotdataroot**</span><span class="sxs-lookup"><span data-stu-id="727ab-462">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-463">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="727ab-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-464">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="727ab-464">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="727ab-465">Der Pfad eines Verzeichnisses, in dem Informationen zu den Momentaufnahmen der virtuellen Maschine gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="727ab-465">The path of a directory where information about the virtual machine snapshots is stored.</span></span> <span data-ttu-id="727ab-466">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="727ab-466">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="727ab-467">**Suspenddataroot**</span><span class="sxs-lookup"><span data-stu-id="727ab-467">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-468">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="727ab-468">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-469">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="727ab-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="727ab-470">Der Pfad eines Verzeichnisses, in dem Informationen zu den Informationen zum Aussetzen der virtuellen Maschine gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="727ab-470">The path of a directory where information about the virtual machine suspend-related information is stored.</span></span> <span data-ttu-id="727ab-471">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="727ab-471">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="727ab-472">**Austauschen von Daten**</span><span class="sxs-lookup"><span data-stu-id="727ab-472">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-473">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="727ab-473">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-474">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="727ab-474">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="727ab-475">Der Pfad eines Verzeichnisses, in dem die Auslagerungs Dateien für den virtuellen Computer gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="727ab-475">The path of a directory where swap files for the virtual machine are stored.</span></span> <span data-ttu-id="727ab-476">Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="727ab-476">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="727ab-477">**Usersnapshottype**</span><span class="sxs-lookup"><span data-stu-id="727ab-477">**UserSnapshotType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-478">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="727ab-478">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-479">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="727ab-479">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="727ab-480">Gibt den Typ der benutzerdefinierten Momentaufnahme an.</span><span class="sxs-lookup"><span data-stu-id="727ab-480">Indicates the user-defined snapshot type.</span></span>

> [!Note]  
> <span data-ttu-id="727ab-481">In Windows 10 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="727ab-481">Added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="727ab-482"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Deaktivieren** (2)</span><span class="sxs-lookup"><span data-stu-id="727ab-482"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="727ab-483">Hiermit wird die Erstellung einer Momentaufnahme deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="727ab-483">Disable the creation of any snapshot.</span></span>

</dd> <dt>

<span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>

<span data-ttu-id="727ab-484"><span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>**Productionfallbacktetest** (3)</span><span class="sxs-lookup"><span data-stu-id="727ab-484"><span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>**ProductionFallbackToTest** (3)</span></span>


</dt> <dd>

<span data-ttu-id="727ab-485">Daten konsistente Momentaufnahme für die Verwendung in der Produktionsumgebung. Führt eine Momentaufnahme mit einem Anwendungs Zustand aus, wenn die Möglichkeit zum Erstellen einer Daten konsistenten Momentaufnahme nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="727ab-485">Data-consistent snapshot for use in the production environment.Performs a snapshot with application state when the ability to create data consistent snapshot is not available.</span></span>

</dd> <dt>

<span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>

<span data-ttu-id="727ab-486"><span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>**Productionnofallback** (4)</span><span class="sxs-lookup"><span data-stu-id="727ab-486"><span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>**ProductionNoFallback** (4)</span></span>


</dt> <dd>

<span data-ttu-id="727ab-487">Daten konsistente Momentaufnahme für die Verwendung in der Produktionsumgebung. Erstellt keine Momentaufnahme mit dem Anwendungs Zustand, wenn keine Daten konsistente Momentaufnahme erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="727ab-487">Data-consistent snapshot for use in the production environment.Does not create a snapshot with application state if it is not possible to create a data consistent snapshot.</span></span>

</dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="727ab-488"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (5)</span><span class="sxs-lookup"><span data-stu-id="727ab-488"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (5)</span></span>


</dt> <dd>

<span data-ttu-id="727ab-489">Momentaufnahme, die Arbeitsspeicher-und Geräteinformationen zu Test-und Entwicklungszwecken enthält.</span><span class="sxs-lookup"><span data-stu-id="727ab-489">Snapshot that contains memory and device information for test and development purpose.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="727ab-490">**Version**</span><span class="sxs-lookup"><span data-stu-id="727ab-490">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-491">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="727ab-491">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-492">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="727ab-492">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="727ab-493">Die Version des virtuellen Computers im Format "Major. Minor", z. b. "2,0".</span><span class="sxs-lookup"><span data-stu-id="727ab-493">The version of the virtual machine in a format of "major.minor", for example "2.0".</span></span>

</dd> <dt>

<span data-ttu-id="727ab-494">**Virtualnumaaktivierte**</span><span class="sxs-lookup"><span data-stu-id="727ab-494">**VirtualNumaEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-495">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="727ab-495">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-496">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="727ab-496">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="727ab-497">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**MSVM \_ processorsettingdata**](msvm-processorsettingdata.md).**Maxprocessorspernumanode**","[**MSVM \_ memorysettingdata**](msvm-memorysettingdata.md).**Maxmemoryblockspernumanode**")</span><span class="sxs-lookup"><span data-stu-id="727ab-497">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_ProcessorSettingData**](msvm-processorsettingdata.md).**MaxProcessorsPerNumaNode**", "[**Msvm\_MemorySettingData**](msvm-memorysettingdata.md).**MaxMemoryBlocksPerNumaNode**")</span></span>
</dt> </dl>

<span data-ttu-id="727ab-498">**True** , wenn virtuelle NUMA-Knoten (Non-Uniform Memory Access, nicht einheitlicher Speicherzugriff) in den virtuellen Computer projiziert werden. **False** , wenn der virtuelle Computer über einen einzelnen Knoten verfügt.</span><span class="sxs-lookup"><span data-stu-id="727ab-498">**True** if virtual non-uniform memory access (NUMA) nodes are projected into the virtual machine; **False** if the virtual machine will have a single node.</span></span> <span data-ttu-id="727ab-499">**True** gibt an, dass die Anzahl der virtuellen NUMA-Knoten, die in den virtuellen Computer projiziert werden, von den Werten der Eigenschaften [**MSVM \_ processorsettingdata. maxprocessorspernumanode**](msvm-processorsettingdata.md) und [**MSVM \_ memorysettingdata. maxmemoryblockspernumanode**](msvm-memorysettingdata.md) bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="727ab-499">If **True**, the number of virtual NUMA nodes projected into the virtual machine is determined from the values of the [**Msvm\_ProcessorSettingData.MaxProcessorsPerNumaNode**](msvm-processorsettingdata.md) and [**Msvm\_MemorySettingData.MaxMemoryBlocksPerNumaNode**](msvm-memorysettingdata.md) properties.</span></span>

</dd> <dt>

<span data-ttu-id="727ab-500">**Virtualsystemidentifier**</span><span class="sxs-lookup"><span data-stu-id="727ab-500">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-501">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="727ab-501">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-502">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="727ab-502">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="727ab-503">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ virtualsystemsettingdata. virtualsystedentifier"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Computersystem**](cim-computersystem.md).**Name**")</span><span class="sxs-lookup"><span data-stu-id="727ab-503">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemSettingData.VirtualSystemIdentifier"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="727ab-504">Der Name des [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Objekts, zu dem diese Einstellungsdaten gehören.</span><span class="sxs-lookup"><span data-stu-id="727ab-504">The name of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) object to which this setting data belongs.</span></span> <span data-ttu-id="727ab-505">Diese Eigenschaft ist eine außer Kraft Setzung von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="727ab-505">This property is an override from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="727ab-506">**VirtualSystemSubType**</span><span class="sxs-lookup"><span data-stu-id="727ab-506">**VirtualSystemSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-507">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="727ab-507">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-508">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="727ab-508">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="727ab-509">Gültige Werte für diese Eigenschaft sind Microsoft: Hyper-v: SubType: 1 und Microsoft: Hyper-v: SubType: 2.</span><span class="sxs-lookup"><span data-stu-id="727ab-509">The valid values for this property are Microsoft:Hyper-V:SubType:1 and Microsoft:Hyper-V:SubType:2.</span></span> <span data-ttu-id="727ab-510">Eine VM der Generation 1 ist Untertyp 1.</span><span class="sxs-lookup"><span data-stu-id="727ab-510">A  Generation 1  VM is subtype 1.</span></span> <span data-ttu-id="727ab-511">Eine VM der Generation 2 ist der Untertyp 2.</span><span class="sxs-lookup"><span data-stu-id="727ab-511">A  Generation 2  VM is subtype 2.</span></span>

<span data-ttu-id="727ab-512">**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="727ab-512">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

<span data-ttu-id="727ab-513">**Microsoft: Hyper-v: Untertyp: 1** ("Microsoft: Hyper-v: SubType: 1")</span><span class="sxs-lookup"><span data-stu-id="727ab-513">**Microsoft:Hyper-V:SubType:1** ("Microsoft:Hyper-V:SubType:1")</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

<span data-ttu-id="727ab-514">**Microsoft: Hyper-v: SubType: 2** ("Microsoft: Hyper-v: SubType: 2")</span><span class="sxs-lookup"><span data-stu-id="727ab-514">**Microsoft:Hyper-V:SubType:2** ("Microsoft:Hyper-V:SubType:2")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="727ab-515">**Virtualsystemtype**</span><span class="sxs-lookup"><span data-stu-id="727ab-515">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="727ab-516">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="727ab-516">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="727ab-517">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="727ab-517">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="727ab-518">Gibt den Typ der virtuellen Maschine an, die die Einstellungsdaten darstellen.</span><span class="sxs-lookup"><span data-stu-id="727ab-518">Specifies the type of virtual machine the setting data represents.</span></span> <span data-ttu-id="727ab-519">Diese Eigenschaft wird von der [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85)) -Klasse geerbt.</span><span class="sxs-lookup"><span data-stu-id="727ab-519">This property is inherited from the [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) class.</span></span> <span data-ttu-id="727ab-520">Dabei handelt es sich um einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="727ab-520">This will be one of the following values.</span></span>



| <span data-ttu-id="727ab-521">Wert</span><span class="sxs-lookup"><span data-stu-id="727ab-521">Value</span></span>                                                                                                                                 | <span data-ttu-id="727ab-522">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="727ab-522">Meaning</span></span>                                              |
|---------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="727ab-523"><dt>"Microsoft: Hyper-V: System: realisiert"</dt></span><span class="sxs-lookup"><span data-stu-id="727ab-523"><dt>"Microsoft:Hyper-V:System:Realized"</dt></span></span> </dl>                        | <span data-ttu-id="727ab-524">Ein realisierter virtueller Computer.</span><span class="sxs-lookup"><span data-stu-id="727ab-524">A realized virtual machine.</span></span><br/>               |
| <dl> <span data-ttu-id="727ab-525"><dt>"Microsoft: Hyper-V: System: geplant"</dt></span><span class="sxs-lookup"><span data-stu-id="727ab-525"><dt>"Microsoft:Hyper-V:System:Planned"</dt></span></span> </dl>                         | <span data-ttu-id="727ab-526">Eine geplante virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="727ab-526">A planned virtual machine.</span></span><br/>                |
| <dl> <span data-ttu-id="727ab-527"><dt>"Microsoft: Hyper-V: Snapshot: realisiert"</dt></span><span class="sxs-lookup"><span data-stu-id="727ab-527"><dt>"Microsoft:Hyper-V:Snapshot:Realized"</dt></span></span> </dl>                      | <span data-ttu-id="727ab-528">Eine Momentaufnahme eines erkannten virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="727ab-528">A snapshot of a realized virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="727ab-529"><dt>"Microsoft: Hyper-V: Snapshot: Recovery"</dt></span><span class="sxs-lookup"><span data-stu-id="727ab-529"><dt>"Microsoft:Hyper-V:Snapshot:Recovery"</dt></span></span> </dl>                      | <span data-ttu-id="727ab-530">Eine Momentaufnahme eines virtuellen Wiederherstellungs Computers.</span><span class="sxs-lookup"><span data-stu-id="727ab-530">A snapshot of a recovery virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="727ab-531"><dt>"Microsoft: Hyper-V: Snapshot: geplant"</dt></span><span class="sxs-lookup"><span data-stu-id="727ab-531"><dt>"Microsoft:Hyper-V:Snapshot:Planned"</dt></span></span> </dl>                       | <span data-ttu-id="727ab-532">Eine Momentaufnahme eines geplanten virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="727ab-532">A snapshot of a planned virtual machine.</span></span><br/>  |
| <dl> <span data-ttu-id="727ab-533"><dt>"Microsoft: Hyper-V: Snapshot: Missing"</dt></span><span class="sxs-lookup"><span data-stu-id="727ab-533"><dt>"Microsoft:Hyper-V:Snapshot:Missing"</dt></span></span> </dl>                       | <span data-ttu-id="727ab-534">Eine fehlende Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="727ab-534">A missing snapshot.</span></span><br/>                       |
| <dl> <span data-ttu-id="727ab-535"><dt>"Microsoft: Hyper-V: Snapshot: Replica: Standard"</dt></span><span class="sxs-lookup"><span data-stu-id="727ab-535"><dt>"Microsoft:Hyper-V:Snapshot:Replica:Standard"</dt></span></span> </dl>              | <span data-ttu-id="727ab-536">Eine zeitbasierte Replikations Punkt Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="727ab-536">A time-based replication point snapshot.</span></span><br/>  |
| <dl> <span data-ttu-id="727ab-537"><dt>"Microsoft: Hyper-V: Snapshot: Replica: applicationkonsistentes"</dt></span><span class="sxs-lookup"><span data-stu-id="727ab-537"><dt>"Microsoft:Hyper-V:Snapshot:Replica:ApplicationConsistent"</dt></span></span> </dl> | <span data-ttu-id="727ab-538">Eine VSS-Replikations Punkt Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="727ab-538">A VSS replication point snapshot.</span></span><br/>         |
| <dl> <span data-ttu-id="727ab-539"><dt>"Microsoft: Hyper-V: Snapshot: Replica: plannedfailover"</dt></span><span class="sxs-lookup"><span data-stu-id="727ab-539"><dt>"Microsoft:Hyper-V:Snapshot:Replica:PlannedFailover"</dt></span></span> </dl>       | <span data-ttu-id="727ab-540">Eine geplante Replikations Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="727ab-540">A planned replication snapshot.</span></span><br/>           |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="727ab-541">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="727ab-541">Remarks</span></span>

<span data-ttu-id="727ab-542">Der Zugriff auf die **MSVM \_ virtualsystemsettingdata** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="727ab-542">Access to the **Msvm\_VirtualSystemSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="727ab-543">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="727ab-543">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="727ab-544">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="727ab-544">Requirements</span></span>



| <span data-ttu-id="727ab-545">Anforderung</span><span class="sxs-lookup"><span data-stu-id="727ab-545">Requirement</span></span> | <span data-ttu-id="727ab-546">Wert</span><span class="sxs-lookup"><span data-stu-id="727ab-546">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="727ab-547">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="727ab-547">Minimum supported client</span></span><br/> | <span data-ttu-id="727ab-548">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="727ab-548">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="727ab-549">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="727ab-549">Minimum supported server</span></span><br/> | <span data-ttu-id="727ab-550">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="727ab-550">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="727ab-551">Namespace</span><span class="sxs-lookup"><span data-stu-id="727ab-551">Namespace</span></span><br/>                | <span data-ttu-id="727ab-552">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="727ab-552">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="727ab-553">MOF</span><span class="sxs-lookup"><span data-stu-id="727ab-553">MOF</span></span><br/>                      | <dl> <span data-ttu-id="727ab-554"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="727ab-554"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="727ab-555">DLL</span><span class="sxs-lookup"><span data-stu-id="727ab-555">DLL</span></span><br/>                      | <dl> <span data-ttu-id="727ab-556"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="727ab-556"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="727ab-557">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="727ab-557">See also</span></span>

<dl> <dt>

[<span data-ttu-id="727ab-558">**CIM \_ virtualsystemsettingdata**</span><span class="sxs-lookup"><span data-stu-id="727ab-558">**CIM\_VirtualSystemSettingData**</span></span>](cim-virtualsystemsettingdata.md)
</dt> <dt>

<span data-ttu-id="727ab-559">[**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="727ab-559">[**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="727ab-560">Klassen des virtuellen Systems</span><span class="sxs-lookup"><span data-stu-id="727ab-560">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

