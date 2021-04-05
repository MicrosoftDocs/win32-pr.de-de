---
description: Stellt einen internen Ethernet-Port (Netzwerkadapter) dar.
ms.assetid: 43277FA7-E040-49F2-A086-AF19B29D4F75
title: Msvm_InternalEthernetPort-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InternalEthernetPort
- Msvm_InternalEthernetPort.SetPowerState
- Msvm_InternalEthernetPort.EnableDevice
- Msvm_InternalEthernetPort.OnlineDevice
- Msvm_InternalEthernetPort.QuiesceDevice
- Msvm_InternalEthernetPort.SaveProperties
- Msvm_InternalEthernetPort.RestoreProperties
- Msvm_InternalEthernetPort.InstanceID
- Msvm_InternalEthernetPort.Caption
- Msvm_InternalEthernetPort.Description
- Msvm_InternalEthernetPort.ElementName
- Msvm_InternalEthernetPort.InstallDate
- Msvm_InternalEthernetPort.Name
- Msvm_InternalEthernetPort.OperationalStatus
- Msvm_InternalEthernetPort.StatusDescriptions
- Msvm_InternalEthernetPort.Status
- Msvm_InternalEthernetPort.HealthState
- Msvm_InternalEthernetPort.CommunicationStatus
- Msvm_InternalEthernetPort.DetailedStatus
- Msvm_InternalEthernetPort.OperatingStatus
- Msvm_InternalEthernetPort.PrimaryStatus
- Msvm_InternalEthernetPort.EnabledState
- Msvm_InternalEthernetPort.OtherEnabledState
- Msvm_InternalEthernetPort.RequestedState
- Msvm_InternalEthernetPort.EnabledDefault
- Msvm_InternalEthernetPort.TimeOfLastStateChange
- Msvm_InternalEthernetPort.AvailableRequestedStates
- Msvm_InternalEthernetPort.TransitioningToState
- Msvm_InternalEthernetPort.SystemCreationClassName
- Msvm_InternalEthernetPort.SystemName
- Msvm_InternalEthernetPort.CreationClassName
- Msvm_InternalEthernetPort.DeviceID
- Msvm_InternalEthernetPort.PowerManagementSupported
- Msvm_InternalEthernetPort.PowerManagementCapabilities
- Msvm_InternalEthernetPort.Availability
- Msvm_InternalEthernetPort.StatusInfo
- Msvm_InternalEthernetPort.LastErrorCode
- Msvm_InternalEthernetPort.ErrorDescription
- Msvm_InternalEthernetPort.ErrorCleared
- Msvm_InternalEthernetPort.OtherIdentifyingInfo
- Msvm_InternalEthernetPort.PowerOnHours
- Msvm_InternalEthernetPort.TotalPowerOnHours
- Msvm_InternalEthernetPort.IdentifyingDescriptions
- Msvm_InternalEthernetPort.AdditionalAvailability
- Msvm_InternalEthernetPort.MaxQuiesceTime
- Msvm_InternalEthernetPort.MaxSpeed
- Msvm_InternalEthernetPort.RequestedSpeed
- Msvm_InternalEthernetPort.UsageRestriction
- Msvm_InternalEthernetPort.OtherPortType
- Msvm_InternalEthernetPort.Speed
- Msvm_InternalEthernetPort.OtherNetworkPortType
- Msvm_InternalEthernetPort.PortNumber
- Msvm_InternalEthernetPort.LinkTechnology
- Msvm_InternalEthernetPort.OtherLinkTechnology
- Msvm_InternalEthernetPort.PermanentAddress
- Msvm_InternalEthernetPort.FullDuplex
- Msvm_InternalEthernetPort.AutoSense
- Msvm_InternalEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_InternalEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_InternalEthernetPort.PortType
- Msvm_InternalEthernetPort.NetworkAddresses
- Msvm_InternalEthernetPort.MaxDataSize
- Msvm_InternalEthernetPort.Capabilities
- Msvm_InternalEthernetPort.CapabilityDescriptions
- Msvm_InternalEthernetPort.EnabledCapabilities
- Msvm_InternalEthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a1441055fc7b86b97c69a40758236261b20f75c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752368"
---
# <a name="msvm_internalethernetport-class"></a><span data-ttu-id="27d2e-103">MSVM \_ internalethernetport-Klasse</span><span class="sxs-lookup"><span data-stu-id="27d2e-103">Msvm\_InternalEthernetPort class</span></span>

<span data-ttu-id="27d2e-104">Stellt einen internen Ethernet-Port (Netzwerkadapter) dar.</span><span class="sxs-lookup"><span data-stu-id="27d2e-104">Represents an internal Ethernet port (network adapter).</span></span> <span data-ttu-id="27d2e-105">Diese Art von Ethernet-Port ermöglicht virtuellen Computern den Zugriff auf den Virtualisierungsserver, auf dem die Netzwerk Software ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="27d2e-105">This type of Ethernet port gives virtual machines access to the virtualization server running the networking software.</span></span> <span data-ttu-id="27d2e-106">Mit den internen Netzwerkadaptern kann der Netzwerk Datenverkehr der virtuellen Computer weitergeleitet oder gefiltert werden, bevor das physische System verlässt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-106">The internal network adapters allow the virtual machines network traffic to be routed or filtered before leaving the physical system.</span></span>

<span data-ttu-id="27d2e-107">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="27d2e-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="27d2e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="27d2e-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_InternalEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Port";
  string   Description = "Microsoft Internal Ethernet Port";
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
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_InternalEthernetPort";
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
  uint16   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  uint64   MaxSpeed = 1000000000;
  uint64   RequestedSpeed = 1000000000;
  uint16   UsageRestriction = 4;
  string   OtherPortType;
  uint64   Speed;
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology = 2;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  boolean  FullDuplex = True;
  boolean  AutoSense = True;
  uint64   SupportedMaximumTransmissionUnit = 1500;
  uint64   ActiveMaximumTransmissionUnit = 1500;
  uint16   PortType;
  string   NetworkAddresses[];
  uint32   MaxDataSize = 1500;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  uint16   EnabledCapabilities[];
  string   OtherEnabledCapabilities[];
};
```

## <a name="members"></a><span data-ttu-id="27d2e-109">Member</span><span class="sxs-lookup"><span data-stu-id="27d2e-109">Members</span></span>

<span data-ttu-id="27d2e-110">Die **MSVM \_ internalethernetport** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="27d2e-110">The **Msvm\_InternalEthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="27d2e-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="27d2e-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="27d2e-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="27d2e-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="27d2e-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="27d2e-113">Methods</span></span>

<span data-ttu-id="27d2e-114">Die **MSVM \_ internalethernetport** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="27d2e-114">The **Msvm\_InternalEthernetPort** class has these methods.</span></span>



| <span data-ttu-id="27d2e-115">Methode</span><span class="sxs-lookup"><span data-stu-id="27d2e-115">Method</span></span>                                                                     | <span data-ttu-id="27d2e-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27d2e-116">Description</span></span>                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="27d2e-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="27d2e-117">**EnableDevice**</span></span>                                                           | <span data-ttu-id="27d2e-118">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="27d2e-119">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="27d2e-119">**OnlineDevice**</span></span>                                                           | <span data-ttu-id="27d2e-120">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="27d2e-121">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="27d2e-121">**QuiesceDevice**</span></span>                                                          | <span data-ttu-id="27d2e-122">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="27d2e-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="27d2e-123">**RequestStateChange**</span></span>](msvm-internalethernetport-requeststatechange.md) | <span data-ttu-id="27d2e-124">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="27d2e-124">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="27d2e-125">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="27d2e-125">**Reset**</span></span>](msvm-internalethernetport-reset.md)                           | <span data-ttu-id="27d2e-126">Setzt das virtuelle Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="27d2e-126">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="27d2e-127">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="27d2e-127">**RestoreProperties**</span></span>                                                      | <span data-ttu-id="27d2e-128">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="27d2e-129">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="27d2e-129">**SaveProperties**</span></span>                                                         | <span data-ttu-id="27d2e-130">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="27d2e-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="27d2e-131">**SetPowerState**</span></span>                                                          | <span data-ttu-id="27d2e-132">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="27d2e-133">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="27d2e-133">Properties</span></span>

<span data-ttu-id="27d2e-134">Die **MSVM \_ internalethernetport** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="27d2e-134">The **Msvm\_InternalEthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="27d2e-135">**Activemaximumtransmissionunit**</span><span class="sxs-lookup"><span data-stu-id="27d2e-135">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-136">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="27d2e-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-138">Die aktive oder ausgehandelte maximale Übertragungseinheit (Maximum Transmission Unit, MTU), die unterstützt werden kann.</span><span class="sxs-lookup"><span data-stu-id="27d2e-138">The active or negotiated maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="27d2e-139">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-139">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-140">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="27d2e-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-141">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="27d2e-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-143">Alle zusätzlichen Verfügbarkeit und den Status des Geräts, außer den in der **Availability** -Eigenschaft angegebenen.</span><span class="sxs-lookup"><span data-stu-id="27d2e-143">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="27d2e-144">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-145">**AutoSense**</span><span class="sxs-lookup"><span data-stu-id="27d2e-145">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-146">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="27d2e-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-148">Gibt an, ob der Netzwerkport die Geschwindigkeit oder andere Kommunikationsmerkmale der angeschlossenen Netzwerk Medien automatisch bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="27d2e-148">Indicates whether the network port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="27d2e-149">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-149">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-150">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="27d2e-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-151">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27d2e-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-153">Die primäre Verfügbarkeit und den Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="27d2e-153">The primary availability and status of the device.</span></span> <span data-ttu-id="27d2e-154">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="27d2e-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-155">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="27d2e-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-156">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="27d2e-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-158">Gibt die möglichen Werte für den *requestedstate* -Parameter der [**requestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) -Methode an, die zum Initiieren einer Zustandsänderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="27d2e-158">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="27d2e-159">Bei den aufgelisteten Werten handelt es sich um eine Teilmenge der Werte, die in der **requestedstaatsupported** -Eigenschaft der zugeordneten Instanz von **CIM \_ enabledlogicalelementfunctions** enthalten sind, wobei die ausgewählten Werte eine Funktion des aktuellen Zustands des [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) -Objekts sind.</span><span class="sxs-lookup"><span data-stu-id="27d2e-159">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="27d2e-160">Diese Eigenschaft darf nicht **null** sein, wenn eine Implementierung den Satz möglicher Werte als Funktion des aktuellen Zustands ankündigen kann.</span><span class="sxs-lookup"><span data-stu-id="27d2e-160">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="27d2e-161">Diese Eigenschaft ist **null** , wenn eine Implementierung den Satz möglicher Werte nicht als Funktion des aktuellen Zustands bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="27d2e-161">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="27d2e-162">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="27d2e-162">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-163">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="27d2e-163">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-164">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="27d2e-164">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-166">Funktionen des Ethernet-Ports.</span><span class="sxs-lookup"><span data-stu-id="27d2e-166">Capabilities of the Ethernet port.</span></span> <span data-ttu-id="27d2e-167">Wenn Failover-oder Lasten Ausgleichs Funktionen aufgelistet werden, sollte auch eine [**CIM- \_ SpareGroup**](/windows/desktop/CIMWin32Prov/cim-sparegroup) (Failover) oder [**CIM \_ extracapacitygroup**](/windows/desktop/CIMWin32Prov/cim-extracapacitygroup) (Lastenausgleich) definiert werden, um die Funktion vollständig zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="27d2e-167">If failover or load balancing capabilities are listed, a [**CIM\_SpareGroup**](/windows/desktop/CIMWin32Prov/cim-sparegroup) (failover) or [**CIM\_ExtraCapacityGroup**](/windows/desktop/CIMWin32Prov/cim-extracapacitygroup) (load balancing) should also be defined to completely describe the capability.</span></span> <span data-ttu-id="27d2e-168">Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-168">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="27d2e-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="27d2e-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="27d2e-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-171"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**Alertonlan** (2)</span><span class="sxs-lookup"><span data-stu-id="27d2e-171"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-172"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**Wake-on-LAN** (3)</span><span class="sxs-lookup"><span data-stu-id="27d2e-172"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-173"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Failover** (4)</span><span class="sxs-lookup"><span data-stu-id="27d2e-173"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-174"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**Loadbalancing** (5)</span><span class="sxs-lookup"><span data-stu-id="27d2e-174"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="27d2e-175">**Capabilitybeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="27d2e-175">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-176">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="27d2e-176">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-178">Ein Array von Freiform-Zeichen folgen, das Ausführlichere Erläuterungen zu allen Ethernet-Port Features bereitstellt **, die im Funktions Array angegeben** sind.</span><span class="sxs-lookup"><span data-stu-id="27d2e-178">An array of free-form strings that provides more detailed explanations for any of the Ethernet port features that are indicated in the **Capabilities** array.</span></span> <span data-ttu-id="27d2e-179">Beachten Sie, dass jeder Eintrag dieses Arrays mit dem Eintrag im **Funktions Array verknüpft ist, der sich** am selben Index befindet.</span><span class="sxs-lookup"><span data-stu-id="27d2e-179">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span> <span data-ttu-id="27d2e-180">Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-180">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-181">**Caption**</span><span class="sxs-lookup"><span data-stu-id="27d2e-181">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-182">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="27d2e-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-184">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="27d2e-184">A short description of the object.</span></span> <span data-ttu-id="27d2e-185">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-186">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="27d2e-186">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-187">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27d2e-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-189">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="27d2e-189">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="27d2e-190">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="27d2e-190">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="27d2e-191">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-192">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="27d2e-192">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-193">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="27d2e-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-195">Der Name der Klasse oder der Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="27d2e-195">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="27d2e-196">Wenn diese Eigenschaft mit den anderen Schlüsseleigenschaften dieser Klasse verwendet wird, können alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="27d2e-196">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="27d2e-197">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-197">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-198">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="27d2e-198">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-199">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="27d2e-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-200">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-201">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="27d2e-201">A description of the object.</span></span> <span data-ttu-id="27d2e-202">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-202">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-203">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="27d2e-203">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-204">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27d2e-204">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-205">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-206">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="27d2e-206">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="27d2e-207">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="27d2e-207">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="27d2e-208">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-208">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-209">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="27d2e-209">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-210">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="27d2e-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-212">Eine Adresse oder andere identifizierende Informationen, die verwendet werden, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="27d2e-212">An address or other identifying information used to uniquely name the logical device.</span></span> <span data-ttu-id="27d2e-213">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und auf "Microsoft:*GUID* \\ *gerätespezifische Daten*" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-213">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific data*".</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-214">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="27d2e-214">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-215">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="27d2e-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-216">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="27d2e-216">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-217">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-217">A display name for the object.</span></span> <span data-ttu-id="27d2e-218">Mit dieser Eigenschaft kann jede Instanz zusätzlich zu ihren Schlüsseleigenschaften, Identitätsdaten und Beschreibungs Informationen einen anzeigen Amen definieren.</span><span class="sxs-lookup"><span data-stu-id="27d2e-218">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="27d2e-219">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) geerbt und wird basierend auf der NIC generiert, die auf dem Host vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="27d2e-219">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) and is generated based on the NIC present in the host.</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-220">**Enabled-Funktionen**</span><span class="sxs-lookup"><span data-stu-id="27d2e-220">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-221">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="27d2e-221">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-222">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-223">Gibt an, welche Funktionen in der Liste aller unterstützten Funktionen aktiviert sind, die im Funktions **Array definiert** sind.</span><span class="sxs-lookup"><span data-stu-id="27d2e-223">Specifies which capabilities are enabled from the list of all supported ones, which are defined in the **Capabilities** array.</span></span> <span data-ttu-id="27d2e-224">Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-224">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="27d2e-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="27d2e-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-226"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="27d2e-226"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-227"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**Alertonlan** (2)</span><span class="sxs-lookup"><span data-stu-id="27d2e-227"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-228"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**Wake-on-LAN** (3)</span><span class="sxs-lookup"><span data-stu-id="27d2e-228"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-229"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Failover** (4)</span><span class="sxs-lookup"><span data-stu-id="27d2e-229"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-230"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**Loadbalancing** (5)</span><span class="sxs-lookup"><span data-stu-id="27d2e-230"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="27d2e-231">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="27d2e-231">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-232">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27d2e-232">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-233">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-234">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="27d2e-234">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="27d2e-235">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-235">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-236">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="27d2e-236">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-237">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27d2e-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-238">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-239">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="27d2e-239">The enabled and disabled states of an element.</span></span> <span data-ttu-id="27d2e-240">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-240">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-241">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="27d2e-241">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-242">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="27d2e-242">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-243">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-244">Gibt an, ob der in der **LastErrorCode** -Eigenschaft gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="27d2e-244">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="27d2e-245">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="27d2e-245">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-246">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="27d2e-246">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-247">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="27d2e-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-248">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-249">Eine Zeichenfolge, die weitere Informationen über den in der **LastErrorCode** -Eigenschaft aufgezeichneten Fehler sowie Informationen zu ggf. durchzuführenden Maßnahmen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-249">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="27d2e-250">Diese Eigenschaft wird von der [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -Eigenschaft geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="27d2e-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) property and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-251">**Vollduplex**</span><span class="sxs-lookup"><span data-stu-id="27d2e-251">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-252">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="27d2e-252">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-253">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-254">Gibt an, ob der Port im Vollduplex Modus betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="27d2e-254">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="27d2e-255">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-255">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-256">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="27d2e-256">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-257">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27d2e-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-258">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-259">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="27d2e-259">The current health of the element.</span></span> <span data-ttu-id="27d2e-260">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="27d2e-260">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="27d2e-261">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-261">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-262">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="27d2e-262">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-263">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="27d2e-263">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-264">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-265">Ein Array von Freiform-Zeichen folgen, die Erklärungen und Details hinter den Einträgen im Eigenschafts Array " **OtherIdentifyingInfo** " bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="27d2e-265">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="27d2e-266">Jeder Eintrag dieses Arrays bezieht sich auf den Eintrag im Eigenschafts Array " **OtherIdentifyingInfo** ", der sich am selben Index befindet.</span><span class="sxs-lookup"><span data-stu-id="27d2e-266">Each entry of this array is related to the entry in the **OtherIdentifyingInfo** property array that is located at the same index.</span></span> <span data-ttu-id="27d2e-267">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="27d2e-267">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-268">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="27d2e-268">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-269">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="27d2e-269">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-270">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-271">Ein **DateTime** -Wert, der angibt, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="27d2e-271">A **datetime** value that indicates when the object was installed.</span></span> <span data-ttu-id="27d2e-272">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="27d2e-272">Lack of a value does not indicate that the object is not installed.</span></span> <span data-ttu-id="27d2e-273">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-273">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-274">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="27d2e-274">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-275">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="27d2e-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-276">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-277">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="27d2e-277">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-278">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="27d2e-278">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="27d2e-279">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-279">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-280">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="27d2e-280">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-281">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="27d2e-281">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-282">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-283">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="27d2e-283">The last error code reported by the logical device.</span></span> <span data-ttu-id="27d2e-284">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="27d2e-284">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-285">**Linktechnology**</span><span class="sxs-lookup"><span data-stu-id="27d2e-285">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-286">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27d2e-286">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-287">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-288">Die Linktypen.</span><span class="sxs-lookup"><span data-stu-id="27d2e-288">The types of links.</span></span> <span data-ttu-id="27d2e-289">Wenn der Wert auf 1 (Other) festgelegt ist, enthält die zugehörige Eigenschaft **otherlinktechnology** eine Zeichen folgen Beschreibung des linktyps.</span><span class="sxs-lookup"><span data-stu-id="27d2e-289">When set to 1 (Other), the related property **OtherLinkTechnology** contains a string description of the type of link.</span></span> <span data-ttu-id="27d2e-290">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-290">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>



| <span data-ttu-id="27d2e-291">Wert</span><span class="sxs-lookup"><span data-stu-id="27d2e-291">Value</span></span>                                                                        | <span data-ttu-id="27d2e-292">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="27d2e-292">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="27d2e-293"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="27d2e-293"><dt>2</dt></span></span> </dl> | <span data-ttu-id="27d2e-294">Ethernet</span><span class="sxs-lookup"><span data-stu-id="27d2e-294">Ethernet</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="27d2e-295">**Maxdatasize**</span><span class="sxs-lookup"><span data-stu-id="27d2e-295">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-296">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="27d2e-296">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-297">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-298">Die maximale Größe des Felds Info (nicht-Mac), das empfangen oder übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="27d2e-298">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="27d2e-299">Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-299">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-300">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="27d2e-300">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-301">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="27d2e-301">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-302">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-303">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="27d2e-303">This property has been deprecated.</span></span> <span data-ttu-id="27d2e-304">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="27d2e-304">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-305">**MAXSPEED**</span><span class="sxs-lookup"><span data-stu-id="27d2e-305">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-306">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="27d2e-306">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-307">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-308">Die maximale Bandbreite des Ports (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="27d2e-308">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="27d2e-309">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-309">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-310">**Name**</span><span class="sxs-lookup"><span data-stu-id="27d2e-310">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-311">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="27d2e-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-312">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-313">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="27d2e-313">The label by which the object is known.</span></span> <span data-ttu-id="27d2e-314">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="27d2e-314">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="27d2e-315">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-315">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-316">**"Networkaddresses"**</span><span class="sxs-lookup"><span data-stu-id="27d2e-316">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-317">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="27d2e-317">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-318">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-319">Die Ethernet/802.3-Mac-Adressen, die als zwölf hexadezimal Ziffern formatiert sind (z. b. "010203040506"), wobei jedes Paar eines der sechs Oktette der Mac-Adresse in der kanonischen bidirektionalen Reihenfolge darstellt (das Gruppen Adressbit befindet sich im niedrig wertigen Bit des ersten Zeichens der Zeichenfolge). Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-319">The Ethernet/802.3 MAC addresses formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order (the Group address bit is found in the low order bit of the first character of the string.) This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-320">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="27d2e-320">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-321">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27d2e-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-322">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-323">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="27d2e-323">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="27d2e-324">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="27d2e-324">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="27d2e-325">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-326">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="27d2e-326">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-327">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="27d2e-327">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-328">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-329">Die aktuellen Status des Elements.</span><span class="sxs-lookup"><span data-stu-id="27d2e-329">The current statuses of the element.</span></span> <span data-ttu-id="27d2e-330">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-330">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-331">**Otherenabled-Funktionen**</span><span class="sxs-lookup"><span data-stu-id="27d2e-331">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-332">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="27d2e-332">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-333">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-334">Ein Array von Freiform-Zeichen folgen, das Ausführlichere Erläuterungen für jede der aktivierten Funktionen bereitstellt, die als 1 (Sonstiges) angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="27d2e-334">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as 1 (Other).</span></span> <span data-ttu-id="27d2e-335">Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-335">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-336">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="27d2e-336">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-337">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="27d2e-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-338">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-339">Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 (sonstige) festgelegt ist. Diese Eigenschaft muss auf **null** festgelegt werden, wenn die **enabledstate** -Eigenschaft einen anderen Wert als 1 hat.</span><span class="sxs-lookup"><span data-stu-id="27d2e-339">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other.) This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="27d2e-340">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-340">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-341">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="27d2e-341">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-342">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="27d2e-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-343">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-344">Alle Daten, zusätzlich zu den Informationen zur Geräte-ID, die zum Identifizieren eines logischen Geräts verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="27d2e-344">Any data, in addition to device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="27d2e-345">Beispielsweise können Sie diese Eigenschaft verwenden, um den anzeigen amen des Betriebssystems für das Gerät zu speichern.</span><span class="sxs-lookup"><span data-stu-id="27d2e-345">For example, you could use this property to hold the operating system's display name for the device.</span></span> <span data-ttu-id="27d2e-346">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="27d2e-346">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-347">**Otherlinktechnology**</span><span class="sxs-lookup"><span data-stu-id="27d2e-347">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-348">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="27d2e-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-349">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-350">Ein Zeichen folgen Wert, der die **linktechnology** -Eigenschaft beschreibt, wenn Sie auf 1 (sonstige) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="27d2e-350">A string value that describes the **LinkTechnology** property when it is set to 1 (Other).</span></span> <span data-ttu-id="27d2e-351">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-351">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-352">**Othernetworkporttype**</span><span class="sxs-lookup"><span data-stu-id="27d2e-352">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-353">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="27d2e-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-354">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-355">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="27d2e-355">This property is deprecated.</span></span> <span data-ttu-id="27d2e-356">Verwenden Sie die **portType** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="27d2e-356">Use the **PortType** property.</span></span> <span data-ttu-id="27d2e-357">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-357">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<span data-ttu-id="27d2e-358">Veraltete Beschreibung: der Modultyp, wenn die **portType** -Eigenschaft auf 1 (sonstige) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="27d2e-358">Deprecated description: The type of module, when the **PortType** property is set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-359">**Otherporttype**</span><span class="sxs-lookup"><span data-stu-id="27d2e-359">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-360">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="27d2e-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-361">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-362">Der Modultyp, wenn die **portType** -Eigenschaft auf 1 (sonstige) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="27d2e-362">The type of module, when the **PortType** property is set to 1 (Other).</span></span> <span data-ttu-id="27d2e-363">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85)) geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-363">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)) .</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-364">**Permanent Address**</span><span class="sxs-lookup"><span data-stu-id="27d2e-364">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-365">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="27d2e-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-366">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-367">Die Netzwerkadresse, die in einem Port hart codiert ist.</span><span class="sxs-lookup"><span data-stu-id="27d2e-367">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="27d2e-368">Diese Adresse kann mithilfe eines Firmwareupdates oder einer Softwarekonfiguration geändert werden.</span><span class="sxs-lookup"><span data-stu-id="27d2e-368">This address can be changed using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="27d2e-369">Wenn diese Änderung vorgenommen wird, sollte das Feld gleichzeitig aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="27d2e-369">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="27d2e-370">Dies sollte leer bleiben, wenn keine hart codierte Adresse für den Netzwerkadapter vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="27d2e-370">This should be left blank if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="27d2e-371">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-371">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-372">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="27d2e-372">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-373">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27d2e-373">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-374">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-375">Netzwerkports sind häufig in Bezug auf ein logisches Modul oder ein Netzwerkelement nummeriert.</span><span class="sxs-lookup"><span data-stu-id="27d2e-375">Network ports are often numbered relative to either a logical module or a network element.</span></span> <span data-ttu-id="27d2e-376">Dieser Wert ist 1 für emulierten NICs, 0 für alle anderen.</span><span class="sxs-lookup"><span data-stu-id="27d2e-376">This value is 1 for emulated NICs, 0 for all others.</span></span> <span data-ttu-id="27d2e-377">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-377">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-378">**PortType**</span><span class="sxs-lookup"><span data-stu-id="27d2e-378">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-379">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27d2e-379">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-380">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-381">Der bestimmte Modus, der derzeit für den Port aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="27d2e-381">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="27d2e-382">Wenn der Wert auf 1 (Sonstiges) festgelegt ist, enthält die zugehörige Eigenschaft **otherporttype** eine Zeichen folgen Beschreibung für den Porttyp.</span><span class="sxs-lookup"><span data-stu-id="27d2e-382">When set to 1 (Other), the related property **OtherPortType** contains a string description of the type of port.</span></span> <span data-ttu-id="27d2e-383">Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-383">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="27d2e-384"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="27d2e-384"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-385"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="27d2e-385"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-386"><span id="__50_Copper_10BaseT"></span><span id="__50_copper_10baset"></span><span id="__50_COPPER_10BASET"></span>**50 Kupfer 10BaseT** (50)</span><span class="sxs-lookup"><span data-stu-id="27d2e-386"><span id="__50_Copper_10BaseT"></span><span id="__50_copper_10baset"></span><span id="__50_COPPER_10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-387"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100-BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="27d2e-387"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-388"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100 BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="27d2e-388"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-389"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000 BaseT** (53)</span><span class="sxs-lookup"><span data-stu-id="27d2e-389"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-390"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500baset** (54)</span><span class="sxs-lookup"><span data-stu-id="27d2e-390"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-391"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10gbaset** (55)</span><span class="sxs-lookup"><span data-stu-id="27d2e-391"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-392"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="27d2e-392"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-393"><span id="__100_Fibre_100Base-FX"></span><span id="__100_fibre_100base-fx"></span><span id="__100_FIBRE_100BASE-FX"></span>**100 Fibre 100Base-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="27d2e-393"><span id="__100_Fibre_100Base-FX"></span><span id="__100_fibre_100base-fx"></span><span id="__100_FIBRE_100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-394"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100BASE-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="27d2e-394"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-395"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000 Base-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="27d2e-395"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-396"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000 Base-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="27d2e-396"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-397"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000 Base-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="27d2e-397"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-398"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="27d2e-398"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-399"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="27d2e-399"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-400"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="27d2e-400"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-401"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="27d2e-401"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-402"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="27d2e-402"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-403"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-er** (110)</span><span class="sxs-lookup"><span data-stu-id="27d2e-403"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-404"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span><span class="sxs-lookup"><span data-stu-id="27d2e-404"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-405"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (16000 65535)</span><span class="sxs-lookup"><span data-stu-id="27d2e-405"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (16000 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="27d2e-406">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="27d2e-406">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-407">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="27d2e-407">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-408">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-409">Die Energie Verwaltungsfunktionen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="27d2e-409">The power management capabilities of the device.</span></span> <span data-ttu-id="27d2e-410">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="27d2e-410">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-411">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="27d2e-411">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-412">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="27d2e-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-413">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-414">Gibt an, ob das Gerät Energie gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="27d2e-414">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="27d2e-415">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="27d2e-415">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-416">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="27d2e-416">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-417">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="27d2e-417">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-418">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-419">Gibt an, wie viele aufeinanderfolgende Stunden dieses Gerät seit dem letzten Strom Umgebung eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="27d2e-419">The number of consecutive hours that this device has been powered, since its last power cycle.</span></span> <span data-ttu-id="27d2e-420">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="27d2e-420">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-421">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="27d2e-421">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-422">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27d2e-422">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-423">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-423">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-424">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="27d2e-424">Provides high level status information.</span></span> <span data-ttu-id="27d2e-425">Diese Eigenschaft sollte in Verbindung mit der **detailedstatus** -Eigenschaft verwendet werden, um allgemeine und ausführliche Integritäts Statusinformationen für das-Element und seine unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="27d2e-425">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="27d2e-426">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="27d2e-426">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="27d2e-427">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-427">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-428">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="27d2e-428">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-429">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="27d2e-429">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-430">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-431">Die angeforderte Bandbreite des Ports (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="27d2e-431">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="27d2e-432">Die tatsächliche Bandbreite wird in der Eigenschaft **Geschwindigkeit** gemeldet.</span><span class="sxs-lookup"><span data-stu-id="27d2e-432">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="27d2e-433">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-433">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-434">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="27d2e-434">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-435">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27d2e-435">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-436">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-437">Der zuletzt angeforderte oder gewünschte Status für den Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="27d2e-437">The last requested or desired state for the management service.</span></span> <span data-ttu-id="27d2e-438">Wenn die **enabledstate** -Eigenschaft auf 5 festgelegt ist (nicht zutreffend), hat diese Eigenschaft keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="27d2e-438">When the **EnabledState** property is set to 5 (Not Applicable), then this property has no meaning.</span></span> <span data-ttu-id="27d2e-439">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-439">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-440">**Geschwindigkeit**</span><span class="sxs-lookup"><span data-stu-id="27d2e-440">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-441">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="27d2e-441">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-442">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-442">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-443">Qualifizierer: **außer Kraft** setzung, **Einheiten** ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="27d2e-443">Qualifiers: **Override**, **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-444">Die aktuelle Bandbreite des Ports in Bits pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="27d2e-444">The current bandwidth of the port in bits per second.</span></span> <span data-ttu-id="27d2e-445">Für Ports, die die Bandbreite variieren, oder für diejenigen, bei denen keine genaue Schätzung vorgenommen werden kann, sollte diese Eigenschaft die nominale Bandbreite enthalten.</span><span class="sxs-lookup"><span data-stu-id="27d2e-445">For ports that vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span> <span data-ttu-id="27d2e-446">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-446">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-447">**Status**</span><span class="sxs-lookup"><span data-stu-id="27d2e-447">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-448">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="27d2e-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-449">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-450">Der aktuelle Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="27d2e-450">The current status of the object.</span></span> <span data-ttu-id="27d2e-451">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="27d2e-451">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-452">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="27d2e-452">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-453">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="27d2e-453">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-454">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-454">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-455">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="27d2e-455">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="27d2e-456">Einträge in diesem Array korrelieren mit denjenigen, die sich im selben Array Index in **OperationalStatus** befinden.</span><span class="sxs-lookup"><span data-stu-id="27d2e-456">Entries in this array are correlated with those at the same array index in **OperationalStatus**.</span></span> <span data-ttu-id="27d2e-457">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-457">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-458">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="27d2e-458">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-459">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27d2e-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-460">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-461">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="27d2e-461">The state of the logical device.</span></span> <span data-ttu-id="27d2e-462">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="27d2e-462">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-463">**Supportedmaximumtransmissionunit**</span><span class="sxs-lookup"><span data-stu-id="27d2e-463">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-464">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="27d2e-464">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-465">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-466">Die maximale Übertragungseinheit (MTU), die unterstützt werden kann.</span><span class="sxs-lookup"><span data-stu-id="27d2e-466">The maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="27d2e-467">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-467">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-468">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="27d2e-468">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-469">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="27d2e-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-470">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-471">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="27d2e-471">The scoping system's creation class name.</span></span> <span data-ttu-id="27d2e-472">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, wird aber nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-472">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not supported</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-473">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="27d2e-473">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-474">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="27d2e-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-475">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-476">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="27d2e-476">The name of the scoping system.</span></span> <span data-ttu-id="27d2e-477">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-477">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-478">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="27d2e-478">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-479">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="27d2e-479">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-480">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-480">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-481">Das Datum oder die Uhrzeit der letzten Änderung der **enabledstate** -Eigenschaft des Elements.</span><span class="sxs-lookup"><span data-stu-id="27d2e-481">The date or time when the **EnabledState** property of the element last changed.</span></span> <span data-ttu-id="27d2e-482">Wenn der Zustand des Elements nicht geändert wurde und diese Eigenschaft aufgefüllt ist, muss Sie auf einen Wert von 0 Intervall festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="27d2e-482">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="27d2e-483">Wenn eine Zustandsänderung angefordert, aber abgelehnt oder noch nicht verarbeitet wurde, darf die Eigenschaft nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="27d2e-483">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="27d2e-484">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="27d2e-484">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-485">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="27d2e-485">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-486">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27d2e-486">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-487">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-488">Die Gesamtanzahl der Stunden, für die dieses Gerät eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="27d2e-488">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="27d2e-489">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="27d2e-489">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-490">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="27d2e-490">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-491">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27d2e-491">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-492">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-492">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-493">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="27d2e-493">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="27d2e-494">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="27d2e-494">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="27d2e-495">**Einsatz Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="27d2e-495">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d2e-496">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27d2e-496">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="27d2e-497">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27d2e-497">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27d2e-498">Unter bestimmten Umständen kann ein logischer Port als Front-End-oder Back-End-Port identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="27d2e-498">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="27d2e-499">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="27d2e-499">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>



| <span data-ttu-id="27d2e-500">Wert</span><span class="sxs-lookup"><span data-stu-id="27d2e-500">Value</span></span>                                                                        | <span data-ttu-id="27d2e-501">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="27d2e-501">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="27d2e-502"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="27d2e-502"><dt>4</dt></span></span> </dl> | <span data-ttu-id="27d2e-503">Nicht eingeschränkt</span><span class="sxs-lookup"><span data-stu-id="27d2e-503">Not Restricted</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="27d2e-504">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27d2e-504">Remarks</span></span>

<span data-ttu-id="27d2e-505">Der Zugriff auf die **MSVM \_ internalethernetport** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="27d2e-505">Access to the **Msvm\_InternalEthernetPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="27d2e-506">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="27d2e-506">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="27d2e-507">Beispiele</span><span class="sxs-lookup"><span data-stu-id="27d2e-507">Examples</span></span>

<span data-ttu-id="27d2e-508">Weitere Informationen finden Sie unter [Abfragen von Netzwerk Objekten](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="27d2e-508">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="27d2e-509">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27d2e-509">Requirements</span></span>



| <span data-ttu-id="27d2e-510">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27d2e-510">Requirement</span></span> | <span data-ttu-id="27d2e-511">Wert</span><span class="sxs-lookup"><span data-stu-id="27d2e-511">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27d2e-512">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="27d2e-512">Minimum supported client</span></span><br/> | <span data-ttu-id="27d2e-513">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27d2e-513">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="27d2e-514">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="27d2e-514">Minimum supported server</span></span><br/> | <span data-ttu-id="27d2e-515">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27d2e-515">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="27d2e-516">Namespace</span><span class="sxs-lookup"><span data-stu-id="27d2e-516">Namespace</span></span><br/>                | <span data-ttu-id="27d2e-517">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="27d2e-517">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="27d2e-518">MOF</span><span class="sxs-lookup"><span data-stu-id="27d2e-518">MOF</span></span><br/>                      | <dl> <span data-ttu-id="27d2e-519"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="27d2e-519"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="27d2e-520">DLL</span><span class="sxs-lookup"><span data-stu-id="27d2e-520">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27d2e-521"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="27d2e-521"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="27d2e-522">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27d2e-522">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27d2e-523">**CIM- \_ Ethernetport**</span><span class="sxs-lookup"><span data-stu-id="27d2e-523">**CIM\_EthernetPort**</span></span>](cim-ethernetport.md)
</dt> <dt>

[<span data-ttu-id="27d2e-524">**CIM- \_ Ethernetport**</span><span class="sxs-lookup"><span data-stu-id="27d2e-524">**CIM\_EthernetPort**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 

