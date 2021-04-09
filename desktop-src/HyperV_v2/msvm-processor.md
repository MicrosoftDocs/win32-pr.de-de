---
description: Stellt den virtuellen Prozessor in einem virtuellen Computer dar.
ms.assetid: 4BA91C44-0F85-42D1-A8B5-147E1D532FB5
title: Msvm_Processor-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Processor
- Msvm_Processor.SetPowerState
- Msvm_Processor.EnableDevice
- Msvm_Processor.OnlineDevice
- Msvm_Processor.QuiesceDevice
- Msvm_Processor.SaveProperties
- Msvm_Processor.RestoreProperties
- Msvm_Processor.InstanceID
- Msvm_Processor.Caption
- Msvm_Processor.Description
- Msvm_Processor.ElementName
- Msvm_Processor.InstallDate
- Msvm_Processor.Name
- Msvm_Processor.OperationalStatus
- Msvm_Processor.StatusDescriptions
- Msvm_Processor.Status
- Msvm_Processor.HealthState
- Msvm_Processor.CommunicationStatus
- Msvm_Processor.DetailedStatus
- Msvm_Processor.OperatingStatus
- Msvm_Processor.PrimaryStatus
- Msvm_Processor.EnabledState
- Msvm_Processor.OtherEnabledState
- Msvm_Processor.RequestedState
- Msvm_Processor.EnabledDefault
- Msvm_Processor.TimeOfLastStateChange
- Msvm_Processor.AvailableRequestedStates
- Msvm_Processor.TransitioningToState
- Msvm_Processor.SystemCreationClassName
- Msvm_Processor.SystemName
- Msvm_Processor.CreationClassName
- Msvm_Processor.DeviceID
- Msvm_Processor.PowerManagementSupported
- Msvm_Processor.PowerManagementCapabilities
- Msvm_Processor.Availability
- Msvm_Processor.StatusInfo
- Msvm_Processor.LastErrorCode
- Msvm_Processor.ErrorDescription
- Msvm_Processor.ErrorCleared
- Msvm_Processor.OtherIdentifyingInfo
- Msvm_Processor.PowerOnHours
- Msvm_Processor.TotalPowerOnHours
- Msvm_Processor.IdentifyingDescriptions
- Msvm_Processor.AdditionalAvailability
- Msvm_Processor.MaxQuiesceTime
- Msvm_Processor.Role
- Msvm_Processor.Family
- Msvm_Processor.OtherFamilyDescription
- Msvm_Processor.UpgradeMethod
- Msvm_Processor.MaxClockSpeed
- Msvm_Processor.CurrentClockSpeed
- Msvm_Processor.DataWidth
- Msvm_Processor.AddressWidth
- Msvm_Processor.LoadPercentage
- Msvm_Processor.Stepping
- Msvm_Processor.UniqueID
- Msvm_Processor.CPUStatus
- Msvm_Processor.ExternalBusClockSpeed
- Msvm_Processor.LoadPercentageHistory
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 14ed1e2bbb9e15f89376234da8981faffb1a6809
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865528"
---
# <a name="msvm_processor-class"></a><span data-ttu-id="41093-103">MSVM- \_ Prozessor Klasse</span><span class="sxs-lookup"><span data-stu-id="41093-103">Msvm\_Processor class</span></span>

<span data-ttu-id="41093-104">Stellt den virtuellen Prozessor in einem virtuellen Computer dar.</span><span class="sxs-lookup"><span data-stu-id="41093-104">Represents the virtual processor in a virtual machine.</span></span>

<span data-ttu-id="41093-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="41093-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="41093-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="41093-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Processor : CIM_Processor
{
  string   InstanceID;
  string   Caption = "Processor";
  string   Description = " A logical processor of the hypervisor running on the host computer system.";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 2;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_Processor";
  string   DeviceID = "Microsoft:GUID\device specific data";
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
  uint16   AdditionalAvailability[];
  uint64   MaxQuiesceTime;
  string   Role = "Central Processor";
  uint16   Family;
  string   OtherFamilyDescription;
  uint16   UpgradeMethod;
  uint32   MaxClockSpeed;
  uint32   CurrentClockSpeed;
  uint16   DataWidth;
  uint16   AddressWidth;
  uint16   LoadPercentage;
  string   Stepping;
  string   UniqueID;
  uint16   CPUStatus;
  uint32   ExternalBusClockSpeed;
  uint16   LoadPercentageHistory[];
};
```

## <a name="members"></a><span data-ttu-id="41093-107">Member</span><span class="sxs-lookup"><span data-stu-id="41093-107">Members</span></span>

<span data-ttu-id="41093-108">Die **MSVM- \_ Prozessor** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="41093-108">The **Msvm\_Processor** class has these types of members:</span></span>

-   [<span data-ttu-id="41093-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="41093-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="41093-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="41093-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="41093-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="41093-111">Methods</span></span>

<span data-ttu-id="41093-112">Die **MSVM- \_ Prozessor** Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="41093-112">The **Msvm\_Processor** class has these methods.</span></span>



| <span data-ttu-id="41093-113">Methode</span><span class="sxs-lookup"><span data-stu-id="41093-113">Method</span></span>                                                          | <span data-ttu-id="41093-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="41093-114">Description</span></span>                              |
|:----------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="41093-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="41093-115">**EnableDevice**</span></span>                                                | <span data-ttu-id="41093-116">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="41093-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="41093-117">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="41093-117">**OnlineDevice**</span></span>                                                | <span data-ttu-id="41093-118">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="41093-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="41093-119">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="41093-119">**QuiesceDevice**</span></span>                                               | <span data-ttu-id="41093-120">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="41093-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="41093-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="41093-121">**RequestStateChange**</span></span>](msvm-processor-requeststatechange.md) | <span data-ttu-id="41093-122">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="41093-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="41093-123">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="41093-123">**Reset**</span></span>](msvm-processor-reset.md)                           | <span data-ttu-id="41093-124">Setzt das virtuelle Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="41093-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="41093-125">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="41093-125">**RestoreProperties**</span></span>                                           | <span data-ttu-id="41093-126">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="41093-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="41093-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="41093-127">**SaveProperties**</span></span>                                              | <span data-ttu-id="41093-128">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="41093-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="41093-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="41093-129">**SetPowerState**</span></span>                                               | <span data-ttu-id="41093-130">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="41093-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="41093-131">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="41093-131">Properties</span></span>

<span data-ttu-id="41093-132">Die **MSVM- \_ Prozessor** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="41093-132">The **Msvm\_Processor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="41093-133">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="41093-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-134">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="41093-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="41093-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-136">Alle zusätzlichen Verfügbarkeit und den Status des Geräts, außer den in der **Availability** -Eigenschaft angegebenen.</span><span class="sxs-lookup"><span data-stu-id="41093-136">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="41093-137">Die **Availability** -Eigenschaft gibt den primären Status und die Verfügbarkeit des Geräts an.</span><span class="sxs-lookup"><span data-stu-id="41093-137">The **Availability** property denotes the primary status and availability of the device.</span></span> <span data-ttu-id="41093-138">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41093-138">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="41093-139">**Addresswidth**</span><span class="sxs-lookup"><span data-stu-id="41093-139">**AddressWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-140">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41093-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41093-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-142">Die Prozessor Adress Breite in Bits.</span><span class="sxs-lookup"><span data-stu-id="41093-142">The processor address width, in bits.</span></span> <span data-ttu-id="41093-143">Diese Eigenschaft wird vom [**CIM- \_ Prozessor**](/windows/desktop/CIMWin32Prov/cim-processor)geerbt, und der Wert ist entweder 32 oder 64, abhängig von den Merkmalen der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="41093-143">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor), and the value is either 32 or 64, depending on the characteristics of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="41093-144">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="41093-144">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-145">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41093-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41093-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-147">Die primäre Verfügbarkeit und den Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="41093-147">The primary availability and status of the device.</span></span> <span data-ttu-id="41093-148">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="41093-148">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="41093-149">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="41093-149">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-150">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="41093-150">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="41093-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-152">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="41093-152">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="41093-153">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="41093-153">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="41093-154">**Caption**</span><span class="sxs-lookup"><span data-stu-id="41093-154">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-155">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41093-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41093-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41093-157">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="41093-157">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="41093-158">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="41093-158">A short description of the object.</span></span> <span data-ttu-id="41093-159">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41093-159">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="41093-160">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="41093-160">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-161">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41093-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41093-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-163">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="41093-163">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="41093-164">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="41093-164">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="41093-165">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41093-165">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="41093-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="41093-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="41093-167"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="41093-167"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="41093-168"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="41093-168"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="41093-169"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="41093-169"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="41093-170"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="41093-170"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="41093-171"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="41093-171"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="41093-172"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="41093-172"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="41093-173">)</span><span class="sxs-lookup"><span data-stu-id="41093-173">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="41093-174">**Cpustatus**</span><span class="sxs-lookup"><span data-stu-id="41093-174">**CPUStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-175">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41093-175">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41093-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-177">Der aktuelle Status des Prozessors.</span><span class="sxs-lookup"><span data-stu-id="41093-177">The current status of the processor.</span></span> <span data-ttu-id="41093-178">Diese Eigenschaft wird vom [**CIM- \_ Prozessor**](/windows/desktop/CIMWin32Prov/cim-processor)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41093-178">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="41093-179">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="41093-179">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-180">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41093-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41093-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41093-182">Qualifizierer: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="41093-182">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="41093-183">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="41093-183">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="41093-184">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="41093-184">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="41093-185">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41093-185">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="41093-186">**Weise**</span><span class="sxs-lookup"><span data-stu-id="41093-186">**CurrentClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-187">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="41093-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41093-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-189">Die maximale Geschwindigkeit des physischen Prozessors unter Berücksichtigung der Kapazität für den virtuellen Prozessor.</span><span class="sxs-lookup"><span data-stu-id="41093-189">The maximum speed of the physical processor, taking into account the capacity for the virtual processor.</span></span> <span data-ttu-id="41093-190">Diese Eigenschaft wird vom [**CIM- \_ Prozessor**](/windows/desktop/CIMWin32Prov/cim-processor)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41093-190">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="41093-191">**DataWidth**</span><span class="sxs-lookup"><span data-stu-id="41093-191">**DataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-192">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41093-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41093-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-194">Die Prozessor Daten Breite in Bits.</span><span class="sxs-lookup"><span data-stu-id="41093-194">The processor data width, in bits.</span></span> <span data-ttu-id="41093-195">Diese Eigenschaft wird vom [**CIM- \_ Prozessor**](/windows/desktop/CIMWin32Prov/cim-processor)geerbt, und der Wert ist entweder 32 oder 64, abhängig von den Merkmalen der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="41093-195">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor), and the value is either 32 or 64, depending on the characteristics of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="41093-196">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="41093-196">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-197">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41093-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41093-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-199">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="41093-199">A description of the object.</span></span> <span data-ttu-id="41093-200">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41093-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="41093-201">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="41093-201">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-202">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41093-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41093-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-204">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="41093-204">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="41093-205">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="41093-205">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="41093-206">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41093-206">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="41093-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="41093-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="41093-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="41093-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="41093-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="41093-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="41093-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="41093-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="41093-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="41093-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="41093-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="41093-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="41093-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="41093-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="41093-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="41093-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="41093-215">)</span><span class="sxs-lookup"><span data-stu-id="41093-215">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="41093-216">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="41093-216">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-217">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41093-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41093-218">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-219">Eine Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="41093-219">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="41093-220">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf "Microsoft:*GUID* \\ *gerätespezifische Daten*" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="41093-220">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*\\*device specific data*".</span></span>

</dd> <dt>

<span data-ttu-id="41093-221">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="41093-221">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-222">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41093-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41093-223">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-224">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="41093-224">A display name for the object.</span></span> <span data-ttu-id="41093-225">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41093-225">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="41093-226">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="41093-226">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-227">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41093-227">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41093-228">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-229">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="41093-229">An administrator's default or startup configuration for the Enabled State of an element.</span></span> <span data-ttu-id="41093-230">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="41093-230">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="41093-231">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="41093-231">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-232">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41093-232">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41093-233">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-234">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="41093-234">The enabled and disabled states of an element.</span></span> <span data-ttu-id="41093-235">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="41093-235">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="41093-236">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="41093-236">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-237">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="41093-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="41093-238">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-239">Gibt an, ob der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="41093-239">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="41093-240">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="41093-240">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="41093-241">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="41093-241">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-242">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41093-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41093-243">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-244">Eine Zeichenfolge, die weitere Informationen über den Fehler enthält, der in **LastErrorCode** aufgezeichnet wurde, sowie Informationen über alle Maßnahmen, die ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="41093-244">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="41093-245">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="41093-245">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="41093-246">**Externalbusclockspeed**</span><span class="sxs-lookup"><span data-stu-id="41093-246">**ExternalBusClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-247">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="41093-247">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41093-248">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-249">Die Geschwindigkeit der externen busuhr des zugrunde liegenden physischen Prozessors.</span><span class="sxs-lookup"><span data-stu-id="41093-249">The external bus clock speed of the underlying physical processor.</span></span> <span data-ttu-id="41093-250">Diese Eigenschaft wird vom [**CIM- \_ Prozessor**](/windows/desktop/CIMWin32Prov/cim-processor)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41093-250">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="41093-251">**Familie**</span><span class="sxs-lookup"><span data-stu-id="41093-251">**Family**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-252">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41093-252">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41093-253">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-254">Die Prozessorfamilie des zugrunde liegenden physischen Prozessors.</span><span class="sxs-lookup"><span data-stu-id="41093-254">The processor family of the underlying physical processor.</span></span> <span data-ttu-id="41093-255">Diese Eigenschaft wird vom [**CIM- \_ Prozessor**](/windows/desktop/CIMWin32Prov/cim-processor)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41093-255">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="41093-256">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="41093-256">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-257">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41093-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41093-258">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-259">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="41093-259">The current health of the element.</span></span> <span data-ttu-id="41093-260">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41093-260">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="41093-261">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="41093-261">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-262">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="41093-262">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="41093-263">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-264">Ein Array von Freiform-Zeichen folgen, die Erklärungen und Details hinter den Einträgen im " [**OtherIdentifyingInfo**](msvm-keyboard.md) "-Array bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="41093-264">An array of free-form strings that provide explanations and details behind the entries in the [**OtherIdentifyingInfo**](msvm-keyboard.md) array.</span></span> <span data-ttu-id="41093-265">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="41093-265">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="41093-266">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="41093-266">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-267">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="41093-267">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="41093-268">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-269">Das Datum und die Uhrzeit der Erstellung der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="41093-269">The date and time when the virtual machine was created.</span></span> <span data-ttu-id="41093-270">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41093-270">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="41093-271">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="41093-271">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-272">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41093-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41093-273">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41093-274">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="41093-274">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="41093-275">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="41093-275">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="41093-276">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41093-276">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="41093-277">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="41093-277">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-278">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="41093-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41093-279">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-280">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="41093-280">The last error code reported by the logical device.</span></span> <span data-ttu-id="41093-281">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="41093-281">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="41093-282">**Loadprozentsatz**</span><span class="sxs-lookup"><span data-stu-id="41093-282">**LoadPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-283">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41093-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41093-284">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-285">Der aktuelle Prozentsatz der gesamten Verarbeitungsleistung, die vom virtuellen Computer beansprucht wird.</span><span class="sxs-lookup"><span data-stu-id="41093-285">The current percentage of the total processing power being consumed by the virtual machine.</span></span> <span data-ttu-id="41093-286">Diese Eigenschaft wird vom [**CIM- \_ Prozessor**](/windows/desktop/CIMWin32Prov/cim-processor)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41093-286">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="41093-287">**Loadprozentuagehistory**</span><span class="sxs-lookup"><span data-stu-id="41093-287">**LoadPercentageHistory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-288">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="41093-288">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="41093-289">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41093-290">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="41093-290">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="41093-291">Der aufgezeichnete Verlauf des Prozentsatzes der gesamten Verarbeitungsleistung, die vom virtuellen Computer beansprucht wird.</span><span class="sxs-lookup"><span data-stu-id="41093-291">The recorded history of percentage of the total processing power being consumed by the virtual machine.</span></span> <span data-ttu-id="41093-292">Dabei handelt es sich um ein Array mit Beispielen.</span><span class="sxs-lookup"><span data-stu-id="41093-292">This is an array containing samples.</span></span>

</dd> <dt>

<span data-ttu-id="41093-293">**MaxClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="41093-293">**MaxClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-294">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="41093-294">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41093-295">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-296">Die maximale Taktfrequenz des virtuellen Prozessors in Megahertz.</span><span class="sxs-lookup"><span data-stu-id="41093-296">The maximum clock speed, in megahertz, of the virtual processor.</span></span> <span data-ttu-id="41093-297">Diese Eigenschaft wird vom [**CIM- \_ Prozessor**](/windows/desktop/CIMWin32Prov/cim-processor)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41093-297">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="41093-298">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="41093-298">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-299">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="41093-299">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="41093-300">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-301">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="41093-301">This property has been deprecated.</span></span> <span data-ttu-id="41093-302">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="41093-302">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="41093-303">**Name**</span><span class="sxs-lookup"><span data-stu-id="41093-303">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-304">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41093-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41093-305">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41093-306">Qualifizierer: **maxlen** (1024)</span><span class="sxs-lookup"><span data-stu-id="41093-306">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="41093-307">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="41093-307">The label by which the object is known.</span></span> <span data-ttu-id="41093-308">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="41093-308">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="41093-309">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41093-309">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="41093-310">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="41093-310">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-311">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41093-311">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41093-312">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-313">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="41093-313">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="41093-314">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="41093-314">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="41093-315">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41093-315">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="41093-316"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="41093-316"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="41093-317"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="41093-317"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="41093-318"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="41093-318"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="41093-319"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="41093-319"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="41093-320"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="41093-320"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="41093-321"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="41093-321"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="41093-322"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="41093-322"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="41093-323"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="41093-323"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="41093-324"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="41093-324"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="41093-325"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="41093-325"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="41093-326"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="41093-326"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="41093-327"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="41093-327"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="41093-328"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="41093-328"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="41093-329"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="41093-329"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="41093-330"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="41093-330"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="41093-331"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="41093-331"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="41093-332"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="41093-332"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="41093-333"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="41093-333"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="41093-334"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="41093-334"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="41093-335">)</span><span class="sxs-lookup"><span data-stu-id="41093-335">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="41093-336">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="41093-336">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-337">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="41093-337">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="41093-338">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-339">Der aktuelle Status des Elements.</span><span class="sxs-lookup"><span data-stu-id="41093-339">The current status of the element.</span></span> <span data-ttu-id="41093-340">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41093-340">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="41093-341">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="41093-341">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-342">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41093-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41093-343">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-344">Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="41093-344">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="41093-345">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="41093-345">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="41093-346">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="41093-346">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="41093-347">**Otherfamilydescription**</span><span class="sxs-lookup"><span data-stu-id="41093-347">**OtherFamilyDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-348">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41093-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41093-349">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-350">Eine Beschreibung des Typs der Prozessorfamilie.</span><span class="sxs-lookup"><span data-stu-id="41093-350">A description of the processor family type.</span></span> <span data-ttu-id="41093-351">Diese Eigenschaft wird vom [**CIM- \_ Prozessor**](/windows/desktop/CIMWin32Prov/cim-processor)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="41093-351">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="41093-352">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="41093-352">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-353">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="41093-353">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="41093-354">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-355">Alle zusätzlichen Daten über Geräte-ID-Informationen, die zur Identifizierung eines logischen Geräts verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="41093-355">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="41093-356">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41093-356">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="41093-357">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="41093-357">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-358">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="41093-358">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="41093-359">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-360">Die Energie Verwaltungsfunktionen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="41093-360">The power management capabilities of the device.</span></span> <span data-ttu-id="41093-361">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="41093-361">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="41093-362">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="41093-362">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-363">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="41093-363">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="41093-364">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-365">Gibt an, ob die Energie Verwaltung auf dem Gerät unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="41093-365">Indicates whether power management is supported on the device.</span></span> <span data-ttu-id="41093-366">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="41093-366">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="41093-367">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="41093-367">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-368">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="41093-368">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="41093-369">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-370">Gibt an, wie viele aufeinanderfolgende Stunden dieses Gerät seit dem letzten Strom Umgebung eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="41093-370">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="41093-371">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="41093-371">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="41093-372">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="41093-372">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-373">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41093-373">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41093-374">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-375">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="41093-375">Provides high level status information.</span></span> <span data-ttu-id="41093-376">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="41093-376">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="41093-377">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="41093-377">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="41093-378">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41093-378">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="41093-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="41093-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="41093-380"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="41093-380"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="41093-381"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="41093-381"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="41093-382"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="41093-382"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="41093-383"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="41093-383"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="41093-384"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="41093-384"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="41093-385">)</span><span class="sxs-lookup"><span data-stu-id="41093-385">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="41093-386">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="41093-386">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-387">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41093-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41093-388">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-389">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="41093-389">The last requested or desired state for the element.</span></span> <span data-ttu-id="41093-390">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="41093-390">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="41093-391">**Rolle**</span><span class="sxs-lookup"><span data-stu-id="41093-391">**Role**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-392">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41093-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41093-393">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-394">Eine Zeichenfolge, die die Rolle des Prozessors beschreibt.</span><span class="sxs-lookup"><span data-stu-id="41093-394">A string that describes the role of the processor.</span></span> <span data-ttu-id="41093-395">Beispielsweise "Central Processor" oder "math Processor".</span><span class="sxs-lookup"><span data-stu-id="41093-395">For example, "Central Processor" or "Math Processor".</span></span> <span data-ttu-id="41093-396">Diese Eigenschaft wird vom [**CIM- \_ Prozessor**](/windows/desktop/CIMWin32Prov/cim-processor)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41093-396">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="41093-397">**Status**</span><span class="sxs-lookup"><span data-stu-id="41093-397">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-398">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41093-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41093-399">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-400">Der aktuelle Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="41093-400">The current status of the object.</span></span> <span data-ttu-id="41093-401">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="41093-401">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="41093-402">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="41093-402">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-403">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="41093-403">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="41093-404">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-405">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="41093-405">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="41093-406">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41093-406">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="41093-407">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="41093-407">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-408">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41093-408">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41093-409">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-410">Der aktuelle Zustand des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="41093-410">The current state of the logical device.</span></span> <span data-ttu-id="41093-411">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="41093-411">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="41093-412">**Schrittweises Ausführen**</span><span class="sxs-lookup"><span data-stu-id="41093-412">**Stepping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-413">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41093-413">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41093-414">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-415">Die Revisions Ebene des Prozessors in der Prozessorfamilie des zugrunde liegenden physischen Prozessors.</span><span class="sxs-lookup"><span data-stu-id="41093-415">The revision level of the processor within the processor family of the underlying physical processor.</span></span> <span data-ttu-id="41093-416">Diese Eigenschaft wird vom [**CIM- \_ Prozessor**](/windows/desktop/CIMWin32Prov/cim-processor)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41093-416">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="41093-417">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="41093-417">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-418">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41093-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41093-419">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41093-420">Qualifizierer: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="41093-420">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="41093-421">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="41093-421">The creation class name of the scoping system.</span></span> <span data-ttu-id="41093-422">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41093-422">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="41093-423">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="41093-423">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-424">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41093-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41093-425">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41093-426">Qualifizierer: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="41093-426">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="41093-427">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="41093-427">The name of the scoping system.</span></span> <span data-ttu-id="41093-428">Dieser Wert entspricht dem Wert der [**Name**](msvm-computersystem.md) -Eigenschaft der **MSVM \_ Computersystem** -Klasse für die Bereichs bezogene virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="41093-428">This value corresponds to the value of the [**Name**](msvm-computersystem.md) property of the **Msvm\_ComputerSystem** class for the scoping virtual machine.</span></span> <span data-ttu-id="41093-429">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41093-429">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="41093-430">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="41093-430">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-431">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="41093-431">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="41093-432">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-433">Das Datum oder die Uhrzeit der Änderung des Status der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="41093-433">The date or time at which the virtual machine's state was changed.</span></span> <span data-ttu-id="41093-434">Wenn der Zustand des Elements nicht geändert wurde und diese Eigenschaft aufgefüllt ist, muss Sie auf einen Wert von 0 Intervall festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="41093-434">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="41093-435">Wenn eine Zustandsänderung angefordert, aber abgelehnt oder noch nicht verarbeitet wurde, darf die Eigenschaft nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="41093-435">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="41093-436">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="41093-436">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="41093-437">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="41093-437">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-438">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="41093-438">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="41093-439">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-440">Die Gesamtanzahl der Stunden, für die dieses Gerät eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="41093-440">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="41093-441">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="41093-441">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="41093-442">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="41093-442">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-443">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41093-443">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41093-444">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-444">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-445">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="41093-445">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="41093-446">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="41093-446">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="41093-447">**UniqueId**</span><span class="sxs-lookup"><span data-stu-id="41093-447">**UniqueID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-448">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41093-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41093-449">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-450">Eine Globally Unique Identifier für den Prozessor.</span><span class="sxs-lookup"><span data-stu-id="41093-450">A globally unique identifier for the processor.</span></span> <span data-ttu-id="41093-451">Dieser Bezeichner kann nur innerhalb einer Prozessorfamilie eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="41093-451">This identifier can only be unique within a processor family.</span></span> <span data-ttu-id="41093-452">Diese Eigenschaft wird vom [**CIM- \_ Prozessor**](/windows/desktop/CIMWin32Prov/cim-processor)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="41093-452">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="41093-453">**Upgrademethod**</span><span class="sxs-lookup"><span data-stu-id="41093-453">**UpgradeMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41093-454">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41093-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41093-455">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41093-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41093-456">Die CPU-Socketinformationen, die Daten zum Upgrade des Prozessors enthalten (wenn Upgrades unterstützt werden).</span><span class="sxs-lookup"><span data-stu-id="41093-456">The CPU socket information, which includes data on how to upgrade the processor (if upgrades are supported).</span></span> <span data-ttu-id="41093-457">Diese Eigenschaft wird vom [**CIM- \_ Prozessor**](/windows/desktop/CIMWin32Prov/cim-processor)geerbt.</span><span class="sxs-lookup"><span data-stu-id="41093-457">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41093-458">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41093-458">Remarks</span></span>

<span data-ttu-id="41093-459">Der Zugriff auf die **MSVM- \_ Prozessor** Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="41093-459">Access to the **Msvm\_Processor** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="41093-460">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="41093-460">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="41093-461">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41093-461">Requirements</span></span>



| <span data-ttu-id="41093-462">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41093-462">Requirement</span></span> | <span data-ttu-id="41093-463">Wert</span><span class="sxs-lookup"><span data-stu-id="41093-463">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41093-464">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="41093-464">Minimum supported client</span></span><br/> | <span data-ttu-id="41093-465">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="41093-465">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="41093-466">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="41093-466">Minimum supported server</span></span><br/> | <span data-ttu-id="41093-467">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="41093-467">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="41093-468">Namespace</span><span class="sxs-lookup"><span data-stu-id="41093-468">Namespace</span></span><br/>                | <span data-ttu-id="41093-469">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="41093-469">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="41093-470">MOF</span><span class="sxs-lookup"><span data-stu-id="41093-470">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41093-471"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="41093-471"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="41093-472">DLL</span><span class="sxs-lookup"><span data-stu-id="41093-472">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41093-473"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="41093-473"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="41093-474">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41093-474">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41093-475">**CIM- \_ Prozessor**</span><span class="sxs-lookup"><span data-stu-id="41093-475">**CIM\_Processor**</span></span>](cim-processor.md)
</dt> <dt>

[<span data-ttu-id="41093-476">**CIM- \_ Prozessor**</span><span class="sxs-lookup"><span data-stu-id="41093-476">**CIM\_Processor**</span></span>](/windows/desktop/CIMWin32Prov/cim-processor)
</dt> <dt>

[<span data-ttu-id="41093-477">Prozessor Klassen</span><span class="sxs-lookup"><span data-stu-id="41093-477">Processor Classes</span></span>](processor-classes.md)
</dt> </dl>

 

