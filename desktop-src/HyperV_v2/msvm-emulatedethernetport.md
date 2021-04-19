---
description: Stellt einen emulierten Ethernet-Adapter dar.
ms.assetid: 8E990C76-7D48-42B0-BB4D-C4C07B1C482A
title: Msvm_EmulatedEthernetPort-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EmulatedEthernetPort
- Msvm_EmulatedEthernetPort.SetPowerState
- Msvm_EmulatedEthernetPort.EnableDevice
- Msvm_EmulatedEthernetPort.OnlineDevice
- Msvm_EmulatedEthernetPort.QuiesceDevice
- Msvm_EmulatedEthernetPort.SaveProperties
- Msvm_EmulatedEthernetPort.RestoreProperties
- Msvm_EmulatedEthernetPort.InstanceID
- Msvm_EmulatedEthernetPort.Caption
- Msvm_EmulatedEthernetPort.Description
- Msvm_EmulatedEthernetPort.ElementName
- Msvm_EmulatedEthernetPort.InstallDate
- Msvm_EmulatedEthernetPort.Name
- Msvm_EmulatedEthernetPort.OperationalStatus
- Msvm_EmulatedEthernetPort.StatusDescriptions
- Msvm_EmulatedEthernetPort.Status
- Msvm_EmulatedEthernetPort.HealthState
- Msvm_EmulatedEthernetPort.CommunicationStatus
- Msvm_EmulatedEthernetPort.DetailedStatus
- Msvm_EmulatedEthernetPort.OperatingStatus
- Msvm_EmulatedEthernetPort.PrimaryStatus
- Msvm_EmulatedEthernetPort.EnabledState
- Msvm_EmulatedEthernetPort.OtherEnabledState
- Msvm_EmulatedEthernetPort.RequestedState
- Msvm_EmulatedEthernetPort.EnabledDefault
- Msvm_EmulatedEthernetPort.TimeOfLastStateChange
- Msvm_EmulatedEthernetPort.AvailableRequestedStates
- Msvm_EmulatedEthernetPort.TransitioningToState
- Msvm_EmulatedEthernetPort.SystemCreationClassName
- Msvm_EmulatedEthernetPort.SystemName
- Msvm_EmulatedEthernetPort.CreationClassName
- Msvm_EmulatedEthernetPort.DeviceID
- Msvm_EmulatedEthernetPort.PowerManagementSupported
- Msvm_EmulatedEthernetPort.PowerManagementCapabilities
- Msvm_EmulatedEthernetPort.Availability
- Msvm_EmulatedEthernetPort.StatusInfo
- Msvm_EmulatedEthernetPort.LastErrorCode
- Msvm_EmulatedEthernetPort.ErrorDescription
- Msvm_EmulatedEthernetPort.ErrorCleared
- Msvm_EmulatedEthernetPort.OtherIdentifyingInfo
- Msvm_EmulatedEthernetPort.PowerOnHours
- Msvm_EmulatedEthernetPort.TotalPowerOnHours
- Msvm_EmulatedEthernetPort.IdentifyingDescriptions
- Msvm_EmulatedEthernetPort.AdditionalAvailability
- Msvm_EmulatedEthernetPort.MaxQuiesceTime
- Msvm_EmulatedEthernetPort.Speed
- Msvm_EmulatedEthernetPort.MaxSpeed
- Msvm_EmulatedEthernetPort.RequestedSpeed
- Msvm_EmulatedEthernetPort.UsageRestriction
- Msvm_EmulatedEthernetPort.PortType
- Msvm_EmulatedEthernetPort.OtherPortType
- Msvm_EmulatedEthernetPort.OtherNetworkPortType
- Msvm_EmulatedEthernetPort.PortNumber
- Msvm_EmulatedEthernetPort.LinkTechnology
- Msvm_EmulatedEthernetPort.OtherLinkTechnology
- Msvm_EmulatedEthernetPort.PermanentAddress
- Msvm_EmulatedEthernetPort.NetworkAddresses
- Msvm_EmulatedEthernetPort.FullDuplex
- Msvm_EmulatedEthernetPort.AutoSense
- Msvm_EmulatedEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_EmulatedEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_EmulatedEthernetPort.MaxDataSize
- Msvm_EmulatedEthernetPort.Capabilities
- Msvm_EmulatedEthernetPort.CapabilityDescriptions
- Msvm_EmulatedEthernetPort.EnabledCapabilities
- Msvm_EmulatedEthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1ec13ae369f6d5e3d884f74c96d7df27c2f5fa97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359963"
---
# <a name="msvm_emulatedethernetport-class"></a><span data-ttu-id="d2288-103">MSVM \_ emuatedethernetport-Klasse</span><span class="sxs-lookup"><span data-stu-id="d2288-103">Msvm\_EmulatedEthernetPort class</span></span>

<span data-ttu-id="d2288-104">Stellt einen emulierten Ethernet-Adapter dar.</span><span class="sxs-lookup"><span data-stu-id="d2288-104">Represents an emulated Ethernet adapter.</span></span> <span data-ttu-id="d2288-105">Dieser Adapter wird verwendet, wenn ein virtueller Computer nicht in der Lage ist, den synthetischen Ethernet-Port zu verwenden, wenn keine integrierten Verbindungen im Gast Betriebssystem installiert sind.</span><span class="sxs-lookup"><span data-stu-id="d2288-105">This adapter is used when a virtual machine is not capable of running the synthetic Ethernet port when no integrated circuits are installed in the guest.</span></span>

> [!Note]  
> <span data-ttu-id="d2288-106">Diese Klasse ist für virtuelle Maschinen der Generation 2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d2288-106">This class is not available to generation 2 virtual machines.</span></span>

 

<span data-ttu-id="d2288-107">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d2288-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2288-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2288-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EmulatedEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Port";
  string   Description = "Microsoft Emulated Ethernet Port";
  string   ElementName = "Legacy Network Adapter";
  datetime InstallDate;
  string   Name = "Ethernet Port";
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
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
  string   CreationClassName = "Msvm_EmulatedEthernetPort";
  string   DeviceID = "Microsoft:GUID\device-specific data";
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint16   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  uint64   Speed = 1000000000;
  uint64   MaxSpeed = 1000000000;
  uint64   RequestedSpeed = 1000000000;
  uint16   UsageRestriction = 4;
  uint16   PortType = 1;
  string   OtherPortType = "Virtual Ethernet";
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology = 2;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  string   NetworkAddresses[];
  boolean  FullDuplex = True;
  boolean  AutoSense = True;
  string   SupportedMaximumTransmissionUnit = 1500;
  uint64   ActiveMaximumTransmissionUnit = 1500;
  uint32   MaxDataSize = 1500;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  uint16   EnabledCapabilities[];
  string   OtherEnabledCapabilities[];
};
```

## <a name="members"></a><span data-ttu-id="d2288-109">Member</span><span class="sxs-lookup"><span data-stu-id="d2288-109">Members</span></span>

<span data-ttu-id="d2288-110">Die **MSVM- \_ emulatedethernetport** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d2288-110">The **Msvm\_EmulatedEthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="d2288-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="d2288-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="d2288-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d2288-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d2288-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="d2288-113">Methods</span></span>

<span data-ttu-id="d2288-114">Die **MSVM- \_ emulatedethernetport** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="d2288-114">The **Msvm\_EmulatedEthernetPort** class has these methods.</span></span>



| <span data-ttu-id="d2288-115">Methode</span><span class="sxs-lookup"><span data-stu-id="d2288-115">Method</span></span>                                                                     | <span data-ttu-id="d2288-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2288-116">Description</span></span>                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="d2288-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="d2288-117">**EnableDevice**</span></span>                                                           | <span data-ttu-id="d2288-118">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d2288-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d2288-119">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="d2288-119">**OnlineDevice**</span></span>                                                           | <span data-ttu-id="d2288-120">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d2288-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d2288-121">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="d2288-121">**QuiesceDevice**</span></span>                                                          | <span data-ttu-id="d2288-122">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d2288-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="d2288-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="d2288-123">**RequestStateChange**</span></span>](msvm-emulatedethernetport-requeststatechange.md) | <span data-ttu-id="d2288-124">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="d2288-124">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="d2288-125">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="d2288-125">**Reset**</span></span>](msvm-emulatedethernetport-reset.md)                           | <span data-ttu-id="d2288-126">Setzt das emulierten Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="d2288-126">Resets the emulated device.</span></span><br/>   |
| <span data-ttu-id="d2288-127">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="d2288-127">**RestoreProperties**</span></span>                                                      | <span data-ttu-id="d2288-128">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d2288-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d2288-129">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="d2288-129">**SaveProperties**</span></span>                                                         | <span data-ttu-id="d2288-130">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d2288-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d2288-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="d2288-131">**SetPowerState**</span></span>                                                          | <span data-ttu-id="d2288-132">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d2288-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d2288-133">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d2288-133">Properties</span></span>

<span data-ttu-id="d2288-134">Die **MSVM- \_ emulatedethernetport** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d2288-134">The **Msvm\_EmulatedEthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d2288-135">**Activemaximumtransmissionunit**</span><span class="sxs-lookup"><span data-stu-id="d2288-135">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-136">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d2288-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-138">Die aktive oder ausgehandelte maximale Übertragungseinheit (Maximum Transmission Unit, MTU), die unterstützt werden kann.</span><span class="sxs-lookup"><span data-stu-id="d2288-138">The active or negotiated maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="d2288-139">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt und ist immer auf 1500 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2288-139">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="d2288-140">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="d2288-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-141">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="d2288-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d2288-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-143">Alle zusätzlichen Verfügbarkeit und den Status des Geräts, außer den in der **Availability** -Eigenschaft angegebenen.</span><span class="sxs-lookup"><span data-stu-id="d2288-143">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="d2288-144">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf 6 ("nicht zutreffend") festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2288-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 ("Not Applicable").</span></span>

</dd> <dt>

<span data-ttu-id="d2288-145">**AutoSense**</span><span class="sxs-lookup"><span data-stu-id="d2288-145">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-146">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d2288-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-148">Gibt an, ob der Netzwerkport die Geschwindigkeit oder andere Kommunikationsmerkmale der angeschlossenen Netzwerk Medien automatisch bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="d2288-148">Indicates whether the network port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="d2288-149">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt und ist immer auf " **true**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2288-149">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="d2288-150">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="d2288-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-151">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2288-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-153">Die primäre Verfügbarkeit und den Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="d2288-153">The primary availability and status of the device.</span></span> <span data-ttu-id="d2288-154">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2288-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d2288-155">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="d2288-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-156">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="d2288-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d2288-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-158">Gibt die möglichen Werte für den *requestedstate* -Parameter der [**requestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) -Methode an, die zum Initiieren einer Zustandsänderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d2288-158">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="d2288-159">Bei den aufgelisteten Werten handelt es sich um eine Teilmenge der Werte in der **requestedstaatsupported** -Eigenschaft der zugeordneten Instanz von **CIM \_ enabledlogicalelementfunctions**, bei der die ausgewählten Werte eine Funktion des aktuellen Zustands des [**CIM- \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))sind.</span><span class="sxs-lookup"><span data-stu-id="d2288-159">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="d2288-160">Diese Eigenschaft darf nicht **null** sein, wenn eine Implementierung den Satz möglicher Werte als Funktion des aktuellen Zustands ankündigen kann.</span><span class="sxs-lookup"><span data-stu-id="d2288-160">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="d2288-161">Diese Eigenschaft ist **null** , wenn eine Implementierung den Satz möglicher Werte nicht als Funktion des aktuellen Zustands bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="d2288-161">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="d2288-162">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="d2288-162">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="d2288-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="d2288-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d2288-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="d2288-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d2288-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Herunter** fahren (4)</span><span class="sxs-lookup"><span data-stu-id="d2288-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d2288-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="d2288-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d2288-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="d2288-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="d2288-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>Zurück **stellen (8** )</span><span class="sxs-lookup"><span data-stu-id="d2288-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d2288-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Still **legung (9** )</span><span class="sxs-lookup"><span data-stu-id="d2288-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="d2288-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Neustart** (10)</span><span class="sxs-lookup"><span data-stu-id="d2288-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="d2288-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Zurücksetzen** (11)</span><span class="sxs-lookup"><span data-stu-id="d2288-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="d2288-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reserviert** (..</span><span class="sxs-lookup"><span data-stu-id="d2288-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="d2288-173">)</span><span class="sxs-lookup"><span data-stu-id="d2288-173">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d2288-174">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="d2288-174">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-175">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="d2288-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d2288-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-177">Funktionen des Ethernet-Ports.</span><span class="sxs-lookup"><span data-stu-id="d2288-177">Capabilities of the Ethernet port.</span></span> <span data-ttu-id="d2288-178">Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2288-178">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2288-179">**Capabilitybeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="d2288-179">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-180">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="d2288-180">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d2288-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-182">Ein Array von Freiform-Zeichen folgen, das Ausführlichere Erläuterungen zu allen Ethernet-Port Features bereitstellt **, die im Funktions Array angegeben** sind.</span><span class="sxs-lookup"><span data-stu-id="d2288-182">An array of free-form strings that provides more detailed explanations for any of the Ethernet port features that are indicated in the **Capabilities** array.</span></span> <span data-ttu-id="d2288-183">Beachten Sie, dass jeder Eintrag dieses Arrays mit dem Eintrag im **Funktions Array verknüpft ist, der sich** am selben Index befindet.</span><span class="sxs-lookup"><span data-stu-id="d2288-183">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span> <span data-ttu-id="d2288-184">Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2288-184">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2288-185">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d2288-185">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-186">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2288-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-188">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="d2288-188">A short description of the object.</span></span> <span data-ttu-id="d2288-189">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ethernet-Port" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2288-189">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="d2288-190">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="d2288-190">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-191">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2288-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-193">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="d2288-193">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="d2288-194">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="d2288-194">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d2288-195">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d2288-195">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2288-196">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="d2288-196">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-197">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2288-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-199">Der Name der Klasse oder der Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d2288-199">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="d2288-200">Wenn diese Eigenschaft mit den anderen Schlüsseleigenschaften dieser Klasse verwendet wird, können alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="d2288-200">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="d2288-201">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf "MSVM \_ emuatedethernetport" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2288-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_EmulatedEthernetPort".</span></span>

</dd> <dt>

<span data-ttu-id="d2288-202">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d2288-202">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-203">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2288-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-205">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="d2288-205">A description of the object.</span></span> <span data-ttu-id="d2288-206">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Microsoft emulierten Ethernet-Port" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2288-206">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Emulated Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="d2288-207">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="d2288-207">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-208">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2288-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-210">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="d2288-210">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="d2288-211">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="d2288-211">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d2288-212">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d2288-212">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2288-213">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="d2288-213">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-214">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2288-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-215">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-216">Eine Adresse oder andere identifizierende Informationen, die verwendet werden, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="d2288-216">An address or other identifying information used to uniquely name the logical device.</span></span> <span data-ttu-id="d2288-217">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf "Microsoft:*GUID* \\ *gerätespezifische Daten*" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2288-217">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*\\*device-specific data*".</span></span>

</dd> <dt>

<span data-ttu-id="d2288-218">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d2288-218">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-219">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2288-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-220">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-221">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d2288-221">A display name for the object.</span></span> <span data-ttu-id="d2288-222">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Legacy-Netzwerk Adapter" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2288-222">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Legacy Network Adapter".</span></span>

</dd> <dt>

<span data-ttu-id="d2288-223">**Enabled-Funktionen**</span><span class="sxs-lookup"><span data-stu-id="d2288-223">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-224">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="d2288-224">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d2288-225">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-226">Die Funktionen, die in der Liste aller unterstützten Funktionen aktiviert sind **, die im Funktions Array definiert** sind.</span><span class="sxs-lookup"><span data-stu-id="d2288-226">The capabilities that are enabled from the list of all supported ones, which are defined in the **Capabilities** array.</span></span> <span data-ttu-id="d2288-227">Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2288-227">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2288-228">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="d2288-228">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-229">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2288-229">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-230">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-231">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="d2288-231">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="d2288-232">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) geerbt und ist immer auf 2 ("aktiviert") festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2288-232">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is always set to 2 ("Enabled").</span></span>

</dd> <dt>

<span data-ttu-id="d2288-233">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="d2288-233">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-234">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2288-234">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-235">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-236">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="d2288-236">The enabled and disabled states of an element.</span></span> <span data-ttu-id="d2288-237">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 5 ("nicht zutreffend") festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2288-237">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 ("Not Applicable").</span></span>

</dd> <dt>

<span data-ttu-id="d2288-238">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="d2288-238">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-239">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d2288-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-240">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-241">Gibt an, ob der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="d2288-241">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="d2288-242">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2288-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2288-243">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="d2288-243">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-244">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2288-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-245">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-246">Eine Zeichenfolge, die weitere Informationen über den Fehler enthält, der in **LastErrorCode** aufgezeichnet wurde, sowie Informationen zu den Maßnahmen, die ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="d2288-246">A string that provides more information about the error recorded in **LastErrorCode**, and information on any corrective actions that can be taken.</span></span> <span data-ttu-id="d2288-247">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2288-247">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2288-248">**Vollduplex**</span><span class="sxs-lookup"><span data-stu-id="d2288-248">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-249">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d2288-249">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-250">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-251">Gibt an, ob der Port im Vollduplex Modus betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="d2288-251">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="d2288-252">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt und ist immer auf " **true**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2288-252">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="d2288-253">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="d2288-253">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-254">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2288-254">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-255">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-256">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="d2288-256">The current health of the element.</span></span> <span data-ttu-id="d2288-257">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="d2288-257">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="d2288-258">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 5 ("OK") festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2288-258">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 ("OK").</span></span>

</dd> <dt>

<span data-ttu-id="d2288-259">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d2288-259">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-260">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="d2288-260">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d2288-261">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-262">Ein Array von Freiform-Zeichen folgen, die Erklärungen und Details hinter den Einträgen im " **OtherIdentifyingInfo** "-Array bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d2288-262">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="d2288-263">Jeder Eintrag dieses Arrays bezieht sich auf den Eintrag in " **OtherIdentifyingInfo** ", der sich im gleichen Index befindet.</span><span class="sxs-lookup"><span data-stu-id="d2288-263">Each entry of this array is related to the entry in **OtherIdentifyingInfo** that is located at the same index.</span></span> <span data-ttu-id="d2288-264">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2288-264">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2288-265">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d2288-265">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-266">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="d2288-266">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-267">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-268">Ein **DateTime** -Wert, der angibt, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d2288-268">A **datetime** value that indicates when the object was installed.</span></span> <span data-ttu-id="d2288-269">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d2288-269">Lack of a value does not indicate that the object is not installed.</span></span> <span data-ttu-id="d2288-270">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d2288-270">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2288-271">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d2288-271">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-272">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2288-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-273">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2288-274">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="d2288-274">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d2288-275">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="d2288-275">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d2288-276">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d2288-276">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2288-277">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d2288-277">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-278">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d2288-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-279">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-280">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="d2288-280">The last error code reported by the logical device.</span></span> <span data-ttu-id="d2288-281">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2288-281">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2288-282">**Linktechnology**</span><span class="sxs-lookup"><span data-stu-id="d2288-282">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-283">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2288-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-284">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-285">Die Linktypen.</span><span class="sxs-lookup"><span data-stu-id="d2288-285">The types of links.</span></span> <span data-ttu-id="d2288-286">Wenn der Wert auf 1 ("Other") festgelegt ist, enthält die zugehörige Eigenschaft **otherlinktechnology** eine Zeichen folgen Beschreibung des linktyps.</span><span class="sxs-lookup"><span data-stu-id="d2288-286">When set to 1 ("Other"), the related property **OtherLinkTechnology** contains a string description of the type of link.</span></span> <span data-ttu-id="d2288-287">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) geerbt und ist immer auf 2 ("Ethernet") festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2288-287">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) and is always set to 2 ("Ethernet").</span></span>

</dd> <dt>

<span data-ttu-id="d2288-288">**Maxdatasize**</span><span class="sxs-lookup"><span data-stu-id="d2288-288">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-289">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d2288-289">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-290">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-291">Die maximale Größe des Felds Info (nicht-Mac), das empfangen oder übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="d2288-291">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="d2288-292">Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)geerbt und ist immer auf 1500 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2288-292">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="d2288-293">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="d2288-293">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-294">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d2288-294">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-295">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-296">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2288-296">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2288-297">**MAXSPEED**</span><span class="sxs-lookup"><span data-stu-id="d2288-297">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-298">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d2288-298">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-299">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-300">Die maximale Bandbreite des Ports (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="d2288-300">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="d2288-301">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt und ist immer auf 1 Milliarde festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2288-301">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)), and it is always set to 1000000000.</span></span>

</dd> <dt>

<span data-ttu-id="d2288-302">**Name**</span><span class="sxs-lookup"><span data-stu-id="d2288-302">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-303">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2288-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-304">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-305">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="d2288-305">The label by which the object is known.</span></span> <span data-ttu-id="d2288-306">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="d2288-306">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="d2288-307">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf "Ethernet-Port" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2288-307">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="d2288-308">**"Networkaddresses"**</span><span class="sxs-lookup"><span data-stu-id="d2288-308">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-309">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="d2288-309">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d2288-310">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-311">Die Ethernet/802.3-Mac-Adressen, die als zwölf hexadezimal Ziffern (z. b. "010203040506") formatiert sind, wobei jedes Paar eines der sechs Oktette der Mac-Adresse in der kanonischen bidirektionalen Reihenfolge darstellt (das Gruppen Adressbit befindet sich im niedrig wertigen Bit des ersten Zeichens der Zeichenfolge).</span><span class="sxs-lookup"><span data-stu-id="d2288-311">The Ethernet/802.3 MAC addresses, formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order (the group address bit is found in the low order bit of the first character of the string).</span></span> <span data-ttu-id="d2288-312">Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2288-312">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2288-313">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="d2288-313">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-314">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2288-314">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-315">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-316">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d2288-316">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="d2288-317">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="d2288-317">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d2288-318">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d2288-318">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2288-319">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="d2288-319">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-320">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="d2288-320">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d2288-321">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-322">Die aktuellen Status des Elements.</span><span class="sxs-lookup"><span data-stu-id="d2288-322">The current statuses of the element.</span></span> <span data-ttu-id="d2288-323">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 2 ("OK") festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2288-323">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 ("OK").</span></span>

</dd> <dt>

<span data-ttu-id="d2288-324">**Otherenabled-Funktionen**</span><span class="sxs-lookup"><span data-stu-id="d2288-324">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-325">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="d2288-325">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d2288-326">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-327">Ein Array von Freiform-Zeichen folgen, das Ausführlichere Erläuterungen für jede der aktivierten Funktionen bereitstellt, die als "Other" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="d2288-327">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as "Other".</span></span> <span data-ttu-id="d2288-328">Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2288-328">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2288-329">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="d2288-329">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-330">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2288-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-331">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-332">Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 ("Other") festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d2288-332">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="d2288-333">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="d2288-333">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="d2288-334">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2288-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2288-335">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="d2288-335">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-336">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="d2288-336">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d2288-337">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-338">Alle Daten, zusätzlich zu den Informationen zur Geräte-ID, die zum Identifizieren eines logischen Geräts verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="d2288-338">Any data, in addition to device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="d2288-339">Beispielsweise können Sie diese Eigenschaft verwenden, um den anzeigen amen des Betriebssystems für das Gerät zu speichern.</span><span class="sxs-lookup"><span data-stu-id="d2288-339">For example, you could use this property to hold the operating system's display name for the device.</span></span> <span data-ttu-id="d2288-340">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2288-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2288-341">**Otherlinktechnology**</span><span class="sxs-lookup"><span data-stu-id="d2288-341">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-342">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2288-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-343">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-344">Ein Zeichen folgen Wert, der **linktechnology** beschreibt, wenn er auf 1 ("Other") festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d2288-344">A string value that describes **LinkTechnology** when it is set to 1 ("Other").</span></span> <span data-ttu-id="d2288-345">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2288-345">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2288-346">**Othernetworkporttype**</span><span class="sxs-lookup"><span data-stu-id="d2288-346">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-347">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2288-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-348">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-349">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) geerbt und auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2288-349">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) and is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d2288-350">**Otherporttype**</span><span class="sxs-lookup"><span data-stu-id="d2288-350">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-351">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2288-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-352">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-353">Der Modultyp, wenn **portType** auf 1 ("Other") festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d2288-353">The type of module, when **PortType** is set to 1 ("Other").</span></span> <span data-ttu-id="d2288-354">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85)) geerbt und ist immer auf "Virtuelles Ethernet" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2288-354">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)) and is always set to "Virtual Ethernet".</span></span>

</dd> <dt>

<span data-ttu-id="d2288-355">**Permanent Address**</span><span class="sxs-lookup"><span data-stu-id="d2288-355">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-356">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2288-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-357">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-358">Die Netzwerkadresse, die in einem Port hart codiert ist.</span><span class="sxs-lookup"><span data-stu-id="d2288-358">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="d2288-359">Diese Adresse kann mithilfe eines Firmwareupdates oder einer Softwarekonfiguration geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d2288-359">This address can be changed using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="d2288-360">Wenn diese Änderung vorgenommen wird, sollte das Feld gleichzeitig aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d2288-360">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="d2288-361">Dies sollte leer bleiben, wenn keine hart codierte Adresse für den Netzwerkadapter vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d2288-361">This should be left blank if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="d2288-362">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d2288-362">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d2288-363">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="d2288-363">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-364">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2288-364">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-365">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-366">Netzwerkports sind häufig in Bezug auf ein logisches Modul oder ein Netzwerkelement nummeriert.</span><span class="sxs-lookup"><span data-stu-id="d2288-366">Network ports are often numbered relative to either a logical module or a network element.</span></span> <span data-ttu-id="d2288-367">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d2288-367">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>



| <span data-ttu-id="d2288-368">Wert</span><span class="sxs-lookup"><span data-stu-id="d2288-368">Value</span></span>                                                                        | <span data-ttu-id="d2288-369">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d2288-369">Meaning</span></span>                             |
|------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="d2288-370"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d2288-370"><dt>0</dt></span></span> </dl> | <span data-ttu-id="d2288-371">Die NIC wird nicht emuliert.</span><span class="sxs-lookup"><span data-stu-id="d2288-371">The NIC is not emulated.</span></span><br/> |
| <dl> <span data-ttu-id="d2288-372"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d2288-372"><dt>1</dt></span></span> </dl> | <span data-ttu-id="d2288-373">Die NIC wird emuliert.</span><span class="sxs-lookup"><span data-stu-id="d2288-373">The NIC is emulated.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="d2288-374">**PortType**</span><span class="sxs-lookup"><span data-stu-id="d2288-374">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-375">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2288-375">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-376">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-377">Der bestimmte Modus, der derzeit für den Port aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d2288-377">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="d2288-378">Wenn der Wert auf 1 ("Other") festgelegt ist, enthält die zugehörige Eigenschaft " **otherporttype** " eine Zeichen folgen Beschreibung für den Porttyp.</span><span class="sxs-lookup"><span data-stu-id="d2288-378">When set to 1 ("Other"), the related property **OtherPortType** contains a string description of the type of port.</span></span> <span data-ttu-id="d2288-379">Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)geerbt und ist immer auf 1 ("Other") festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2288-379">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is always set to 1 ("Other").</span></span>

</dd> <dt>

<span data-ttu-id="d2288-380">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="d2288-380">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-381">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="d2288-381">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d2288-382">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-383">Die Energie Verwaltungsfunktionen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="d2288-383">The power management capabilities of the device.</span></span> <span data-ttu-id="d2288-384">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2288-384">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2288-385">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="d2288-385">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-386">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d2288-386">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-387">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-388">Gibt an, ob das Gerät Energie gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="d2288-388">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="d2288-389">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2288-389">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2288-390">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="d2288-390">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-391">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d2288-391">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-392">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-393">Gibt an, wie viele aufeinanderfolgende Stunden dieses Gerät seit dem letzten Strom Umgebung eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="d2288-393">The number of consecutive hours that this device has been powered, since its last power cycle.</span></span> <span data-ttu-id="d2288-394">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2288-394">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2288-395">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="d2288-395">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-396">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2288-396">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-397">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-398">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="d2288-398">Provides high level status information.</span></span> <span data-ttu-id="d2288-399">Diese Eigenschaft sollte in Verbindung mit der **detailedstatus** -Eigenschaft verwendet werden, um allgemeine und ausführliche Integritäts Statusinformationen für das-Element und seine unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d2288-399">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="d2288-400">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="d2288-400">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d2288-401">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d2288-401">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2288-402">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="d2288-402">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-403">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d2288-403">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-404">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-405">Die angeforderte Bandbreite des Ports (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="d2288-405">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="d2288-406">Die tatsächliche Bandbreite wird in logicalport. Speed gemeldet.</span><span class="sxs-lookup"><span data-stu-id="d2288-406">The actual bandwidth is reported in LogicalPort.Speed.</span></span> <span data-ttu-id="d2288-407">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt und ist immer auf 1 Milliarde festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2288-407">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)), and it is always set to 1000000000.</span></span>

</dd> <dt>

<span data-ttu-id="d2288-408">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="d2288-408">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-409">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2288-409">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-410">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-411">Der zuletzt angeforderte oder gewünschte Status für den Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="d2288-411">The last requested or desired state for the management service.</span></span> <span data-ttu-id="d2288-412">Wenn **enabledstate** auf 5 ("nicht zutreffend") festgelegt ist, hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="d2288-412">When **EnabledState** is set to 5 ("Not Applicable"), then this property has no meaning.</span></span> <span data-ttu-id="d2288-413">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 12 ("nicht zutreffend") festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2288-413">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 ("Not Applicable").</span></span>

</dd> <dt>

<span data-ttu-id="d2288-414">**Geschwindigkeit**</span><span class="sxs-lookup"><span data-stu-id="d2288-414">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-415">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d2288-415">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-416">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-417">Die aktuelle Bandbreite des Ports (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="d2288-417">The current bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="d2288-418">Für Ports, die die Bandbreite variieren, oder für diejenigen, bei denen keine genaue Schätzung vorgenommen werden kann, sollte diese Eigenschaft die nominale Bandbreite enthalten.</span><span class="sxs-lookup"><span data-stu-id="d2288-418">For ports that vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span> <span data-ttu-id="d2288-419">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt und ist immer auf 1 Milliarde festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2288-419">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to 1000000000.</span></span>

</dd> <dt>

<span data-ttu-id="d2288-420">**Status**</span><span class="sxs-lookup"><span data-stu-id="d2288-420">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-421">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2288-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-422">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-423">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2288-423">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2288-424">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="d2288-424">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-425">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="d2288-425">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d2288-426">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-427">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="d2288-427">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="d2288-428">Einträge in diesem Array korrelieren mit denjenigen, die sich im selben Array Index in **OperationalStatus** befinden.</span><span class="sxs-lookup"><span data-stu-id="d2288-428">Entries in this array are correlated with those at the same array index in **OperationalStatus**.</span></span> <span data-ttu-id="d2288-429">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf "OK" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2288-429">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="d2288-430">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="d2288-430">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-431">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2288-431">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-432">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-433">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="d2288-433">The state of the logical device.</span></span> <span data-ttu-id="d2288-434">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2288-434">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2288-435">**Supportedmaximumtransmissionunit**</span><span class="sxs-lookup"><span data-stu-id="d2288-435">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-436">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2288-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-437">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2288-438">Qualifizierer: **Einheiten** ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="d2288-438">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="d2288-439">Die maximale Anzahl von Übertragungs Einheiten (MTU), die unterstützt werden können, in Byte.</span><span class="sxs-lookup"><span data-stu-id="d2288-439">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="d2288-440">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt und ist immer auf 1500 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2288-440">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="d2288-441">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="d2288-441">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-442">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2288-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-443">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-444">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="d2288-444">The creation class name of the scoping system.</span></span> <span data-ttu-id="d2288-445">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf "MSVM \_ Computersystem" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2288-445">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="d2288-446">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="d2288-446">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-447">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2288-447">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-448">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-449">Die ID der virtuellen Maschine im **GUID** -Format.</span><span class="sxs-lookup"><span data-stu-id="d2288-449">The virtual machine ID in **GUID** form.</span></span> <span data-ttu-id="d2288-450">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d2288-450">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d2288-451">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="d2288-451">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-452">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="d2288-452">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-453">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-453">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-454">Das Datum oder die Uhrzeit der letzten Änderung des **enabledstate** des Elements.</span><span class="sxs-lookup"><span data-stu-id="d2288-454">The date or time when the **EnabledState** of the element last changed.</span></span> <span data-ttu-id="d2288-455">Wenn der Zustand des Elements nicht geändert wurde und diese Eigenschaft aufgefüllt ist, muss Sie auf einen Wert von 0 Intervall festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d2288-455">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="d2288-456">Wenn eine Zustandsänderung angefordert, aber abgelehnt oder noch nicht verarbeitet wurde, darf die Eigenschaft nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d2288-456">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="d2288-457">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2288-457">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2288-458">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="d2288-458">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-459">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2288-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-460">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-461">Die Gesamtanzahl der Stunden, für die dieses Gerät eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="d2288-461">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="d2288-462">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2288-462">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2288-463">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="d2288-463">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-464">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2288-464">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-465">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-466">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="d2288-466">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="d2288-467">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2288-467">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2288-468">**Einsatz Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="d2288-468">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2288-469">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2288-469">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2288-470">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2288-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2288-471">Unter bestimmten Umständen kann ein logischer Port als Front-End-oder Back-End-Port identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="d2288-471">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="d2288-472">Wenn die Verwendung des Ports nicht eingeschränkt ist, sollte der Wert auf 4 ("nicht eingeschränkt") festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d2288-472">If there is no restriction on the use of the port, then the value should be set to 4 ("Not Restricted").</span></span> <span data-ttu-id="d2288-473">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85)) geerbt und ist immer auf 4 ("nicht eingeschränkt") festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2288-473">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)) and is always set to 4 ("Not Restricted").</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2288-474">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2288-474">Remarks</span></span>

<span data-ttu-id="d2288-475">Der Zugriff auf die **MSVM- \_ emulatedethernetport** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="d2288-475">Access to the **Msvm\_EmulatedEthernetPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d2288-476">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d2288-476">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="d2288-477">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d2288-477">Examples</span></span>

<span data-ttu-id="d2288-478">Weitere Informationen finden Sie unter [Abfragen von Netzwerk Objekten](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="d2288-478">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d2288-479">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2288-479">Requirements</span></span>



| <span data-ttu-id="d2288-480">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2288-480">Requirement</span></span> | <span data-ttu-id="d2288-481">Wert</span><span class="sxs-lookup"><span data-stu-id="d2288-481">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2288-482">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d2288-482">Minimum supported client</span></span><br/> | <span data-ttu-id="d2288-483">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2288-483">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d2288-484">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d2288-484">Minimum supported server</span></span><br/> | <span data-ttu-id="d2288-485">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2288-485">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d2288-486">Namespace</span><span class="sxs-lookup"><span data-stu-id="d2288-486">Namespace</span></span><br/>                | <span data-ttu-id="d2288-487">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="d2288-487">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d2288-488">MOF</span><span class="sxs-lookup"><span data-stu-id="d2288-488">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2288-489"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d2288-489"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2288-490">DLL</span><span class="sxs-lookup"><span data-stu-id="d2288-490">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2288-491"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d2288-491"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d2288-492">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2288-492">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2288-493">**CIM- \_ Ethernetport**</span><span class="sxs-lookup"><span data-stu-id="d2288-493">**CIM\_EthernetPort**</span></span>](cim-ethernetport.md)
</dt> <dt>

[<span data-ttu-id="d2288-494">**CIM- \_ Ethernetport**</span><span class="sxs-lookup"><span data-stu-id="d2288-494">**CIM\_EthernetPort**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 

