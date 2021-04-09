---
description: Stellt den Arbeitsspeicher dar, der einem virtuellen Computer zurzeit zugeordnet ist.
ms.assetid: 4CAA64FC-5A06-409B-9E92-32DF3F47D5FD
title: Msvm_Memory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Memory
- Msvm_Memory.SetPowerState
- Msvm_Memory.EnableDevice
- Msvm_Memory.OnlineDevice
- Msvm_Memory.QuiesceDevice
- Msvm_Memory.SaveProperties
- Msvm_Memory.RestoreProperties
- Msvm_Memory.InstanceID
- Msvm_Memory.Caption
- Msvm_Memory.Description
- Msvm_Memory.ElementName
- Msvm_Memory.InstallDate
- Msvm_Memory.OperationalStatus
- Msvm_Memory.StatusDescriptions
- Msvm_Memory.Status
- Msvm_Memory.HealthState
- Msvm_Memory.CommunicationStatus
- Msvm_Memory.DetailedStatus
- Msvm_Memory.OperatingStatus
- Msvm_Memory.PrimaryStatus
- Msvm_Memory.EnabledState
- Msvm_Memory.OtherEnabledState
- Msvm_Memory.RequestedState
- Msvm_Memory.EnabledDefault
- Msvm_Memory.TimeOfLastStateChange
- Msvm_Memory.AvailableRequestedStates
- Msvm_Memory.TransitioningToState
- Msvm_Memory.SystemCreationClassName
- Msvm_Memory.SystemName
- Msvm_Memory.CreationClassName
- Msvm_Memory.DeviceID
- Msvm_Memory.PowerManagementSupported
- Msvm_Memory.PowerManagementCapabilities
- Msvm_Memory.Availability
- Msvm_Memory.StatusInfo
- Msvm_Memory.LastErrorCode
- Msvm_Memory.ErrorDescription
- Msvm_Memory.ErrorCleared
- Msvm_Memory.OtherIdentifyingInfo
- Msvm_Memory.PowerOnHours
- Msvm_Memory.TotalPowerOnHours
- Msvm_Memory.IdentifyingDescriptions
- Msvm_Memory.AdditionalAvailability
- Msvm_Memory.MaxQuiesceTime
- Msvm_Memory.DataOrganization
- Msvm_Memory.Purpose
- Msvm_Memory.Access
- Msvm_Memory.BlockSize
- Msvm_Memory.NumberOfBlocks
- Msvm_Memory.ConsumableBlocks
- Msvm_Memory.IsBasedOnUnderlyingRedundancy
- Msvm_Memory.SequentialAccess
- Msvm_Memory.ExtentStatus
- Msvm_Memory.NoSinglePointOfFailure
- Msvm_Memory.DataRedundancy
- Msvm_Memory.PackageRedundancy
- Msvm_Memory.DeltaReservation
- Msvm_Memory.Primordial
- Msvm_Memory.Name
- Msvm_Memory.NameFormat
- Msvm_Memory.NameNamespace
- Msvm_Memory.OtherNameNamespace
- Msvm_Memory.OtherNameFormat
- Msvm_Memory.Volatile
- Msvm_Memory.ErrorMethodology
- Msvm_Memory.StartingAddress
- Msvm_Memory.EndingAddress
- Msvm_Memory.ErrorInfo
- Msvm_Memory.OtherErrorDescription
- Msvm_Memory.CorrectableError
- Msvm_Memory.ErrorTime
- Msvm_Memory.ErrorAccess
- Msvm_Memory.ErrorTransferSize
- Msvm_Memory.ErrorData
- Msvm_Memory.ErrorDataOrder
- Msvm_Memory.ErrorAddress
- Msvm_Memory.SystemLevelAddress
- Msvm_Memory.ErrorResolution
- Msvm_Memory.AdditionalErrorData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ec6b287f3281fd0224e9c2efc39391781bd7f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868511"
---
# <a name="msvm_memory-class"></a><span data-ttu-id="51583-103">MSVM- \_ Speicher Klasse</span><span class="sxs-lookup"><span data-stu-id="51583-103">Msvm\_Memory class</span></span>

<span data-ttu-id="51583-104">Stellt den Arbeitsspeicher dar, der einem virtuellen Computer zurzeit zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="51583-104">Represents the memory currently allocated to a virtual machine.</span></span>

<span data-ttu-id="51583-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="51583-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="51583-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="51583-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Memory : CIM_Memory
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   CreationClassName;
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  uint16   DataOrganization = 2;
  string   Purpose = "System Memory";
  uint16   Access = 3;
  uint64   BlockSize = 1048576;
  uint64   NumberOfBlocks;
  uint64   ConsumableBlocks;
  boolean  IsBasedOnUnderlyingRedundancy = False;
  boolean  SequentialAccess = False;
  uint16   ExtentStatus[] = 2;
  boolean  NoSinglePointOfFailure = False;
  uint16   DataRedundancy = 1;
  uint16   PackageRedundancy = 0;
  uint8    DeltaReservation = 0;
  boolean  Primordial;
  string   Name = "GUID";
  uint16   NameFormat = 0;
  uint16   NameNamespace = 0;
  string   OtherNameNamespace;
  string   OtherNameFormat;
  boolean  Volatile = True;
  string   ErrorMethodology;
  uint64   StartingAddress = 0;
  uint64   EndingAddress;
  uint16   ErrorInfo;
  string   OtherErrorDescription;
  boolean  CorrectableError;
  datetime ErrorTime;
  uint16   ErrorAccess;
  uint32   ErrorTransferSize;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  uint64   ErrorAddress;
  boolean  SystemLevelAddress;
  uint64   ErrorResolution;
  uint8    AdditionalErrorData[];
};
```

## <a name="members"></a><span data-ttu-id="51583-107">Member</span><span class="sxs-lookup"><span data-stu-id="51583-107">Members</span></span>

<span data-ttu-id="51583-108">Die **MSVM- \_ Speicher** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="51583-108">The **Msvm\_Memory** class has these types of members:</span></span>

-   [<span data-ttu-id="51583-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="51583-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="51583-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51583-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="51583-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="51583-111">Methods</span></span>

<span data-ttu-id="51583-112">Die **MSVM- \_ Speicher** Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="51583-112">The **Msvm\_Memory** class has these methods.</span></span>



| <span data-ttu-id="51583-113">Methode</span><span class="sxs-lookup"><span data-stu-id="51583-113">Method</span></span>                                                       | <span data-ttu-id="51583-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="51583-114">Description</span></span>                              |
|:-------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="51583-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="51583-115">**EnableDevice**</span></span>                                             | <span data-ttu-id="51583-116">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="51583-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="51583-117">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="51583-117">**OnlineDevice**</span></span>                                             | <span data-ttu-id="51583-118">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="51583-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="51583-119">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="51583-119">**QuiesceDevice**</span></span>                                            | <span data-ttu-id="51583-120">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="51583-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="51583-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="51583-121">**RequestStateChange**</span></span>](msvm-memory-requeststatechange.md) | <span data-ttu-id="51583-122">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="51583-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="51583-123">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="51583-123">**Reset**</span></span>](msvm-memory-reset.md)                           | <span data-ttu-id="51583-124">Setzt den virtuellen Arbeitsspeicher zurück.</span><span class="sxs-lookup"><span data-stu-id="51583-124">Resets the virtual memory.</span></span><br/>    |
| <span data-ttu-id="51583-125">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="51583-125">**RestoreProperties**</span></span>                                        | <span data-ttu-id="51583-126">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="51583-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="51583-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="51583-127">**SaveProperties**</span></span>                                           | <span data-ttu-id="51583-128">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="51583-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="51583-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="51583-129">**SetPowerState**</span></span>                                            | <span data-ttu-id="51583-130">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="51583-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="51583-131">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51583-131">Properties</span></span>

<span data-ttu-id="51583-132">Die **MSVM- \_ Speicher** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="51583-132">The **Msvm\_Memory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="51583-133">**zugreifen**</span><span class="sxs-lookup"><span data-stu-id="51583-133">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-134">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51583-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51583-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-136">Beschreibt die Lese-/Schreibeigenschaften des Mediums.</span><span class="sxs-lookup"><span data-stu-id="51583-136">Describes the read/write properties of the media.</span></span> <span data-ttu-id="51583-137">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt und ist standardmäßig auf 3 festgelegt (Lese-/Schreibzugriff wird unterstützt).</span><span class="sxs-lookup"><span data-stu-id="51583-137">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is set to 3 (Read/Write Supported) by default.</span></span>

</dd> <dt>

<span data-ttu-id="51583-138">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="51583-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-139">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="51583-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="51583-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-141">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist auf 6 festgelegt (nicht zutreffend).</span><span class="sxs-lookup"><span data-stu-id="51583-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="51583-142">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="51583-142">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-143">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="51583-143">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="51583-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-145">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](/windows/desktop/CIMWin32Prov/cim-memory)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51583-145">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="51583-146">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="51583-146">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-147">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51583-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51583-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-149">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="51583-149">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="51583-150">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="51583-150">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-151">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="51583-151">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="51583-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-153">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="51583-153">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="51583-154">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="51583-154">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="51583-155">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="51583-155">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-156">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="51583-156">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="51583-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-158">Die Größe (in Bytes) der Blöcke, die den Speicherblock bilden.</span><span class="sxs-lookup"><span data-stu-id="51583-158">The size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="51583-159">Bei variabler Blockgröße sollte die maximale Blockgröße in Bytes angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="51583-159">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="51583-160">Wenn die Blockgröße unbekannt ist oder ein Block Konzept nicht gültig ist (z. b. für Aggregat Blöcke, Arbeitsspeicher oder logische Datenträger), geben Sie 1 (eins) ein.</span><span class="sxs-lookup"><span data-stu-id="51583-160">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span> <span data-ttu-id="51583-161">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt und ist immer auf 1048576 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51583-161">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 1048576.</span></span>

</dd> <dt>

<span data-ttu-id="51583-162">**Caption**</span><span class="sxs-lookup"><span data-stu-id="51583-162">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-163">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51583-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51583-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-165">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="51583-165">A short description of the object.</span></span> <span data-ttu-id="51583-166">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="51583-166">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="51583-167">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="51583-167">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-168">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51583-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51583-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-170">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="51583-170">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="51583-171">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="51583-171">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="51583-172">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="51583-172">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="51583-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="51583-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="51583-174"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="51583-174"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="51583-175"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="51583-175"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="51583-176"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="51583-176"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="51583-177"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="51583-177"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="51583-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="51583-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="51583-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="51583-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="51583-180">)</span><span class="sxs-lookup"><span data-stu-id="51583-180">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="51583-181">**Consumableblocks**</span><span class="sxs-lookup"><span data-stu-id="51583-181">**ConsumableBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-182">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="51583-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="51583-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-184">Die maximale Anzahl von Blöcken der Größe **Blockgröße**, die für die Nutzung verfügbar sind, wenn die Schichten Speicherblöcke mithilfe der BasedOn-Zuordnung erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="51583-184">The maximum number of blocks, of size **BlockSize**, that are available for consumption when layering storage extents using the BasedOn association.</span></span> <span data-ttu-id="51583-185">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51583-185">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="51583-186">**Korrektur Fehler**</span><span class="sxs-lookup"><span data-stu-id="51583-186">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-187">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51583-187">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="51583-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-189">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](/windows/desktop/CIMWin32Prov/cim-memory)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51583-189">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="51583-190">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="51583-190">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-191">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51583-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51583-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-193">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="51583-193">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="51583-194">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="51583-194">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="51583-195">**Dataorganization**</span><span class="sxs-lookup"><span data-stu-id="51583-195">**DataOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-196">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51583-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51583-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-198">Der Typ der verwendeten Datenorganisation.</span><span class="sxs-lookup"><span data-stu-id="51583-198">The type of data organization used.</span></span> <span data-ttu-id="51583-199">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt und ist immer auf 2 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51583-199">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 2.</span></span>

</dd> <dt>

<span data-ttu-id="51583-200">**Dataredundancy**</span><span class="sxs-lookup"><span data-stu-id="51583-200">**DataRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-201">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51583-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51583-202">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-203">Die Anzahl der kompletten Kopien von Daten, die zurzeit verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="51583-203">The number of complete copies of data that is currently maintained.</span></span> <span data-ttu-id="51583-204">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt und ist immer auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51583-204">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="51583-205">**Delta Service**</span><span class="sxs-lookup"><span data-stu-id="51583-205">**DeltaReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-206">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="51583-206">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="51583-207">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-208">Der aktuelle Wert für die Delta Reservierung.</span><span class="sxs-lookup"><span data-stu-id="51583-208">The current value for delta reservation.</span></span> <span data-ttu-id="51583-209">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt und immer auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51583-209">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="51583-210">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="51583-210">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-211">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51583-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51583-212">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-213">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="51583-213">A description of the object.</span></span> <span data-ttu-id="51583-214">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="51583-214">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="51583-215">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="51583-215">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-216">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51583-216">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51583-217">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-218">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="51583-218">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="51583-219">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="51583-219">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="51583-220">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="51583-220">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="51583-221"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="51583-221"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="51583-222"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="51583-222"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="51583-223"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="51583-223"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="51583-224"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="51583-224"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="51583-225"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="51583-225"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="51583-226"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="51583-226"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="51583-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="51583-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="51583-228"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="51583-228"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="51583-229">)</span><span class="sxs-lookup"><span data-stu-id="51583-229">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="51583-230">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="51583-230">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-231">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51583-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51583-232">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-233">Eine Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="51583-233">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="51583-234">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="51583-234">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="51583-235">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="51583-235">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-236">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51583-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51583-237">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-238">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="51583-238">A display name for the object.</span></span> <span data-ttu-id="51583-239">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="51583-239">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="51583-240">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="51583-240">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-241">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51583-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51583-242">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-243">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="51583-243">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="51583-244">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="51583-244">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="51583-245">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="51583-245">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-246">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51583-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51583-247">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-248">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="51583-248">The enabled and disabled states of an element.</span></span> <span data-ttu-id="51583-249">Sie kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben.</span><span class="sxs-lookup"><span data-stu-id="51583-249">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="51583-250">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="51583-250">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="51583-251">Wert</span><span class="sxs-lookup"><span data-stu-id="51583-251">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="51583-252">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="51583-252">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="51583-253"><dt>**Unbekannter**</dt> Wert <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="51583-253"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="51583-254">Der Zustand des Elements konnte nicht bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="51583-254">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="51583-255"><dt>**Sonstige**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="51583-255"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="51583-256"><dt>**Aktiviert**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="51583-256"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="51583-257">Das-Element wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="51583-257">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="51583-258"><dt>**Deaktiviert**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="51583-258"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="51583-259">Das Element ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="51583-259">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="51583-260"><dt>4</dt> wird <dt>**heruntergefahren**</dt></span><span class="sxs-lookup"><span data-stu-id="51583-260"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="51583-261">Das Element wird gerade in den deaktivierten Zustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="51583-261">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="51583-262"><dt>**Nicht zutreffend**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="51583-262"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="51583-263">Das Element unterstützt das Aktivieren oder Deaktivieren des Elements nicht.</span><span class="sxs-lookup"><span data-stu-id="51583-263">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="51583-264"><dt>**Aktiviert, aber offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="51583-264"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="51583-265">Das Element kann Befehle abschließen und löscht alle neuen Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="51583-265">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="51583-266"><dt>**In Test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="51583-266"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="51583-267">Das-Element befindet sich in einem Testzustand.</span><span class="sxs-lookup"><span data-stu-id="51583-267">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="51583-268"><dt></dt> Verzögert <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="51583-268"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="51583-269">Das Element kann Befehle abschließen, aber alle neuen Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="51583-269">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="51583-270"><dt>**Inesce**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="51583-270"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="51583-271">Das-Element ist aktiviert, befindet sich jedoch in einem eingeschränkten Modus.</span><span class="sxs-lookup"><span data-stu-id="51583-271">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="51583-272">Das Verhalten des-Elements ähnelt dem aktivierten Status (2), aber es verarbeitet nur einen eingeschränkten Satz von Befehlen.</span><span class="sxs-lookup"><span data-stu-id="51583-272">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="51583-273">Alle anderen Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="51583-273">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="51583-274"><dt>**Start**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="51583-274"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="51583-275">Das Element wechselt in den Zustand "aktiviert" (2).</span><span class="sxs-lookup"><span data-stu-id="51583-275">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="51583-276">Neue Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="51583-276">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="51583-277">**"Endadresse"**</span><span class="sxs-lookup"><span data-stu-id="51583-277">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-278">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="51583-278">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="51583-279">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-280">Die Endadresse des zusammenhängenden Speicherblocks.</span><span class="sxs-lookup"><span data-stu-id="51583-280">The ending address of the contiguous memory block.</span></span> <span data-ttu-id="51583-281">Da die Eigenschaft " **StartingAddress** " immer 0 ist, spiegelt dieser Wert immer die Gesamtmenge des Arbeitsspeichers auf dem virtuellen Computer wider.</span><span class="sxs-lookup"><span data-stu-id="51583-281">Since the **StartingAddress** property is always 0, this value always reflects the total amount of memory in the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="51583-282">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="51583-282">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-283">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51583-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51583-284">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-285">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](/windows/desktop/CIMWin32Prov/cim-memory)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51583-285">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="51583-286">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="51583-286">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-287">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="51583-287">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="51583-288">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-289">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](/windows/desktop/CIMWin32Prov/cim-memory)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51583-289">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="51583-290">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="51583-290">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-291">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51583-291">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="51583-292">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-293">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51583-293">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="51583-294">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="51583-294">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-295">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="51583-295">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="51583-296">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-297">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](/windows/desktop/CIMWin32Prov/cim-memory)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51583-297">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="51583-298">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="51583-298">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-299">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51583-299">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51583-300">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-301">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](/windows/desktop/CIMWin32Prov/cim-memory)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51583-301">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="51583-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="51583-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-303">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51583-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51583-304">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-305">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51583-305">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="51583-306">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="51583-306">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-307">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51583-307">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51583-308">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-309">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](/windows/desktop/CIMWin32Prov/cim-memory)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51583-309">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="51583-310">**Errormethodmethodologie**</span><span class="sxs-lookup"><span data-stu-id="51583-310">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-311">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51583-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51583-312">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-313">Eine Zeichenfolge, die den Typ der Fehlererkennung und-Korrektur beschreibt, die von diesem Speicherblock unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="51583-313">A string that describes the type of error detection and correction supported by this storage extent.</span></span> <span data-ttu-id="51583-314">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](/windows/desktop/CIMWin32Prov/cim-memory)geerbt und immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51583-314">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="51583-315">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="51583-315">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-316">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="51583-316">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="51583-317">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-318">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](/windows/desktop/CIMWin32Prov/cim-memory)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51583-318">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="51583-319">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="51583-319">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-320">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="51583-320">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="51583-321">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-322">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](/windows/desktop/CIMWin32Prov/cim-memory) geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51583-322">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory) but it not used.</span></span>

</dd> <dt>

<span data-ttu-id="51583-323">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="51583-323">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-324">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51583-324">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51583-325">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-326">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](/windows/desktop/CIMWin32Prov/cim-memory)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51583-326">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="51583-327">**Extentstatus**</span><span class="sxs-lookup"><span data-stu-id="51583-327">**ExtentStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-328">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="51583-328">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="51583-329">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-330">Speicherblöcke verfügen über zusätzliche Statusinformationen, die über das in **OperationalStatus** erfasste und andere Eigenschaften verfügen, die von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt wurden.</span><span class="sxs-lookup"><span data-stu-id="51583-330">Storage extents have additional status information beyond that captured in the **OperationalStatus** and other properties inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span> <span data-ttu-id="51583-331">Diese zusätzlichen Informationen (z. b. "Schutz deaktiviert", Wert = 9) werden in der **Volumestatus** -Eigenschaft aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="51583-331">This additional information (for example, "Protection Disabled", value=9) is captured in the **VolumeStatus** property.</span></span> <span data-ttu-id="51583-332">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt und ist immer auf 2 (keine/nicht zutreffend) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51583-332">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 2 (None/Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="51583-333">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="51583-333">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-334">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51583-334">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51583-335">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-336">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="51583-336">The current health of the element.</span></span> <span data-ttu-id="51583-337">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="51583-337">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="51583-338">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="51583-338">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="51583-339">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 5 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51583-339">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="51583-340">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="51583-340">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-341">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="51583-341">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="51583-342">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-343">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51583-343">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="51583-344">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="51583-344">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-345">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="51583-345">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="51583-346">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-347">Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="51583-347">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="51583-348">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="51583-348">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="51583-349">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="51583-349">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-350">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51583-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51583-351">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51583-352">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="51583-352">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="51583-353">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="51583-353">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="51583-354">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="51583-354">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="51583-355">**Isbasedonunderlyingredundancy**</span><span class="sxs-lookup"><span data-stu-id="51583-355">**IsBasedOnUnderlyingRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-356">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51583-356">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="51583-357">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-358">**True** , wenn die zugrunde liegenden Speicherblöcke an einer Speicher Redundanz Gruppe teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="51583-358">**True** if the underlying storage extents participate in a Storage Redundancy Group.</span></span> <span data-ttu-id="51583-359">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt und ist immer auf **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51583-359">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="51583-360">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="51583-360">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-361">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51583-361">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51583-362">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-363">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51583-363">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="51583-364">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="51583-364">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-365">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="51583-365">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="51583-366">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-367">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51583-367">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="51583-368">**Name**</span><span class="sxs-lookup"><span data-stu-id="51583-368">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-369">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51583-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51583-370">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51583-371">Qualifizierer: **maxlen** (1024), **override** ("Name")</span><span class="sxs-lookup"><span data-stu-id="51583-371">Qualifiers: **MaxLen** (1024), **Override** ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="51583-372">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="51583-372">The label by which the object is known.</span></span> <span data-ttu-id="51583-373">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="51583-373">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="51583-374">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt und ist immer auf "*GUID*" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51583-374">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to "*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="51583-375">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="51583-375">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-376">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51583-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51583-377">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-378">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt und immer auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51583-378">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="51583-379">**Namenamespace**</span><span class="sxs-lookup"><span data-stu-id="51583-379">**NameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-380">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51583-380">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51583-381">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-382">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt und immer auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51583-382">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="51583-383">**Nosinglepoinpoffailure**</span><span class="sxs-lookup"><span data-stu-id="51583-383">**NoSinglePointOfFailure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-384">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51583-384">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="51583-385">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-386">**True** , wenn keine Single Point of Failure vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="51583-386">**True** if there exists no single point of failure.</span></span> <span data-ttu-id="51583-387">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt und ist immer auf **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51583-387">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="51583-388">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="51583-388">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-389">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="51583-389">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="51583-390">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-391">Ein berechneter Wert, der die Gesamtmenge des Arbeitsspeichers dividiert durch die **BLOCKSIZE** darstellt.</span><span class="sxs-lookup"><span data-stu-id="51583-391">A calculated value that represents the total amount of memory divided by the **BlockSize**.</span></span> <span data-ttu-id="51583-392">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt.</span><span class="sxs-lookup"><span data-stu-id="51583-392">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="51583-393">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="51583-393">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-394">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51583-394">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51583-395">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-396">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="51583-396">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="51583-397">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="51583-397">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="51583-398">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="51583-398">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="51583-399"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="51583-399"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="51583-400"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="51583-400"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="51583-401"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="51583-401"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="51583-402"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="51583-402"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="51583-403"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="51583-403"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="51583-404"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="51583-404"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="51583-405"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="51583-405"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="51583-406"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="51583-406"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="51583-407"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="51583-407"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="51583-408"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="51583-408"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="51583-409"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="51583-409"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="51583-410"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="51583-410"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="51583-411"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="51583-411"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="51583-412"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="51583-412"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="51583-413"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="51583-413"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="51583-414"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="51583-414"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="51583-415"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="51583-415"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="51583-416"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="51583-416"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="51583-417"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="51583-417"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="51583-418">)</span><span class="sxs-lookup"><span data-stu-id="51583-418">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="51583-419">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="51583-419">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-420">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="51583-420">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="51583-421">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-422">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="51583-422">The current statuses of the object.</span></span> <span data-ttu-id="51583-423">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="51583-423">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="51583-424">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="51583-424">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-425">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51583-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51583-426">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-427">Der aktivierte oder deaktivierte Status des Elements, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="51583-427">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="51583-428">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="51583-428">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="51583-429">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51583-429">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="51583-430">**Othererrordescription**</span><span class="sxs-lookup"><span data-stu-id="51583-430">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-431">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51583-431">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51583-432">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-433">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](/windows/desktop/CIMWin32Prov/cim-memory)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51583-433">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="51583-434">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="51583-434">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-435">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="51583-435">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="51583-436">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-437">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51583-437">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="51583-438">**Othernameformat**</span><span class="sxs-lookup"><span data-stu-id="51583-438">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-439">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51583-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51583-440">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-441">Der Namespace der **Name** -Eigenschaft, wenn die **NameFormat** -Eigenschaft den Wert 1 (Other ") enthält.</span><span class="sxs-lookup"><span data-stu-id="51583-441">The namespace of the **Name** property when the **NameFormat** property includes the value 1 (Other").</span></span> <span data-ttu-id="51583-442">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51583-442">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="51583-443">**Othernamenamespace**</span><span class="sxs-lookup"><span data-stu-id="51583-443">**OtherNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-444">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51583-444">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51583-445">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-446">Der Namespace der **Name** -Eigenschaft, wenn die **namenamespace** -Eigenschaft den Wert 1 (Sonstiges) enthält.</span><span class="sxs-lookup"><span data-stu-id="51583-446">The namespace of the **Name** property when the **NameNamespace** property includes the value 1 (Other).</span></span> <span data-ttu-id="51583-447">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51583-447">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="51583-448">**Packageredundancy**</span><span class="sxs-lookup"><span data-stu-id="51583-448">**PackageRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-449">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51583-449">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51583-450">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-451">Die Anzahl von physischen Paketen, die derzeit ohne Datenverlust fehlschlagen können.</span><span class="sxs-lookup"><span data-stu-id="51583-451">The number of physical packages that can currently fail without data loss.</span></span> <span data-ttu-id="51583-452">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt und immer auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51583-452">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="51583-453">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="51583-453">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-454">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="51583-454">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="51583-455">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-456">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51583-456">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="51583-457">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="51583-457">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-458">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51583-458">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="51583-459">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-460">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51583-460">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="51583-461">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="51583-461">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-462">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="51583-462">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="51583-463">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-463">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-464">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51583-464">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="51583-465">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="51583-465">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-466">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51583-466">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51583-467">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-467">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-468">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="51583-468">Provides high level status information.</span></span> <span data-ttu-id="51583-469">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="51583-469">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="51583-470">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="51583-470">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="51583-471">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="51583-471">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="51583-472"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="51583-472"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="51583-473"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="51583-473"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="51583-474"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="51583-474"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="51583-475"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="51583-475"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="51583-476"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="51583-476"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="51583-477"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="51583-477"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="51583-478">)</span><span class="sxs-lookup"><span data-stu-id="51583-478">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="51583-479">**Ursprünglich**</span><span class="sxs-lookup"><span data-stu-id="51583-479">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-480">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51583-480">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="51583-481">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-481">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-482">**True** , wenn das enthaltende System dieses Betriebs Element nicht erstellen oder löschen kann.</span><span class="sxs-lookup"><span data-stu-id="51583-482">**True** if the containing system does not have the ability to create or delete this operational element.</span></span> <span data-ttu-id="51583-483">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt.</span><span class="sxs-lookup"><span data-stu-id="51583-483">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="51583-484">**Zweck**</span><span class="sxs-lookup"><span data-stu-id="51583-484">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-485">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51583-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51583-486">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-487">Eine Zeichenfolge, die die Medien und deren Verwendung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="51583-487">A string that describes the media and its use.</span></span> <span data-ttu-id="51583-488">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt und ist immer auf "System Speicher" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51583-488">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to "System Memory".</span></span>

</dd> <dt>

<span data-ttu-id="51583-489">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="51583-489">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-490">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51583-490">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51583-491">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-491">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-492">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="51583-492">The last requested or desired state for the element.</span></span> <span data-ttu-id="51583-493">Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="51583-493">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="51583-494">Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuell aktivierten oder deaktivierten Zustände zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="51583-494">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="51583-495">Eine bestimmte Instanz von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) unterstützt möglicherweise nicht die **requestStateChange** -Methode.</span><span class="sxs-lookup"><span data-stu-id="51583-495">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="51583-496">Wenn dies auftritt, wird der Wert 12 (nicht zutreffend) verwendet.</span><span class="sxs-lookup"><span data-stu-id="51583-496">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="51583-497">Diese Eigenschaft wird von **CIM \_ enabledlogicalelement** geerbt.</span><span class="sxs-lookup"><span data-stu-id="51583-497">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="51583-498">**SequentialAccess**</span><span class="sxs-lookup"><span data-stu-id="51583-498">**SequentialAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-499">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51583-499">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="51583-500">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-500">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-501">**True** , wenn ein Medien Zugriffsgerät sequenziell auf den Speicher zugreift.</span><span class="sxs-lookup"><span data-stu-id="51583-501">**True** if the storage is sequentially accessed by a media access device.</span></span> <span data-ttu-id="51583-502">Eine Band Partition ist ein Beispiel für einen Speicherblock, auf den sequenziell zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="51583-502">A tape partition is an example of a sequentially accessed storage extent.</span></span> <span data-ttu-id="51583-503">Speichervolumes, Datenträger Partitionen und logische Datenträger stellen nach dem Zufallsprinzip zugriffene Blöcke dar.</span><span class="sxs-lookup"><span data-stu-id="51583-503">Storage volumes, disk partitions, and logical disks represent randomly accessed extents.</span></span> <span data-ttu-id="51583-504">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt und ist immer auf **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51583-504">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="51583-505">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="51583-505">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-506">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="51583-506">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="51583-507">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-508">Die Anfangsadresse, auf die von einer Anwendung oder einem Betriebssystem verwiesen wird und die von einem Speichercontroller für dieses Speicher Objekt zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="51583-508">The beginning address referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="51583-509">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](/windows/desktop/CIMWin32Prov/cim-memory)geerbt und immer auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51583-509">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="51583-510">**Status**</span><span class="sxs-lookup"><span data-stu-id="51583-510">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-511">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51583-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51583-512">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-512">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-513">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51583-513">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="51583-514">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="51583-514">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-515">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="51583-515">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="51583-516">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-516">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-517">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="51583-517">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="51583-518">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="51583-518">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="51583-519">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="51583-519">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-520">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51583-520">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51583-521">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-521">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-522">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51583-522">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="51583-523">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="51583-523">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-524">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51583-524">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51583-525">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-525">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-526">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="51583-526">The scoping system's creation class name.</span></span> <span data-ttu-id="51583-527">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="51583-527">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="51583-528">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="51583-528">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-529">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51583-529">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="51583-530">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-530">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-531">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](/windows/desktop/CIMWin32Prov/cim-memory)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51583-531">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="51583-532">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="51583-532">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-533">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51583-533">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51583-534">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-534">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-535">Der eindeutige Bezeichner für die Bereichs bezogene virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="51583-535">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="51583-536">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="51583-536">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="51583-537">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="51583-537">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-538">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="51583-538">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="51583-539">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-539">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-540">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="51583-540">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="51583-541">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf "Null" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51583-541">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to "NULL".</span></span>

</dd> <dt>

<span data-ttu-id="51583-542">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="51583-542">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-543">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="51583-543">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="51583-544">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-544">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-545">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51583-545">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="51583-546">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="51583-546">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-547">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51583-547">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51583-548">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-548">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-549">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="51583-549">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="51583-550">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="51583-550">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="51583-551">**Ständigem**</span><span class="sxs-lookup"><span data-stu-id="51583-551">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51583-552">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51583-552">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="51583-553">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51583-553">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51583-554">Gibt an, ob der Speicher flüchtig ist.</span><span class="sxs-lookup"><span data-stu-id="51583-554">Indicates whether memory is volatile.</span></span> <span data-ttu-id="51583-555">Diese Eigenschaft wird vom [**CIM- \_ Speicher**](/windows/desktop/CIMWin32Prov/cim-memory)geerbt und ist immer auf " **true**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51583-555">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), and it is always set to **True**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51583-556">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51583-556">Remarks</span></span>

<span data-ttu-id="51583-557">Der Zugriff auf die **MSVM- \_ Speicher** Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="51583-557">Access to the **Msvm\_Memory** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="51583-558">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="51583-558">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="51583-559">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51583-559">Requirements</span></span>



| <span data-ttu-id="51583-560">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51583-560">Requirement</span></span> | <span data-ttu-id="51583-561">Wert</span><span class="sxs-lookup"><span data-stu-id="51583-561">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51583-562">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="51583-562">Minimum supported client</span></span><br/> | <span data-ttu-id="51583-563">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="51583-563">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="51583-564">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="51583-564">Minimum supported server</span></span><br/> | <span data-ttu-id="51583-565">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="51583-565">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="51583-566">Namespace</span><span class="sxs-lookup"><span data-stu-id="51583-566">Namespace</span></span><br/>                | <span data-ttu-id="51583-567">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="51583-567">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="51583-568">MOF</span><span class="sxs-lookup"><span data-stu-id="51583-568">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51583-569"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="51583-569"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="51583-570">DLL</span><span class="sxs-lookup"><span data-stu-id="51583-570">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51583-571"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="51583-571"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="51583-572">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51583-572">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51583-573">**CIM- \_ Speicher**</span><span class="sxs-lookup"><span data-stu-id="51583-573">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> <dt>

[<span data-ttu-id="51583-574">**CIM- \_ Speicher**</span><span class="sxs-lookup"><span data-stu-id="51583-574">**CIM\_Memory**</span></span>](/windows/desktop/CIMWin32Prov/cim-memory)
</dt> <dt>

[<span data-ttu-id="51583-575">Speicher Klassen</span><span class="sxs-lookup"><span data-stu-id="51583-575">Memory Classes</span></span>](memory-classes.md)
</dt> </dl>

 

