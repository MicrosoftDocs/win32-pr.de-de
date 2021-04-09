---
description: Stellt einen seriellen Anschluss dar, der dem seriellen Controller zugeordnet ist.
ms.assetid: 856823A5-7481-453A-8476-1CDAB1D84123
title: Msvm_SerialPort-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialPort
- Msvm_SerialPort.SetPowerState
- Msvm_SerialPort.EnableDevice
- Msvm_SerialPort.OnlineDevice
- Msvm_SerialPort.QuiesceDevice
- Msvm_SerialPort.SaveProperties
- Msvm_SerialPort.RestoreProperties
- Msvm_SerialPort.InstanceID
- Msvm_SerialPort.Caption
- Msvm_SerialPort.Description
- Msvm_SerialPort.ElementName
- Msvm_SerialPort.InstallDate
- Msvm_SerialPort.Name
- Msvm_SerialPort.OperationalStatus
- Msvm_SerialPort.StatusDescriptions
- Msvm_SerialPort.Status
- Msvm_SerialPort.HealthState
- Msvm_SerialPort.CommunicationStatus
- Msvm_SerialPort.DetailedStatus
- Msvm_SerialPort.OperatingStatus
- Msvm_SerialPort.PrimaryStatus
- Msvm_SerialPort.EnabledState
- Msvm_SerialPort.OtherEnabledState
- Msvm_SerialPort.RequestedState
- Msvm_SerialPort.EnabledDefault
- Msvm_SerialPort.TimeOfLastStateChange
- Msvm_SerialPort.AvailableRequestedStates
- Msvm_SerialPort.TransitioningToState
- Msvm_SerialPort.SystemCreationClassName
- Msvm_SerialPort.SystemName
- Msvm_SerialPort.CreationClassName
- Msvm_SerialPort.DeviceID
- Msvm_SerialPort.PowerManagementSupported
- Msvm_SerialPort.PowerManagementCapabilities
- Msvm_SerialPort.Availability
- Msvm_SerialPort.StatusInfo
- Msvm_SerialPort.LastErrorCode
- Msvm_SerialPort.ErrorDescription
- Msvm_SerialPort.ErrorCleared
- Msvm_SerialPort.OtherIdentifyingInfo
- Msvm_SerialPort.PowerOnHours
- Msvm_SerialPort.TotalPowerOnHours
- Msvm_SerialPort.IdentifyingDescriptions
- Msvm_SerialPort.AdditionalAvailability
- Msvm_SerialPort.MaxQuiesceTime
- Msvm_SerialPort.Speed
- Msvm_SerialPort.MaxSpeed
- Msvm_SerialPort.RequestedSpeed
- Msvm_SerialPort.UsageRestriction
- Msvm_SerialPort.PortType
- Msvm_SerialPort.OtherPortType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bc9ff5e1ce4b0a750866a9957c0cffc4bc8501e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865515"
---
# <a name="msvm_serialport-class"></a><span data-ttu-id="cb9a7-103">MSVM- \_ SerialPort-Klasse</span><span class="sxs-lookup"><span data-stu-id="cb9a7-103">Msvm\_SerialPort class</span></span>

<span data-ttu-id="cb9a7-104">Stellt einen seriellen Anschluss dar, der dem seriellen Controller zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-104">Represents a serial port associated with the serial controller.</span></span>

<span data-ttu-id="cb9a7-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb9a7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb9a7-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialPort : CIM_LogicalPort
{
  string   InstanceID;
  string   Caption;
  string   Description = "Microsoft Virtual Serial Port";
  string   ElementName;
  datetime InstallDate;
  string   Name;
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
  string   CreationClassName = "Msvm_SerialPort";
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
  uint64   Speed = 115200;
  uint32   MaxSpeed = 115200;
  uint64   RequestedSpeed = 115200;
  uint16   UsageRestriction = 4;
  uint16   PortType = 1;
  string   OtherPortType = "Serial Port";
};
```

## <a name="members"></a><span data-ttu-id="cb9a7-107">Member</span><span class="sxs-lookup"><span data-stu-id="cb9a7-107">Members</span></span>

<span data-ttu-id="cb9a7-108">Die **MSVM- \_ SerialPort** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="cb9a7-108">The **Msvm\_SerialPort** class has these types of members:</span></span>

-   [<span data-ttu-id="cb9a7-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="cb9a7-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="cb9a7-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cb9a7-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cb9a7-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="cb9a7-111">Methods</span></span>

<span data-ttu-id="cb9a7-112">Die **MSVM- \_ SerialPort** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-112">The **Msvm\_SerialPort** class has these methods.</span></span>



| <span data-ttu-id="cb9a7-113">Methode</span><span class="sxs-lookup"><span data-stu-id="cb9a7-113">Method</span></span>                                                           | <span data-ttu-id="cb9a7-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cb9a7-114">Description</span></span>                              |
|:-----------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="cb9a7-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-115">**EnableDevice**</span></span>                                                 | <span data-ttu-id="cb9a7-116">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="cb9a7-117">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-117">**OnlineDevice**</span></span>                                                 | <span data-ttu-id="cb9a7-118">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="cb9a7-119">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-119">**QuiesceDevice**</span></span>                                                | <span data-ttu-id="cb9a7-120">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="cb9a7-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-121">**RequestStateChange**</span></span>](msvm-serialport-requeststatechange.md) | <span data-ttu-id="cb9a7-122">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="cb9a7-123">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-123">**Reset**</span></span>](msvm-serialport-reset.md)                           | <span data-ttu-id="cb9a7-124">Setzt das virtuelle Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="cb9a7-125">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-125">**RestoreProperties**</span></span>                                            | <span data-ttu-id="cb9a7-126">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="cb9a7-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-127">**SaveProperties**</span></span>                                               | <span data-ttu-id="cb9a7-128">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="cb9a7-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-129">**SetPowerState**</span></span>                                                | <span data-ttu-id="cb9a7-130">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="cb9a7-131">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cb9a7-131">Properties</span></span>

<span data-ttu-id="cb9a7-132">Die **MSVM- \_ SerialPort** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-132">The **Msvm\_SerialPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cb9a7-133">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-134">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="cb9a7-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-136">Alle zusätzlichen Verfügbarkeit und der Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="cb9a7-137">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="cb9a7-138">Wert</span><span class="sxs-lookup"><span data-stu-id="cb9a7-138">Value</span></span>                                                                            | <span data-ttu-id="cb9a7-139">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cb9a7-139">Meaning</span></span>                   |
|----------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="cb9a7-140"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="cb9a7-140"><dt>{ 6 }</dt></span></span> </dl> |                           |
| <dl> <span data-ttu-id="cb9a7-141"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="cb9a7-141"><dt>6</dt></span></span> </dl>     | <span data-ttu-id="cb9a7-142">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="cb9a7-142">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cb9a7-143">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-144">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-146">Die primäre Verfügbarkeit und den Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-146">The primary availability and status of the device.</span></span> <span data-ttu-id="cb9a7-147">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-147">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="cb9a7-148">Wert</span><span class="sxs-lookup"><span data-stu-id="cb9a7-148">Value</span></span>                                                                        | <span data-ttu-id="cb9a7-149">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cb9a7-149">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="cb9a7-150"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="cb9a7-150"><dt>6</dt></span></span> </dl> | <span data-ttu-id="cb9a7-151">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="cb9a7-151">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cb9a7-152">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-152">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-153">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="cb9a7-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-155">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-155">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="cb9a7-156">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-156">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cb9a7-157">**Caption**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-157">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-158">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-160">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-160">A short description of the object.</span></span> <span data-ttu-id="cb9a7-161">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="cb9a7-162">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-162">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-163">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-165">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-165">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="cb9a7-166">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-166">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="cb9a7-167">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="cb9a7-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-169"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-169"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-170"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-170"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-171"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-171"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-172"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-172"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-173"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-173"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-174"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="cb9a7-174"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="cb9a7-175">)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-175">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cb9a7-176">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-176">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-179">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-179">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="cb9a7-180">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-180">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="cb9a7-181">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-181">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-182">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-184">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-184">A description of the object.</span></span> <span data-ttu-id="cb9a7-185">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="cb9a7-186">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-186">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-187">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-189">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-189">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="cb9a7-190">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-190">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="cb9a7-191">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="cb9a7-192"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-192"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-193"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-193"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-194"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-194"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-195"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-195"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-196"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-196"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-197"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-197"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-199"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="cb9a7-199"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="cb9a7-200">)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-200">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cb9a7-201">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-201">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-202">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-204">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und auf "Microsoft:*GUID* \\ *Device-Specific-Data*" festgelegt, wobei *gerätespezifische Daten* optional sind.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-204">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*", where *device-specific-data* is optional.</span></span>

</dd> <dt>

<span data-ttu-id="cb9a7-205">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-205">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-206">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-207">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-208">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-208">A display name for the object.</span></span> <span data-ttu-id="cb9a7-209">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-209">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="cb9a7-210">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-210">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-211">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-212">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-213">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-213">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="cb9a7-214">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-214">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="cb9a7-215">Wert</span><span class="sxs-lookup"><span data-stu-id="cb9a7-215">Value</span></span>                                                                        | <span data-ttu-id="cb9a7-216">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cb9a7-216">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="cb9a7-217"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="cb9a7-217"><dt>2</dt></span></span> </dl> | <span data-ttu-id="cb9a7-218">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="cb9a7-218">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cb9a7-219">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-219">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-220">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-221">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-222">Der aktivierte Status des Elements.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-222">The enabled state of the element.</span></span> <span data-ttu-id="cb9a7-223">Sie kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-223">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="cb9a7-224">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-224">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="cb9a7-225">Wert</span><span class="sxs-lookup"><span data-stu-id="cb9a7-225">Value</span></span>                                                                        | <span data-ttu-id="cb9a7-226">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cb9a7-226">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="cb9a7-227"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="cb9a7-227"><dt>5</dt></span></span> </dl> | <span data-ttu-id="cb9a7-228">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="cb9a7-228">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cb9a7-229">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-229">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-230">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="cb9a7-230">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-231">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-232">Gibt an, ob der in der **LastErrorCode** -Eigenschaft gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-232">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="cb9a7-233">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-233">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cb9a7-234">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-234">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-235">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-236">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-237">Eine Zeichenfolge, die weitere Informationen über den in der **LastErrorCode** -Eigenschaft aufgezeichneten Fehler sowie Informationen zu ggf. durchzuführenden Maßnahmen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-237">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="cb9a7-238">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-238">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cb9a7-239">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-239">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-240">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-240">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-241">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-242">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-242">The current health of the element.</span></span> <span data-ttu-id="cb9a7-243">Dadurch wird die Integrität dieses Elements, jedoch nicht notwendigerweise der seiner unter Komponenten ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-243">This expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="cb9a7-244">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-244">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="cb9a7-245">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="cb9a7-246">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-246">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-247">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="cb9a7-247">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-248">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-249">Ein Array von Freiform-Zeichen folgen, die Erklärungen und Details hinter den Einträgen im Eigenschafts Array " **OtherIdentifyingInfo** " bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-249">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="cb9a7-250">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="cb9a7-251">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-251">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-252">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-252">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-253">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-254">Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-254">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="cb9a7-255">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-255">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="cb9a7-256">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-256">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-257">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-258">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-259">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-259">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-260">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-260">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="cb9a7-261">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-261">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="cb9a7-262">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-262">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-263">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-263">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-264">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-265">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-265">The last error code reported by the logical device.</span></span> <span data-ttu-id="cb9a7-266">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-266">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cb9a7-267">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-267">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-268">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-268">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-269">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-270">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-270">This property has been deprecated.</span></span> <span data-ttu-id="cb9a7-271">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-271">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="cb9a7-272">**MAXSPEED**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-272">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-273">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-274">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-275">Die maximale Bandbreite des Ports (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="cb9a7-275">The maximum bandwidth of the port, in bits-per-second.</span></span> <span data-ttu-id="cb9a7-276">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-276">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="cb9a7-277">**Name**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-277">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-278">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-279">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-280">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-280">The label by which the object is known.</span></span> <span data-ttu-id="cb9a7-281">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und entspricht der Element **Name** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-281">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="cb9a7-282">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-282">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-283">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-284">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-285">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-285">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="cb9a7-286">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-286">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="cb9a7-287">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-287">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="cb9a7-288"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-288"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-289"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-289"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-290"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-290"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-291"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-291"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-292"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="cb9a7-292"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-293"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-293"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-294"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-294"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-295"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-295"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-296"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-296"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-297"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-297"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-298"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-298"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-299"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-299"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-300"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-300"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-301"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-301"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-302"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-302"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-303"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-303"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-304"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-304"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-305"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-305"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-306"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="cb9a7-306"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="cb9a7-307">)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-307">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cb9a7-308">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-308">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-309">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="cb9a7-309">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-310">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-311">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-311">The current statuses of the object.</span></span> <span data-ttu-id="cb9a7-312">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="cb9a7-313">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-313">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-314">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-315">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-316">Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-316">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="cb9a7-317">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-317">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="cb9a7-318">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-318">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="cb9a7-319">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-319">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-320">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="cb9a7-320">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-321">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-322">Alle zusätzlichen Daten über Geräte-ID-Informationen, die zur Identifizierung eines logischen Geräts verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-322">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="cb9a7-323">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-323">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="cb9a7-324">**Otherporttype**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-324">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-325">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-326">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-327">Der Modultyp, wenn **portType** auf 1 (Other) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-327">The type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="cb9a7-328">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-328">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="cb9a7-329">**PortType**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-329">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-330">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-330">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-331">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-332">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-332">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>



| <span data-ttu-id="cb9a7-333">Wert</span><span class="sxs-lookup"><span data-stu-id="cb9a7-333">Value</span></span>                                                                        | <span data-ttu-id="cb9a7-334">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cb9a7-334">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="cb9a7-335"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="cb9a7-335"><dt>1</dt></span></span> </dl> | <span data-ttu-id="cb9a7-336">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="cb9a7-336">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cb9a7-337">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-337">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-338">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="cb9a7-338">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-339">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-340">Die Energie Verwaltungsfunktionen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-340">The power management capabilities of the device.</span></span> <span data-ttu-id="cb9a7-341">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-341">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cb9a7-342">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-342">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-343">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="cb9a7-343">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-344">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-345">Gibt an, ob das Gerät Energie gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-345">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="cb9a7-346">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-346">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cb9a7-347">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-347">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-348">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-348">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-349">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-350">Gibt an, wie viele aufeinanderfolgende Stunden dieses Gerät seit dem letzten Strom Umgebung eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-350">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="cb9a7-351">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-351">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cb9a7-352">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-352">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-353">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-353">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-354">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-355">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-355">Provides high level status information.</span></span> <span data-ttu-id="cb9a7-356">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-356">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="cb9a7-357">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-357">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="cb9a7-358">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-358">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="cb9a7-359"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-359"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-360"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-360"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-361"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="cb9a7-361"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-362"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-362"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-363"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-363"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-364"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="cb9a7-364"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="cb9a7-365">)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-365">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cb9a7-366">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-366">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-367">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-367">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-368">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-369">Die angeforderte Bandbreite des Ports (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="cb9a7-369">The requested bandwidth of the port, in bits-per-second.</span></span> <span data-ttu-id="cb9a7-370">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-370">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="cb9a7-371">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-371">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-372">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-372">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-373">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-374">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-374">The last requested or desired state for the element.</span></span> <span data-ttu-id="cb9a7-375">Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-375">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="cb9a7-376">Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuell aktivierten oder deaktivierten Zustände zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-376">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="cb9a7-377">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-377">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="cb9a7-378">Wert</span><span class="sxs-lookup"><span data-stu-id="cb9a7-378">Value</span></span>                                                                         | <span data-ttu-id="cb9a7-379">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cb9a7-379">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="cb9a7-380"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="cb9a7-380"><dt>12</dt></span></span> </dl> | <span data-ttu-id="cb9a7-381">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="cb9a7-381">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cb9a7-382">**Geschwindigkeit**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-382">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-383">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-383">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-384">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-385">Die Bandbreite des Ports (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="cb9a7-385">The bandwidth of the port, in bits-per-second.</span></span> <span data-ttu-id="cb9a7-386">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-386">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="cb9a7-387">**Status**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-387">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-388">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-389">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-390">Der aktuelle Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-390">The current status of the object.</span></span> <span data-ttu-id="cb9a7-391">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-391">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cb9a7-392">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-392">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-393">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="cb9a7-393">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-394">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-395">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-395">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="cb9a7-396">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-396">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="cb9a7-397">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-397">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-398">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-399">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-400">Der aktuelle Zustand des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-400">The current state of the logical device.</span></span> <span data-ttu-id="cb9a7-401">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-401">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cb9a7-402">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-402">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-403">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-404">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-405">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-405">The scoping system's creation class name.</span></span> <span data-ttu-id="cb9a7-406">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-406">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="cb9a7-407">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-407">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-408">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-409">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-410">Der eindeutige Bezeichner für die Bereichs bezogene virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-410">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="cb9a7-411">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-411">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="cb9a7-412">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-412">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-413">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-413">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-414">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-415">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-415">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="cb9a7-416">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-416">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="cb9a7-417">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-417">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-418">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-418">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-419">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-420">Die Gesamtanzahl der Stunden, für die dieses Gerät eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-420">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="cb9a7-421">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-421">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cb9a7-422">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-422">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-423">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-423">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-424">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-424">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-425">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-425">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="cb9a7-426">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-426">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cb9a7-427">**Einsatz Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-427">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb9a7-428">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-428">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cb9a7-429">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb9a7-430">Unter bestimmten Umständen kann ein logischer Port als Front-End-oder Back-End-Port identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-430">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="cb9a7-431">Ein Beispiel für diese Situation wäre ein Speicher Array, das Back-End-Ports für die Kommunikation mit Datenträgern und Front-End-Ports für die Kommunikation mit Hosts aufweisen könnte.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-431">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="cb9a7-432">Wenn keine Einschränkung für die Verwendung des Ports vorliegt, sollte der Wert auf 4 (nicht eingeschränkt) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-432">If there is no restriction on the use of the port, then the value should be set to 4 (Not Restricted).</span></span> <span data-ttu-id="cb9a7-433">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-433">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>



| <span data-ttu-id="cb9a7-434">Wert</span><span class="sxs-lookup"><span data-stu-id="cb9a7-434">Value</span></span>                                                                        | <span data-ttu-id="cb9a7-435">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cb9a7-435">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="cb9a7-436"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="cb9a7-436"><dt>4</dt></span></span> </dl> | <span data-ttu-id="cb9a7-437">Nicht eingeschränkt</span><span class="sxs-lookup"><span data-stu-id="cb9a7-437">Not Restricted</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cb9a7-438">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cb9a7-438">Remarks</span></span>

<span data-ttu-id="cb9a7-439">Der Zugriff auf die **MSVM- \_ SerialPort** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="cb9a7-439">Access to the **Msvm\_SerialPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="cb9a7-440">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="cb9a7-440">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="cb9a7-441">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb9a7-441">Requirements</span></span>



| <span data-ttu-id="cb9a7-442">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cb9a7-442">Requirement</span></span> | <span data-ttu-id="cb9a7-443">Wert</span><span class="sxs-lookup"><span data-stu-id="cb9a7-443">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb9a7-444">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-444">Minimum supported client</span></span><br/> | <span data-ttu-id="cb9a7-445">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb9a7-445">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cb9a7-446">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cb9a7-446">Minimum supported server</span></span><br/> | <span data-ttu-id="cb9a7-447">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb9a7-447">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cb9a7-448">Namespace</span><span class="sxs-lookup"><span data-stu-id="cb9a7-448">Namespace</span></span><br/>                | <span data-ttu-id="cb9a7-449">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="cb9a7-449">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cb9a7-450">MOF</span><span class="sxs-lookup"><span data-stu-id="cb9a7-450">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb9a7-451"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cb9a7-451"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cb9a7-452">DLL</span><span class="sxs-lookup"><span data-stu-id="cb9a7-452">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb9a7-453"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cb9a7-453"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cb9a7-454">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb9a7-454">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb9a7-455">**CIM \_ logicalport**</span><span class="sxs-lookup"><span data-stu-id="cb9a7-455">**CIM\_LogicalPort**</span></span>](cim-logicalport.md)
</dt> <dt>

<span data-ttu-id="cb9a7-456">[**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cb9a7-456">[**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="cb9a7-457">Serielle Geräteklassen</span><span class="sxs-lookup"><span data-stu-id="cb9a7-457">Serial Devices Classes</span></span>](serial-devices-classes.md)
</dt> </dl>

 

