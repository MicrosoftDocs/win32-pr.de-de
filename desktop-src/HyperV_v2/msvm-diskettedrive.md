---
description: Stellt ein Diskettenlaufwerk innerhalb des virtuellen Computers dar.
ms.assetid: 4624ABAF-3761-416F-9044-7A39EBF53D3D
title: Msvm_DisketteDrive-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DisketteDrive
- Msvm_DisketteDrive.SetPowerState
- Msvm_DisketteDrive.EnableDevice
- Msvm_DisketteDrive.OnlineDevice
- Msvm_DisketteDrive.QuiesceDevice
- Msvm_DisketteDrive.SaveProperties
- Msvm_DisketteDrive.RestoreProperties
- Msvm_DisketteDrive.InstanceID
- Msvm_DisketteDrive.Caption
- Msvm_DisketteDrive.Description
- Msvm_DisketteDrive.ElementName
- Msvm_DisketteDrive.InstallDate
- Msvm_DisketteDrive.Name
- Msvm_DisketteDrive.OperationalStatus
- Msvm_DisketteDrive.StatusDescriptions
- Msvm_DisketteDrive.Status
- Msvm_DisketteDrive.HealthState
- Msvm_DisketteDrive.CommunicationStatus
- Msvm_DisketteDrive.DetailedStatus
- Msvm_DisketteDrive.OperatingStatus
- Msvm_DisketteDrive.PrimaryStatus
- Msvm_DisketteDrive.EnabledState
- Msvm_DisketteDrive.OtherEnabledState
- Msvm_DisketteDrive.RequestedState
- Msvm_DisketteDrive.EnabledDefault
- Msvm_DisketteDrive.TimeOfLastStateChange
- Msvm_DisketteDrive.AvailableRequestedStates
- Msvm_DisketteDrive.TransitioningToState
- Msvm_DisketteDrive.SystemCreationClassName
- Msvm_DisketteDrive.SystemName
- Msvm_DisketteDrive.CreationClassName
- Msvm_DisketteDrive.DeviceID
- Msvm_DisketteDrive.PowerManagementSupported
- Msvm_DisketteDrive.PowerManagementCapabilities
- Msvm_DisketteDrive.Availability
- Msvm_DisketteDrive.StatusInfo
- Msvm_DisketteDrive.LastErrorCode
- Msvm_DisketteDrive.ErrorDescription
- Msvm_DisketteDrive.ErrorCleared
- Msvm_DisketteDrive.OtherIdentifyingInfo
- Msvm_DisketteDrive.PowerOnHours
- Msvm_DisketteDrive.TotalPowerOnHours
- Msvm_DisketteDrive.IdentifyingDescriptions
- Msvm_DisketteDrive.AdditionalAvailability
- Msvm_DisketteDrive.MaxQuiesceTime
- Msvm_DisketteDrive.Capabilities
- Msvm_DisketteDrive.CapabilityDescriptions
- Msvm_DisketteDrive.ErrorMethodology
- Msvm_DisketteDrive.CompressionMethod
- Msvm_DisketteDrive.NumberOfMediaSupported
- Msvm_DisketteDrive.MaxMediaSize
- Msvm_DisketteDrive.DefaultBlockSize
- Msvm_DisketteDrive.MaxBlockSize
- Msvm_DisketteDrive.MinBlockSize
- Msvm_DisketteDrive.NeedsCleaning
- Msvm_DisketteDrive.MediaIsLocked
- Msvm_DisketteDrive.Security
- Msvm_DisketteDrive.LastCleaned
- Msvm_DisketteDrive.MaxAccessTime
- Msvm_DisketteDrive.UncompressedDataRate
- Msvm_DisketteDrive.LoadTime
- Msvm_DisketteDrive.UnloadTime
- Msvm_DisketteDrive.MountCount
- Msvm_DisketteDrive.TimeOfLastMount
- Msvm_DisketteDrive.TotalMountTime
- Msvm_DisketteDrive.UnitsDescription
- Msvm_DisketteDrive.MaxUnitsBeforeCleaning
- Msvm_DisketteDrive.UnitsUsed
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1dbc9e21626e2f5e8269fb3a398dd48a6ea442e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757656"
---
# <a name="msvm_diskettedrive-class"></a><span data-ttu-id="6b700-103">MSVM \_ diskettedrive-Klasse</span><span class="sxs-lookup"><span data-stu-id="6b700-103">Msvm\_DisketteDrive class</span></span>

<span data-ttu-id="6b700-104">Stellt ein Diskettenlaufwerk innerhalb des virtuellen Computers dar.</span><span class="sxs-lookup"><span data-stu-id="6b700-104">Represents a floppy drive inside the virtual machine.</span></span> <span data-ttu-id="6b700-105">Ein Diskettenlaufwerk kann mit einer Datei aufgefüllt werden, die Disketten Medien darstellt, oder das Laufwerk kann leer sein.</span><span class="sxs-lookup"><span data-stu-id="6b700-105">A floppy drive can be populated with a file representing floppy media or the drive can be empty.</span></span> <span data-ttu-id="6b700-106">Physische Medien werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6b700-106">Physical media is not supported.</span></span> <span data-ttu-id="6b700-107">Es ist genau ein Diskettenlaufwerk pro Disketten Controller vorhanden, und es kann nicht entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="6b700-107">There is exactly one floppy drive per floppy controller and it is not removable.</span></span>

<span data-ttu-id="6b700-108">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6b700-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b700-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b700-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DisketteDrive : CIM_DisketteDrive
{
  string   InstanceID;
  string   Caption = "Diskette Drive";
  string   Description = "Microsoft Virtual Diskette Drive";
  string   ElementName = "Diskette Drive";
  datetime InstallDate;
  string   Name = "Diskette Drive";
  uint16   OperationalStatus[] = { 2 };
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
  uint16   CreationClassName = "Msvm_DisketteDrive";
  string   DeviceID = "Microsoft:GUID\device-specific-data";
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
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  uint16   Capabilities[] = {3, 4, 7};
  string   CapabilityDescriptions[] = {"Random Access", "Supports Writing", "Supports Removable Media"};
  string   ErrorMethodology = { "None" };
  string   CompressionMethod = "Not Compressed";
  uint32   NumberOfMediaSupported = 1;
  uint64   MaxMediaSize = 1440;
  uint64   DefaultBlockSize = 512;
  uint64   MaxBlockSize = 512;
  uint64   MinBlockSize = 512;
  boolean  NeedsCleaning = False;
  boolean  MediaIsLocked = False;
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
  uint64   MaxUnitsBeforeCleaning = 18446744073709551615;
  uint64   UnitsUsed = 0;
};
```

## <a name="members"></a><span data-ttu-id="6b700-110">Member</span><span class="sxs-lookup"><span data-stu-id="6b700-110">Members</span></span>

<span data-ttu-id="6b700-111">Die **MSVM \_ diskettedrive** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6b700-111">The **Msvm\_DisketteDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="6b700-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="6b700-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="6b700-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6b700-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6b700-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="6b700-114">Methods</span></span>

<span data-ttu-id="6b700-115">Die **MSVM \_ diskettedrive** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="6b700-115">The **Msvm\_DisketteDrive** class has these methods.</span></span>



| <span data-ttu-id="6b700-116">Methode</span><span class="sxs-lookup"><span data-stu-id="6b700-116">Method</span></span>                                                              | <span data-ttu-id="6b700-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b700-117">Description</span></span>                              |
|:--------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="6b700-118">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="6b700-118">**EnableDevice**</span></span>                                                    | <span data-ttu-id="6b700-119">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6b700-119">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="6b700-120">**Lockmedia**</span><span class="sxs-lookup"><span data-stu-id="6b700-120">**LockMedia**</span></span>](msvm-diskettedrive-lockmedia.md)                   | <span data-ttu-id="6b700-121">Sperrt oder gibt die Medien frei.</span><span class="sxs-lookup"><span data-stu-id="6b700-121">Locks or releases the media.</span></span><br/>  |
| <span data-ttu-id="6b700-122">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="6b700-122">**OnlineDevice**</span></span>                                                    | <span data-ttu-id="6b700-123">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6b700-123">This method is not supported.</span></span><br/> |
| <span data-ttu-id="6b700-124">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="6b700-124">**QuiesceDevice**</span></span>                                                   | <span data-ttu-id="6b700-125">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6b700-125">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="6b700-126">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="6b700-126">**RequestStateChange**</span></span>](msvm-diskettedrive-requeststatechange.md) | <span data-ttu-id="6b700-127">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="6b700-127">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="6b700-128">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="6b700-128">**Reset**</span></span>](msvm-diskettedrive-reset.md)                           | <span data-ttu-id="6b700-129">Setzt das virtuelle Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="6b700-129">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="6b700-130">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="6b700-130">**RestoreProperties**</span></span>                                               | <span data-ttu-id="6b700-131">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6b700-131">This method is not supported.</span></span><br/> |
| <span data-ttu-id="6b700-132">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="6b700-132">**SaveProperties**</span></span>                                                  | <span data-ttu-id="6b700-133">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6b700-133">This method is not supported.</span></span><br/> |
| <span data-ttu-id="6b700-134">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="6b700-134">**SetPowerState**</span></span>                                                   | <span data-ttu-id="6b700-135">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6b700-135">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6b700-136">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6b700-136">Properties</span></span>

<span data-ttu-id="6b700-137">Die **MSVM \_ diskettedrive** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6b700-137">The **Msvm\_DisketteDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6b700-138">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="6b700-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-139">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="6b700-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6b700-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-141">Alle zusätzlichen Verfügbarkeit und der Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="6b700-141">Any additional availability and status of the device.</span></span> <span data-ttu-id="6b700-142">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="6b700-143">Wert</span><span class="sxs-lookup"><span data-stu-id="6b700-143">Value</span></span>                                                                        | <span data-ttu-id="6b700-144">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6b700-144">Meaning</span></span>                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="6b700-145"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="6b700-145"><dt>6</dt></span></span> </dl> | <span data-ttu-id="6b700-146">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="6b700-146">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6b700-147">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="6b700-147">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-148">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6b700-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-150">Die primäre Verfügbarkeit und den Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="6b700-150">The primary availability and status of the device.</span></span> <span data-ttu-id="6b700-151">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-151">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="6b700-152">Wert</span><span class="sxs-lookup"><span data-stu-id="6b700-152">Value</span></span>                                                                        | <span data-ttu-id="6b700-153">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6b700-153">Meaning</span></span>                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="6b700-154"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="6b700-154"><dt>6</dt></span></span> </dl> | <span data-ttu-id="6b700-155">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="6b700-155">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6b700-156">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="6b700-156">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-157">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="6b700-157">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6b700-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-159">Gibt die möglichen Werte für den *requestedstate* -Parameter der [**requestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) -Methode an, die zum Initiieren einer Zustandsänderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6b700-159">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="6b700-160">Bei den aufgelisteten Werten handelt es sich um eine Teilmenge der Werte, die in der **requestedstaatsupported** -Eigenschaft der zugeordneten Instanz von **CIM \_ enabledlogicalelementfunctions** enthalten sind, wobei die ausgewählten Werte eine Funktion des aktuellen Zustands des [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) -Objekts sind.</span><span class="sxs-lookup"><span data-stu-id="6b700-160">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="6b700-161">Diese Eigenschaft darf nicht **null** sein, wenn eine Implementierung den Satz möglicher Werte als Funktion des aktuellen Zustands ankündigen kann.</span><span class="sxs-lookup"><span data-stu-id="6b700-161">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="6b700-162">Diese Eigenschaft ist **null** , wenn eine Implementierung den Satz möglicher Werte nicht als Funktion des aktuellen Zustands bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="6b700-162">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="6b700-163">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-163">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-164">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="6b700-164">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-165">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="6b700-165">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6b700-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-167">Die Funktionen des Medien Zugriffs Geräts.</span><span class="sxs-lookup"><span data-stu-id="6b700-167">The capabilities of the media access device.</span></span> <span data-ttu-id="6b700-168">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt und auf die folgenden Werte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b700-168">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to the following values.</span></span>



| <span data-ttu-id="6b700-169">Wert</span><span class="sxs-lookup"><span data-stu-id="6b700-169">Value</span></span>                                                                                | <span data-ttu-id="6b700-170">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6b700-170">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6b700-171"><dt>{3, 4, 7}</dt></span><span class="sxs-lookup"><span data-stu-id="6b700-171"><dt>{3, 4, 7}</dt></span></span> </dl> |                                                                                                 |
| <dl> <span data-ttu-id="6b700-172"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="6b700-172"><dt>3</dt></span></span> </dl>         | <span data-ttu-id="6b700-173">Der entsprechende Eintrag in **capabilitybeschreibungen** ist "zufälliger Zugriff".</span><span class="sxs-lookup"><span data-stu-id="6b700-173">The corresponding entry in **CapabilityDescriptions** is "Random Access".</span></span><br/>            |
| <dl> <span data-ttu-id="6b700-174"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="6b700-174"><dt>4</dt></span></span> </dl>         | <span data-ttu-id="6b700-175">Der entsprechende Eintrag in **capabilitybeschreibungen** ist "unterstützt Schreibvorgänge".</span><span class="sxs-lookup"><span data-stu-id="6b700-175">The corresponding entry in **CapabilityDescriptions** is "Supports Writing".</span></span><br/>         |
| <dl> <span data-ttu-id="6b700-176"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="6b700-176"><dt>7</dt></span></span> </dl>         | <span data-ttu-id="6b700-177">Der entsprechende Eintrag in **capabilitybeschreibungen** ist "unterstützt Wechselmedien".</span><span class="sxs-lookup"><span data-stu-id="6b700-177">The corresponding entry in **CapabilityDescriptions** is "Supports Removable Media".</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6b700-178">**Capabilitybeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="6b700-178">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-179">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="6b700-179">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6b700-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-181">Ein Array von Freiform-Zeichen folgen, das ausführliche Erläuterungen für den Zugriff auf Gerätefunktionen bereitstellt, die im **Eigenschaften Array Funktionen** angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="6b700-181">An array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** property array.</span></span> <span data-ttu-id="6b700-182">Jeder Eintrag dieses Arrays bezieht sich auf den Eintrag im **Funktions Array, der sich** am selben Index befindet.</span><span class="sxs-lookup"><span data-stu-id="6b700-182">Each entry of this array is related to the entry in the **Capabilities** array, located at the same index.</span></span> <span data-ttu-id="6b700-183">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-183">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-184">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6b700-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-185">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b700-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-187">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="6b700-187">A short description of the object.</span></span> <span data-ttu-id="6b700-188">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-189">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="6b700-189">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-190">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6b700-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-192">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="6b700-192">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="6b700-193">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="6b700-193">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6b700-194">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-195">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="6b700-195">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-196">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b700-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-198">Eine Zeichenfolge, die den Algorithmus oder das Tool angibt, das zum Komprimieren der logischen Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6b700-198">A string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="6b700-199">Wenn das Komprimierungs Schema unbekannt oder nicht beschrieben ist, verwenden Sie "unknown".</span><span class="sxs-lookup"><span data-stu-id="6b700-199">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="6b700-200">Wenn die logische Datei komprimiert ist, das Komprimierungs Schema jedoch unbekannt oder nicht beschrieben ist, verwenden Sie "komprimiert".</span><span class="sxs-lookup"><span data-stu-id="6b700-200">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="6b700-201">Wenn die logische Datei nicht komprimiert ist, verwenden Sie "nicht komprimiert".</span><span class="sxs-lookup"><span data-stu-id="6b700-201">If the logical file is not compressed, use "Not Compressed".</span></span> <span data-ttu-id="6b700-202">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-202">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

<span data-ttu-id="6b700-203">"Nicht komprimiert"</span><span class="sxs-lookup"><span data-stu-id="6b700-203">"Not Compressed"</span></span>

<span data-ttu-id="6b700-204">Unbekannter</span><span class="sxs-lookup"><span data-stu-id="6b700-204">"Unknown"</span></span>

<span data-ttu-id="6b700-205">Komprimierte</span><span class="sxs-lookup"><span data-stu-id="6b700-205">"Compressed"</span></span>

<span data-ttu-id="6b700-206">"Nicht komprimiert"</span><span class="sxs-lookup"><span data-stu-id="6b700-206">"Not Compressed"</span></span>

</dd> <dt>

<span data-ttu-id="6b700-207">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="6b700-207">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-208">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6b700-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-210">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6b700-210">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="6b700-211">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-211">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-212">**Defaultblocksize**</span><span class="sxs-lookup"><span data-stu-id="6b700-212">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-213">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6b700-213">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-214">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-215">Die Standard Blockgröße (in Bytes) für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="6b700-215">The default block size, in bytes, for the device.</span></span> <span data-ttu-id="6b700-216">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-216">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-217">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6b700-217">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-218">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b700-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-219">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-220">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="6b700-220">A description of the object.</span></span> <span data-ttu-id="6b700-221">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-221">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-222">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="6b700-222">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-223">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6b700-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-225">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="6b700-225">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="6b700-226">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="6b700-226">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6b700-227">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-227">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-228">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="6b700-228">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-229">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b700-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-230">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-231">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und auf "Microsoft:*GUID* \\ *Device-Specific-Data*" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b700-231">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="6b700-232">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="6b700-232">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-233">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b700-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-234">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-235">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="6b700-235">A display name for the object.</span></span> <span data-ttu-id="6b700-236">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-236">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-237">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="6b700-237">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-238">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6b700-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-239">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-240">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="6b700-240">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="6b700-241">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) geerbt und ist immer auf 2 (aktiviert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b700-241">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-242">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="6b700-242">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-243">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b700-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-244">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-245">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="6b700-245">The enabled and disabled states of an element.</span></span> <span data-ttu-id="6b700-246">Sie kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben.</span><span class="sxs-lookup"><span data-stu-id="6b700-246">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="6b700-247">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 5 festgelegt (nicht zutreffend).</span><span class="sxs-lookup"><span data-stu-id="6b700-247">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-248">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="6b700-248">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-249">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="6b700-249">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-250">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-251">Gibt an, ob der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="6b700-251">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="6b700-252">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b700-252">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6b700-253">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="6b700-253">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-254">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b700-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-255">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-256">Eine Zeichenfolge, die weitere Informationen über den Fehler enthält, der in **LastErrorCode** aufgezeichnet wurde, sowie Informationen über alle Maßnahmen, die ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="6b700-256">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="6b700-257">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b700-257">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6b700-258">**Errormethodmethodologie**</span><span class="sxs-lookup"><span data-stu-id="6b700-258">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-259">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b700-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-260">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-261">Eine Zeichenfolge, die die von diesem Gerät unterstützten Fehler Erkennungs-und Korrektur Typen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="6b700-261">A string that describes the types of error detection and correction supported by this device.</span></span> <span data-ttu-id="6b700-262">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-262">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-263">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="6b700-263">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-264">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6b700-264">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-265">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-266">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="6b700-266">The current health of the element.</span></span> <span data-ttu-id="6b700-267">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="6b700-267">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="6b700-268">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="6b700-268">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="6b700-269">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 5 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b700-269">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="6b700-270">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="6b700-270">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-271">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="6b700-271">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6b700-272">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-273">Ein Array von Freiform-Zeichen folgen, die Erklärungen und Details hinter den Einträgen im Eigenschafts Array " **OtherIdentifyingInfo** " bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6b700-273">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="6b700-274">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b700-274">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6b700-275">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6b700-275">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-276">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="6b700-276">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-277">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-278">Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="6b700-278">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="6b700-279">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-279">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-280">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6b700-280">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-281">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b700-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-282">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b700-283">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="6b700-283">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="6b700-284">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="6b700-284">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="6b700-285">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-285">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-286">**Lastbereinigt**</span><span class="sxs-lookup"><span data-stu-id="6b700-286">**LastCleaned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-287">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="6b700-287">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-288">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-289">Das Datum und die Uhrzeit der letzten Bereinigung des Geräts.</span><span class="sxs-lookup"><span data-stu-id="6b700-289">The date and time on which the device was last cleaned.</span></span> <span data-ttu-id="6b700-290">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-290">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-291">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="6b700-291">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-292">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6b700-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-293">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-294">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="6b700-294">The last error code reported by the logical device.</span></span> <span data-ttu-id="6b700-295">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b700-295">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6b700-296">**Loadtime**</span><span class="sxs-lookup"><span data-stu-id="6b700-296">**LoadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-297">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6b700-297">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-298">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-299">Die Zeit (in Millisekunden) von der Auslastung bis zum Lesen oder Schreiben eines Mediums.</span><span class="sxs-lookup"><span data-stu-id="6b700-299">The time, in milliseconds, from load to being able to read or write a media.</span></span> <span data-ttu-id="6b700-300">Beispielsweise ist dies das Intervall für Laufwerke zwischen einem Datenträger, der nicht auf die Festplatte zeigt, dass er für Lese-/Schreibzugriff bereit ist (d. h., der Datenträger wird mit nominaler Geschwindigkeit).</span><span class="sxs-lookup"><span data-stu-id="6b700-300">For example, for disk drives, this is the interval between a disk not spinning to the disk reporting that it is ready for read/write (that is, the disk spinning at nominal speeds).</span></span> <span data-ttu-id="6b700-301">Bei Bandlaufwerken ist dies der Zeitpunkt, zu dem ein Medium eingefügt wird, um zu melden, dass es für eine Anwendung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="6b700-301">For tape drives, this is the time from a media being injected to reporting that it is ready for an application.</span></span> <span data-ttu-id="6b700-302">Dies befindet sich normalerweise im botbereich des Bands.</span><span class="sxs-lookup"><span data-stu-id="6b700-302">This is usually at the tape's BOT area.</span></span> <span data-ttu-id="6b700-303">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-303">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-304">**Maxaccesstime**</span><span class="sxs-lookup"><span data-stu-id="6b700-304">**MaxAccessTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-305">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6b700-305">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-306">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-307">Die Zeit (in Millisekunden), die von der ersten Position auf dem Medium an den Speicherort verschoben werden soll, der in Bezug auf die Zeit am weitesten ist.</span><span class="sxs-lookup"><span data-stu-id="6b700-307">The time, in milliseconds, to move from the first location on the media to the location that is furthest with respect to time.</span></span> <span data-ttu-id="6b700-308">Bei einem Laufwerk stellt dies eine vollständige Suche und eine vollständige Rotationsverzögerung dar.</span><span class="sxs-lookup"><span data-stu-id="6b700-308">For a disk drive, this represents full seek + full rotational delay.</span></span> <span data-ttu-id="6b700-309">Bei Bandlaufwerken stellt dies eine Suche zwischen dem Anfang des Bands und dem physisch entfernten Punkt dar.</span><span class="sxs-lookup"><span data-stu-id="6b700-309">For tape drives, this represents a search from the beginning of the tape to the most physically distant point.</span></span> <span data-ttu-id="6b700-310">(Das Ende eines Bands kann sich am physisch entfernten Punkt befinden, dies ist jedoch nicht unbedingt der Fall.) Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-310">(The end of a tape may be at its most physically distant point, but this is not necessarily true.) This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-311">**Maxblocksize**</span><span class="sxs-lookup"><span data-stu-id="6b700-311">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-312">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6b700-312">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-313">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-314">Die maximale Blockgröße (in Bytes) für Medien, auf die das Gerät zugreift.</span><span class="sxs-lookup"><span data-stu-id="6b700-314">The maximum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="6b700-315">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-315">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-316">**Maxmediasize**</span><span class="sxs-lookup"><span data-stu-id="6b700-316">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-317">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6b700-317">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-318">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-319">Die maximale Größe des von diesem Gerät unterstützten Mediums in Kilobyte.</span><span class="sxs-lookup"><span data-stu-id="6b700-319">The maximum size, in kilobytes, of media supported by this device.</span></span> <span data-ttu-id="6b700-320">Kilobytes werden als Anzahl von Bytes, multipliziert mit 1000, interpretiert (nicht die Anzahl der Bytes multipliziert mit 1024).</span><span class="sxs-lookup"><span data-stu-id="6b700-320">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span> <span data-ttu-id="6b700-321">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-321">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-322">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="6b700-322">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-323">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6b700-323">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-324">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-325">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="6b700-325">This property has been deprecated.</span></span> <span data-ttu-id="6b700-326">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b700-326">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6b700-327">**Maxunitionbeforecforec**</span><span class="sxs-lookup"><span data-stu-id="6b700-327">**MaxUnitsBeforeCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-328">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6b700-328">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-329">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-330">Die maximalen Einheiten, die verwendet werden können, bevor das Gerät bereinigt wird.</span><span class="sxs-lookup"><span data-stu-id="6b700-330">The maximum units that can be used before the device should be cleaned.</span></span> <span data-ttu-id="6b700-331">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-331">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-332">**Mediaislocked**</span><span class="sxs-lookup"><span data-stu-id="6b700-332">**MediaIsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-333">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="6b700-333">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-334">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-335">**True** , wenn die Medien im Gerät gesperrt sind und nicht aussteht. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="6b700-335">**True** if the media is locked in the device and cannot be ejected; otherwise, **False**.</span></span> <span data-ttu-id="6b700-336">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-336">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-337">**Minblocksize**</span><span class="sxs-lookup"><span data-stu-id="6b700-337">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-338">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6b700-338">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-339">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-340">Die minimale Blockgröße (in Bytes) für Medien, auf die das Gerät zugreift.</span><span class="sxs-lookup"><span data-stu-id="6b700-340">The minimum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="6b700-341">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-341">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-342">**Mountcount**</span><span class="sxs-lookup"><span data-stu-id="6b700-342">**MountCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-343">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6b700-343">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-344">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-345">Bei Geräten, die Wechselmedien unterstützen, gibt es die Häufigkeit, mit der Medien für die Datenübertragung bereitgestellt oder das Gerät bereinigt werden.</span><span class="sxs-lookup"><span data-stu-id="6b700-345">For a device that supports removable media, the number of times that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="6b700-346">Bei Geräten, die auf nicht Wechselmedien (z. b. Festplatten) zugreifen, ist diese Eigenschaft nicht anwendbar und sollte auf 0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6b700-346">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="6b700-347">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-347">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-348">**Name**</span><span class="sxs-lookup"><span data-stu-id="6b700-348">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-349">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b700-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-350">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-351">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="6b700-351">The label by which the object is known.</span></span> <span data-ttu-id="6b700-352">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und entspricht der Element **Name** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6b700-352">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="6b700-353">**Unnötig**</span><span class="sxs-lookup"><span data-stu-id="6b700-353">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-354">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="6b700-354">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-355">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-356">**True** , wenn das Medien Zugriffsgerät bereinigt werden muss. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="6b700-356">**True** if the media access device needs cleaning; otherwise, **False**.</span></span> <span data-ttu-id="6b700-357">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-357">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-358">**"Numofmediasupportiert"**</span><span class="sxs-lookup"><span data-stu-id="6b700-358">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-359">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6b700-359">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-360">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-361">Die maximale Anzahl von mehreren einzelnen Medien, die unterstützt oder eingefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="6b700-361">The maximum number of multiple individual media that can be supported or inserted.</span></span> <span data-ttu-id="6b700-362">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-362">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-363">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="6b700-363">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-364">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6b700-364">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-365">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-366">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6b700-366">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="6b700-367">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="6b700-367">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6b700-368">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-368">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-369">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="6b700-369">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-370">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="6b700-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6b700-371">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-372">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="6b700-372">The current statuses of the object.</span></span> <span data-ttu-id="6b700-373">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf 2 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b700-373">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-374">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="6b700-374">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-375">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b700-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-376">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-377">Der aktivierte oder deaktivierte Status des Elements, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6b700-377">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="6b700-378">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="6b700-378">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="6b700-379">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b700-379">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6b700-380">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="6b700-380">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-381">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="6b700-381">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6b700-382">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-383">Alle zusätzlichen Daten über Geräte-ID-Informationen, die zur Identifizierung eines logischen Geräts verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="6b700-383">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="6b700-384">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b700-384">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6b700-385">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="6b700-385">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-386">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="6b700-386">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6b700-387">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-388">Die Energie Verwaltungsfunktionen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="6b700-388">The power management capabilities of the device.</span></span> <span data-ttu-id="6b700-389">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b700-389">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6b700-390">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="6b700-390">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-391">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="6b700-391">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-392">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-393">Gibt an, ob das Gerät Energie gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="6b700-393">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="6b700-394">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b700-394">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6b700-395">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="6b700-395">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-396">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6b700-396">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-397">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-398">Gibt an, wie viele aufeinanderfolgende Stunden dieses Gerät seit dem letzten Strom Umgebung eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="6b700-398">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="6b700-399">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b700-399">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6b700-400">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="6b700-400">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-401">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6b700-401">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-402">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-403">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="6b700-403">Provides high level status information.</span></span> <span data-ttu-id="6b700-404">Diese Eigenschaft sollte in Verbindung mit der **detailedstatus** -Eigenschaft verwendet werden, um allgemeine und ausführliche Integritäts Statusinformationen für das-Element und seine unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6b700-404">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="6b700-405">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="6b700-405">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6b700-406">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-406">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-407">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="6b700-407">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-408">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6b700-408">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-409">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-410">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="6b700-410">The last requested or desired state for the element.</span></span> <span data-ttu-id="6b700-411">Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="6b700-411">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="6b700-412">Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuell aktivierten oder deaktivierten Zustände zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="6b700-412">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="6b700-413">**RequestStateChange** kann von einer bestimmten Instanz von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="6b700-413">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support **RequestStateChange**.</span></span> <span data-ttu-id="6b700-414">Wenn dies auftritt, wird der Wert 12 (nicht zutreffend) verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b700-414">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="6b700-415">Diese Eigenschaft wird von **CIM \_ enabledlogicalelement** geerbt und ist immer auf 12 (nicht zutreffend) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b700-415">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-416">**Security**</span><span class="sxs-lookup"><span data-stu-id="6b700-416">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-417">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6b700-417">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-418">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-419">Die für das Gerät definierte Betriebssicherheit.</span><span class="sxs-lookup"><span data-stu-id="6b700-419">The operational security defined for the device.</span></span> <span data-ttu-id="6b700-420">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-420">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>



| <span data-ttu-id="6b700-421">Wert</span><span class="sxs-lookup"><span data-stu-id="6b700-421">Value</span></span>                                                                        | <span data-ttu-id="6b700-422">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6b700-422">Meaning</span></span>         |
|------------------------------------------------------------------------------|-----------------|
| <dl> <span data-ttu-id="6b700-423"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="6b700-423"><dt>3</dt></span></span> </dl> | <span data-ttu-id="6b700-424">Keine</span><span class="sxs-lookup"><span data-stu-id="6b700-424">None</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6b700-425">**Status**</span><span class="sxs-lookup"><span data-stu-id="6b700-425">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-426">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b700-426">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-427">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-427">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-428">Der aktuelle Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="6b700-428">The current status of the object.</span></span> <span data-ttu-id="6b700-429">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b700-429">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6b700-430">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="6b700-430">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-431">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="6b700-431">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6b700-432">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-433">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="6b700-433">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="6b700-434">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf "OK" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b700-434">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="6b700-435">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="6b700-435">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-436">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6b700-436">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-437">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-438">Der aktuelle Zustand des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="6b700-438">The current state of the logical device.</span></span> <span data-ttu-id="6b700-439">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b700-439">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6b700-440">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="6b700-440">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-441">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b700-441">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-442">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-443">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="6b700-443">The scoping system's creation class name.</span></span> <span data-ttu-id="6b700-444">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-444">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-445">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="6b700-445">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-446">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b700-446">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-447">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-448">Der eindeutige Bezeichner für die Bereichs bezogene virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="6b700-448">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="6b700-449">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-449">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-450">**Timeoflastmount**</span><span class="sxs-lookup"><span data-stu-id="6b700-450">**TimeOfLastMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-451">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="6b700-451">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-452">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-452">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-453">Für ein Gerät, das Wechselmedien unterstützt, das Datum und die Uhrzeit der letzten Bereitstellung des Mediums auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="6b700-453">For a device that supports removable media, the most recent date and time that media was mounted on the device.</span></span> <span data-ttu-id="6b700-454">Bei Geräten, die auf nicht Wechselmedien wie Festplatten zugreifen, hat diese Eigenschaft keine Bedeutung und ist nicht anwendbar.</span><span class="sxs-lookup"><span data-stu-id="6b700-454">For devices accessing nonremovable media, such as hard disks, this property has no meaning and is not applicable.</span></span> <span data-ttu-id="6b700-455">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-455">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-456">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="6b700-456">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-457">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="6b700-457">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-458">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-458">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-459">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="6b700-459">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="6b700-460">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b700-460">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6b700-461">**Totalmounttime**</span><span class="sxs-lookup"><span data-stu-id="6b700-461">**TotalMountTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-462">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6b700-462">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-463">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-463">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-464">Für ein Gerät, das Wechselmedien unterstützt, die Gesamtzeit (in Sekunden), die Medien für die Datenübertragung bereitgestellt wurden, oder um das Gerät zu bereinigen.</span><span class="sxs-lookup"><span data-stu-id="6b700-464">For a device that supports removable media, the total time (in seconds) that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="6b700-465">Bei Geräten, die auf nicht Wechselmedien (z. b. Festplatten) zugreifen, ist diese Eigenschaft nicht anwendbar und sollte auf 0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6b700-465">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="6b700-466">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-466">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-467">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="6b700-467">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-468">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6b700-468">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-469">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-470">Die Gesamtanzahl der Stunden, für die dieses Gerät eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="6b700-470">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="6b700-471">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b700-471">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6b700-472">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="6b700-472">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-473">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6b700-473">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-474">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-474">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-475">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="6b700-475">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="6b700-476">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b700-476">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6b700-477">**Uncompresseddatarate**</span><span class="sxs-lookup"><span data-stu-id="6b700-477">**UncompressedDataRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-478">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6b700-478">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-479">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-479">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-480">Die dauerhafte Datenübertragungsrate in KB/Sek., die das Gerät lesen und in ein Medium schreiben kann.</span><span class="sxs-lookup"><span data-stu-id="6b700-480">The sustained data transfer rate, in KB/sec, that the device can read from and write to a media.</span></span> <span data-ttu-id="6b700-481">Dies ist eine dauerhafte, Rohdaten Rate.</span><span class="sxs-lookup"><span data-stu-id="6b700-481">This is a sustained, raw data rate.</span></span> <span data-ttu-id="6b700-482">Die maximale Anzahl von Raten oder raten, bei denen die Komprimierung nicht in dieser Eigenschaft gemeldet werden sollte</span><span class="sxs-lookup"><span data-stu-id="6b700-482">Maximum rates or rates assuming compression should not be reported in this property.</span></span> <span data-ttu-id="6b700-483">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-483">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-484">**Unitydescription**</span><span class="sxs-lookup"><span data-stu-id="6b700-484">**UnitsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-485">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b700-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-486">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-487">Die Einheiten in Relation zur Verwendung in **maxunitionbeforecforec.**</span><span class="sxs-lookup"><span data-stu-id="6b700-487">The units relative to its use in **MaxUnitsBeforeCleaning**.</span></span> <span data-ttu-id="6b700-488">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt und ist auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b700-488">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6b700-489">**Unitsused**</span><span class="sxs-lookup"><span data-stu-id="6b700-489">**UnitsUsed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-490">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6b700-490">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-491">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-491">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-492">Die aktuelle Anzahl der verwendeten Einheiten.</span><span class="sxs-lookup"><span data-stu-id="6b700-492">The current number of units used.</span></span> <span data-ttu-id="6b700-493">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-493">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6b700-494">**Unloadtime**</span><span class="sxs-lookup"><span data-stu-id="6b700-494">**UnloadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b700-495">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6b700-495">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6b700-496">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b700-496">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b700-497">Die Zeit (in Millisekunden), die in der Lage ist, ein Medium in seinen "Entladevorgang" zu lesen oder zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="6b700-497">The time, in milliseconds, from being able to read or write a media to its 'unload'.</span></span> <span data-ttu-id="6b700-498">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6b700-498">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b700-499">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b700-499">Remarks</span></span>

<span data-ttu-id="6b700-500">Der Zugriff auf die **MSVM \_ diskettedrive** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="6b700-500">Access to the **Msvm\_DisketteDrive** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="6b700-501">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="6b700-501">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="6b700-502">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b700-502">Requirements</span></span>



| <span data-ttu-id="6b700-503">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b700-503">Requirement</span></span> | <span data-ttu-id="6b700-504">Wert</span><span class="sxs-lookup"><span data-stu-id="6b700-504">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b700-505">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b700-505">Minimum supported client</span></span><br/> | <span data-ttu-id="6b700-506">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b700-506">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6b700-507">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b700-507">Minimum supported server</span></span><br/> | <span data-ttu-id="6b700-508">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b700-508">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6b700-509">Namespace</span><span class="sxs-lookup"><span data-stu-id="6b700-509">Namespace</span></span><br/>                | <span data-ttu-id="6b700-510">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="6b700-510">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6b700-511">MOF</span><span class="sxs-lookup"><span data-stu-id="6b700-511">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b700-512"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6b700-512"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b700-513">DLL</span><span class="sxs-lookup"><span data-stu-id="6b700-513">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b700-514"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6b700-514"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6b700-515">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b700-515">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b700-516">**CIM- \_ Diskettelaufwerk**</span><span class="sxs-lookup"><span data-stu-id="6b700-516">**CIM\_DisketteDrive**</span></span>](cim-diskettedrive.md)
</dt> <dt>

[<span data-ttu-id="6b700-517">**CIM- \_ Diskettelaufwerk**</span><span class="sxs-lookup"><span data-stu-id="6b700-517">**CIM\_DisketteDrive**</span></span>](/windows/desktop/CIMWin32Prov/cim-diskettedrive)
</dt> <dt>

[<span data-ttu-id="6b700-518">Speicher Klassen</span><span class="sxs-lookup"><span data-stu-id="6b700-518">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

