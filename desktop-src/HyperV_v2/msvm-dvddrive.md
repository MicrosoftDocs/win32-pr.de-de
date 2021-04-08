---
description: Stellt ein DVD-Laufwerk innerhalb eines virtuellen Computers dar.
ms.assetid: BA813950-436F-46F1-8C1F-79C5AB1A459B
title: Msvm_DVDDrive-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DVDDrive
- Msvm_DVDDrive.SetPowerState
- Msvm_DVDDrive.EnableDevice
- Msvm_DVDDrive.OnlineDevice
- Msvm_DVDDrive.QuiesceDevice
- Msvm_DVDDrive.SaveProperties
- Msvm_DVDDrive.RestoreProperties
- Msvm_DVDDrive.InstanceID
- Msvm_DVDDrive.Caption
- Msvm_DVDDrive.Description
- Msvm_DVDDrive.ElementName
- Msvm_DVDDrive.InstallDate
- Msvm_DVDDrive.Name
- Msvm_DVDDrive.OperationalStatus
- Msvm_DVDDrive.StatusDescriptions
- Msvm_DVDDrive.Status
- Msvm_DVDDrive.HealthState
- Msvm_DVDDrive.CommunicationStatus
- Msvm_DVDDrive.DetailedStatus
- Msvm_DVDDrive.OperatingStatus
- Msvm_DVDDrive.PrimaryStatus
- Msvm_DVDDrive.EnabledState
- Msvm_DVDDrive.OtherEnabledState
- Msvm_DVDDrive.RequestedState
- Msvm_DVDDrive.EnabledDefault
- Msvm_DVDDrive.TimeOfLastStateChange
- Msvm_DVDDrive.AvailableRequestedStates
- Msvm_DVDDrive.TransitioningToState
- Msvm_DVDDrive.SystemCreationClassName
- Msvm_DVDDrive.SystemName
- Msvm_DVDDrive.CreationClassName
- Msvm_DVDDrive.DeviceID
- Msvm_DVDDrive.PowerManagementSupported
- Msvm_DVDDrive.PowerManagementCapabilities
- Msvm_DVDDrive.Availability
- Msvm_DVDDrive.StatusInfo
- Msvm_DVDDrive.LastErrorCode
- Msvm_DVDDrive.ErrorDescription
- Msvm_DVDDrive.ErrorCleared
- Msvm_DVDDrive.OtherIdentifyingInfo
- Msvm_DVDDrive.PowerOnHours
- Msvm_DVDDrive.TotalPowerOnHours
- Msvm_DVDDrive.IdentifyingDescriptions
- Msvm_DVDDrive.AdditionalAvailability
- Msvm_DVDDrive.MaxQuiesceTime
- Msvm_DVDDrive.Capabilities
- Msvm_DVDDrive.CapabilityDescriptions
- Msvm_DVDDrive.ErrorMethodology
- Msvm_DVDDrive.CompressionMethod
- Msvm_DVDDrive.NumberOfMediaSupported
- Msvm_DVDDrive.MaxMediaSize
- Msvm_DVDDrive.DefaultBlockSize
- Msvm_DVDDrive.MaxBlockSize
- Msvm_DVDDrive.MinBlockSize
- Msvm_DVDDrive.NeedsCleaning
- Msvm_DVDDrive.MediaIsLocked
- Msvm_DVDDrive.Security
- Msvm_DVDDrive.LastCleaned
- Msvm_DVDDrive.MaxAccessTime
- Msvm_DVDDrive.UncompressedDataRate
- Msvm_DVDDrive.LoadTime
- Msvm_DVDDrive.UnloadTime
- Msvm_DVDDrive.MountCount
- Msvm_DVDDrive.TimeOfLastMount
- Msvm_DVDDrive.TotalMountTime
- Msvm_DVDDrive.UnitsDescription
- Msvm_DVDDrive.MaxUnitsBeforeCleaning
- Msvm_DVDDrive.UnitsUsed
- Msvm_DVDDrive.FormatsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e4b3c9006babb2c7e18b6aed6e85cbee47299429
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867955"
---
# <a name="msvm_dvddrive-class"></a><span data-ttu-id="277b0-103">MSVM \_ dvddrive-Klasse</span><span class="sxs-lookup"><span data-stu-id="277b0-103">Msvm\_DVDDrive class</span></span>

<span data-ttu-id="277b0-104">Stellt ein DVD-Laufwerk innerhalb eines virtuellen Computers dar.</span><span class="sxs-lookup"><span data-stu-id="277b0-104">Represents a DVD drive inside of a virtual machine.</span></span> <span data-ttu-id="277b0-105">Bei diesem DVD-Laufwerk kann es sich entweder um ein Pass-Through-Gerät (wenn eine physische Festplatte an den virtuellen Computer angefügt wurde) oder um synthetische und mit ISO-Datei Medien gefüllte Medien handeln.</span><span class="sxs-lookup"><span data-stu-id="277b0-105">This DVD drive can either be a pass-through device (if a physical hard disk was attached to the virtual machine) or synthetic and populated with ISO file media.</span></span> <span data-ttu-id="277b0-106">Da virtuelle und physische DVD-Laufwerke dem virtuellen Computer hinzugefügt und daraus entfernt werden können, gibt es zwei Ressourcenpools, die dieser Klasse zugeordnet sind, eine für Pass-Through-DVD-Laufwerke und die andere für virtuelle DVD-Laufwerke.</span><span class="sxs-lookup"><span data-stu-id="277b0-106">Because virtual and physical DVD drives can be added and removed from the virtual machine, there are two resource pools associated with this class, one for pass-through DVD drives, and the other for virtual DVD drives.</span></span> <span data-ttu-id="277b0-107">DVD-Laufwerke können nur dann hinzugefügt oder entfernt werden, wenn der virtuelle Computer offline ist.</span><span class="sxs-lookup"><span data-stu-id="277b0-107">DVD drives can only be added or removed if the virtual machine is offline.</span></span>

<span data-ttu-id="277b0-108">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="277b0-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="277b0-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="277b0-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DVDDrive : CIM_DVDDrive
{
  string   InstanceID;
  string   Caption = "DVD Drive";
  string   Description = "Microsoft Virtual DVD Drive";
  string   ElementName = "DVD Drive";
  datetime InstallDate;
  string   Name = "DVD Drive";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_DVDDrive";
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
  uint32   Capabilities[] = {3, 7};
  string   CapabilityDescriptions[] = {"Random Access", "Supports Removable Media"};
  string   ErrorMethodology = "None";
  string   CompressionMethod = "Not Compressed";
  uint32   NumberOfMediaSupported = 1;
  uint64   MaxMediaSize = 9400000;
  uint64   DefaultBlockSize = 2048;
  uint64   MaxBlockSize = 2048;
  uint64   MinBlockSize = 2048;
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
  uint64   MaxUnitsBeforeCleaning = 0xffffffffffffffff;
  uint64   UnitsUsed = 0;
  uint16   FormatsSupported[] = {16, 22};
};
```

## <a name="members"></a><span data-ttu-id="277b0-110">Member</span><span class="sxs-lookup"><span data-stu-id="277b0-110">Members</span></span>

<span data-ttu-id="277b0-111">Die **MSVM- \_ dvddrive** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="277b0-111">The **Msvm\_DVDDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="277b0-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="277b0-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="277b0-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="277b0-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="277b0-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="277b0-114">Methods</span></span>

<span data-ttu-id="277b0-115">Die **MSVM- \_ dvddrive** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="277b0-115">The **Msvm\_DVDDrive** class has these methods.</span></span>



| <span data-ttu-id="277b0-116">Methode</span><span class="sxs-lookup"><span data-stu-id="277b0-116">Method</span></span>                                                         | <span data-ttu-id="277b0-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="277b0-117">Description</span></span>                              |
|:---------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="277b0-118">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="277b0-118">**EnableDevice**</span></span>                                               | <span data-ttu-id="277b0-119">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="277b0-119">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="277b0-120">**Lockmedia**</span><span class="sxs-lookup"><span data-stu-id="277b0-120">**LockMedia**</span></span>](msvm-dvddrive-lockmedia.md)                   | <span data-ttu-id="277b0-121">Sperrt oder gibt die Medien frei.</span><span class="sxs-lookup"><span data-stu-id="277b0-121">Locks or releases the media.</span></span><br/>  |
| <span data-ttu-id="277b0-122">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="277b0-122">**OnlineDevice**</span></span>                                               | <span data-ttu-id="277b0-123">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="277b0-123">This method is not supported.</span></span><br/> |
| <span data-ttu-id="277b0-124">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="277b0-124">**QuiesceDevice**</span></span>                                              | <span data-ttu-id="277b0-125">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="277b0-125">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="277b0-126">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="277b0-126">**RequestStateChange**</span></span>](msvm-dvddrive-requeststatechange.md) | <span data-ttu-id="277b0-127">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="277b0-127">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="277b0-128">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="277b0-128">**Reset**</span></span>](msvm-dvddrive-reset.md)                           | <span data-ttu-id="277b0-129">Setzt das virtuelle Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="277b0-129">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="277b0-130">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="277b0-130">**RestoreProperties**</span></span>                                          | <span data-ttu-id="277b0-131">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="277b0-131">This method is not supported.</span></span><br/> |
| <span data-ttu-id="277b0-132">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="277b0-132">**SaveProperties**</span></span>                                             | <span data-ttu-id="277b0-133">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="277b0-133">This method is not supported.</span></span><br/> |
| <span data-ttu-id="277b0-134">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="277b0-134">**SetPowerState**</span></span>                                              | <span data-ttu-id="277b0-135">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="277b0-135">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="277b0-136">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="277b0-136">Properties</span></span>

<span data-ttu-id="277b0-137">Die **MSVM- \_ dvddrive** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="277b0-137">The **Msvm\_DVDDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="277b0-138">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="277b0-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-139">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="277b0-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="277b0-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-141">Alle zusätzlichen Verfügbarkeit und der Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="277b0-141">Any additional availability and status of the device.</span></span> <span data-ttu-id="277b0-142">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist auf 6 festgelegt (nicht zutreffend).</span><span class="sxs-lookup"><span data-stu-id="277b0-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-143">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="277b0-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-144">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="277b0-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-146">Die primäre Verfügbarkeit und den Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="277b0-146">The primary availability and status of the device.</span></span> <span data-ttu-id="277b0-147">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist auf 6 festgelegt (nicht zutreffend).</span><span class="sxs-lookup"><span data-stu-id="277b0-147">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-148">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="277b0-148">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-149">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="277b0-149">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="277b0-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-151">Gibt die möglichen Werte für den *requestedstate* -Parameter der [**requestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) -Methode an, die zum Initiieren einer Zustandsänderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="277b0-151">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="277b0-152">Bei den aufgelisteten Werten handelt es sich um eine Teilmenge der Werte, die in der **requestedstaatsupported** -Eigenschaft der zugeordneten Instanz von **CIM \_ enabledlogicalelementfunctions** enthalten sind, wobei die ausgewählten Werte eine Funktion des aktuellen Zustands des [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) -Objekts sind.</span><span class="sxs-lookup"><span data-stu-id="277b0-152">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="277b0-153">Diese Eigenschaft darf nicht **null** sein, wenn eine Implementierung den Satz möglicher Werte als Funktion des aktuellen Zustands ankündigen kann.</span><span class="sxs-lookup"><span data-stu-id="277b0-153">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="277b0-154">Diese Eigenschaft ist **null** , wenn eine Implementierung den Satz möglicher Werte nicht als Funktion des aktuellen Zustands bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="277b0-154">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="277b0-155">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-155">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-156">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="277b0-156">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-157">Datentyp: **UInt32** Array</span><span class="sxs-lookup"><span data-stu-id="277b0-157">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="277b0-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-159">Die Funktionen des Medien Zugriffs Geräts.</span><span class="sxs-lookup"><span data-stu-id="277b0-159">The capabilities of the media access device.</span></span> <span data-ttu-id="277b0-160">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt und auf die folgenden Werte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="277b0-160">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to the following values.</span></span>



| <span data-ttu-id="277b0-161">Wert</span><span class="sxs-lookup"><span data-stu-id="277b0-161">Value</span></span>                                                                             | <span data-ttu-id="277b0-162">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="277b0-162">Meaning</span></span>                                                                                         |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="277b0-163"><dt>{3, 7}</dt></span><span class="sxs-lookup"><span data-stu-id="277b0-163"><dt>{3, 7}</dt></span></span> </dl> |                                                                                                 |
| <dl> <span data-ttu-id="277b0-164"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="277b0-164"><dt>3</dt></span></span> </dl>      | <span data-ttu-id="277b0-165">Der entsprechende Eintrag in **capabilitybeschreibungen** ist "zufälliger Zugriff".</span><span class="sxs-lookup"><span data-stu-id="277b0-165">The corresponding entry in **CapabilityDescriptions** is "Random Access".</span></span><br/>            |
| <dl> <span data-ttu-id="277b0-166"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="277b0-166"><dt>7</dt></span></span> </dl>      | <span data-ttu-id="277b0-167">Der entsprechende Eintrag in **capabilitybeschreibungen** ist "unterstützt Wechselmedien".</span><span class="sxs-lookup"><span data-stu-id="277b0-167">The corresponding entry in **CapabilityDescriptions** is "Supports Removable Media".</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="277b0-168">**Capabilitybeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="277b0-168">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-169">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="277b0-169">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="277b0-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-171">Ein Array von Freiform-Zeichen folgen, das ausführliche Erläuterungen für den Zugriff auf Gerätefunktionen bereitstellt, die im **Eigenschaften Array Funktionen** angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="277b0-171">An array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** property array.</span></span> <span data-ttu-id="277b0-172">Jeder Eintrag dieses Arrays bezieht sich auf den Eintrag im Eigenschafts Array " **Funktionen** ", der sich am selben Index befindet.</span><span class="sxs-lookup"><span data-stu-id="277b0-172">Each entry of this array is related to the entry in the **Capabilities** property array, located at the same index.</span></span> <span data-ttu-id="277b0-173">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-173">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-174">**Caption**</span><span class="sxs-lookup"><span data-stu-id="277b0-174">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-175">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="277b0-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-177">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="277b0-177">A short description of the object.</span></span> <span data-ttu-id="277b0-178">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-178">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-179">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="277b0-179">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-180">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="277b0-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-182">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="277b0-182">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="277b0-183">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="277b0-183">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="277b0-184">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-184">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-185">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="277b0-185">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-186">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="277b0-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-188">Eine Zeichenfolge, die den Algorithmus oder das Tool angibt, das zum Komprimieren der logischen Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="277b0-188">A string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="277b0-189">Wenn das Komprimierungs Schema unbekannt oder nicht beschrieben ist, verwenden Sie "unknown".</span><span class="sxs-lookup"><span data-stu-id="277b0-189">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="277b0-190">Wenn die logische Datei komprimiert ist, das Komprimierungs Schema jedoch unbekannt oder nicht beschrieben ist, verwenden Sie "komprimiert".</span><span class="sxs-lookup"><span data-stu-id="277b0-190">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="277b0-191">Wenn die logische Datei nicht komprimiert ist, verwenden Sie "nicht komprimiert".</span><span class="sxs-lookup"><span data-stu-id="277b0-191">If the logical file is not compressed, use "Not Compressed".</span></span> <span data-ttu-id="277b0-192">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-192">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

<span data-ttu-id="277b0-193">"Nicht komprimiert"</span><span class="sxs-lookup"><span data-stu-id="277b0-193">"Not Compressed"</span></span>

<span data-ttu-id="277b0-194">Unbekannter</span><span class="sxs-lookup"><span data-stu-id="277b0-194">"Unknown"</span></span>

<span data-ttu-id="277b0-195">Komprimierte</span><span class="sxs-lookup"><span data-stu-id="277b0-195">"Compressed"</span></span>

<span data-ttu-id="277b0-196">"Nicht komprimiert"</span><span class="sxs-lookup"><span data-stu-id="277b0-196">"Not Compressed"</span></span>

</dd> <dt>

<span data-ttu-id="277b0-197">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="277b0-197">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-198">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="277b0-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-200">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="277b0-200">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="277b0-201">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-202">**Defaultblocksize**</span><span class="sxs-lookup"><span data-stu-id="277b0-202">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-203">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="277b0-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-205">Die Standard Blockgröße (in Bytes) für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="277b0-205">The default block size, in bytes, for the device.</span></span> <span data-ttu-id="277b0-206">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-206">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-207">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="277b0-207">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-208">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="277b0-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-210">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="277b0-210">A description of the object.</span></span> <span data-ttu-id="277b0-211">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-211">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-212">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="277b0-212">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-213">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="277b0-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-214">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-215">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="277b0-215">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="277b0-216">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="277b0-216">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="277b0-217">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-218">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="277b0-218">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-219">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="277b0-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-220">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-221">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und auf "Microsoft:*GUID* \\ *Device-Specific-Data*" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="277b0-221">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="277b0-222">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="277b0-222">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-223">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="277b0-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-225">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="277b0-225">A display name for the object.</span></span> <span data-ttu-id="277b0-226">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-226">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-227">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="277b0-227">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-228">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="277b0-228">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-229">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-230">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="277b0-230">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="277b0-231">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-231">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-232">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="277b0-232">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-233">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="277b0-233">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-234">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-235">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="277b0-235">The enabled and disabled states of an element.</span></span> <span data-ttu-id="277b0-236">Sie kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben.</span><span class="sxs-lookup"><span data-stu-id="277b0-236">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="277b0-237">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-237">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-238">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="277b0-238">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-239">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="277b0-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-240">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-241">Gibt an, ob der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="277b0-241">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="277b0-242">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="277b0-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="277b0-243">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="277b0-243">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-244">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="277b0-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-245">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-246">Eine Zeichenfolge, die weitere Informationen über den Fehler enthält, der in **LastErrorCode** aufgezeichnet wurde, sowie Informationen über alle Maßnahmen, die ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="277b0-246">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="277b0-247">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="277b0-247">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="277b0-248">**Errormethodmethodologie**</span><span class="sxs-lookup"><span data-stu-id="277b0-248">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-249">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="277b0-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-250">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-251">Eine Zeichenfolge, die die von diesem Gerät unterstützten Fehler Erkennungs-und Korrektur Typen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="277b0-251">A string that describes the types of error detection and correction supported by this device.</span></span> <span data-ttu-id="277b0-252">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-252">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-253">**Formatssupported**</span><span class="sxs-lookup"><span data-stu-id="277b0-253">**FormatsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-254">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="277b0-254">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="277b0-255">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-256">Die CD-und DVD-Formate, die von diesem Gerät unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="277b0-256">The CD and DVD formats that are supported by this device.</span></span> <span data-ttu-id="277b0-257">Diese Eigenschaft wird von [**CIM \_ dvddrive**](/previous-versions//cc136812(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-257">This property is inherited from [**CIM\_DVDDrive**](/previous-versions//cc136812(v=vs.85)).</span></span>

<span data-ttu-id="277b0-258">Dieses Array enthält die folgenden Werte für ISO.</span><span class="sxs-lookup"><span data-stu-id="277b0-258">This array contains the following values for ISO.</span></span>

<dl> <dt>

<span data-ttu-id="277b0-259">{16, 22}</span><span class="sxs-lookup"><span data-stu-id="277b0-259">{16, 22}</span></span>
</dt> <dt>

<span data-ttu-id="277b0-260"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span><span class="sxs-lookup"><span data-stu-id="277b0-260"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span></span>
</dt> <dt>

<span data-ttu-id="277b0-261"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span><span class="sxs-lookup"><span data-stu-id="277b0-261"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span></span>
</dt> </dl>

<span data-ttu-id="277b0-262">Dieses Array enthält die folgenden Werte für die physische Pass-Through.</span><span class="sxs-lookup"><span data-stu-id="277b0-262">This array contains the following values for physical pass-through.</span></span>

<dl> <dt>

<span data-ttu-id="277b0-263"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="277b0-263"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="277b0-264"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="277b0-264"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="277b0-265"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span><span class="sxs-lookup"><span data-stu-id="277b0-265"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span></span>
</dt> <dt>

<span data-ttu-id="277b0-266"><span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>**CD-ROM/XA** (17)</span><span class="sxs-lookup"><span data-stu-id="277b0-266"><span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>**CD-ROM/XA** (17)</span></span>
</dt> <dt>

<span data-ttu-id="277b0-267"><span id="CD-I"></span><span id="cd-i"></span>**CD-I** (18)</span><span class="sxs-lookup"><span data-stu-id="277b0-267"><span id="CD-I"></span><span id="cd-i"></span>**CD-I** (18)</span></span>
</dt> <dt>

<span data-ttu-id="277b0-268"><span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>**CD-Recordable** (19)</span><span class="sxs-lookup"><span data-stu-id="277b0-268"><span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>**CD Recordable** (19)</span></span>
</dt> <dt>

<span data-ttu-id="277b0-269"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span><span class="sxs-lookup"><span data-stu-id="277b0-269"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span></span>
</dt> <dt>

<span data-ttu-id="277b0-270"><span id="DVD-RW_"></span><span id="dvd-rw_"></span>**DVD-RW +** (23)</span><span class="sxs-lookup"><span data-stu-id="277b0-270"><span id="DVD-RW_"></span><span id="dvd-rw_"></span>**DVD-RW+** (23)</span></span>
</dt> <dt>

<span data-ttu-id="277b0-271"><span id="DVD-RAM"></span><span id="dvd-ram"></span>**DVD-RAM** (24)</span><span class="sxs-lookup"><span data-stu-id="277b0-271"><span id="DVD-RAM"></span><span id="dvd-ram"></span>**DVD-RAM** (24)</span></span>
</dt> <dt>

<span data-ttu-id="277b0-272"><span id="DVD-ROM"></span><span id="dvd-rom"></span>**DVD-ROM** (25)</span><span class="sxs-lookup"><span data-stu-id="277b0-272"><span id="DVD-ROM"></span><span id="dvd-rom"></span>**DVD-ROM** (25)</span></span>
</dt> <dt>

<span data-ttu-id="277b0-273"><span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>**DVD-Video** (26)</span><span class="sxs-lookup"><span data-stu-id="277b0-273"><span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>**DVD-Video** (26)</span></span>
</dt> <dt>

<span data-ttu-id="277b0-274"><span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>**MPEG** (27)</span><span class="sxs-lookup"><span data-stu-id="277b0-274"><span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>**Divx** (27)</span></span>
</dt> <dt>

<span data-ttu-id="277b0-275"><span id="CD-RW"></span><span id="cd-rw"></span>**CD-RW** (33)</span><span class="sxs-lookup"><span data-stu-id="277b0-275"><span id="CD-RW"></span><span id="cd-rw"></span>**CD-RW** (33)</span></span>
</dt> <dt>

<span data-ttu-id="277b0-276"><span id="CD-DA"></span><span id="cd-da"></span>**CD-da** (34)</span><span class="sxs-lookup"><span data-stu-id="277b0-276"><span id="CD-DA"></span><span id="cd-da"></span>**CD-DA** (34)</span></span>
</dt> <dt>

<span data-ttu-id="277b0-277"><span id="CD_"></span><span id="cd_"></span>**CD +** (35)</span><span class="sxs-lookup"><span data-stu-id="277b0-277"><span id="CD_"></span><span id="cd_"></span>**CD+** (35)</span></span>
</dt> <dt>

<span data-ttu-id="277b0-278"><span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>**DVD-Recordable** (36)</span><span class="sxs-lookup"><span data-stu-id="277b0-278"><span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>**DVD Recordable** (36)</span></span>
</dt> <dt>

<span data-ttu-id="277b0-279"><span id="DVD-RW"></span><span id="dvd-rw"></span>**DVD-RW** (37)</span><span class="sxs-lookup"><span data-stu-id="277b0-279"><span id="DVD-RW"></span><span id="dvd-rw"></span>**DVD-RW** (37)</span></span>
</dt> <dt>

<span data-ttu-id="277b0-280"><span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>**DVD-Audiodaten** (38)</span><span class="sxs-lookup"><span data-stu-id="277b0-280"><span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>**DVD-Audio** (38)</span></span>
</dt> <dt>

<span data-ttu-id="277b0-281"><span id="DVD-5"></span><span id="dvd-5"></span>**DVD-5** (39)</span><span class="sxs-lookup"><span data-stu-id="277b0-281"><span id="DVD-5"></span><span id="dvd-5"></span>**DVD-5** (39)</span></span>
</dt> <dt>

<span data-ttu-id="277b0-282"><span id="DVD-9"></span><span id="dvd-9"></span>**DVD-9** (40)</span><span class="sxs-lookup"><span data-stu-id="277b0-282"><span id="DVD-9"></span><span id="dvd-9"></span>**DVD-9** (40)</span></span>
</dt> <dt>

<span data-ttu-id="277b0-283"><span id="DVD-10"></span><span id="dvd-10"></span>**DVD-10** (41)</span><span class="sxs-lookup"><span data-stu-id="277b0-283"><span id="DVD-10"></span><span id="dvd-10"></span>**DVD-10** (41)</span></span>
</dt> <dt>

<span data-ttu-id="277b0-284"><span id="DVD-18"></span><span id="dvd-18"></span>**DVD-18** (42)</span><span class="sxs-lookup"><span data-stu-id="277b0-284"><span id="DVD-18"></span><span id="dvd-18"></span>**DVD-18** (42)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="277b0-285">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="277b0-285">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-286">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="277b0-286">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-287">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-288">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="277b0-288">The current health of the element.</span></span> <span data-ttu-id="277b0-289">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="277b0-289">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="277b0-290">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="277b0-290">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="277b0-291">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-291">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-292">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="277b0-292">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-293">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="277b0-293">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="277b0-294">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-295">Ein Array von Freiform-Zeichen folgen, die Erklärungen und Details hinter den Einträgen im Eigenschafts Array " **OtherIdentifyingInfo** " bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="277b0-295">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="277b0-296">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="277b0-296">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="277b0-297">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="277b0-297">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-298">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="277b0-298">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-299">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-300">Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="277b0-300">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="277b0-301">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-301">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-302">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="277b0-302">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-303">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="277b0-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-304">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="277b0-305">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="277b0-305">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="277b0-306">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="277b0-306">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="277b0-307">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-307">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-308">**Lastbereinigt**</span><span class="sxs-lookup"><span data-stu-id="277b0-308">**LastCleaned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-309">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="277b0-309">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-310">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-311">Das Datum und die Uhrzeit der letzten Bereinigung des Geräts.</span><span class="sxs-lookup"><span data-stu-id="277b0-311">The date and time on which the device was last cleaned.</span></span> <span data-ttu-id="277b0-312">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-312">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-313">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="277b0-313">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-314">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="277b0-314">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-315">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-316">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="277b0-316">The last error code reported by the logical device.</span></span> <span data-ttu-id="277b0-317">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="277b0-317">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="277b0-318">**Loadtime**</span><span class="sxs-lookup"><span data-stu-id="277b0-318">**LoadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-319">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="277b0-319">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-320">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-321">Die Zeit (in Millisekunden) von "Load" bis zum Lesen oder Schreiben eines Mediums.</span><span class="sxs-lookup"><span data-stu-id="277b0-321">The time, in milliseconds, from 'load' to being able to read or write a media.</span></span> <span data-ttu-id="277b0-322">Beispielsweise ist dies das Intervall für Laufwerke zwischen einem Datenträger, der nicht auf die Festplatte zeigt, dass er für Lese-/Schreibzugriff bereit ist (d. h., der Datenträger wird mit nominaler Geschwindigkeit).</span><span class="sxs-lookup"><span data-stu-id="277b0-322">For example, for disk drives, this is the interval between a disk not spinning to the disk reporting that it is ready for read/write (that is, the disk spinning at nominal speeds).</span></span> <span data-ttu-id="277b0-323">Bei Bandlaufwerken ist dies der Zeitpunkt, zu dem ein Medium eingefügt wird, um zu melden, dass es für eine Anwendung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="277b0-323">For tape drives, this is the time from a media being injected to reporting that it is ready for an application.</span></span> <span data-ttu-id="277b0-324">Dies befindet sich normalerweise im botbereich des Bands.</span><span class="sxs-lookup"><span data-stu-id="277b0-324">This is usually at the tape's BOT area.</span></span> <span data-ttu-id="277b0-325">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-325">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-326">**Maxaccesstime**</span><span class="sxs-lookup"><span data-stu-id="277b0-326">**MaxAccessTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-327">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="277b0-327">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-328">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-329">Die Zeit (in Millisekunden), die von der ersten Position auf dem Medium an den Speicherort verschoben werden soll, der in Bezug auf die Zeit am weitesten ist.</span><span class="sxs-lookup"><span data-stu-id="277b0-329">The time, in milliseconds, to move from the first location on the media to the location that is furthest with respect to time.</span></span> <span data-ttu-id="277b0-330">Bei einem Laufwerk stellt dies eine vollständige Suche und eine vollständige Rotationsverzögerung dar.</span><span class="sxs-lookup"><span data-stu-id="277b0-330">For a disk drive, this represents full seek + full rotational delay.</span></span> <span data-ttu-id="277b0-331">Bei Bandlaufwerken stellt dies eine Suche zwischen dem Anfang des Bands und dem physisch entfernten Punkt dar.</span><span class="sxs-lookup"><span data-stu-id="277b0-331">For tape drives, this represents a search from the beginning of the tape to the most physically distant point.</span></span> <span data-ttu-id="277b0-332">(Das Ende eines Bands kann sich am physisch entfernten Punkt befinden, dies ist jedoch nicht unbedingt der Fall.) Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-332">(The end of a tape may be at its most physically distant point, but this is not necessarily true.) This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-333">**Maxblocksize**</span><span class="sxs-lookup"><span data-stu-id="277b0-333">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-334">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="277b0-334">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-335">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-336">Die maximale Blockgröße (in Bytes) für Medien, auf die das Gerät zugreift.</span><span class="sxs-lookup"><span data-stu-id="277b0-336">The maximum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="277b0-337">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-337">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-338">**Maxmediasize**</span><span class="sxs-lookup"><span data-stu-id="277b0-338">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-339">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="277b0-339">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-340">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-341">Die maximale Größe des von diesem Gerät unterstützten Mediums in Kilobyte.</span><span class="sxs-lookup"><span data-stu-id="277b0-341">The maximum size, in kilobytes, of media supported by this device.</span></span> <span data-ttu-id="277b0-342">Kilobytes werden als Anzahl von Bytes, multipliziert mit 1000, interpretiert (nicht die Anzahl der Bytes multipliziert mit 1024).</span><span class="sxs-lookup"><span data-stu-id="277b0-342">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span> <span data-ttu-id="277b0-343">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-343">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-344">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="277b0-344">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-345">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="277b0-345">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-346">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-347">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="277b0-347">This property has been deprecated.</span></span> <span data-ttu-id="277b0-348">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="277b0-348">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="277b0-349">**Maxunitionbeforecforec**</span><span class="sxs-lookup"><span data-stu-id="277b0-349">**MaxUnitsBeforeCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-350">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="277b0-350">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-351">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-352">Die maximalen Einheiten, die verwendet werden können, bevor das Gerät bereinigt wird.</span><span class="sxs-lookup"><span data-stu-id="277b0-352">The maximum units that can be used before the device should be cleaned.</span></span> <span data-ttu-id="277b0-353">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-353">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-354">**Mediaislocked**</span><span class="sxs-lookup"><span data-stu-id="277b0-354">**MediaIsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-355">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="277b0-355">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-356">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-357">**True** , wenn die Medien im Gerät gesperrt sind und nicht aussteht. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="277b0-357">**True** if the media is locked in the device and cannot be ejected; otherwise, **False**.</span></span> <span data-ttu-id="277b0-358">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-358">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-359">**Minblocksize**</span><span class="sxs-lookup"><span data-stu-id="277b0-359">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-360">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="277b0-360">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-361">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-362">Die minimale Blockgröße (in Bytes) für Medien, auf die das Gerät zugreift.</span><span class="sxs-lookup"><span data-stu-id="277b0-362">The minimum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="277b0-363">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-363">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-364">**Mountcount**</span><span class="sxs-lookup"><span data-stu-id="277b0-364">**MountCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-365">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="277b0-365">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-366">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-367">Bei Geräten, die Wechselmedien unterstützen, gibt es die Häufigkeit, mit der Medien für die Datenübertragung bereitgestellt oder das Gerät bereinigt werden.</span><span class="sxs-lookup"><span data-stu-id="277b0-367">For a device that supports removable media, the number of times that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="277b0-368">Bei Geräten, die auf nicht Wechselmedien (z. b. Festplatten) zugreifen, ist diese Eigenschaft nicht anwendbar und sollte auf 0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="277b0-368">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="277b0-369">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-369">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-370">**Name**</span><span class="sxs-lookup"><span data-stu-id="277b0-370">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-371">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="277b0-371">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-372">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-373">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="277b0-373">The label by which the object is known.</span></span> <span data-ttu-id="277b0-374">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und entspricht der Element **Name** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="277b0-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="277b0-375">**Unnötig**</span><span class="sxs-lookup"><span data-stu-id="277b0-375">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-376">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="277b0-376">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-377">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-378">**True** , wenn das Medien Zugriffsgerät bereinigt werden muss. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="277b0-378">**True** if the media access device needs cleaning; otherwise, **False**.</span></span> <span data-ttu-id="277b0-379">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-379">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-380">**"Numofmediasupportiert"**</span><span class="sxs-lookup"><span data-stu-id="277b0-380">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-381">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="277b0-381">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-382">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-383">Die maximale Anzahl von mehreren einzelnen Medien, die unterstützt oder eingefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="277b0-383">The maximum number of multiple individual media that can be supported or inserted.</span></span> <span data-ttu-id="277b0-384">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-384">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-385">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="277b0-385">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-386">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="277b0-386">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-387">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-388">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="277b0-388">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="277b0-389">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="277b0-389">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="277b0-390">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-390">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-391">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="277b0-391">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-392">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="277b0-392">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="277b0-393">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-394">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="277b0-394">The current statuses of the object.</span></span> <span data-ttu-id="277b0-395">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-395">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-396">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="277b0-396">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-397">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="277b0-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-398">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-399">Der aktivierte oder deaktivierte Status des Elements, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="277b0-399">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="277b0-400">Diese Eigenschaft muss auf **null** festgelegt werden, wenn die **enabledstate** -Eigenschaft einen anderen Wert als 1 hat.</span><span class="sxs-lookup"><span data-stu-id="277b0-400">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="277b0-401">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-401">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-402">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="277b0-402">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-403">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="277b0-403">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="277b0-404">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-405">Alle zusätzlichen Daten über Geräte-ID-Informationen, die zur Identifizierung eines logischen Geräts verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="277b0-405">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="277b0-406">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="277b0-406">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="277b0-407">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="277b0-407">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-408">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="277b0-408">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="277b0-409">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-410">Die Energie Verwaltungsfunktionen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="277b0-410">The power management capabilities of the device.</span></span> <span data-ttu-id="277b0-411">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="277b0-411">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="277b0-412">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="277b0-412">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-413">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="277b0-413">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-414">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-415">Gibt an, ob das Gerät Energie gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="277b0-415">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="277b0-416">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="277b0-416">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="277b0-417">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="277b0-417">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-418">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="277b0-418">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-419">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-420">Gibt an, wie viele aufeinanderfolgende Stunden dieses Gerät seit dem letzten Strom Umgebung eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="277b0-420">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="277b0-421">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="277b0-421">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="277b0-422">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="277b0-422">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-423">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="277b0-423">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-424">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-424">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-425">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="277b0-425">Provides high level status information.</span></span> <span data-ttu-id="277b0-426">Diese Eigenschaft sollte in Verbindung mit der **detailedstatus** -Eigenschaft verwendet werden, um allgemeine und ausführliche Integritäts Statusinformationen für das-Element und seine unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="277b0-426">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="277b0-427">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="277b0-427">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="277b0-428">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-428">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-429">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="277b0-429">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-430">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="277b0-430">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-431">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-432">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="277b0-432">The last requested or desired state for the element.</span></span> <span data-ttu-id="277b0-433">Der tatsächliche Zustand des Elements wird durch die **enabledstate** -Eigenschaft dargestellt.</span><span class="sxs-lookup"><span data-stu-id="277b0-433">The actual state of the element is represented by the **EnabledState** property.</span></span> <span data-ttu-id="277b0-434">Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuell aktivierten oder deaktivierten Zustände zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="277b0-434">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="277b0-435">Eine bestimmte Instanz von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) unterstützt möglicherweise nicht die **requestStateChange** -Methode.</span><span class="sxs-lookup"><span data-stu-id="277b0-435">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="277b0-436">Wenn dies auftritt, wird der Wert 12 (nicht zutreffend) verwendet.</span><span class="sxs-lookup"><span data-stu-id="277b0-436">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="277b0-437">Diese Eigenschaft wird von **CIM \_ enabledlogicalelement** geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-437">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="277b0-438">**Security**</span><span class="sxs-lookup"><span data-stu-id="277b0-438">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-439">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="277b0-439">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-440">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-441">Die für das Gerät definierte Betriebssicherheit.</span><span class="sxs-lookup"><span data-stu-id="277b0-441">The operational security defined for the device.</span></span> <span data-ttu-id="277b0-442">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-442">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-443">**Status**</span><span class="sxs-lookup"><span data-stu-id="277b0-443">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-444">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="277b0-444">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-445">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-446">Der aktuelle Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="277b0-446">The current status of the object.</span></span> <span data-ttu-id="277b0-447">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="277b0-447">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="277b0-448">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="277b0-448">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-449">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="277b0-449">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="277b0-450">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-451">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="277b0-451">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="277b0-452">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-452">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-453">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="277b0-453">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-454">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="277b0-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-455">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-456">Der aktuelle Zustand des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="277b0-456">The current state of the logical device.</span></span> <span data-ttu-id="277b0-457">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="277b0-457">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="277b0-458">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="277b0-458">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-459">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="277b0-459">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-460">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-461">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="277b0-461">The scoping system's creation class name.</span></span> <span data-ttu-id="277b0-462">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-462">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-463">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="277b0-463">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-464">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="277b0-464">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-465">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-466">Der eindeutige Bezeichner für die Bereichs bezogene virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="277b0-466">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="277b0-467">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-467">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-468">**Timeoflastmount**</span><span class="sxs-lookup"><span data-stu-id="277b0-468">**TimeOfLastMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-469">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="277b0-469">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-470">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-471">Für ein Gerät, das Wechselmedien unterstützt, das Datum und die Uhrzeit der letzten Bereitstellung des Mediums auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="277b0-471">For a device that supports removable media, the most recent date and time that media was mounted on the device.</span></span> <span data-ttu-id="277b0-472">Bei Geräten, die auf nicht Wechselmedien wie Festplatten zugreifen, hat diese Eigenschaft keine Bedeutung und ist nicht anwendbar.</span><span class="sxs-lookup"><span data-stu-id="277b0-472">For devices accessing nonremovable media, such as hard disks, this property has no meaning and is not applicable.</span></span> <span data-ttu-id="277b0-473">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-473">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-474">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="277b0-474">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-475">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="277b0-475">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-476">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-476">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-477">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="277b0-477">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="277b0-478">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="277b0-478">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="277b0-479">**Totalmounttime**</span><span class="sxs-lookup"><span data-stu-id="277b0-479">**TotalMountTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-480">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="277b0-480">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-481">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-481">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-482">Für ein Gerät, das Wechselmedien unterstützt, die Gesamtzeit (in Sekunden), die Medien für die Datenübertragung bereitgestellt wurden, oder um das Gerät zu bereinigen.</span><span class="sxs-lookup"><span data-stu-id="277b0-482">For a device that supports removable media, the total time (in seconds) that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="277b0-483">Bei Geräten, die auf nicht Wechselmedien (z. b. Festplatten) zugreifen, ist diese Eigenschaft nicht anwendbar und sollte auf 0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="277b0-483">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="277b0-484">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-484">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-485">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="277b0-485">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-486">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="277b0-486">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-487">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-488">Die Gesamtanzahl der Stunden, für die dieses Gerät eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="277b0-488">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="277b0-489">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="277b0-489">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="277b0-490">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="277b0-490">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-491">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="277b0-491">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-492">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-492">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-493">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="277b0-493">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="277b0-494">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="277b0-494">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="277b0-495">**Uncompresseddatarate**</span><span class="sxs-lookup"><span data-stu-id="277b0-495">**UncompressedDataRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-496">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="277b0-496">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-497">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-497">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-498">Die dauerhafte Datenübertragungsrate in KB/Sek., die das Gerät lesen und in ein Medium schreiben kann.</span><span class="sxs-lookup"><span data-stu-id="277b0-498">The sustained data transfer rate, in KB/sec, that the device can read from and write to a media.</span></span> <span data-ttu-id="277b0-499">Dies ist eine dauerhafte, Rohdaten Rate.</span><span class="sxs-lookup"><span data-stu-id="277b0-499">This is a sustained, raw data rate.</span></span> <span data-ttu-id="277b0-500">Die maximale Anzahl von Raten oder raten, bei denen die Komprimierung nicht in dieser Eigenschaft gemeldet werden sollte</span><span class="sxs-lookup"><span data-stu-id="277b0-500">Maximum rates or rates assuming compression should not be reported in this property.</span></span> <span data-ttu-id="277b0-501">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-501">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-502">**Unitydescription**</span><span class="sxs-lookup"><span data-stu-id="277b0-502">**UnitsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-503">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="277b0-503">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-504">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-505">Die Einheiten in Relation zur Verwendung in **maxunitionbeforecforec.**</span><span class="sxs-lookup"><span data-stu-id="277b0-505">The units relative to its use in **MaxUnitsBeforeCleaning**.</span></span> <span data-ttu-id="277b0-506">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-506">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-507">**Unitsused**</span><span class="sxs-lookup"><span data-stu-id="277b0-507">**UnitsUsed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-508">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="277b0-508">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-509">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-509">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-510">Die aktuelle Anzahl der verwendeten Einheiten.</span><span class="sxs-lookup"><span data-stu-id="277b0-510">The current number of units used.</span></span> <span data-ttu-id="277b0-511">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-511">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="277b0-512">**Unloadtime**</span><span class="sxs-lookup"><span data-stu-id="277b0-512">**UnloadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277b0-513">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="277b0-513">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="277b0-514">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="277b0-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277b0-515">Die Zeit (in Millisekunden), die in der Lage ist, ein Medium in seinen "Entladevorgang" zu lesen oder zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="277b0-515">The time, in milliseconds, from being able to read or write a media to its 'unload'.</span></span> <span data-ttu-id="277b0-516">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="277b0-516">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="277b0-517">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="277b0-517">Remarks</span></span>

<span data-ttu-id="277b0-518">Der Zugriff auf die **MSVM- \_ dvddrive** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="277b0-518">Access to the **Msvm\_DVDDrive** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="277b0-519">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="277b0-519">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="277b0-520">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="277b0-520">Requirements</span></span>



| <span data-ttu-id="277b0-521">Anforderung</span><span class="sxs-lookup"><span data-stu-id="277b0-521">Requirement</span></span> | <span data-ttu-id="277b0-522">Wert</span><span class="sxs-lookup"><span data-stu-id="277b0-522">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="277b0-523">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="277b0-523">Minimum supported client</span></span><br/> | <span data-ttu-id="277b0-524">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="277b0-524">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="277b0-525">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="277b0-525">Minimum supported server</span></span><br/> | <span data-ttu-id="277b0-526">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="277b0-526">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="277b0-527">Namespace</span><span class="sxs-lookup"><span data-stu-id="277b0-527">Namespace</span></span><br/>                | <span data-ttu-id="277b0-528">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="277b0-528">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="277b0-529">MOF</span><span class="sxs-lookup"><span data-stu-id="277b0-529">MOF</span></span><br/>                      | <dl> <span data-ttu-id="277b0-530"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="277b0-530"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="277b0-531">DLL</span><span class="sxs-lookup"><span data-stu-id="277b0-531">DLL</span></span><br/>                      | <dl> <span data-ttu-id="277b0-532"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="277b0-532"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="277b0-533">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="277b0-533">See also</span></span>

<dl> <dt>

[<span data-ttu-id="277b0-534">**CIM- \_ dvddrive**</span><span class="sxs-lookup"><span data-stu-id="277b0-534">**CIM\_DVDDrive**</span></span>](cim-dvddrive.md)
</dt> <dt>

<span data-ttu-id="277b0-535">[**CIM- \_ dvddrive**](/previous-versions//cc136812(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="277b0-535">[**CIM\_DVDDrive**](/previous-versions//cc136812(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="277b0-536">Speicher Klassen</span><span class="sxs-lookup"><span data-stu-id="277b0-536">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

