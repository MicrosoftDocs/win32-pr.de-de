---
description: Stellt ein Festplattenlaufwerk innerhalb eines virtuellen Computers dar.
ms.assetid: BF03CD02-7CDE-45E2-84D1-EC8E4457094A
title: Msvm_DiskDrive-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DiskDrive
- Msvm_DiskDrive.SetPowerState
- Msvm_DiskDrive.EnableDevice
- Msvm_DiskDrive.OnlineDevice
- Msvm_DiskDrive.QuiesceDevice
- Msvm_DiskDrive.SaveProperties
- Msvm_DiskDrive.RestoreProperties
- Msvm_DiskDrive.InstanceID
- Msvm_DiskDrive.Caption
- Msvm_DiskDrive.Description
- Msvm_DiskDrive.ElementName
- Msvm_DiskDrive.InstallDate
- Msvm_DiskDrive.Name
- Msvm_DiskDrive.OperationalStatus
- Msvm_DiskDrive.StatusDescriptions
- Msvm_DiskDrive.Status
- Msvm_DiskDrive.HealthState
- Msvm_DiskDrive.CommunicationStatus
- Msvm_DiskDrive.DetailedStatus
- Msvm_DiskDrive.OperatingStatus
- Msvm_DiskDrive.PrimaryStatus
- Msvm_DiskDrive.EnabledState
- Msvm_DiskDrive.OtherEnabledState
- Msvm_DiskDrive.RequestedState
- Msvm_DiskDrive.EnabledDefault
- Msvm_DiskDrive.TimeOfLastStateChange
- Msvm_DiskDrive.AvailableRequestedStates
- Msvm_DiskDrive.TransitioningToState
- Msvm_DiskDrive.SystemCreationClassName
- Msvm_DiskDrive.SystemName
- Msvm_DiskDrive.CreationClassName
- Msvm_DiskDrive.DeviceID
- Msvm_DiskDrive.PowerManagementSupported
- Msvm_DiskDrive.PowerManagementCapabilities
- Msvm_DiskDrive.Availability
- Msvm_DiskDrive.StatusInfo
- Msvm_DiskDrive.LastErrorCode
- Msvm_DiskDrive.ErrorDescription
- Msvm_DiskDrive.ErrorCleared
- Msvm_DiskDrive.OtherIdentifyingInfo
- Msvm_DiskDrive.PowerOnHours
- Msvm_DiskDrive.TotalPowerOnHours
- Msvm_DiskDrive.IdentifyingDescriptions
- Msvm_DiskDrive.AdditionalAvailability
- Msvm_DiskDrive.MaxQuiesceTime
- Msvm_DiskDrive.Capabilities
- Msvm_DiskDrive.CapabilityDescriptions
- Msvm_DiskDrive.ErrorMethodology
- Msvm_DiskDrive.CompressionMethod
- Msvm_DiskDrive.NumberOfMediaSupported
- Msvm_DiskDrive.MaxMediaSize
- Msvm_DiskDrive.DefaultBlockSize
- Msvm_DiskDrive.MaxBlockSize
- Msvm_DiskDrive.MinBlockSize
- Msvm_DiskDrive.NeedsCleaning
- Msvm_DiskDrive.MediaIsLocked
- Msvm_DiskDrive.Security
- Msvm_DiskDrive.LastCleaned
- Msvm_DiskDrive.MaxAccessTime
- Msvm_DiskDrive.UncompressedDataRate
- Msvm_DiskDrive.LoadTime
- Msvm_DiskDrive.UnloadTime
- Msvm_DiskDrive.MountCount
- Msvm_DiskDrive.TimeOfLastMount
- Msvm_DiskDrive.TotalMountTime
- Msvm_DiskDrive.UnitsDescription
- Msvm_DiskDrive.MaxUnitsBeforeCleaning
- Msvm_DiskDrive.UnitsUsed
- Msvm_DiskDrive.DriveNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 60a08a2b73149285ddf3b0edf0003e5490b1c5c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867959"
---
# <a name="msvm_diskdrive-class"></a><span data-ttu-id="22348-103">MSVM \_ diskdrive-Klasse</span><span class="sxs-lookup"><span data-stu-id="22348-103">Msvm\_DiskDrive class</span></span>

<span data-ttu-id="22348-104">Stellt ein Festplattenlaufwerk innerhalb eines virtuellen Computers dar.</span><span class="sxs-lookup"><span data-stu-id="22348-104">Represents a hard disk drive inside of a virtual machine.</span></span> <span data-ttu-id="22348-105">Bei dieser Festplatte kann es sich entweder um ein Pass-Through-Gerät (wenn eine physische Festplatte an den virtuellen Computer angefügt wurde) oder um ein synthetisches Gerät handeln, das mit virtuellen Festplatten Medien gefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="22348-105">This hard disk drive can be either a pass-through device (if a physical hard disk was attached to the virtual machine) or a synthetic device that is populated with virtual hard disk media.</span></span> <span data-ttu-id="22348-106">Da virtuelle und physische Festplatten dem virtuellen Computer hinzugefügt und daraus entfernt werden können, gibt es zwei Ressourcenpools, die dieser Klasse zugeordnet sind, eine für Pass-Through-Festplatten und die andere für virtuelle Festplatten.</span><span class="sxs-lookup"><span data-stu-id="22348-106">Because virtual and physical hard disks can be added and removed from the virtual machine, there are two resource pools associated with this class, one for pass-through hard disks and the other for virtual hard disks.</span></span> <span data-ttu-id="22348-107">Festplatten können nur dem virtuellen SCSI-Controller hinzugefügt oder daraus entfernt werden, wenn der virtuelle Computer online ist.</span><span class="sxs-lookup"><span data-stu-id="22348-107">Hard disks can only be added to or removed from the virtual SCSI controller when the virtual machine is online.</span></span> <span data-ttu-id="22348-108">Datenträger können nur dem virtuellen IDE-Controller hinzugefügt oder daraus entfernt werden, wenn der virtuelle Computer offline ist.</span><span class="sxs-lookup"><span data-stu-id="22348-108">Disks can only be added to or removed from the virtual IDE controller when the virtual machine is offline.</span></span>

<span data-ttu-id="22348-109">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="22348-109">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="22348-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="22348-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DiskDrive : CIM_DiskDrive
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
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
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   ErrorMethodology = "None";
  string   CompressionMethod = "Not Compressed";
  uint32   NumberOfMediaSupported = 1;
  uint64   MaxMediaSize = 2000000000;
  uint64   DefaultBlockSize = 512;
  uint64   MaxBlockSize;
  uint64   MinBlockSize = 512;
  boolean  NeedsCleaning = False;
  boolean  MediaIsLocked = True;
  uint16   Security = 3;
  datetime LastCleaned;
  uint64   MaxAccessTime = 0;
  uint32   UncompressedDataRate;
  uint64   LoadTime = 0;
  uint64   UnloadTime = 0;
  uint64   MountCount = 0;
  datetime TimeOfLastMount;
  uint64   TotalMountTime = 0;
  string   UnitsDescription;
  uint64   MaxUnitsBeforeCleaning = 0xffffffffffffffff;
  uint64   UnitsUsed = 0;
  uint32   DriveNumber;
};
```

## <a name="members"></a><span data-ttu-id="22348-111">Member</span><span class="sxs-lookup"><span data-stu-id="22348-111">Members</span></span>

<span data-ttu-id="22348-112">Die **MSVM \_ diskdrive** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="22348-112">The **Msvm\_DiskDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="22348-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="22348-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="22348-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="22348-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="22348-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="22348-115">Methods</span></span>

<span data-ttu-id="22348-116">Die **MSVM \_ diskdrive** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="22348-116">The **Msvm\_DiskDrive** class has these methods.</span></span>



| <span data-ttu-id="22348-117">Methode</span><span class="sxs-lookup"><span data-stu-id="22348-117">Method</span></span>                                                          | <span data-ttu-id="22348-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="22348-118">Description</span></span>                              |
|:----------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="22348-119">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="22348-119">**EnableDevice**</span></span>                                                | <span data-ttu-id="22348-120">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="22348-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="22348-121">**Lockmedia**</span><span class="sxs-lookup"><span data-stu-id="22348-121">**LockMedia**</span></span>](msvm-diskdrive-lockmedia.md)                   | <span data-ttu-id="22348-122">Sperrt oder gibt die Medien frei.</span><span class="sxs-lookup"><span data-stu-id="22348-122">Locks or releases the media.</span></span><br/>  |
| <span data-ttu-id="22348-123">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="22348-123">**OnlineDevice**</span></span>                                                | <span data-ttu-id="22348-124">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="22348-124">This method is not supported.</span></span><br/> |
| <span data-ttu-id="22348-125">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="22348-125">**QuiesceDevice**</span></span>                                               | <span data-ttu-id="22348-126">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="22348-126">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="22348-127">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="22348-127">**RequestStateChange**</span></span>](msvm-diskdrive-requeststatechange.md) | <span data-ttu-id="22348-128">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="22348-128">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="22348-129">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="22348-129">**Reset**</span></span>](msvm-diskdrive-reset.md)                           | <span data-ttu-id="22348-130">Setzt das virtuelle Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="22348-130">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="22348-131">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="22348-131">**RestoreProperties**</span></span>                                           | <span data-ttu-id="22348-132">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="22348-132">This method is not supported.</span></span><br/> |
| <span data-ttu-id="22348-133">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="22348-133">**SaveProperties**</span></span>                                              | <span data-ttu-id="22348-134">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="22348-134">This method is not supported.</span></span><br/> |
| <span data-ttu-id="22348-135">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="22348-135">**SetPowerState**</span></span>                                               | <span data-ttu-id="22348-136">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="22348-136">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="22348-137">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="22348-137">Properties</span></span>

<span data-ttu-id="22348-138">Die **MSVM \_ diskdrive** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="22348-138">The **Msvm\_DiskDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="22348-139">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="22348-139">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-140">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="22348-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="22348-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-142">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist auf 6 festgelegt (nicht zutreffend).</span><span class="sxs-lookup"><span data-stu-id="22348-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="22348-143">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="22348-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-144">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22348-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22348-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-146">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="22348-146">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="22348-147">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="22348-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-148">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="22348-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="22348-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-150">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="22348-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="22348-151">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="22348-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="22348-152">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="22348-152">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-153">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="22348-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="22348-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-155">Die Funktionen des Medien Zugriffs Geräts.</span><span class="sxs-lookup"><span data-stu-id="22348-155">The capabilities of the media access device.</span></span> <span data-ttu-id="22348-156">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt und auf die folgenden Werte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22348-156">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to the following values.</span></span>



| <span data-ttu-id="22348-157">Wert</span><span class="sxs-lookup"><span data-stu-id="22348-157">Value</span></span>                                                                        | <span data-ttu-id="22348-158">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="22348-158">Meaning</span></span>                                                                                 |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="22348-159"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="22348-159"><dt>3</dt></span></span> </dl> | <span data-ttu-id="22348-160">Der entsprechende Eintrag in **capabilitybeschreibungen** ist "zufälliger Zugriff".</span><span class="sxs-lookup"><span data-stu-id="22348-160">The corresponding entry in **CapabilityDescriptions** is "Random Access".</span></span><br/>    |
| <dl> <span data-ttu-id="22348-161"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="22348-161"><dt>4</dt></span></span> </dl> | <span data-ttu-id="22348-162">Der entsprechende Eintrag in **capabilitybeschreibungen** ist "unterstützt Schreibvorgänge".</span><span class="sxs-lookup"><span data-stu-id="22348-162">The corresponding entry in **CapabilityDescriptions** is "Supports Writing".</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="22348-163">**Capabilitybeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="22348-163">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-164">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="22348-164">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="22348-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-166">Ein Array von Freiform-Zeichen folgen, das ausführliche Erläuterungen für den Zugriff auf Gerätefunktionen bereitstellt, die im **Eigenschaften Array Funktionen** angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="22348-166">An array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** property array.</span></span> <span data-ttu-id="22348-167">Jeder Eintrag dieses Arrays bezieht sich auf den Eintrag im Eigenschafts Array " **Funktionen** ", der sich am selben Index befindet.</span><span class="sxs-lookup"><span data-stu-id="22348-167">Each entry of this array is related to the entry in the **Capabilities** property array, located at the same index.</span></span> <span data-ttu-id="22348-168">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="22348-168">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="22348-169">**Caption**</span><span class="sxs-lookup"><span data-stu-id="22348-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-170">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="22348-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22348-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-172">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="22348-172">A short description of the object.</span></span> <span data-ttu-id="22348-173">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="22348-173">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="22348-174">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="22348-174">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-175">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22348-175">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22348-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-177">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="22348-177">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="22348-178">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="22348-178">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="22348-179">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="22348-179">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="22348-180"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="22348-180"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="22348-181"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="22348-181"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="22348-182"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="22348-182"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="22348-183"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="22348-183"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="22348-184"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="22348-184"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="22348-185"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="22348-185"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="22348-186"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="22348-186"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="22348-187">)</span><span class="sxs-lookup"><span data-stu-id="22348-187">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="22348-188">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="22348-188">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-189">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="22348-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22348-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-191">Eine Zeichenfolge, die den Algorithmus oder das Tool angibt, das zum Komprimieren der logischen Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="22348-191">A string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="22348-192">Wenn das Komprimierungs Schema unbekannt oder nicht beschrieben ist, verwenden Sie "unknown".</span><span class="sxs-lookup"><span data-stu-id="22348-192">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="22348-193">Wenn die logische Datei komprimiert ist, das Komprimierungs Schema jedoch unbekannt oder nicht beschrieben ist, verwenden Sie "komprimiert".</span><span class="sxs-lookup"><span data-stu-id="22348-193">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="22348-194">Wenn die logische Datei nicht komprimiert ist, verwenden Sie "nicht komprimiert".</span><span class="sxs-lookup"><span data-stu-id="22348-194">If the logical file is not compressed, use "Not Compressed".</span></span> <span data-ttu-id="22348-195">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt und ist auf "nicht komprimiert" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22348-195">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to "Not Compressed".</span></span>

</dd> <dt>

<span data-ttu-id="22348-196">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="22348-196">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-197">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22348-197">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22348-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-199">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="22348-199">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="22348-200">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="22348-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="22348-201">**Defaultblocksize**</span><span class="sxs-lookup"><span data-stu-id="22348-201">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-202">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="22348-202">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="22348-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-204">Die Standard Blockgröße (in Bytes) für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="22348-204">The default block size, in bytes, for the device.</span></span> <span data-ttu-id="22348-205">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt und auf 512 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22348-205">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 512.</span></span>

</dd> <dt>

<span data-ttu-id="22348-206">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="22348-206">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-207">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="22348-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22348-208">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-209">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="22348-209">A description of the object.</span></span> <span data-ttu-id="22348-210">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="22348-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="22348-211">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="22348-211">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-212">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22348-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22348-213">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-214">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="22348-214">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="22348-215">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="22348-215">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="22348-216">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="22348-216">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="22348-217"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="22348-217"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="22348-218"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="22348-218"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="22348-219"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="22348-219"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="22348-220"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="22348-220"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="22348-221"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="22348-221"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="22348-222"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="22348-222"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="22348-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="22348-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="22348-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="22348-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="22348-225">)</span><span class="sxs-lookup"><span data-stu-id="22348-225">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="22348-226">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="22348-226">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-227">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="22348-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22348-228">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-229">Eine Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="22348-229">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="22348-230">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="22348-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="22348-231">**Drivenreiber**</span><span class="sxs-lookup"><span data-stu-id="22348-231">**DriveNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-232">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="22348-232">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="22348-233">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-234">Die Anzahl der physischen Laufwerke auf dem hostingcomputersystem.</span><span class="sxs-lookup"><span data-stu-id="22348-234">The number of the physical drives on the hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="22348-235">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="22348-235">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-236">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="22348-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22348-237">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-238">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="22348-238">A display name for the object.</span></span> <span data-ttu-id="22348-239">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="22348-239">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="22348-240">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="22348-240">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-241">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22348-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22348-242">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-243">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="22348-243">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="22348-244">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="22348-244">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="22348-245">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="22348-245">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-246">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22348-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22348-247">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-248">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="22348-248">The enabled and disabled states of an element.</span></span> <span data-ttu-id="22348-249">Sie kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben.</span><span class="sxs-lookup"><span data-stu-id="22348-249">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="22348-250">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="22348-250">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="22348-251">Wert</span><span class="sxs-lookup"><span data-stu-id="22348-251">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="22348-252">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="22348-252">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="22348-253"><dt>**Unbekannter**</dt> Wert <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="22348-253"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="22348-254">Der Zustand des Elements konnte nicht bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="22348-254">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="22348-255"><dt>**Sonstige**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="22348-255"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="22348-256"><dt>**Aktiviert**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="22348-256"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="22348-257">Das-Element wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="22348-257">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="22348-258"><dt>**Deaktiviert**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="22348-258"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="22348-259">Das Element ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="22348-259">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="22348-260"><dt>4</dt> wird <dt>**heruntergefahren**</dt></span><span class="sxs-lookup"><span data-stu-id="22348-260"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="22348-261">Das Element wird gerade in den deaktivierten Zustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="22348-261">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="22348-262"><dt>**Nicht zutreffend**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="22348-262"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="22348-263">Das Element unterstützt das Aktivieren oder Deaktivieren des Elements nicht.</span><span class="sxs-lookup"><span data-stu-id="22348-263">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="22348-264"><dt>**Aktiviert, aber offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="22348-264"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="22348-265">Das Element kann Befehle abschließen und löscht alle neuen Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="22348-265">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="22348-266"><dt>**In Test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="22348-266"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="22348-267">Das-Element befindet sich in einem Testzustand.</span><span class="sxs-lookup"><span data-stu-id="22348-267">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="22348-268"><dt></dt> Verzögert <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="22348-268"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="22348-269">Das Element kann Befehle abschließen, aber alle neuen Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="22348-269">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="22348-270"><dt>**Inesce**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="22348-270"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="22348-271">Das-Element ist aktiviert, befindet sich jedoch in einem eingeschränkten Modus.</span><span class="sxs-lookup"><span data-stu-id="22348-271">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="22348-272">Das Verhalten des-Elements ähnelt dem aktivierten Status (2), aber es verarbeitet nur einen eingeschränkten Satz von Befehlen.</span><span class="sxs-lookup"><span data-stu-id="22348-272">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="22348-273">Alle anderen Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="22348-273">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="22348-274"><dt>**Start**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="22348-274"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="22348-275">Das Element wechselt in den Zustand "aktiviert" (2).</span><span class="sxs-lookup"><span data-stu-id="22348-275">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="22348-276">Neue Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="22348-276">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="22348-277">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="22348-277">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-278">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="22348-278">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="22348-279">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-280">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="22348-280">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="22348-281">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="22348-281">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-282">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="22348-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22348-283">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-284">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="22348-284">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="22348-285">**Errormethodmethodologie**</span><span class="sxs-lookup"><span data-stu-id="22348-285">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-286">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="22348-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22348-287">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-288">Eine Zeichenfolge, die die von diesem Gerät unterstützten Fehler Erkennungs-und Korrektur Typen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="22348-288">A string that describes the types of error detection and correction supported by this device.</span></span> <span data-ttu-id="22348-289">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt und ist auf "None" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22348-289">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to "None".</span></span>

</dd> <dt>

<span data-ttu-id="22348-290">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="22348-290">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-291">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22348-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22348-292">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-293">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="22348-293">The current health of the element.</span></span> <span data-ttu-id="22348-294">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="22348-294">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="22348-295">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="22348-295">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="22348-296">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 5 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22348-296">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="22348-297">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="22348-297">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-298">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="22348-298">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="22348-299">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-300">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22348-300">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="22348-301">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="22348-301">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-302">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="22348-302">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="22348-303">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-304">Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="22348-304">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="22348-305">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="22348-305">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="22348-306">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="22348-306">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-307">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="22348-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22348-308">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22348-309">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="22348-309">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="22348-310">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="22348-310">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="22348-311">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="22348-311">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="22348-312">**Lastbereinigt**</span><span class="sxs-lookup"><span data-stu-id="22348-312">**LastCleaned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-313">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="22348-313">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="22348-314">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-315">Das Datum und die Uhrzeit der letzten Bereinigung des Geräts.</span><span class="sxs-lookup"><span data-stu-id="22348-315">The date and time when the device was last cleaned.</span></span> <span data-ttu-id="22348-316">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt und ist auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22348-316">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="22348-317">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="22348-317">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-318">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="22348-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="22348-319">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-320">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="22348-320">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="22348-321">**Loadtime**</span><span class="sxs-lookup"><span data-stu-id="22348-321">**LoadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-322">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="22348-322">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="22348-323">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-324">Die Zeit (in Millisekunden) von der Auslastung bis zum Lesen oder Schreiben eines Mediums.</span><span class="sxs-lookup"><span data-stu-id="22348-324">The time, in milliseconds, from load to being able to read or write a media.</span></span> <span data-ttu-id="22348-325">Beispielsweise ist dies das Intervall für Laufwerke zwischen einem Datenträger, der nicht auf die Festplatte zeigt, dass er für Lese-/Schreibzugriff bereit ist (d. h., der Datenträger wird mit nominaler Geschwindigkeit).</span><span class="sxs-lookup"><span data-stu-id="22348-325">For example, for disk drives, this is the interval between a disk not spinning to the disk reporting that it is ready for read/write (that is, the disk spinning at nominal speeds).</span></span> <span data-ttu-id="22348-326">Bei Bandlaufwerken ist dies der Zeitpunkt, zu dem ein Medium eingefügt wird, um zu melden, dass es für eine Anwendung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="22348-326">For tape drives, this is the time from a media being injected to reporting that it is ready for an application.</span></span> <span data-ttu-id="22348-327">Dies befindet sich normalerweise im botbereich des Bands.</span><span class="sxs-lookup"><span data-stu-id="22348-327">This is usually at the tape's BOT area.</span></span> <span data-ttu-id="22348-328">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice) geerbt und auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22348-328">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice) and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="22348-329">**Maxaccesstime**</span><span class="sxs-lookup"><span data-stu-id="22348-329">**MaxAccessTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-330">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="22348-330">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="22348-331">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-332">Die Zeit (in Millisekunden), die von der ersten Position auf dem Medium an den Speicherort verschoben werden soll, der in Bezug auf die Zeit am weitesten ist.</span><span class="sxs-lookup"><span data-stu-id="22348-332">The time, in milliseconds, to move from the first location on the media to the location that is furthest with respect to time.</span></span> <span data-ttu-id="22348-333">Bei einem Laufwerk stellt dies eine vollständige Suche und eine vollständige Rotationsverzögerung dar.</span><span class="sxs-lookup"><span data-stu-id="22348-333">For a disk drive, this represents full seek and full rotational delay.</span></span> <span data-ttu-id="22348-334">Bei Bandlaufwerken stellt dies eine Suche zwischen dem Anfang des Bands und dem physisch entfernten Punkt dar.</span><span class="sxs-lookup"><span data-stu-id="22348-334">For tape drives, this represents a search from the beginning of the tape to the most physically distant point.</span></span> <span data-ttu-id="22348-335">(Das Ende eines Bands kann sich am physisch entfernten Punkt befinden, dies ist jedoch nicht unbedingt der Fall.) Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt und auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22348-335">(The end of a tape may be at its most physically distant point, but this is not necessarily true.) This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="22348-336">**Maxblocksize**</span><span class="sxs-lookup"><span data-stu-id="22348-336">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-337">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="22348-337">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="22348-338">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-339">Die maximale Blockgröße (in Bytes) für Medien, auf die das Gerät zugreift.</span><span class="sxs-lookup"><span data-stu-id="22348-339">The maximum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="22348-340">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt und ist für virtuelle Festplattenlaufwerke auf 512 festgelegt, Variable für Pass-Through-Laufwerke.</span><span class="sxs-lookup"><span data-stu-id="22348-340">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 512 for virtual hard disk drives, variable for pass-through drives.</span></span>

</dd> <dt>

<span data-ttu-id="22348-341">**Maxmediasize**</span><span class="sxs-lookup"><span data-stu-id="22348-341">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-342">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="22348-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="22348-343">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-344">Die maximale Größe des von diesem Gerät unterstützten Mediums in Kilobyte.</span><span class="sxs-lookup"><span data-stu-id="22348-344">The maximum size, in kilobytes, of media supported by this device.</span></span> <span data-ttu-id="22348-345">Kilobytes werden als Anzahl von Bytes, multipliziert mit 1000, interpretiert (nicht die Anzahl der Bytes multipliziert mit 1024).</span><span class="sxs-lookup"><span data-stu-id="22348-345">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span> <span data-ttu-id="22348-346">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt und ist für virtuelle Festplattenlaufwerke auf 2 Milliarden festgelegt, Variable für Pass-Through-Laufwerke.</span><span class="sxs-lookup"><span data-stu-id="22348-346">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 2,000,000,000 for virtual hard disk drives, variable for pass-through drives.</span></span>

</dd> <dt>

<span data-ttu-id="22348-347">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="22348-347">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-348">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="22348-348">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="22348-349">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-350">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="22348-350">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="22348-351">**Maxunitionbeforecforec**</span><span class="sxs-lookup"><span data-stu-id="22348-351">**MaxUnitsBeforeCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-352">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="22348-352">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="22348-353">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-354">Die maximalen Einheiten, die verwendet werden können, bevor das Gerät bereinigt wird.</span><span class="sxs-lookup"><span data-stu-id="22348-354">The maximum units that can be used before the device should be cleaned.</span></span> <span data-ttu-id="22348-355">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt und auf 0xFFFFFFFFFFFFFFFF festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22348-355">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0xffffffffffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="22348-356">**Mediaislocked**</span><span class="sxs-lookup"><span data-stu-id="22348-356">**MediaIsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-357">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="22348-357">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="22348-358">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-359">**True** , wenn die Medien im Gerät gesperrt sind und nicht aussteht. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="22348-359">**True** if the media is locked in the device and cannot be ejected; otherwise, **False**.</span></span> <span data-ttu-id="22348-360">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt und ist auf **true** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22348-360">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="22348-361">**Minblocksize**</span><span class="sxs-lookup"><span data-stu-id="22348-361">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-362">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="22348-362">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="22348-363">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-364">Die minimale Blockgröße (in Bytes) für Medien, auf die das Gerät zugreift.</span><span class="sxs-lookup"><span data-stu-id="22348-364">The minimum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="22348-365">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt und auf 512 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22348-365">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 512.</span></span>

</dd> <dt>

<span data-ttu-id="22348-366">**Mountcount**</span><span class="sxs-lookup"><span data-stu-id="22348-366">**MountCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-367">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="22348-367">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="22348-368">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-369">Bei Geräten, die Wechselmedien unterstützen, gibt es die Häufigkeit, mit der Medien für die Datenübertragung bereitgestellt oder das Gerät bereinigt werden.</span><span class="sxs-lookup"><span data-stu-id="22348-369">For a device that supports removable media, the number of times that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="22348-370">Bei Geräten, die auf nicht Wechselmedien (z. b. Festplatten) zugreifen, ist diese Eigenschaft nicht anwendbar und sollte auf 0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="22348-370">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="22348-371">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt und auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22348-371">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="22348-372">**Name**</span><span class="sxs-lookup"><span data-stu-id="22348-372">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-373">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="22348-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22348-374">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-375">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="22348-375">The label by which the object is known.</span></span> <span data-ttu-id="22348-376">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="22348-376">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="22348-377">**Unnötig**</span><span class="sxs-lookup"><span data-stu-id="22348-377">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-378">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="22348-378">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="22348-379">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-380">**True** , wenn das Medien Zugriffsgerät bereinigt werden muss. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="22348-380">**True** if the media access device needs cleaning; otherwise, **False**.</span></span> <span data-ttu-id="22348-381">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt und ist auf **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22348-381">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="22348-382">**"Numofmediasupportiert"**</span><span class="sxs-lookup"><span data-stu-id="22348-382">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-383">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="22348-383">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="22348-384">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-385">Die maximale Anzahl von mehreren einzelnen Medien, die unterstützt oder eingefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="22348-385">The maximum number of multiple individual media that can be supported or inserted.</span></span> <span data-ttu-id="22348-386">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt und auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22348-386">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="22348-387">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="22348-387">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-388">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22348-388">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22348-389">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-390">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="22348-390">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="22348-391">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="22348-391">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="22348-392">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="22348-392">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="22348-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="22348-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="22348-394"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="22348-394"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="22348-395"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="22348-395"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="22348-396"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="22348-396"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="22348-397"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="22348-397"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="22348-398"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="22348-398"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="22348-399"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="22348-399"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="22348-400"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="22348-400"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="22348-401"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="22348-401"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="22348-402"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="22348-402"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="22348-403"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="22348-403"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="22348-404"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="22348-404"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="22348-405"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="22348-405"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="22348-406"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="22348-406"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="22348-407"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="22348-407"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="22348-408"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="22348-408"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="22348-409"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="22348-409"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="22348-410"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="22348-410"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="22348-411"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="22348-411"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="22348-412">)</span><span class="sxs-lookup"><span data-stu-id="22348-412">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="22348-413">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="22348-413">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-414">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="22348-414">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="22348-415">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-416">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="22348-416">The current statuses of the object.</span></span> <span data-ttu-id="22348-417">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="22348-417">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="22348-418">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="22348-418">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-419">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="22348-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22348-420">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-421">Der aktivierte oder deaktivierte Status des Elements, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="22348-421">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="22348-422">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="22348-422">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="22348-423">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22348-423">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="22348-424">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="22348-424">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-425">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="22348-425">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="22348-426">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-427">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22348-427">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="22348-428">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="22348-428">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-429">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="22348-429">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="22348-430">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-431">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="22348-431">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="22348-432">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="22348-432">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-433">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="22348-433">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="22348-434">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-435">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="22348-435">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="22348-436">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="22348-436">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-437">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="22348-437">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="22348-438">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-438">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-439">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="22348-439">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="22348-440">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="22348-440">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-441">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22348-441">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22348-442">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-443">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="22348-443">Provides high level status information.</span></span> <span data-ttu-id="22348-444">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="22348-444">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="22348-445">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="22348-445">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="22348-446">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="22348-446">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="22348-447"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="22348-447"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="22348-448"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="22348-448"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="22348-449"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="22348-449"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="22348-450"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="22348-450"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="22348-451"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="22348-451"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="22348-452"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="22348-452"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="22348-453">)</span><span class="sxs-lookup"><span data-stu-id="22348-453">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="22348-454">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="22348-454">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-455">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22348-455">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22348-456">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-457">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="22348-457">The last requested or desired state for the element.</span></span> <span data-ttu-id="22348-458">Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="22348-458">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="22348-459">Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuell aktivierten oder deaktivierten Zustände zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="22348-459">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="22348-460">Eine bestimmte Instanz von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) unterstützt möglicherweise nicht die **requestStateChange** -Methode.</span><span class="sxs-lookup"><span data-stu-id="22348-460">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="22348-461">Wenn dies auftritt, wird der Wert 12 (nicht zutreffend) verwendet.</span><span class="sxs-lookup"><span data-stu-id="22348-461">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="22348-462">Diese Eigenschaft wird von **CIM \_ enabledlogicalelement** geerbt.</span><span class="sxs-lookup"><span data-stu-id="22348-462">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="22348-463">**Security**</span><span class="sxs-lookup"><span data-stu-id="22348-463">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-464">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22348-464">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22348-465">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-466">Die für das Gerät definierte Betriebssicherheit.</span><span class="sxs-lookup"><span data-stu-id="22348-466">The operational security defined for the device.</span></span> <span data-ttu-id="22348-467">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt und ist auf 3 (keine) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22348-467">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 3 (None).</span></span>

</dd> <dt>

<span data-ttu-id="22348-468">**Status**</span><span class="sxs-lookup"><span data-stu-id="22348-468">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-469">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="22348-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22348-470">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-471">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="22348-471">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="22348-472">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="22348-472">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-473">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="22348-473">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="22348-474">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-474">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-475">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="22348-475">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="22348-476">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="22348-476">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="22348-477">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="22348-477">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-478">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22348-478">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22348-479">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-479">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-480">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="22348-480">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="22348-481">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="22348-481">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-482">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="22348-482">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22348-483">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-483">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-484">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="22348-484">The scoping system's creation class name.</span></span> <span data-ttu-id="22348-485">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="22348-485">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="22348-486">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="22348-486">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-487">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="22348-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22348-488">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-488">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-489">Der eindeutige Bezeichner für die Bereichs bezogene virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="22348-489">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="22348-490">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="22348-490">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="22348-491">**Timeoflastmount**</span><span class="sxs-lookup"><span data-stu-id="22348-491">**TimeOfLastMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-492">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="22348-492">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="22348-493">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-493">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-494">Für ein Gerät, das Wechselmedien unterstützt, das Datum und die Uhrzeit der letzten Bereitstellung des Mediums auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="22348-494">For a device that supports removable media, the most recent date and time that media was mounted on the device.</span></span> <span data-ttu-id="22348-495">Bei Geräten, die auf nicht Wechselmedien wie Festplatten zugreifen, hat diese Eigenschaft keine Bedeutung und ist nicht anwendbar.</span><span class="sxs-lookup"><span data-stu-id="22348-495">For devices accessing nonremovable media, such as hard disks, this property has no meaning and is not applicable.</span></span> <span data-ttu-id="22348-496">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt und ist auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22348-496">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="22348-497">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="22348-497">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-498">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="22348-498">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="22348-499">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-499">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-500">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="22348-500">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="22348-501">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf "Null" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22348-501">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to "NULL".</span></span>

</dd> <dt>

<span data-ttu-id="22348-502">**Totalmounttime**</span><span class="sxs-lookup"><span data-stu-id="22348-502">**TotalMountTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-503">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="22348-503">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="22348-504">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-505">Für ein Gerät, das Wechselmedien unterstützt, die Gesamtzeit (in Sekunden), die Medien für die Datenübertragung bereitgestellt wurden, oder um das Gerät zu bereinigen.</span><span class="sxs-lookup"><span data-stu-id="22348-505">For a device that supports removable media, the total time (in seconds) that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="22348-506">Bei Geräten, die auf nicht Wechselmedien (z. b. Festplatten) zugreifen, ist diese Eigenschaft nicht anwendbar und sollte auf 0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="22348-506">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="22348-507">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt und auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22348-507">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="22348-508">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="22348-508">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-509">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="22348-509">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="22348-510">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-510">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-511">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="22348-511">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="22348-512">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="22348-512">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-513">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22348-513">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22348-514">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-515">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="22348-515">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="22348-516">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="22348-516">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="22348-517">**Uncompresseddatarate**</span><span class="sxs-lookup"><span data-stu-id="22348-517">**UncompressedDataRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-518">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="22348-518">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="22348-519">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-520">Die dauerhafte Datenübertragungsrate in KB/Sek., mit der das Gerät Lese-und Schreibvorgänge auf ein Medium durchführen kann.</span><span class="sxs-lookup"><span data-stu-id="22348-520">The sustained data transfer rate in KB/sec that the device can read from and write to a media.</span></span> <span data-ttu-id="22348-521">Dies ist eine dauerhafte, Rohdaten Rate.</span><span class="sxs-lookup"><span data-stu-id="22348-521">This is a sustained, raw data rate.</span></span> <span data-ttu-id="22348-522">Die maximale Anzahl von Raten oder raten, bei denen die Komprimierung nicht in dieser Eigenschaft gemeldet werden sollte</span><span class="sxs-lookup"><span data-stu-id="22348-522">Maximum rates or rates assuming compression should not be reported in this property.</span></span> <span data-ttu-id="22348-523">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt und ist auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22348-523">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="22348-524">**Unitydescription**</span><span class="sxs-lookup"><span data-stu-id="22348-524">**UnitsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-525">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="22348-525">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22348-526">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-526">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-527">Die Einheiten in Relation zur Verwendung in **maxunitionbeforecforec.**</span><span class="sxs-lookup"><span data-stu-id="22348-527">The units relative to its use in **MaxUnitsBeforeCleaning**.</span></span> <span data-ttu-id="22348-528">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt und ist auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22348-528">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="22348-529">**Unitsused**</span><span class="sxs-lookup"><span data-stu-id="22348-529">**UnitsUsed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-530">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="22348-530">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="22348-531">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-531">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-532">Die aktuelle Anzahl der verwendeten Einheiten.</span><span class="sxs-lookup"><span data-stu-id="22348-532">The current number of units used.</span></span> <span data-ttu-id="22348-533">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt und auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22348-533">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="22348-534">**Unloadtime**</span><span class="sxs-lookup"><span data-stu-id="22348-534">**UnloadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22348-535">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="22348-535">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="22348-536">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="22348-536">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22348-537">Die Zeit (in Millisekunden), die in der Lage ist, ein Medium zum Entladen zu lesen oder zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="22348-537">The time, in milliseconds, from being able to read or write a media to its unload.</span></span> <span data-ttu-id="22348-538">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt und auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22348-538">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="22348-539">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22348-539">Remarks</span></span>

<span data-ttu-id="22348-540">Der Zugriff auf die **MSVM \_ diskdrive** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="22348-540">Access to the **Msvm\_DiskDrive** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="22348-541">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="22348-541">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="22348-542">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22348-542">Requirements</span></span>



| <span data-ttu-id="22348-543">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22348-543">Requirement</span></span> | <span data-ttu-id="22348-544">Wert</span><span class="sxs-lookup"><span data-stu-id="22348-544">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22348-545">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="22348-545">Minimum supported client</span></span><br/> | <span data-ttu-id="22348-546">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22348-546">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="22348-547">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="22348-547">Minimum supported server</span></span><br/> | <span data-ttu-id="22348-548">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22348-548">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="22348-549">Namespace</span><span class="sxs-lookup"><span data-stu-id="22348-549">Namespace</span></span><br/>                | <span data-ttu-id="22348-550">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="22348-550">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="22348-551">MOF</span><span class="sxs-lookup"><span data-stu-id="22348-551">MOF</span></span><br/>                      | <dl> <span data-ttu-id="22348-552"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="22348-552"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="22348-553">DLL</span><span class="sxs-lookup"><span data-stu-id="22348-553">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22348-554"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="22348-554"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="22348-555">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22348-555">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22348-556">**CIM- \_ diskdrive**</span><span class="sxs-lookup"><span data-stu-id="22348-556">**CIM\_DiskDrive**</span></span>](cim-diskdrive.md)
</dt> <dt>

[<span data-ttu-id="22348-557">**CIM- \_ diskdrive**</span><span class="sxs-lookup"><span data-stu-id="22348-557">**CIM\_DiskDrive**</span></span>](/windows/desktop/CIMWin32Prov/cim-diskdrive)
</dt> <dt>

[<span data-ttu-id="22348-558">Speicher Klassen</span><span class="sxs-lookup"><span data-stu-id="22348-558">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

