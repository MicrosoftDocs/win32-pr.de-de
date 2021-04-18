---
description: Stellt einen Port auf dem Switch dar.
ms.assetid: a2637e53-6b28-41ad-bef9-d3a14b6cf727
title: Msvm_EthernetSwitchPort-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPort
- Msvm_EthernetSwitchPort.SetPowerState
- Msvm_EthernetSwitchPort.EnableDevice
- Msvm_EthernetSwitchPort.OnlineDevice
- Msvm_EthernetSwitchPort.QuiesceDevice
- Msvm_EthernetSwitchPort.SaveProperties
- Msvm_EthernetSwitchPort.RestoreProperties
- Msvm_EthernetSwitchPort.InstanceID
- Msvm_EthernetSwitchPort.Caption
- Msvm_EthernetSwitchPort.Description
- Msvm_EthernetSwitchPort.ElementName
- Msvm_EthernetSwitchPort.InstallDate
- Msvm_EthernetSwitchPort.Name
- Msvm_EthernetSwitchPort.OperationalStatus
- Msvm_EthernetSwitchPort.StatusDescriptions
- Msvm_EthernetSwitchPort.Status
- Msvm_EthernetSwitchPort.HealthState
- Msvm_EthernetSwitchPort.CommunicationStatus
- Msvm_EthernetSwitchPort.DetailedStatus
- Msvm_EthernetSwitchPort.OperatingStatus
- Msvm_EthernetSwitchPort.PrimaryStatus
- Msvm_EthernetSwitchPort.EnabledState
- Msvm_EthernetSwitchPort.OtherEnabledState
- Msvm_EthernetSwitchPort.RequestedState
- Msvm_EthernetSwitchPort.EnabledDefault
- Msvm_EthernetSwitchPort.TimeOfLastStateChange
- Msvm_EthernetSwitchPort.AvailableRequestedStates
- Msvm_EthernetSwitchPort.TransitioningToState
- Msvm_EthernetSwitchPort.SystemCreationClassName
- Msvm_EthernetSwitchPort.SystemName
- Msvm_EthernetSwitchPort.CreationClassName
- Msvm_EthernetSwitchPort.DeviceID
- Msvm_EthernetSwitchPort.PowerManagementSupported
- Msvm_EthernetSwitchPort.PowerManagementCapabilities
- Msvm_EthernetSwitchPort.Availability
- Msvm_EthernetSwitchPort.StatusInfo
- Msvm_EthernetSwitchPort.LastErrorCode
- Msvm_EthernetSwitchPort.ErrorDescription
- Msvm_EthernetSwitchPort.ErrorCleared
- Msvm_EthernetSwitchPort.OtherIdentifyingInfo
- Msvm_EthernetSwitchPort.PowerOnHours
- Msvm_EthernetSwitchPort.TotalPowerOnHours
- Msvm_EthernetSwitchPort.IdentifyingDescriptions
- Msvm_EthernetSwitchPort.AdditionalAvailability
- Msvm_EthernetSwitchPort.MaxQuiesceTime
- Msvm_EthernetSwitchPort.Speed
- Msvm_EthernetSwitchPort.MaxSpeed
- Msvm_EthernetSwitchPort.RequestedSpeed
- Msvm_EthernetSwitchPort.UsageRestriction
- Msvm_EthernetSwitchPort.PortType
- Msvm_EthernetSwitchPort.OtherPortType
- Msvm_EthernetSwitchPort.OtherNetworkPortType
- Msvm_EthernetSwitchPort.PortNumber
- Msvm_EthernetSwitchPort.LinkTechnology
- Msvm_EthernetSwitchPort.OtherLinkTechnology
- Msvm_EthernetSwitchPort.PermanentAddress
- Msvm_EthernetSwitchPort.NetworkAddresses
- Msvm_EthernetSwitchPort.FullDuplex
- Msvm_EthernetSwitchPort.AutoSense
- Msvm_EthernetSwitchPort.SupportedMaximumTransmissionUnit
- Msvm_EthernetSwitchPort.ActiveMaximumTransmissionUnit
- Msvm_EthernetSwitchPort.MaxDataSize
- Msvm_EthernetSwitchPort.Capabilities
- Msvm_EthernetSwitchPort.CapabilityDescriptions
- Msvm_EthernetSwitchPort.EnabledCapabilities
- Msvm_EthernetSwitchPort.OtherEnabledCapabilities
- Msvm_EthernetSwitchPort.VMQOffloadUsage
- Msvm_EthernetSwitchPort.IOVOffloadUsage
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 76c43cbe8dd053808085346b1874781f354b20dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106361093"
---
# <a name="msvm_ethernetswitchport-class"></a><span data-ttu-id="2287c-103">MSVM \_ ethernetzwitchport-Klasse</span><span class="sxs-lookup"><span data-stu-id="2287c-103">Msvm\_EthernetSwitchPort class</span></span>

<span data-ttu-id="2287c-104">Stellt einen Port auf dem Switch dar.</span><span class="sxs-lookup"><span data-stu-id="2287c-104">Represents a port on the switch.</span></span>

<span data-ttu-id="2287c-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2287c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2287c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2287c-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Switch Port";
  string   Description = "Microsoft Virtual Ethernet Switch Port";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
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
  string   SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string   SystemName;
  string   CreationClassName = "Msvm_EthernetSwitchPort";
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
  uint16   AdditionalAvailability[];
  uint64   MaxQuiesceTime;
  uint64   Speed;
  uint64   MaxSpeed;
  uint64   RequestedSpeed;
  uint16   UsageRestriction;
  uint16   PortType;
  string   OtherPortType;
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  string   NetworkAddresses[];
  boolean  FullDuplex;
  boolean  AutoSense;
  uint64   SupportedMaximumTransmissionUnit;
  uint64   ActiveMaximumTransmissionUnit;
  uint32   MaxDataSize;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  uint16   EnabledCapabilities[];
  string   OtherEnabledCapabilities[];
  uint32   VMQOffloadUsage;
  uint32   IOVOffloadUsage;
};
```

## <a name="members"></a><span data-ttu-id="2287c-107">Member</span><span class="sxs-lookup"><span data-stu-id="2287c-107">Members</span></span>

<span data-ttu-id="2287c-108">Die **MSVM \_ ethernetzwitchport** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2287c-108">The **Msvm\_EthernetSwitchPort** class has these types of members:</span></span>

-   [<span data-ttu-id="2287c-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="2287c-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="2287c-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2287c-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2287c-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="2287c-111">Methods</span></span>

<span data-ttu-id="2287c-112">Die **MSVM \_ ethernetzwitchport** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="2287c-112">The **Msvm\_EthernetSwitchPort** class has these methods.</span></span>



| <span data-ttu-id="2287c-113">Methode</span><span class="sxs-lookup"><span data-stu-id="2287c-113">Method</span></span>                                                                   | <span data-ttu-id="2287c-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2287c-114">Description</span></span>                              |
|:-------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="2287c-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="2287c-115">**EnableDevice**</span></span>                                                         | <span data-ttu-id="2287c-116">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2287c-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="2287c-117">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="2287c-117">**OnlineDevice**</span></span>                                                         | <span data-ttu-id="2287c-118">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2287c-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="2287c-119">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="2287c-119">**QuiesceDevice**</span></span>                                                        | <span data-ttu-id="2287c-120">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2287c-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="2287c-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="2287c-121">**RequestStateChange**</span></span>](msvm-ethernetswitchport-requeststatechange.md) | <span data-ttu-id="2287c-122">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="2287c-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="2287c-123">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="2287c-123">**Reset**</span></span>](msvm-ethernetswitchport-reset.md)                           | <span data-ttu-id="2287c-124">Setzt das virtuelle Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="2287c-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="2287c-125">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="2287c-125">**RestoreProperties**</span></span>                                                    | <span data-ttu-id="2287c-126">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2287c-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="2287c-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="2287c-127">**SaveProperties**</span></span>                                                       | <span data-ttu-id="2287c-128">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2287c-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="2287c-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="2287c-129">**SetPowerState**</span></span>                                                        | <span data-ttu-id="2287c-130">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2287c-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2287c-131">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2287c-131">Properties</span></span>

<span data-ttu-id="2287c-132">Die **MSVM \_ ethernetzwitchport** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2287c-132">The **Msvm\_EthernetSwitchPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2287c-133">**Activemaximumtransmissionunit**</span><span class="sxs-lookup"><span data-stu-id="2287c-133">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-134">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2287c-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2287c-136">Qualifizierer: **Einheiten** ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="2287c-136">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2287c-137">Die aktive oder ausgehandelte maximale Übertragungseinheit (Maximum Transmission Unit, MTU), die unterstützt werden kann, in Bytes.</span><span class="sxs-lookup"><span data-stu-id="2287c-137">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="2287c-138">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2287c-138">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="2287c-139">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="2287c-139">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-140">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="2287c-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2287c-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-142">Alle zusätzlichen Verfügbarkeit und der Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="2287c-142">Any additional availability and status of the device.</span></span> <span data-ttu-id="2287c-143">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2287c-143">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2287c-144">**AutoSense**</span><span class="sxs-lookup"><span data-stu-id="2287c-144">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-145">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="2287c-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-147">Gibt an, ob der Port die Geschwindigkeit oder andere Kommunikationsmerkmale der angeschlossenen Netzwerk Medien automatisch bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="2287c-147">Indicates whether the port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="2287c-148">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2287c-148">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="2287c-149">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="2287c-149">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-150">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2287c-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-152">Die primäre Verfügbarkeit und den Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="2287c-152">The primary availability and status of the device.</span></span> <span data-ttu-id="2287c-153">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2287c-153">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2287c-154">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="2287c-154">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-155">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="2287c-155">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2287c-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-157">Gibt die möglichen Werte für den *requestedstate* -Parameter der [**requestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) -Methode an, die zum Initiieren einer Zustandsänderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2287c-157">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="2287c-158">Bei den aufgelisteten Werten handelt es sich um eine Teilmenge der Werte in der **requestedstaatsupported** -Eigenschaft der zugeordneten Instanz von **CIM \_ enabledlogicalelementfunctions**, bei der die ausgewählten Werte eine Funktion des aktuellen Zustands des [**CIM- \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))sind.</span><span class="sxs-lookup"><span data-stu-id="2287c-158">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="2287c-159">Diese Eigenschaft darf nicht **null** sein, wenn eine Implementierung den Satz möglicher Werte als Funktion des aktuellen Zustands ankündigen kann.</span><span class="sxs-lookup"><span data-stu-id="2287c-159">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="2287c-160">Diese Eigenschaft ist **null** , wenn eine Implementierung den Satz möglicher Werte nicht als Funktion des aktuellen Zustands bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="2287c-160">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="2287c-161">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="2287c-161">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="2287c-162"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="2287c-162"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-163"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="2287c-163"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-164"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Herunter** fahren (4)</span><span class="sxs-lookup"><span data-stu-id="2287c-164"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-165"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="2287c-165"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-166"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="2287c-166"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-167"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>Zurück **stellen (8** )</span><span class="sxs-lookup"><span data-stu-id="2287c-167"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-168"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Still **legung (9** )</span><span class="sxs-lookup"><span data-stu-id="2287c-168"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-169"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Neustart** (10)</span><span class="sxs-lookup"><span data-stu-id="2287c-169"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-170"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Zurücksetzen** (11)</span><span class="sxs-lookup"><span data-stu-id="2287c-170"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-171"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reserviert** (..</span><span class="sxs-lookup"><span data-stu-id="2287c-171"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="2287c-172">)</span><span class="sxs-lookup"><span data-stu-id="2287c-172">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2287c-173">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="2287c-173">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-174">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="2287c-174">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2287c-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-176">Ein Array, das die Funktionen des Ports angibt.</span><span class="sxs-lookup"><span data-stu-id="2287c-176">An array that specifies the capabilities of the port.</span></span> <span data-ttu-id="2287c-177">Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2287c-177">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="2287c-178"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="2287c-178"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-179"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="2287c-179"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-180"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**Alertonlan** (2)</span><span class="sxs-lookup"><span data-stu-id="2287c-180"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-181"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**Wake-on-LAN** (3)</span><span class="sxs-lookup"><span data-stu-id="2287c-181"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-182"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Failover** (4)</span><span class="sxs-lookup"><span data-stu-id="2287c-182"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-183"><span id="LoadBalancing_"></span><span id="loadbalancing_"></span><span id="LOADBALANCING_"></span>**Loadbalancing** (5)</span><span class="sxs-lookup"><span data-stu-id="2287c-183"><span id="LoadBalancing_"></span><span id="loadbalancing_"></span><span id="LOADBALANCING_"></span>**LoadBalancing** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2287c-184">**Capabilitybeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="2287c-184">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-185">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="2287c-185">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2287c-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-187">Ein Array von Freiform-Zeichen folgen, das Ausführlichere Erläuterungen für die Port Funktionen enthält **, die im Funktions Array enthalten** sind.</span><span class="sxs-lookup"><span data-stu-id="2287c-187">An array of free-form strings that provides more detailed explanations for the port features that are contained in the **Capabilities** array.</span></span> <span data-ttu-id="2287c-188">Jeder Eintrag dieses Arrays bezieht sich auf den entsprechenden Eintrag im **Funktions Array, der sich** am selben Index befindet.</span><span class="sxs-lookup"><span data-stu-id="2287c-188">Each entry of this array is related to the corresponding entry in the **Capabilities** array that is located at the same index.</span></span> <span data-ttu-id="2287c-189">Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2287c-189">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="2287c-190">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2287c-190">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-191">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2287c-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-193">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="2287c-193">A short description of the object.</span></span> <span data-ttu-id="2287c-194">Diese Eigenschaft wird von der [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) -Klasse geerbt und ist immer auf "Ethernet-Switchport" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2287c-194">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class, and it is always set to "Ethernet Switch Port".</span></span>

</dd> <dt>

<span data-ttu-id="2287c-195">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="2287c-195">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-196">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2287c-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-198">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="2287c-198">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="2287c-199">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="2287c-199">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2287c-200">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2287c-200">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2287c-201">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="2287c-201">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-202">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2287c-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-204">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="2287c-204">The scoping system's creation class name.</span></span> <span data-ttu-id="2287c-205">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf "MSVM \_ ethernetzwitchport" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2287c-205">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_EthernetSwitchPort".</span></span>

</dd> <dt>

<span data-ttu-id="2287c-206">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2287c-206">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-207">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2287c-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-208">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-209">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="2287c-209">A description of the object.</span></span> <span data-ttu-id="2287c-210">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Microsoft Virtual Ethernet Switch Port" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2287c-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Virtual Ethernet Switch Port".</span></span>

</dd> <dt>

<span data-ttu-id="2287c-211">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="2287c-211">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-212">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2287c-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-213">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-214">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="2287c-214">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="2287c-215">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="2287c-215">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2287c-216">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2287c-216">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2287c-217">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="2287c-217">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-218">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2287c-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-219">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-220">Eine Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="2287c-220">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="2287c-221">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2287c-221">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2287c-222">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="2287c-222">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-223">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2287c-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-225">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2287c-225">A display name for the object.</span></span> <span data-ttu-id="2287c-226">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2287c-226">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2287c-227">**Enabled-Funktionen**</span><span class="sxs-lookup"><span data-stu-id="2287c-227">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-228">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="2287c-228">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2287c-229">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-230">Gibt an, welche Funktionen aus der Liste aller unter **stützten Funktionen im Funktions Array aktiviert** werden.</span><span class="sxs-lookup"><span data-stu-id="2287c-230">Specifies which capabilities are enabled from the list of all supported capabilities in the **Capabilities** array.</span></span> <span data-ttu-id="2287c-231">Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2287c-231">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="2287c-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="2287c-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-233"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="2287c-233"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-234"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**Alertonlan** (2)</span><span class="sxs-lookup"><span data-stu-id="2287c-234"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-235"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**Wake-on-LAN** (3)</span><span class="sxs-lookup"><span data-stu-id="2287c-235"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-236"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Failover** (4)</span><span class="sxs-lookup"><span data-stu-id="2287c-236"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-237"><span id="LoadBalancing_"></span><span id="loadbalancing_"></span><span id="LOADBALANCING_"></span>**Loadbalancing** (5)</span><span class="sxs-lookup"><span data-stu-id="2287c-237"><span id="LoadBalancing_"></span><span id="loadbalancing_"></span><span id="LOADBALANCING_"></span>**LoadBalancing** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2287c-238">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="2287c-238">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-239">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2287c-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-240">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-241">Die Standard-oder Startkonfiguration eines Administrators für die **enabledstate** -Eigenschaft eines Elements.</span><span class="sxs-lookup"><span data-stu-id="2287c-241">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="2287c-242">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 2 (aktiviert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2287c-242">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="2287c-243">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="2287c-243">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-244">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2287c-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-245">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-246">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="2287c-246">The enabled and disabled states of an element.</span></span> <span data-ttu-id="2287c-247">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, und es handelt sich um einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="2287c-247">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="2287c-248">Wert</span><span class="sxs-lookup"><span data-stu-id="2287c-248">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="2287c-249">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2287c-249">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="2287c-250"><dt>**Aktiviert**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2287c-250"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="2287c-251">Das-Element wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2287c-251">The element is running.</span></span><br/>    |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="2287c-252"><dt>**Deaktiviert**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2287c-252"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="2287c-253">Das Element ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="2287c-253">The element is turned off.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2287c-254">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="2287c-254">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-255">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="2287c-255">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-256">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-257">Gibt an, ob der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="2287c-257">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="2287c-258">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2287c-258">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2287c-259">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="2287c-259">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-260">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2287c-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-261">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-262">Eine Zeichenfolge, die weitere Informationen über den Fehler enthält, der in **LastErrorCode** aufgezeichnet wurde, sowie Informationen über alle Maßnahmen, die ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="2287c-262">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="2287c-263">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2287c-263">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2287c-264">**Vollduplex**</span><span class="sxs-lookup"><span data-stu-id="2287c-264">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-265">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="2287c-265">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-266">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-267">Gibt an, ob der Port im Vollduplex Modus betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="2287c-267">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="2287c-268">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2287c-268">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="2287c-269">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="2287c-269">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-270">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2287c-270">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-271">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-272">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="2287c-272">The current health of the element.</span></span> <span data-ttu-id="2287c-273">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 5 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2287c-273">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="2287c-274">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="2287c-274">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-275">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="2287c-275">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2287c-276">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-277">Ein Array von Freiform-Zeichen folgen, die Erklärungen und Details hinter den Einträgen im Eigenschafts Array " **OtherIdentifyingInfo** " bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="2287c-277">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="2287c-278">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2287c-278">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2287c-279">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2287c-279">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-280">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="2287c-280">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-281">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-282">Das Datum und die Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="2287c-282">The date and time when the object was installed.</span></span> <span data-ttu-id="2287c-283">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="2287c-283">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="2287c-284">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2287c-284">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2287c-285">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2287c-285">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-286">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2287c-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-287">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2287c-288">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="2287c-288">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2287c-289">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="2287c-289">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="2287c-290">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2287c-290">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2287c-291">**Iovoffloadusage**</span><span class="sxs-lookup"><span data-stu-id="2287c-291">**IOVOffloadUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-292">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2287c-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-293">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-294">Die aktuelle e/a-Virtualisierung (IOV)-Auslastungs Auslastung an diesem Port.</span><span class="sxs-lookup"><span data-stu-id="2287c-294">The current I/O virtualization (IOV) offload usage on this port.</span></span> <span data-ttu-id="2287c-295">Die Verwendung ist die Menge der IOV-Ressourcen, die auf dem Port verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2287c-295">The usage is the amount of IOV resources in use on the port.</span></span>

</dd> <dt>

<span data-ttu-id="2287c-296">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2287c-296">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-297">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2287c-297">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-298">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-299">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="2287c-299">The last error code reported by the logical device.</span></span> <span data-ttu-id="2287c-300">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2287c-300">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2287c-301">**Linktechnology**</span><span class="sxs-lookup"><span data-stu-id="2287c-301">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-302">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2287c-302">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-303">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-304">Gibt den Typ der Link Technologie für den Port an.</span><span class="sxs-lookup"><span data-stu-id="2287c-304">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="2287c-305">Wenn der Wert auf 1 (Sonstiges) festgelegt ist, enthält die **otherlinktechnology** -Eigenschaft eine Zeichen folgen Beschreibung des linktyps.</span><span class="sxs-lookup"><span data-stu-id="2287c-305">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="2287c-306">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2287c-306">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="2287c-307"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="2287c-307"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-308"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="2287c-308"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-309"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="2287c-309"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-310"><span id="IB"></span><span id="ib"></span>**IB** (3)</span><span class="sxs-lookup"><span data-stu-id="2287c-310"><span id="IB"></span><span id="ib"></span>**IB** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-311"><span id="FC"></span><span id="fc"></span>**FC** (4)</span><span class="sxs-lookup"><span data-stu-id="2287c-311"><span id="FC"></span><span id="fc"></span>**FC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-312"><span id="FDDI"></span><span id="fddi"></span>**F-di** (5)</span><span class="sxs-lookup"><span data-stu-id="2287c-312"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-313"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span><span class="sxs-lookup"><span data-stu-id="2287c-313"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-314"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**TokenRing** (7)</span><span class="sxs-lookup"><span data-stu-id="2287c-314"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-315"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span><span class="sxs-lookup"><span data-stu-id="2287c-315"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-316"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrarot** (9)</span><span class="sxs-lookup"><span data-stu-id="2287c-316"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (9)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-317"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**Bluetooth** (10)</span><span class="sxs-lookup"><span data-stu-id="2287c-317"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**BlueTooth** (10)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-318"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Drahtlos LAN** (11)</span><span class="sxs-lookup"><span data-stu-id="2287c-318"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Wireless LAN** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2287c-319">**Maxdatasize**</span><span class="sxs-lookup"><span data-stu-id="2287c-319">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-320">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2287c-320">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-321">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-322">Die maximale Größe des Felds Info (nicht-Mac), das empfangen oder übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="2287c-322">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="2287c-323">Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)geerbt und ist immer auf 1500 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2287c-323">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="2287c-324">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="2287c-324">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-325">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2287c-325">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-326">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-327">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="2287c-327">This property has been deprecated.</span></span> <span data-ttu-id="2287c-328">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2287c-328">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2287c-329">**MAXSPEED**</span><span class="sxs-lookup"><span data-stu-id="2287c-329">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-330">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2287c-330">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-331">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2287c-332">Qualifizierer: **Einheiten** ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="2287c-332">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="2287c-333">Die maximale Bandbreite des Ports (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="2287c-333">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="2287c-334">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="2287c-334">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2287c-335">**Name**</span><span class="sxs-lookup"><span data-stu-id="2287c-335">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-336">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2287c-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-337">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-338">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="2287c-338">The label by which the object is known.</span></span> <span data-ttu-id="2287c-339">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2287c-339">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2287c-340">**"Networkaddresses"**</span><span class="sxs-lookup"><span data-stu-id="2287c-340">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-341">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="2287c-341">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2287c-342">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2287c-343">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="2287c-343">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="2287c-344">Ein Array von Zeichen folgen, die die Mac-Adressen für den Port enthalten.</span><span class="sxs-lookup"><span data-stu-id="2287c-344">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="2287c-345">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2287c-345">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="2287c-346">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="2287c-346">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-347">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2287c-347">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-348">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-349">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="2287c-349">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="2287c-350">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="2287c-350">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2287c-351">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2287c-351">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2287c-352">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="2287c-352">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-353">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="2287c-353">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2287c-354">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-355">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="2287c-355">The current statuses of the object.</span></span> <span data-ttu-id="2287c-356">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf 2 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2287c-356">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="2287c-357">**Otherenabled-Funktionen**</span><span class="sxs-lookup"><span data-stu-id="2287c-357">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-358">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="2287c-358">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2287c-359">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-360">Ein Array von Freiform-Zeichen folgen, das Ausführlichere Erläuterungen für jede der aktivierten Funktionen bereitstellt, die als 1 (Sonstiges) angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="2287c-360">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as 1 (Other).</span></span> <span data-ttu-id="2287c-361">Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2287c-361">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="2287c-362">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="2287c-362">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-363">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2287c-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-364">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-365">Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2287c-365">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="2287c-366">Diese Eigenschaft muss auf **null** festgelegt werden, wenn die **enabledstate** -Eigenschaft einen anderen Wert als 1 hat.</span><span class="sxs-lookup"><span data-stu-id="2287c-366">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="2287c-367">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2287c-367">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2287c-368">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="2287c-368">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-369">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="2287c-369">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2287c-370">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-371">Alle zusätzlichen Daten über Geräte-ID-Informationen, die zur Identifizierung eines logischen Geräts verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="2287c-371">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="2287c-372">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2287c-372">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2287c-373">**Otherlinktechnology**</span><span class="sxs-lookup"><span data-stu-id="2287c-373">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-374">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2287c-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-375">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-376">Ein Zeichen folgen Wert, der **linktechnology** beschreibt, wenn er auf 1 festgelegt ist (andere).</span><span class="sxs-lookup"><span data-stu-id="2287c-376">A string value that describes **LinkTechnology** when it is set to 1, (Other).</span></span> <span data-ttu-id="2287c-377">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2287c-377">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="2287c-378">**Othernetworkporttype**</span><span class="sxs-lookup"><span data-stu-id="2287c-378">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-379">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2287c-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-380">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-381">Die Verwendung dieser Eigenschaft wird anstelle der **portType** -Eigenschaft als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="2287c-381">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="2287c-382">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2287c-382">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="2287c-383">**Otherporttype**</span><span class="sxs-lookup"><span data-stu-id="2287c-383">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-384">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2287c-384">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-385">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-386">Beschreibt den Modultyp, wenn **portType** auf 1 (Other) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2287c-386">Describes the type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="2287c-387">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="2287c-387">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2287c-388">**Permanent Address**</span><span class="sxs-lookup"><span data-stu-id="2287c-388">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-389">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2287c-389">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-390">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2287c-391">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="2287c-391">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="2287c-392">Die Netzwerkadresse, die in einem Port hart codiert ist.</span><span class="sxs-lookup"><span data-stu-id="2287c-392">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="2287c-393">Diese hart codierte Adresse kann mithilfe eines Firmware-Upgrades oder einer Softwarekonfiguration geändert werden.</span><span class="sxs-lookup"><span data-stu-id="2287c-393">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="2287c-394">Wenn diese Änderung vorgenommen wird, sollte das Feld gleichzeitig aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="2287c-394">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="2287c-395">Diese Eigenschaft sollte **null** sein, wenn keine hart codierte Adresse für den Netzwerkadapter vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2287c-395">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="2287c-396">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2287c-396">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="2287c-397">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="2287c-397">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-398">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2287c-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-399">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-400">Die Portnummer.</span><span class="sxs-lookup"><span data-stu-id="2287c-400">The port number.</span></span> <span data-ttu-id="2287c-401">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2287c-401">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="2287c-402">**PortType**</span><span class="sxs-lookup"><span data-stu-id="2287c-402">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-403">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2287c-403">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-404">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-405">Der bestimmte Modus, der derzeit für den Port aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2287c-405">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="2287c-406">Wenn der Wert auf 1 (Sonstiges) festgelegt ist, enthält die zugehörige **otherporttype** -Eigenschaft eine Zeichen folgen Beschreibung des Port Typs.</span><span class="sxs-lookup"><span data-stu-id="2287c-406">When set to 1 (Other), the related **OtherPortType** property contains a string description of the type of port.</span></span> <span data-ttu-id="2287c-407">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="2287c-407">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="2287c-408"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="2287c-408"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-409"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="2287c-409"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-410"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**50 Kupfer 10BaseT** (50)</span><span class="sxs-lookup"><span data-stu-id="2287c-410"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-411"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100-BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="2287c-411"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-412"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100 BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="2287c-412"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-413"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000 BaseT** (53)</span><span class="sxs-lookup"><span data-stu-id="2287c-413"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-414"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500baset** (54)</span><span class="sxs-lookup"><span data-stu-id="2287c-414"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-415"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10gbaset** (55)</span><span class="sxs-lookup"><span data-stu-id="2287c-415"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-416"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="2287c-416"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-417"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**100 Fibre 100Base-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="2287c-417"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-418"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100BASE-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="2287c-418"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-419"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000 Base-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="2287c-419"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-420"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000 Base-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="2287c-420"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-421"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000 Base-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="2287c-421"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-422"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="2287c-422"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-423"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="2287c-423"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-424"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="2287c-424"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-425"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="2287c-425"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-426"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="2287c-426"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-427"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-er** (110)</span><span class="sxs-lookup"><span data-stu-id="2287c-427"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-428"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span><span class="sxs-lookup"><span data-stu-id="2287c-428"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-429"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (16000.65535)</span><span class="sxs-lookup"><span data-stu-id="2287c-429"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (16000..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2287c-430">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="2287c-430">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-431">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="2287c-431">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2287c-432">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-433">Die Energie Verwaltungsfunktionen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="2287c-433">The power management capabilities of the device.</span></span> <span data-ttu-id="2287c-434">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2287c-434">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2287c-435">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="2287c-435">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-436">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="2287c-436">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-437">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-438">Gibt an, ob das Gerät Energie gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="2287c-438">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="2287c-439">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2287c-439">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2287c-440">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="2287c-440">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-441">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2287c-441">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-442">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-443">Gibt an, wie viele aufeinanderfolgende Stunden dieses Gerät seit dem letzten Strom Umgebung eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="2287c-443">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="2287c-444">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2287c-444">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2287c-445">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="2287c-445">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-446">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2287c-446">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-447">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-448">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="2287c-448">Provides high level status information.</span></span> <span data-ttu-id="2287c-449">Diese Eigenschaft sollte in Verbindung mit der **detailedstatus** -Eigenschaft verwendet werden, um allgemeine und ausführliche Integritäts Statusinformationen für das-Element und seine unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="2287c-449">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="2287c-450">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="2287c-450">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2287c-451">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2287c-451">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2287c-452">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="2287c-452">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-453">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2287c-453">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-454">Zugriffstyp: schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-454">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="2287c-455">Qualifizierer: **Einheiten** ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="2287c-455">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="2287c-456">Die angeforderte Bandbreite des Ports (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="2287c-456">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="2287c-457">Die tatsächliche Bandbreite wird in der Eigenschaft **Geschwindigkeit** gemeldet.</span><span class="sxs-lookup"><span data-stu-id="2287c-457">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="2287c-458">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="2287c-458">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2287c-459">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="2287c-459">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-460">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2287c-460">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-461">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-461">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-462">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="2287c-462">The last requested or desired state for the element.</span></span> <span data-ttu-id="2287c-463">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 12 (nicht zutreffend) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2287c-463">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="2287c-464">**Geschwindigkeit**</span><span class="sxs-lookup"><span data-stu-id="2287c-464">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-465">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2287c-465">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-466">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2287c-467">Qualifizierer: **Einheiten** ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="2287c-467">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="2287c-468">Die Bandbreite des Ports (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="2287c-468">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="2287c-469">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="2287c-469">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2287c-470">**Status**</span><span class="sxs-lookup"><span data-stu-id="2287c-470">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-471">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2287c-471">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-472">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-473">Der aktuelle Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="2287c-473">The current status of the object.</span></span> <span data-ttu-id="2287c-474">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2287c-474">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2287c-475">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="2287c-475">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-476">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="2287c-476">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2287c-477">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-477">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-478">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="2287c-478">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="2287c-479">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2287c-479">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2287c-480">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="2287c-480">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-481">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2287c-481">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-482">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-482">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-483">Der aktuelle Zustand des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="2287c-483">The current state of the logical device.</span></span> <span data-ttu-id="2287c-484">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2287c-484">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2287c-485">**Supportedmaximumtransmissionunit**</span><span class="sxs-lookup"><span data-stu-id="2287c-485">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-486">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2287c-486">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-487">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2287c-488">Qualifizierer: **Einheiten** ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="2287c-488">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2287c-489">Die maximale Anzahl von Übertragungs Einheiten (MTU), die unterstützt werden können, in Byte.</span><span class="sxs-lookup"><span data-stu-id="2287c-489">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="2287c-490">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2287c-490">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="2287c-491">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="2287c-491">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-492">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2287c-492">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-493">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-493">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-494">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="2287c-494">The scoping system's creation class name.</span></span> <span data-ttu-id="2287c-495">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf "MSVM \_ virtualethernwitch" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2287c-495">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_VirtualEthernetSwitch".</span></span>

</dd> <dt>

<span data-ttu-id="2287c-496">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="2287c-496">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-497">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2287c-497">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-498">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-498">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-499">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="2287c-499">The scoping system's name.</span></span> <span data-ttu-id="2287c-500">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2287c-500">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2287c-501">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="2287c-501">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-502">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="2287c-502">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-503">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-503">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-504">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="2287c-504">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="2287c-505">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2287c-505">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2287c-506">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="2287c-506">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-507">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2287c-507">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-508">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-508">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-509">Die Gesamtanzahl der Stunden, für die dieses Gerät eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="2287c-509">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="2287c-510">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2287c-510">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2287c-511">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="2287c-511">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-512">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2287c-512">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-513">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-513">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-514">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="2287c-514">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="2287c-515">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2287c-515">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2287c-516">**Einsatz Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="2287c-516">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-517">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2287c-517">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-518">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-518">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-519">Unter bestimmten Umständen kann ein logischer Port als Front-End-oder Back-End-Port identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="2287c-519">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="2287c-520">Ein Beispiel für diese Situation wäre ein Speicher Array, das Back-End-Ports für die Kommunikation mit Datenträgern und Front-End-Ports für die Kommunikation mit Hosts aufweisen könnte.</span><span class="sxs-lookup"><span data-stu-id="2287c-520">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="2287c-521">Wenn keine Einschränkung für die Verwendung des Ports vorliegt, sollte der Wert auf 4 (nicht eingeschränkt) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="2287c-521">If there is no restriction on the use of the port, then the value should be set to 4 (Not restricted).</span></span> <span data-ttu-id="2287c-522">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="2287c-522">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="2287c-523"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="2287c-523"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-524"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Nur Front-End** (2)</span><span class="sxs-lookup"><span data-stu-id="2287c-524"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-525"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Nur Back-End** (3)</span><span class="sxs-lookup"><span data-stu-id="2287c-525"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2287c-526"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Nicht eingeschränkt** (4)</span><span class="sxs-lookup"><span data-stu-id="2287c-526"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Not restricted** (4 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2287c-527">**Vmqoffloadusage**</span><span class="sxs-lookup"><span data-stu-id="2287c-527">**VMQOffloadUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2287c-528">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2287c-528">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2287c-529">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2287c-529">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2287c-530">Die aktuelle Virtual Machine Queue (VMQ)-Auslastungs Auslastung an diesem Port.</span><span class="sxs-lookup"><span data-stu-id="2287c-530">The current virtual machine queue (VMQ) offloading usage on this port.</span></span> <span data-ttu-id="2287c-531">Die Verwendung ist die Menge der VMQ-Ressourcen, die auf dem Port verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2287c-531">The usage is the amount of VMQ resources in use on the port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2287c-532">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2287c-532">Requirements</span></span>



| <span data-ttu-id="2287c-533">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2287c-533">Requirement</span></span> | <span data-ttu-id="2287c-534">Wert</span><span class="sxs-lookup"><span data-stu-id="2287c-534">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2287c-535">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2287c-535">Minimum supported client</span></span><br/> | <span data-ttu-id="2287c-536">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2287c-536">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2287c-537">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2287c-537">Minimum supported server</span></span><br/> | <span data-ttu-id="2287c-538">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2287c-538">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2287c-539">Namespace</span><span class="sxs-lookup"><span data-stu-id="2287c-539">Namespace</span></span><br/>                | <span data-ttu-id="2287c-540">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="2287c-540">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2287c-541">MOF</span><span class="sxs-lookup"><span data-stu-id="2287c-541">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2287c-542"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2287c-542"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2287c-543">DLL</span><span class="sxs-lookup"><span data-stu-id="2287c-543">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2287c-544"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2287c-544"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

