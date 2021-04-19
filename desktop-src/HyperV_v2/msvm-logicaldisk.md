---
description: Stellt Speicher Laufwerk Medien dar und wird verwendet, um die Speicher Laufwerke aufzufüllen.
ms.assetid: 06955C09-CA56-4B4C-997B-9B65AF125375
title: Msvm_LogicalDisk-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LogicalDisk
- Msvm_LogicalDisk.SetPowerState
- Msvm_LogicalDisk.EnableDevice
- Msvm_LogicalDisk.OnlineDevice
- Msvm_LogicalDisk.QuiesceDevice
- Msvm_LogicalDisk.SaveProperties
- Msvm_LogicalDisk.RestoreProperties
- Msvm_LogicalDisk.InstanceID
- Msvm_LogicalDisk.Caption
- Msvm_LogicalDisk.Description
- Msvm_LogicalDisk.ElementName
- Msvm_LogicalDisk.InstallDate
- Msvm_LogicalDisk.Name
- Msvm_LogicalDisk.OperationalStatus
- Msvm_LogicalDisk.StatusDescriptions
- Msvm_LogicalDisk.Status
- Msvm_LogicalDisk.HealthState
- Msvm_LogicalDisk.CommunicationStatus
- Msvm_LogicalDisk.DetailedStatus
- Msvm_LogicalDisk.OperatingStatus
- Msvm_LogicalDisk.PrimaryStatus
- Msvm_LogicalDisk.EnabledState
- Msvm_LogicalDisk.OtherEnabledState
- Msvm_LogicalDisk.RequestedState
- Msvm_LogicalDisk.EnabledDefault
- Msvm_LogicalDisk.TimeOfLastStateChange
- Msvm_LogicalDisk.AvailableRequestedStates
- Msvm_LogicalDisk.TransitioningToState
- Msvm_LogicalDisk.SystemCreationClassName
- Msvm_LogicalDisk.SystemName
- Msvm_LogicalDisk.CreationClassName
- Msvm_LogicalDisk.DeviceID
- Msvm_LogicalDisk.PowerManagementSupported
- Msvm_LogicalDisk.PowerManagementCapabilities
- Msvm_LogicalDisk.Availability
- Msvm_LogicalDisk.StatusInfo
- Msvm_LogicalDisk.LastErrorCode
- Msvm_LogicalDisk.ErrorDescription
- Msvm_LogicalDisk.ErrorCleared
- Msvm_LogicalDisk.OtherIdentifyingInfo
- Msvm_LogicalDisk.PowerOnHours
- Msvm_LogicalDisk.TotalPowerOnHours
- Msvm_LogicalDisk.IdentifyingDescriptions
- Msvm_LogicalDisk.AdditionalAvailability
- Msvm_LogicalDisk.MaxQuiesceTime
- Msvm_LogicalDisk.DataOrganization
- Msvm_LogicalDisk.Purpose
- Msvm_LogicalDisk.Access
- Msvm_LogicalDisk.ErrorMethodology
- Msvm_LogicalDisk.BlockSize
- Msvm_LogicalDisk.NumberOfBlocks
- Msvm_LogicalDisk.ConsumableBlocks
- Msvm_LogicalDisk.IsBasedOnUnderlyingRedundancy
- Msvm_LogicalDisk.SequentialAccess
- Msvm_LogicalDisk.ExtentStatus
- Msvm_LogicalDisk.NoSinglePointOfFailure
- Msvm_LogicalDisk.DataRedundancy
- Msvm_LogicalDisk.PackageRedundancy
- Msvm_LogicalDisk.DeltaReservation
- Msvm_LogicalDisk.Primordial
- Msvm_LogicalDisk.NameFormat
- Msvm_LogicalDisk.NameNamespace
- Msvm_LogicalDisk.OtherNameNamespace
- Msvm_LogicalDisk.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e5071f2a102a32364888c9c7de5121ede5249f47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349259"
---
# <a name="msvm_logicaldisk-class"></a><span data-ttu-id="0348e-103">MSVM \_ LogicalDisk-Klasse</span><span class="sxs-lookup"><span data-stu-id="0348e-103">Msvm\_LogicalDisk class</span></span>

<span data-ttu-id="0348e-104">Stellt Speicher Laufwerk Medien dar und wird verwendet, um die Speicher Laufwerke aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="0348e-104">Represents storage drive media and is used to populate the storage drives.</span></span> <span data-ttu-id="0348e-105">Zu den unterstützten Medientypen zählen virtuelle fest Dateien, virtuelle Disketten, ISO-Dateien und physische Geräte Medien.</span><span class="sxs-lookup"><span data-stu-id="0348e-105">The media types supported include virtual hard files, virtual floppy files, ISO files, and physical device media.</span></span>

<span data-ttu-id="0348e-106">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0348e-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0348e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0348e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LogicalDisk : CIM_LogicalDisk
{
  string   InstanceID;
  string   Caption;
  uint64   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_LogicalDisk";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
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
  string   Purpose;
  uint16   Access;
  string   ErrorMethodology;
  uint64   BlockSize = 512;
  uint64   NumberOfBlocks = 266338304;
  uint64   ConsumableBlocks = 0;
  boolean  IsBasedOnUnderlyingRedundancy = False;
  boolean  SequentialAccess = False;
  uint16   ExtentStatus[] = { 2 };
  boolean  NoSinglePointOfFailure = False;
  uint16   DataRedundancy = 0;
  uint16   PackageRedundancy = 0;
  uint8    DeltaReservation = 0;
  boolean  Primordial = False;
  uint16   NameFormat = 12;
  uint16   NameNamespace = 8;
  string   OtherNameNamespace;
  string   OtherNameFormat;
};
```

## <a name="members"></a><span data-ttu-id="0348e-108">Member</span><span class="sxs-lookup"><span data-stu-id="0348e-108">Members</span></span>

<span data-ttu-id="0348e-109">Die **MSVM \_ LogicalDisk** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0348e-109">The **Msvm\_LogicalDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="0348e-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="0348e-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="0348e-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0348e-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0348e-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="0348e-112">Methods</span></span>

<span data-ttu-id="0348e-113">Die **MSVM \_ LogicalDisk** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="0348e-113">The **Msvm\_LogicalDisk** class has these methods.</span></span>



| <span data-ttu-id="0348e-114">Methode</span><span class="sxs-lookup"><span data-stu-id="0348e-114">Method</span></span>                                                            | <span data-ttu-id="0348e-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0348e-115">Description</span></span>                              |
|:------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="0348e-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="0348e-116">**EnableDevice**</span></span>                                                  | <span data-ttu-id="0348e-117">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0348e-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="0348e-118">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="0348e-118">**OnlineDevice**</span></span>                                                  | <span data-ttu-id="0348e-119">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0348e-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="0348e-120">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="0348e-120">**QuiesceDevice**</span></span>                                                 | <span data-ttu-id="0348e-121">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0348e-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="0348e-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="0348e-122">**RequestStateChange**</span></span>](msvm-logicaldisk-requeststatechange.md) | <span data-ttu-id="0348e-123">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="0348e-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="0348e-124">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="0348e-124">**Reset**</span></span>](msvm-logicaldisk-reset.md)                           | <span data-ttu-id="0348e-125">Setzt den Dienst zurück.</span><span class="sxs-lookup"><span data-stu-id="0348e-125">Resets the service.</span></span><br/>           |
| <span data-ttu-id="0348e-126">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="0348e-126">**RestoreProperties**</span></span>                                             | <span data-ttu-id="0348e-127">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0348e-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="0348e-128">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="0348e-128">**SaveProperties**</span></span>                                                | <span data-ttu-id="0348e-129">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0348e-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="0348e-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="0348e-130">**SetPowerState**</span></span>                                                 | <span data-ttu-id="0348e-131">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0348e-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0348e-132">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0348e-132">Properties</span></span>

<span data-ttu-id="0348e-133">Die **MSVM \_ LogicalDisk** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0348e-133">The **Msvm\_LogicalDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0348e-134">**zugreifen**</span><span class="sxs-lookup"><span data-stu-id="0348e-134">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-135">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0348e-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-137">Gibt an, ob das Medium lesbar, beschreibbar oder beides ist.</span><span class="sxs-lookup"><span data-stu-id="0348e-137">Indicates whether the media is readable, writeable, or both.</span></span> <span data-ttu-id="0348e-138">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-138">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>



| <span data-ttu-id="0348e-139">Wert</span><span class="sxs-lookup"><span data-stu-id="0348e-139">Value</span></span>                                                                        | <span data-ttu-id="0348e-140">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0348e-140">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="0348e-141"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0348e-141"><dt>0</dt></span></span> </dl> | <span data-ttu-id="0348e-142">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="0348e-142">Unknown</span></span><br/>     |
| <dl> <span data-ttu-id="0348e-143"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0348e-143"><dt>1</dt></span></span> </dl> | <span data-ttu-id="0348e-144">Lesbare.</span><span class="sxs-lookup"><span data-stu-id="0348e-144">Readable.</span></span><br/>   |
| <dl> <span data-ttu-id="0348e-145"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0348e-145"><dt>2</dt></span></span> </dl> | <span data-ttu-id="0348e-146">Beschreibbaren.</span><span class="sxs-lookup"><span data-stu-id="0348e-146">Writeable.</span></span><br/>  |
| <dl> <span data-ttu-id="0348e-147"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="0348e-147"><dt>3</dt></span></span> </dl> | <span data-ttu-id="0348e-148">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="0348e-148">Read/write.</span></span><br/> |
| <dl> <span data-ttu-id="0348e-149"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="0348e-149"><dt>4</dt></span></span> </dl> | <span data-ttu-id="0348e-150">Einmal schreiben.</span><span class="sxs-lookup"><span data-stu-id="0348e-150">Write once.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0348e-151">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="0348e-151">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-152">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="0348e-152">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0348e-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-154">Alle zusätzlichen Verfügbarkeit und der Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="0348e-154">Any additional availability and status of the device.</span></span> <span data-ttu-id="0348e-155">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-155">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="0348e-156">Wert</span><span class="sxs-lookup"><span data-stu-id="0348e-156">Value</span></span>                                                                            | <span data-ttu-id="0348e-157">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0348e-157">Meaning</span></span>                    |
|----------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="0348e-158"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="0348e-158"><dt>{ 6 }</dt></span></span> </dl> | <span data-ttu-id="0348e-159">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="0348e-159">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0348e-160">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="0348e-160">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-161">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0348e-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-163">Die primäre Verfügbarkeit und den Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="0348e-163">The primary availability and status of the device.</span></span> <span data-ttu-id="0348e-164">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-164">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="0348e-165">Wert</span><span class="sxs-lookup"><span data-stu-id="0348e-165">Value</span></span>                                                                        | <span data-ttu-id="0348e-166">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0348e-166">Meaning</span></span>                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="0348e-167"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="0348e-167"><dt>6</dt></span></span> </dl> | <span data-ttu-id="0348e-168">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="0348e-168">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0348e-169">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="0348e-169">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-170">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="0348e-170">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0348e-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-172">Gibt die möglichen Werte für den *requestedstate* -Parameter der [**requestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) -Methode an, die zum Initiieren einer Zustandsänderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0348e-172">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="0348e-173">Bei den aufgelisteten Werten handelt es sich um eine Teilmenge der Werte, die in der **requestedstaatsupported** -Eigenschaft der zugeordneten Instanz von **CIM \_ enabledlogicalelementfunctions** enthalten sind, wobei die ausgewählten Werte eine Funktion des aktuellen Zustands des [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) -Objekts sind.</span><span class="sxs-lookup"><span data-stu-id="0348e-173">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="0348e-174">Diese Eigenschaft darf nicht **null** sein, wenn eine Implementierung den Satz möglicher Werte als Funktion des aktuellen Zustands ankündigen kann.</span><span class="sxs-lookup"><span data-stu-id="0348e-174">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="0348e-175">Diese Eigenschaft ist **null** , wenn eine Implementierung den Satz möglicher Werte nicht als Funktion des aktuellen Zustands bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="0348e-175">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="0348e-176">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-176">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0348e-177">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="0348e-177">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-178">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0348e-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-180">Die Größe (in Bytes) der Blöcke, die den Speicherblock bilden.</span><span class="sxs-lookup"><span data-stu-id="0348e-180">The size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="0348e-181">Wenn die Blockgröße variabel ist, muss die maximale Blockgröße in Bytes angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0348e-181">If the block size is variable, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="0348e-182">Wenn die Blockgröße unbekannt ist oder ein Block Konzept nicht gültig ist (z. b. für Aggregat Blöcke, Arbeitsspeicher oder logische Datenträger), enthält dieser Wert 1.</span><span class="sxs-lookup"><span data-stu-id="0348e-182">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), this will contain 1.</span></span> <span data-ttu-id="0348e-183">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-183">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="0348e-184">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0348e-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-185">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0348e-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-187">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="0348e-187">A short description of the object.</span></span> <span data-ttu-id="0348e-188">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="0348e-189">"ISO Disk Image"</span><span class="sxs-lookup"><span data-stu-id="0348e-189">"ISO Disk Image"</span></span>

<span data-ttu-id="0348e-190">"Festplatten Abbild"</span><span class="sxs-lookup"><span data-stu-id="0348e-190">"Hard Disk Image"</span></span>

<span data-ttu-id="0348e-191">"Disketten Image"</span><span class="sxs-lookup"><span data-stu-id="0348e-191">"Floppy Disk Image"</span></span>

<span data-ttu-id="0348e-192">"CD/DVD Disk"</span><span class="sxs-lookup"><span data-stu-id="0348e-192">"CD/DVD Disk"</span></span>

</dd> <dt>

<span data-ttu-id="0348e-193">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="0348e-193">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-194">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0348e-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-196">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="0348e-196">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="0348e-197">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="0348e-197">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0348e-198">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-198">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0348e-199">**Consumableblocks**</span><span class="sxs-lookup"><span data-stu-id="0348e-199">**ConsumableBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-200">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0348e-200">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-201">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-202">Die maximale Anzahl von Blöcken der Größe **Blockgröße**, die für die Nutzung verfügbar sind, wenn die Schichten Speicherblöcke mithilfe der [**MSVM- \_ BasedOn**](msvm-basedon.md) -Zuordnung erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="0348e-202">The maximum number of blocks, of size **BlockSize**, that are available for consumption when layering storage extents using the [**Msvm\_BasedOn**](msvm-basedon.md) association.</span></span> <span data-ttu-id="0348e-203">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-203">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="0348e-204">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="0348e-204">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-205">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0348e-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-206">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-207">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0348e-207">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="0348e-208">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-208">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="0348e-209">**Dataorganization**</span><span class="sxs-lookup"><span data-stu-id="0348e-209">**DataOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-210">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0348e-210">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-212">Der Typ der verwendeten Datenorganisation.</span><span class="sxs-lookup"><span data-stu-id="0348e-212">The type of data organization used.</span></span> <span data-ttu-id="0348e-213">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-213">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>



| <span data-ttu-id="0348e-214">Wert</span><span class="sxs-lookup"><span data-stu-id="0348e-214">Value</span></span>                                                                        | <span data-ttu-id="0348e-215">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0348e-215">Meaning</span></span>                 |
|------------------------------------------------------------------------------|-------------------------|
| <dl> <span data-ttu-id="0348e-216"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0348e-216"><dt>2</dt></span></span> </dl> | <span data-ttu-id="0348e-217">Fester Block.</span><span class="sxs-lookup"><span data-stu-id="0348e-217">Fixed block.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0348e-218">**Dataredundancy**</span><span class="sxs-lookup"><span data-stu-id="0348e-218">**DataRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-219">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0348e-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-220">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-221">Die Anzahl der kompletten Kopien von Daten, die zurzeit verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="0348e-221">The number of complete copies of data currently maintained.</span></span> <span data-ttu-id="0348e-222">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-222">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="0348e-223">**Delta Service**</span><span class="sxs-lookup"><span data-stu-id="0348e-223">**DeltaReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-224">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0348e-224">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-225">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-226">Ein Prozentsatz, der den Speicherplatz angibt, der in einem Replikat reserviert werden soll, um Änderungen zwischenzuspeichern.</span><span class="sxs-lookup"><span data-stu-id="0348e-226">A percentage that specifies the amount of space that should be reserved in a replica for caching changes.</span></span> <span data-ttu-id="0348e-227">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-227">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="0348e-228">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0348e-228">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-229">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0348e-229">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-230">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-231">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="0348e-231">A description of the object.</span></span> <span data-ttu-id="0348e-232">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-232">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0348e-233">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="0348e-233">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-234">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0348e-234">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-235">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-236">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="0348e-236">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="0348e-237">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="0348e-237">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0348e-238">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-238">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0348e-239">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="0348e-239">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-240">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0348e-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-241">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-242">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und auf "Microsoft:*GUID* \\ *Device-Specific-Data*" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0348e-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="0348e-243">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0348e-243">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-244">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0348e-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-245">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-246">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0348e-246">A display name for the object.</span></span> <span data-ttu-id="0348e-247">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-247">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="0348e-248">"ISO Disk Image"</span><span class="sxs-lookup"><span data-stu-id="0348e-248">"ISO Disk Image"</span></span>

<span data-ttu-id="0348e-249">"Festplatten Abbild"</span><span class="sxs-lookup"><span data-stu-id="0348e-249">"Hard Disk Image"</span></span>

<span data-ttu-id="0348e-250">"Disketten Image"</span><span class="sxs-lookup"><span data-stu-id="0348e-250">"Floppy Disk Image"</span></span>

<span data-ttu-id="0348e-251">"CD/DVD Disk"</span><span class="sxs-lookup"><span data-stu-id="0348e-251">"CD/DVD Disk"</span></span>

</dd> <dt>

<span data-ttu-id="0348e-252">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="0348e-252">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-253">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0348e-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-254">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-255">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="0348e-255">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="0348e-256">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-256">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0348e-257">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="0348e-257">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-258">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0348e-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-259">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-260">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="0348e-260">The enabled and disabled states of an element.</span></span> <span data-ttu-id="0348e-261">Sie kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben.</span><span class="sxs-lookup"><span data-stu-id="0348e-261">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="0348e-262">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-262">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0348e-263">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="0348e-263">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-264">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="0348e-264">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-265">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-266">Gibt an, ob der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="0348e-266">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="0348e-267">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0348e-267">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0348e-268">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="0348e-268">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-269">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0348e-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-270">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-271">Eine Zeichenfolge, die weitere Informationen über den Fehler enthält, der in **LastErrorCode** aufgezeichnet wurde, sowie Informationen über alle Maßnahmen, die ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="0348e-271">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="0348e-272">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0348e-272">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0348e-273">**Errormethodmethodologie**</span><span class="sxs-lookup"><span data-stu-id="0348e-273">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-274">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0348e-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-275">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-276">Eine Zeichenfolge, die die von diesem Gerät unterstützten Fehler Erkennungs-und Korrektur Typen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="0348e-276">A string that describes the types of error detection and correction supported by this device.</span></span> <span data-ttu-id="0348e-277">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-277">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="0348e-278">**Extentstatus**</span><span class="sxs-lookup"><span data-stu-id="0348e-278">**ExtentStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-279">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="0348e-279">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0348e-280">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-281">Alle zusätzlichen Statusinformationen, die über die im **OperationalStatus** und anderen geerbten Eigenschaften erfassten hinausgehen.</span><span class="sxs-lookup"><span data-stu-id="0348e-281">Any additional status information beyond that captured in the **OperationalStatus** and other inherited properties.</span></span>



| <span data-ttu-id="0348e-282">Wert</span><span class="sxs-lookup"><span data-stu-id="0348e-282">Value</span></span>                                                                            | <span data-ttu-id="0348e-283">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0348e-283">Meaning</span></span>                         |
|----------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="0348e-284"><dt>2,2</dt></span><span class="sxs-lookup"><span data-stu-id="0348e-284"><dt>{ 2 }</dt></span></span> </dl> | <span data-ttu-id="0348e-285">Keine/nicht zutreffend.</span><span class="sxs-lookup"><span data-stu-id="0348e-285">None/Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0348e-286">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="0348e-286">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-287">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0348e-287">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-288">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-289">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="0348e-289">The current health of the element.</span></span> <span data-ttu-id="0348e-290">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="0348e-290">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="0348e-291">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="0348e-291">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="0348e-292">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-292">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0348e-293">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0348e-293">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-294">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="0348e-294">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0348e-295">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-296">Ein Array von Freiform-Zeichen folgen, die Erklärungen und Details hinter den Einträgen im Eigenschafts Array " **OtherIdentifyingInfo** " bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0348e-296">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="0348e-297">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0348e-297">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0348e-298">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0348e-298">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-299">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="0348e-299">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-300">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-301">Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="0348e-301">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="0348e-302">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-302">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0348e-303">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0348e-303">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-304">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0348e-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-305">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0348e-306">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="0348e-306">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0348e-307">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="0348e-307">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="0348e-308">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-308">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0348e-309">**Isbasedonunderlyingredundancy**</span><span class="sxs-lookup"><span data-stu-id="0348e-309">**IsBasedOnUnderlyingRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-310">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="0348e-310">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-311">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-312">Gibt an, ob die zugrunde liegenden Speicherblöcke an einer Speicher Redundanz Gruppe teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="0348e-312">Indicates whether the underlying storage extents participate in a storage redundancy group.</span></span> <span data-ttu-id="0348e-313">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-313">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="0348e-314">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0348e-314">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-315">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0348e-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-316">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-317">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="0348e-317">The last error code reported by the logical device.</span></span> <span data-ttu-id="0348e-318">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0348e-318">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0348e-319">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="0348e-319">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-320">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0348e-320">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-321">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-322">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="0348e-322">This property has been deprecated.</span></span> <span data-ttu-id="0348e-323">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0348e-323">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0348e-324">**Name**</span><span class="sxs-lookup"><span data-stu-id="0348e-324">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-325">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0348e-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-326">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-327">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="0348e-327">The label by which the object is known.</span></span> <span data-ttu-id="0348e-328">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und entspricht der Element **Name** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="0348e-328">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="0348e-329">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="0348e-329">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-330">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0348e-330">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-331">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-332">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-332">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>



| <span data-ttu-id="0348e-333">Wert</span><span class="sxs-lookup"><span data-stu-id="0348e-333">Value</span></span>                                                                         | <span data-ttu-id="0348e-334">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0348e-334">Meaning</span></span>                                 |
|-------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="0348e-335"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0348e-335"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="0348e-336">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="0348e-336">Other</span></span><br/>                        |
| <dl> <span data-ttu-id="0348e-337"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="0348e-337"><dt>12</dt></span></span> </dl> | <span data-ttu-id="0348e-338">Name des Betriebssystem Geräts</span><span class="sxs-lookup"><span data-stu-id="0348e-338">Operating system device name</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0348e-339">**Namenamespace**</span><span class="sxs-lookup"><span data-stu-id="0348e-339">**NameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-340">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0348e-340">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-341">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-342">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-342">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>



| <span data-ttu-id="0348e-343">Wert</span><span class="sxs-lookup"><span data-stu-id="0348e-343">Value</span></span>                                                                        | <span data-ttu-id="0348e-344">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0348e-344">Meaning</span></span>                                      |
|------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="0348e-345"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0348e-345"><dt>1</dt></span></span> </dl> | <span data-ttu-id="0348e-346">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="0348e-346">Other</span></span><br/>                             |
| <dl> <span data-ttu-id="0348e-347"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="0348e-347"><dt>8</dt></span></span> </dl> | <span data-ttu-id="0348e-348">Namespace des Betriebssystem Geräts</span><span class="sxs-lookup"><span data-stu-id="0348e-348">Operating system device namespace</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0348e-349">**Nosinglepoinpoffailure**</span><span class="sxs-lookup"><span data-stu-id="0348e-349">**NoSinglePointOfFailure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-350">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="0348e-350">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-351">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-352">Gibt an, ob keine Single Point of Failure vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0348e-352">Indicates whether there exists no single point of failure.</span></span> <span data-ttu-id="0348e-353">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-353">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="0348e-354">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="0348e-354">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-355">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0348e-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-356">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-357">Die Anzahl der aufeinanderfolgenden Blöcke, die jeweils die Größe des in der **BLOCKSIZE** -Eigenschaft enthaltenen Werts blockieren, die den Speicherblock bilden.</span><span class="sxs-lookup"><span data-stu-id="0348e-357">The number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, that form the storage extent.</span></span> <span data-ttu-id="0348e-358">Die Gesamtgröße des Speicherbereichs kann berechnet werden, indem der Wert der **BLOCKSIZE** -Eigenschaft mit dem Wert dieser Eigenschaft multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="0348e-358">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="0348e-359">Wenn der Wert von **BLOCKSIZE** 1 ist, entspricht diese Eigenschaft der Gesamtgröße des Speicherblocks.</span><span class="sxs-lookup"><span data-stu-id="0348e-359">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span> <span data-ttu-id="0348e-360">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-360">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="0348e-361">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="0348e-361">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-362">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0348e-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-363">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-364">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="0348e-364">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="0348e-365">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="0348e-365">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0348e-366">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-366">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0348e-367">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="0348e-367">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-368">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="0348e-368">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0348e-369">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0348e-370">Qualifizierer: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="0348e-370">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="0348e-371">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="0348e-371">The current statuses of the object.</span></span> <span data-ttu-id="0348e-372">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-372">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="0348e-373">Wenn die erforderliche QoS-Ebene für den virtuellen Datenträger nicht erfüllt werden kann, wird der primäre Status (OperationalStatus \[ 0 \] ) auf heruntergestuft (3) festgelegt, und das OperationalStatus-Array enthält zusätzlich einen sekundären Statuswert, der den spezifischen Grund für die QoS-Bedingung gemäß dieser Tabelle angibt.</span><span class="sxs-lookup"><span data-stu-id="0348e-373">When the required QoS level for the virtual disk can't be satisfied, the primary status (OperationalStatus\[0\]) is set to Degraded (3) and the OperationalStatus array additionally contains a secondary status value that indicates the specific reason for the QoS condition, according to this table.</span></span>



| <span data-ttu-id="0348e-374">Wert</span><span class="sxs-lookup"><span data-stu-id="0348e-374">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="0348e-375">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0348e-375">Description</span></span>                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0348e-376"><span id="_Insufficient_Throughput___32788_"></span><span id="_insufficient_throughput___32788_"></span><span id="_INSUFFICIENT_THROUGHPUT___32788_"></span> Unzureichender Durchsatz (32788)</span><span class="sxs-lookup"><span data-stu-id="0348e-376"><span id="_Insufficient_Throughput___32788_"></span><span id="_insufficient_throughput___32788_"></span><span id="_INSUFFICIENT_THROUGHPUT___32788_"></span> Insufficient Throughput  (32788)</span></span><br/> | <span data-ttu-id="0348e-377">Die angeforderte minimale IOPS-Rate ist für das Gerät zurzeit nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0348e-377">The requested minimum IOPS rate is currently not available to the device.</span></span> <br/> |



 

> [!Note]  
> <span data-ttu-id="0348e-378">OperationalStatus wird auch zum Melden anderer Fehler-oder Warnungs Bedingungen verwendet (z. b. Protokoll Konflikt zwischen VSP und VSC).</span><span class="sxs-lookup"><span data-stu-id="0348e-378">OperationalStatus is also used to report other error or warning conditions (for example, protocol mismatch between VSP and VSC).</span></span> <span data-ttu-id="0348e-379">Wenn mehrere Bedingungen vorhanden sind, wird der primäre Status auf "heruntergestuft" festgelegt, und mindestens ein sekundärer Statuswert in beliebiger Reihenfolge, beginnend bei Index 1, wird in das Array eingefügt.</span><span class="sxs-lookup"><span data-stu-id="0348e-379">If multiple conditions exists, the primary status is set Degraded, and one or more secondary status values, in any order starting at index 1, is filled in the array.</span></span>

 

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0348e-380"><span id="OK"></span><span id="ok"></span>**OK** (2)</span><span class="sxs-lookup"><span data-stu-id="0348e-380"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0348e-381"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (3** )</span><span class="sxs-lookup"><span data-stu-id="0348e-381"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="0348e-382"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (7)</span><span class="sxs-lookup"><span data-stu-id="0348e-382"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>

<span data-ttu-id="0348e-383"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (11)</span><span class="sxs-lookup"><span data-stu-id="0348e-383"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (11)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="0348e-384">In Windows 10 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0348e-384">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0348e-385"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (12)</span><span class="sxs-lookup"><span data-stu-id="0348e-385"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="0348e-386"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (13)</span><span class="sxs-lookup"><span data-stu-id="0348e-386"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>

<span data-ttu-id="0348e-387"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (16)</span><span class="sxs-lookup"><span data-stu-id="0348e-387"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (16)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="0348e-388">In Windows 10 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0348e-388">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>

<span data-ttu-id="0348e-389"><span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>**Protokoll** Konflikt (32775)</span><span class="sxs-lookup"><span data-stu-id="0348e-389"><span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>**Protocol Mismatch** (32775)</span></span>


</dt> <dd></dd> <dt>

<span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>

<span data-ttu-id="0348e-390"><span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>**Timeout** bei der Kommunikation (32783)</span><span class="sxs-lookup"><span data-stu-id="0348e-390"><span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>**Communication Timed Out** (32783)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="0348e-391">In Windows 10 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0348e-391">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Insufficient_Throughput"></span><span id="insufficient_throughput"></span><span id="INSUFFICIENT_THROUGHPUT"></span>

<span data-ttu-id="0348e-392"><span id="Insufficient_Throughput"></span><span id="insufficient_throughput"></span><span id="INSUFFICIENT_THROUGHPUT"></span>**Unzureichender Durchsatz** (32788)</span><span class="sxs-lookup"><span data-stu-id="0348e-392"><span id="Insufficient_Throughput"></span><span id="insufficient_throughput"></span><span id="INSUFFICIENT_THROUGHPUT"></span>**Insufficient Throughput** (32788)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown_QoS_Policy_ID"></span><span id="unknown_qos_policy_id"></span><span id="UNKNOWN_QOS_POLICY_ID"></span>

<span data-ttu-id="0348e-393"><span id="Unknown_QoS_Policy_ID"></span><span id="unknown_qos_policy_id"></span><span id="UNKNOWN_QOS_POLICY_ID"></span>**Unbekannte QoS-Richtlinien-ID** (32791).</span><span class="sxs-lookup"><span data-stu-id="0348e-393"><span id="Unknown_QoS_Policy_ID"></span><span id="unknown_qos_policy_id"></span><span id="UNKNOWN_QOS_POLICY_ID"></span>**Unknown QoS Policy ID** (32791)</span></span>


</dt> <dd></dd> <dt>

<span id="QoS_Not_Supported"></span><span id="qos_not_supported"></span><span id="QOS_NOT_SUPPORTED"></span>

<span data-ttu-id="0348e-394"><span id="QoS_Not_Supported"></span><span id="qos_not_supported"></span><span id="QOS_NOT_SUPPORTED"></span>**QoS nicht unterstützt** (32792)</span><span class="sxs-lookup"><span data-stu-id="0348e-394"><span id="QoS_Not_Supported"></span><span id="qos_not_supported"></span><span id="QOS_NOT_SUPPORTED"></span>**QoS Not Supported** (32792)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="0348e-395">In Windows 10 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0348e-395">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="QoS_Configuration_Mismatch"></span><span id="qos_configuration_mismatch"></span><span id="QOS_CONFIGURATION_MISMATCH"></span>

<span data-ttu-id="0348e-396"><span id="QoS_Configuration_Mismatch"></span><span id="qos_configuration_mismatch"></span><span id="QOS_CONFIGURATION_MISMATCH"></span>Nicht übereinstimmende **QoS-Konfiguration** (32793)</span><span class="sxs-lookup"><span data-stu-id="0348e-396"><span id="QoS_Configuration_Mismatch"></span><span id="qos_configuration_mismatch"></span><span id="QOS_CONFIGURATION_MISMATCH"></span>**QoS Configuration Mismatch** (32793)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="0348e-397">In Windows 10 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0348e-397">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Disk_Full"></span><span id="disk_full"></span><span id="DISK_FULL"></span>

<span data-ttu-id="0348e-398"><span id="Disk_Full"></span><span id="disk_full"></span><span id="DISK_FULL"></span>**Vollständiger** Datenträger (32794)</span><span class="sxs-lookup"><span data-stu-id="0348e-398"><span id="Disk_Full"></span><span id="disk_full"></span><span id="DISK_FULL"></span>**Disk Full** (32794)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="0348e-399">In Windows 10 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0348e-399">Added in Windows 10.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0348e-400">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="0348e-400">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-401">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0348e-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-402">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-403">Der aktivierte oder deaktivierte Status des Elements, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0348e-403">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="0348e-404">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="0348e-404">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="0348e-405">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-405">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0348e-406">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="0348e-406">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-407">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="0348e-407">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0348e-408">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-409">Alle zusätzlichen Daten über Geräte-ID-Informationen, die zur Identifizierung eines logischen Geräts verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="0348e-409">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="0348e-410">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0348e-410">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0348e-411">**Othernameformat**</span><span class="sxs-lookup"><span data-stu-id="0348e-411">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-412">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0348e-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-413">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-414">Eine Zeichenfolge, die das Format der **Name** -Eigenschaft beschreibt, wenn **NameFormat** den Wert 1 (Sonstiges) enthält.</span><span class="sxs-lookup"><span data-stu-id="0348e-414">A string that describes the format of the **Name** property when **NameFormat** contains the value 1 (Other).</span></span> <span data-ttu-id="0348e-415">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-415">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="0348e-416">**Othernamenamespace**</span><span class="sxs-lookup"><span data-stu-id="0348e-416">**OtherNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-417">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0348e-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-418">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-419">Eine Zeichenfolge, die den Namespace der **Name** -Eigenschaft beschreibt, wenn **namenamespace** den Wert 1 (Sonstiges) enthält.</span><span class="sxs-lookup"><span data-stu-id="0348e-419">A string that describes the namespace of the **Name** property when **NameNamespace** contains the value 1 (Other).</span></span> <span data-ttu-id="0348e-420">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-420">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="0348e-421">**Packageredundancy**</span><span class="sxs-lookup"><span data-stu-id="0348e-421">**PackageRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-422">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0348e-422">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-423">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-423">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-424">Die Anzahl von physischen Paketen, die derzeit ohne Datenverlust fehlschlagen können.</span><span class="sxs-lookup"><span data-stu-id="0348e-424">The number of physical packages that can currently fail without data loss.</span></span> <span data-ttu-id="0348e-425">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-425">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="0348e-426">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="0348e-426">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-427">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="0348e-427">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0348e-428">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-429">Die Energie Verwaltungsfunktionen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="0348e-429">The power management capabilities of the device.</span></span> <span data-ttu-id="0348e-430">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0348e-430">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0348e-431">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="0348e-431">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-432">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="0348e-432">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-433">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-434">Gibt an, ob das Gerät Energie gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="0348e-434">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="0348e-435">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0348e-435">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0348e-436">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="0348e-436">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-437">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0348e-437">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-438">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-438">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-439">Gibt an, wie viele aufeinanderfolgende Stunden dieses Gerät seit dem letzten Strom Umgebung eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="0348e-439">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="0348e-440">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0348e-440">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0348e-441">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="0348e-441">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-442">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0348e-442">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-443">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-444">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="0348e-444">Provides high level status information.</span></span> <span data-ttu-id="0348e-445">Diese Eigenschaft sollte in Verbindung mit der **detailedstatus** -Eigenschaft verwendet werden, um allgemeine und ausführliche Integritäts Statusinformationen für das-Element und seine unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="0348e-445">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="0348e-446">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="0348e-446">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0348e-447">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-447">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0348e-448">**Ursprünglich**</span><span class="sxs-lookup"><span data-stu-id="0348e-448">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-449">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="0348e-449">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-450">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-451">Gibt an, ob das enthaltende System dieses Betriebs Element erstellen oder löschen kann.</span><span class="sxs-lookup"><span data-stu-id="0348e-451">Indicates whether the containing system has the ability to create or delete this operational element.</span></span> <span data-ttu-id="0348e-452">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt und für dateibasierte Medien auf **false** und für Pass-Through-Medien auf **true** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0348e-452">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is set to **False** for file-based media and **True** for pass-through media.</span></span>

</dd> <dt>

<span data-ttu-id="0348e-453">**Zweck**</span><span class="sxs-lookup"><span data-stu-id="0348e-453">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-454">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0348e-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-455">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-456">Eine Zeichenfolge, die die Medien und/oder deren Verwendung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="0348e-456">A string that describes the media and/or its use.</span></span> <span data-ttu-id="0348e-457">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-457">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="0348e-458">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="0348e-458">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-459">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0348e-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-460">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-461">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="0348e-461">The last requested or desired state for the element.</span></span> <span data-ttu-id="0348e-462">Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0348e-462">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="0348e-463">Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuell aktivierten oder deaktivierten Zustände zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="0348e-463">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="0348e-464">Eine bestimmte Instanz von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) unterstützt möglicherweise nicht die **requestStateChange** -Methode.</span><span class="sxs-lookup"><span data-stu-id="0348e-464">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="0348e-465">Wenn dies auftritt, wird der Wert 12 (nicht zutreffend) verwendet.</span><span class="sxs-lookup"><span data-stu-id="0348e-465">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="0348e-466">Diese Eigenschaft wird von **CIM \_ enabledlogicalelement** geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-466">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="0348e-467">**SequentialAccess**</span><span class="sxs-lookup"><span data-stu-id="0348e-467">**SequentialAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-468">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="0348e-468">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-469">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-470">Gibt an, ob ein Medien Zugriffsgerät sequenziell auf den Speicher zugreift.</span><span class="sxs-lookup"><span data-stu-id="0348e-470">Indicates whether the storage is sequentially accessed by a media access device.</span></span> <span data-ttu-id="0348e-471">Ein Pass-Through-Band Medium ist ein Beispiel für einen Speicherblock, auf den sequenziell zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="0348e-471">Pass-through tape media is an example of a sequentially accessed storage extent.</span></span> <span data-ttu-id="0348e-472">Diese Eigenschaft wird von [**CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-472">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="0348e-473">**Status**</span><span class="sxs-lookup"><span data-stu-id="0348e-473">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-474">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0348e-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-475">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-476">Der aktuelle Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="0348e-476">The current status of the object.</span></span> <span data-ttu-id="0348e-477">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0348e-477">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0348e-478">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="0348e-478">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-479">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="0348e-479">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0348e-480">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-480">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-481">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="0348e-481">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="0348e-482">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-482">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0348e-483">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="0348e-483">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-484">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0348e-484">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-485">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-485">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-486">Der aktuelle Zustand des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="0348e-486">The current state of the logical device.</span></span> <span data-ttu-id="0348e-487">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0348e-487">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0348e-488">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="0348e-488">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-489">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0348e-489">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-490">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-490">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-491">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="0348e-491">The scoping system's creation class name.</span></span> <span data-ttu-id="0348e-492">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-492">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="0348e-493">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="0348e-493">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-494">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0348e-494">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-495">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-495">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-496">Der eindeutige Bezeichner für die Bereichs bezogene virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="0348e-496">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="0348e-497">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-497">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="0348e-498">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="0348e-498">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-499">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="0348e-499">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-500">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-500">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-501">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="0348e-501">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="0348e-502">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="0348e-502">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0348e-503">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="0348e-503">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-504">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0348e-504">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-505">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-505">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-506">Die Gesamtanzahl der Stunden, für die dieses Gerät eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="0348e-506">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="0348e-507">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0348e-507">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0348e-508">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="0348e-508">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0348e-509">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0348e-509">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0348e-510">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0348e-510">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0348e-511">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="0348e-511">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="0348e-512">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0348e-512">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0348e-513">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0348e-513">Remarks</span></span>

<span data-ttu-id="0348e-514">Der Zugriff auf die **MSVM \_ LogicalDisk** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="0348e-514">Access to the **Msvm\_LogicalDisk** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="0348e-515">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="0348e-515">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="0348e-516">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0348e-516">Requirements</span></span>



| <span data-ttu-id="0348e-517">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0348e-517">Requirement</span></span> | <span data-ttu-id="0348e-518">Wert</span><span class="sxs-lookup"><span data-stu-id="0348e-518">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0348e-519">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0348e-519">Minimum supported client</span></span><br/> | <span data-ttu-id="0348e-520">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0348e-520">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0348e-521">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0348e-521">Minimum supported server</span></span><br/> | <span data-ttu-id="0348e-522">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0348e-522">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0348e-523">Namespace</span><span class="sxs-lookup"><span data-stu-id="0348e-523">Namespace</span></span><br/>                | <span data-ttu-id="0348e-524">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="0348e-524">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0348e-525">MOF</span><span class="sxs-lookup"><span data-stu-id="0348e-525">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0348e-526"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0348e-526"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0348e-527">DLL</span><span class="sxs-lookup"><span data-stu-id="0348e-527">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0348e-528"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0348e-528"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0348e-529">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0348e-529">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0348e-530">**CIM \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="0348e-530">**CIM\_LogicalDisk**</span></span>](cim-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="0348e-531">**CIM \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="0348e-531">**CIM\_LogicalDisk**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldisk)
</dt> <dt>

[<span data-ttu-id="0348e-532">**MSVM \_ storagealert**</span><span class="sxs-lookup"><span data-stu-id="0348e-532">**Msvm\_StorageAlert**</span></span>](msvm-storagealert.md)
</dt> <dt>

[<span data-ttu-id="0348e-533">Speicher Klassen</span><span class="sxs-lookup"><span data-stu-id="0348e-533">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

