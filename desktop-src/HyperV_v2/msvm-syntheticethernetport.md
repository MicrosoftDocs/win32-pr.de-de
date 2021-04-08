---
description: Stellt einen synthetischen Ethernet-Adapter dar.
ms.assetid: B5CB86A9-015B-42E8-ADF4-2F61970D8437
title: Msvm_SyntheticEthernetPort-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticEthernetPort
- Msvm_SyntheticEthernetPort.SetPowerState
- Msvm_SyntheticEthernetPort.EnableDevice
- Msvm_SyntheticEthernetPort.OnlineDevice
- Msvm_SyntheticEthernetPort.QuiesceDevice
- Msvm_SyntheticEthernetPort.SaveProperties
- Msvm_SyntheticEthernetPort.RestoreProperties
- Msvm_SyntheticEthernetPort.InstanceID
- Msvm_SyntheticEthernetPort.Caption
- Msvm_SyntheticEthernetPort.Description
- Msvm_SyntheticEthernetPort.ElementName
- Msvm_SyntheticEthernetPort.InstallDate
- Msvm_SyntheticEthernetPort.Name
- Msvm_SyntheticEthernetPort.OperationalStatus
- Msvm_SyntheticEthernetPort.StatusDescriptions
- Msvm_SyntheticEthernetPort.Status
- Msvm_SyntheticEthernetPort.HealthState
- Msvm_SyntheticEthernetPort.CommunicationStatus
- Msvm_SyntheticEthernetPort.DetailedStatus
- Msvm_SyntheticEthernetPort.OperatingStatus
- Msvm_SyntheticEthernetPort.PrimaryStatus
- Msvm_SyntheticEthernetPort.EnabledState
- Msvm_SyntheticEthernetPort.OtherEnabledState
- Msvm_SyntheticEthernetPort.RequestedState
- Msvm_SyntheticEthernetPort.EnabledDefault
- Msvm_SyntheticEthernetPort.TimeOfLastStateChange
- Msvm_SyntheticEthernetPort.AvailableRequestedStates
- Msvm_SyntheticEthernetPort.TransitioningToState
- Msvm_SyntheticEthernetPort.SystemCreationClassName
- Msvm_SyntheticEthernetPort.SystemName
- Msvm_SyntheticEthernetPort.CreationClassName
- Msvm_SyntheticEthernetPort.DeviceID
- Msvm_SyntheticEthernetPort.PowerManagementSupported
- Msvm_SyntheticEthernetPort.PowerManagementCapabilities
- Msvm_SyntheticEthernetPort.Availability
- Msvm_SyntheticEthernetPort.StatusInfo
- Msvm_SyntheticEthernetPort.LastErrorCode
- Msvm_SyntheticEthernetPort.ErrorDescription
- Msvm_SyntheticEthernetPort.ErrorCleared
- Msvm_SyntheticEthernetPort.OtherIdentifyingInfo
- Msvm_SyntheticEthernetPort.PowerOnHours
- Msvm_SyntheticEthernetPort.TotalPowerOnHours
- Msvm_SyntheticEthernetPort.IdentifyingDescriptions
- Msvm_SyntheticEthernetPort.AdditionalAvailability
- Msvm_SyntheticEthernetPort.MaxQuiesceTime
- Msvm_SyntheticEthernetPort.Speed
- Msvm_SyntheticEthernetPort.MaxSpeed
- Msvm_SyntheticEthernetPort.RequestedSpeed
- Msvm_SyntheticEthernetPort.UsageRestriction
- Msvm_SyntheticEthernetPort.PortType
- Msvm_SyntheticEthernetPort.OtherPortType
- Msvm_SyntheticEthernetPort.OtherNetworkPortType
- Msvm_SyntheticEthernetPort.PortNumber
- Msvm_SyntheticEthernetPort.LinkTechnology
- Msvm_SyntheticEthernetPort.OtherLinkTechnology
- Msvm_SyntheticEthernetPort.PermanentAddress
- Msvm_SyntheticEthernetPort.NetworkAddresses
- Msvm_SyntheticEthernetPort.FullDuplex
- Msvm_SyntheticEthernetPort.AutoSense
- Msvm_SyntheticEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_SyntheticEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_SyntheticEthernetPort.MaxDataSize
- Msvm_SyntheticEthernetPort.Capabilities
- Msvm_SyntheticEthernetPort.CapabilityDescriptions
- Msvm_SyntheticEthernetPort.EnabledCapabilities
- Msvm_SyntheticEthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c8e2a8c2207e410878a4f5c498ea71a1ce67cd8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863875"
---
# <a name="msvm_syntheticethernetport-class"></a><span data-ttu-id="36d43-103">MSVM \_ syntheticethernetport-Klasse</span><span class="sxs-lookup"><span data-stu-id="36d43-103">Msvm\_SyntheticEthernetPort class</span></span>

<span data-ttu-id="36d43-104">Stellt einen synthetischen Ethernet-Adapter dar.</span><span class="sxs-lookup"><span data-stu-id="36d43-104">Represents a synthetic Ethernet adapter.</span></span> <span data-ttu-id="36d43-105">Dieser Adapter ist der bevorzugte Netzwerkadapter aufgrund seiner Leistung und, da Änderungen an der IT sofort wirksam werden können, während Sie verwendet werden (Hot Configurability).</span><span class="sxs-lookup"><span data-stu-id="36d43-105">This adapter is the preferred network adapter because of its performance and because changes to it can take effect right away, while it is in use (hot configurability).</span></span>

<span data-ttu-id="36d43-106">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="36d43-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="36d43-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="36d43-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
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
  uint16   AdditionalAvailability[] = 6;
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
};
```

## <a name="members"></a><span data-ttu-id="36d43-108">Member</span><span class="sxs-lookup"><span data-stu-id="36d43-108">Members</span></span>

<span data-ttu-id="36d43-109">Die **MSVM \_ syntheticethernetport** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="36d43-109">The **Msvm\_SyntheticEthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="36d43-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="36d43-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="36d43-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="36d43-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="36d43-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="36d43-112">Methods</span></span>

<span data-ttu-id="36d43-113">Die **MSVM \_ syntheticethernetport** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="36d43-113">The **Msvm\_SyntheticEthernetPort** class has these methods.</span></span>



| <span data-ttu-id="36d43-114">Methode</span><span class="sxs-lookup"><span data-stu-id="36d43-114">Method</span></span>                                                                      | <span data-ttu-id="36d43-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36d43-115">Description</span></span>                              |
|:----------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="36d43-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="36d43-116">**EnableDevice**</span></span>                                                            | <span data-ttu-id="36d43-117">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="36d43-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="36d43-118">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="36d43-118">**OnlineDevice**</span></span>                                                            | <span data-ttu-id="36d43-119">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="36d43-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="36d43-120">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="36d43-120">**QuiesceDevice**</span></span>                                                           | <span data-ttu-id="36d43-121">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="36d43-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="36d43-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="36d43-122">**RequestStateChange**</span></span>](msvm-syntheticethernetport-requeststatechange.md) | <span data-ttu-id="36d43-123">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="36d43-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="36d43-124">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="36d43-124">**Reset**</span></span>](msvm-syntheticethernetport-reset.md)                           | <span data-ttu-id="36d43-125">Setzt das Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="36d43-125">Resets the device.</span></span><br/>            |
| <span data-ttu-id="36d43-126">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="36d43-126">**RestoreProperties**</span></span>                                                       | <span data-ttu-id="36d43-127">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="36d43-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="36d43-128">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="36d43-128">**SaveProperties**</span></span>                                                          | <span data-ttu-id="36d43-129">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="36d43-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="36d43-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="36d43-130">**SetPowerState**</span></span>                                                           | <span data-ttu-id="36d43-131">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="36d43-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="36d43-132">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="36d43-132">Properties</span></span>

<span data-ttu-id="36d43-133">Die **MSVM \_ syntheticethernetport** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="36d43-133">The **Msvm\_SyntheticEthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="36d43-134">**Activemaximumtransmissionunit**</span><span class="sxs-lookup"><span data-stu-id="36d43-134">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-135">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="36d43-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36d43-137">Qualifizierer: **Einheiten** ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="36d43-137">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="36d43-138">Die aktive oder ausgehandelte maximale Übertragungseinheit (Maximum Transmission Unit, MTU), die unterstützt werden kann.</span><span class="sxs-lookup"><span data-stu-id="36d43-138">The active or negotiated maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="36d43-139">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-139">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-140">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="36d43-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-141">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="36d43-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="36d43-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-143">Zusätzliche Verfügbarkeit und Status des Geräts, über das hinaus, das in der **Availability** -Eigenschaft angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="36d43-143">Additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="36d43-144">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf 6 festgelegt (nicht zutreffend).</span><span class="sxs-lookup"><span data-stu-id="36d43-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-145">**AutoSense**</span><span class="sxs-lookup"><span data-stu-id="36d43-145">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-146">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="36d43-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-148">Gibt an, ob der Netzwerkport die Geschwindigkeit oder andere Kommunikationsmerkmale der angeschlossenen Netzwerk Medien automatisch bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="36d43-148">Indicates whether the network port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="36d43-149">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-149">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-150">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="36d43-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-151">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="36d43-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-153">Die primäre Verfügbarkeit und den Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="36d43-153">The primary availability and status of the device.</span></span> <span data-ttu-id="36d43-154">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-155">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="36d43-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-156">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="36d43-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="36d43-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-158">Gibt die möglichen Werte für den *requestedstate* -Parameter der [**requestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) -Methode an, die zum Initiieren einer Zustandsänderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="36d43-158">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="36d43-159">Bei den aufgelisteten Werten handelt es sich um eine Teilmenge der Werte in der **requestedstaatsupported** -Eigenschaft der zugeordneten Instanz von **CIM \_ enabledlogicalelementfunctions**, bei der die ausgewählten Werte eine Funktion des aktuellen Zustands des [**CIM- \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))sind.</span><span class="sxs-lookup"><span data-stu-id="36d43-159">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="36d43-160">Diese Eigenschaft darf nicht **null** sein, wenn eine Implementierung den Satz möglicher Werte als Funktion des aktuellen Zustands ankündigen kann.</span><span class="sxs-lookup"><span data-stu-id="36d43-160">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="36d43-161">Diese Eigenschaft ist **null** , wenn eine Implementierung den Satz möglicher Werte nicht als Funktion des aktuellen Zustands bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="36d43-161">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="36d43-162">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-162">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="36d43-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="36d43-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="36d43-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="36d43-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="36d43-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Herunter** fahren (4)</span><span class="sxs-lookup"><span data-stu-id="36d43-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="36d43-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="36d43-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="36d43-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="36d43-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="36d43-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>Zurück **stellen (8** )</span><span class="sxs-lookup"><span data-stu-id="36d43-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="36d43-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Still **legung (9** )</span><span class="sxs-lookup"><span data-stu-id="36d43-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="36d43-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Neustart** (10)</span><span class="sxs-lookup"><span data-stu-id="36d43-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="36d43-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Zurücksetzen** (11)</span><span class="sxs-lookup"><span data-stu-id="36d43-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="36d43-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reserviert** (..</span><span class="sxs-lookup"><span data-stu-id="36d43-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="36d43-173">)</span><span class="sxs-lookup"><span data-stu-id="36d43-173">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="36d43-174">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="36d43-174">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-175">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="36d43-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="36d43-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-177">Die Funktionen des Ethernet-Ports.</span><span class="sxs-lookup"><span data-stu-id="36d43-177">The capabilities of the Ethernet port.</span></span> <span data-ttu-id="36d43-178">Das Gerät unterstützt z. b. alertonlan, wakeonlan, Lastenausgleich oder Failover.</span><span class="sxs-lookup"><span data-stu-id="36d43-178">For example, the device might support AlertOnLan, WakeOnLan, Load Balancing, or FailOver.</span></span> <span data-ttu-id="36d43-179">Wenn Failover-oder Lasten Ausgleichs Funktionen aufgelistet werden, sollte auch eine SpareGroup (Failover) oder extracapacitygroup (Lastenausgleich) definiert werden, um die Funktion vollständig zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="36d43-179">If failover or load balancing capabilities are listed, a SpareGroup (failover) or ExtraCapacityGroup (load balancing) should also be defined to completely describe the capability.</span></span> <span data-ttu-id="36d43-180">Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="36d43-180">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="36d43-181">**Capabilitybeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="36d43-181">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-182">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="36d43-182">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="36d43-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-184">Ein Array von Freiform-Zeichen folgen, das Ausführlichere Erläuterungen für alle Ethernetport-Funktionen bereitstellt, die im Eigenschafts Array der **Funktionen** angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="36d43-184">An array of free-form strings that provides more detailed explanations for any of the EthernetPort features that are indicated in the **Capabilities** property array.</span></span> <span data-ttu-id="36d43-185">Beachten Sie, dass jeder Eintrag dieses Arrays mit dem Eintrag im Eigenschafts Array " **Funktionen** " verknüpft ist, der sich am selben Index befindet.</span><span class="sxs-lookup"><span data-stu-id="36d43-185">Note, each entry of this array is related to the entry in the **Capabilities** property array that is located at the same index.</span></span> <span data-ttu-id="36d43-186">Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="36d43-186">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="36d43-187">**Caption**</span><span class="sxs-lookup"><span data-stu-id="36d43-187">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-188">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="36d43-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-190">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="36d43-190">A short description of the object.</span></span> <span data-ttu-id="36d43-191">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-191">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-192">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="36d43-192">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-193">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="36d43-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-195">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="36d43-195">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="36d43-196">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="36d43-196">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="36d43-197">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-197">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-198">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="36d43-198">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-199">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="36d43-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-200">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-201">Der Name der Klasse oder der Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="36d43-201">The name of the class or the subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="36d43-202">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-202">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-203">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="36d43-203">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-204">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="36d43-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-205">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-206">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="36d43-206">A description of the object.</span></span> <span data-ttu-id="36d43-207">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-207">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-208">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="36d43-208">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-209">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="36d43-209">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-210">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-211">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="36d43-211">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="36d43-212">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="36d43-212">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="36d43-213">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-213">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-214">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="36d43-214">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-215">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="36d43-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-216">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-217">Eine Adresse oder andere identifizierende Informationen, die verwendet werden, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="36d43-217">An address or other identifying information used to uniquely name the logical device.</span></span> <span data-ttu-id="36d43-218">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-218">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-219">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="36d43-219">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-220">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="36d43-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-221">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-222">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="36d43-222">A display name for the object.</span></span> <span data-ttu-id="36d43-223">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-223">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-224">**Enabled-Funktionen**</span><span class="sxs-lookup"><span data-stu-id="36d43-224">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-225">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="36d43-225">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="36d43-226">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-227">Die Funktionen, die in der Liste aller unterstützten Funktionen aktiviert sind, die im Eigenschafts Array " **Funktionen** " definiert sind.</span><span class="sxs-lookup"><span data-stu-id="36d43-227">The capabilities that are enabled from the list of all supported ones, which are defined in the **Capabilities** property array.</span></span> <span data-ttu-id="36d43-228">Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="36d43-228">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="36d43-229">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="36d43-229">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-230">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="36d43-230">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-231">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-232">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="36d43-232">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="36d43-233">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-233">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-234">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="36d43-234">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-235">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="36d43-235">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-236">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-237">Der aktivierte und deaktivierte Status dieses Elements.</span><span class="sxs-lookup"><span data-stu-id="36d43-237">The enabled and disabled states of this element.</span></span> <span data-ttu-id="36d43-238">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-238">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-239">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="36d43-239">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-240">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="36d43-240">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-241">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-242">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="36d43-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="36d43-243">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="36d43-243">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-244">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="36d43-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-245">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-246">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="36d43-246">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="36d43-247">**Vollduplex**</span><span class="sxs-lookup"><span data-stu-id="36d43-247">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-248">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="36d43-248">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-249">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-250">Gibt an, ob der Port im Vollduplex Modus betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="36d43-250">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="36d43-251">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-251">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-252">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="36d43-252">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-253">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="36d43-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-254">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-255">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="36d43-255">The current health of the element.</span></span> <span data-ttu-id="36d43-256">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-257">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="36d43-257">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-258">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="36d43-258">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="36d43-259">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-260">Ein Array von Freiform-Zeichen folgen, die Erklärungen und Details hinter den Einträgen im " **OtherIdentifyingInfo** "-Array bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="36d43-260">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="36d43-261">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="36d43-261">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="36d43-262">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="36d43-262">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-263">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="36d43-263">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-264">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-265">Das Datum, an dem der Ethernet-Port dem virtuellen Computer hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="36d43-265">The date the Ethernet port was added to the virtual machine.</span></span> <span data-ttu-id="36d43-266">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-266">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-267">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="36d43-267">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-268">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="36d43-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-269">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36d43-270">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="36d43-270">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="36d43-271">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="36d43-271">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="36d43-272">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-272">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-273">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="36d43-273">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-274">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="36d43-274">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-275">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-276">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="36d43-276">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="36d43-277">**Linktechnology**</span><span class="sxs-lookup"><span data-stu-id="36d43-277">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-278">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="36d43-278">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-279">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-280">Eine Enumeration der Linktypen.</span><span class="sxs-lookup"><span data-stu-id="36d43-280">An enumeration of the types of links.</span></span> <span data-ttu-id="36d43-281">Wenn der Wert auf 1 (Other) festgelegt ist, enthält die zugehörige Eigenschaft **otherlinktechnology** eine Zeichen folgen Beschreibung des linktyps.</span><span class="sxs-lookup"><span data-stu-id="36d43-281">When set to 1 (Other), the related property **OtherLinkTechnology** contains a string description of the type of link.</span></span> <span data-ttu-id="36d43-282">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-282">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="36d43-283"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="36d43-283"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="36d43-284">**Maxdatasize**</span><span class="sxs-lookup"><span data-stu-id="36d43-284">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-285">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="36d43-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-286">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-287">Die maximale Größe des Felds Info (nicht-Mac), das empfangen oder übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="36d43-287">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="36d43-288">Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-288">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-289">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="36d43-289">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-290">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="36d43-290">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-291">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-292">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="36d43-292">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="36d43-293">**MAXSPEED**</span><span class="sxs-lookup"><span data-stu-id="36d43-293">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-294">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="36d43-294">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-295">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36d43-296">Qualifizierer: **Einheiten** ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="36d43-296">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="36d43-297">Die maximale Bandbreite des Ports in Bits pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="36d43-297">The maximum bandwidth of the port in bits per second.</span></span> <span data-ttu-id="36d43-298">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-298">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-299">**Name**</span><span class="sxs-lookup"><span data-stu-id="36d43-299">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-300">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="36d43-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-301">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-302">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="36d43-302">A display name for the object.</span></span> <span data-ttu-id="36d43-303">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-303">This property is inherited from [**CIM\_ManagedSystemElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-304">**"Networkaddresses"**</span><span class="sxs-lookup"><span data-stu-id="36d43-304">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-305">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="36d43-305">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="36d43-306">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-307">Ethernet/802.3-Mac-Adressen, die als zwölf hexadezimal Ziffern formatiert sind (z. b. "010203040506"), wobei jedes Paar eines der sechs Oktette der Mac-Adresse in kanonischer bidirektionalen Reihenfolge darstellt (das Gruppen Adressbit befindet sich im niedrig wertigen Bit des ersten Zeichens der Zeichenfolge).</span><span class="sxs-lookup"><span data-stu-id="36d43-307">Ethernet/802.3 MAC addresses formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order (the Group address bit is found in the low order bit of the first character of the string).</span></span> <span data-ttu-id="36d43-308">Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="36d43-308">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="36d43-309">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="36d43-309">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-310">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="36d43-310">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-311">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-312">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="36d43-312">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="36d43-313">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="36d43-313">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="36d43-314">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-314">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-315">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="36d43-315">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-316">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="36d43-316">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="36d43-317">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-318">Der aktuelle Status des Elements.</span><span class="sxs-lookup"><span data-stu-id="36d43-318">The current status of the element.</span></span> <span data-ttu-id="36d43-319">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 2 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="36d43-319">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-320">**Otherenabled-Funktionen**</span><span class="sxs-lookup"><span data-stu-id="36d43-320">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-321">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="36d43-321">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="36d43-322">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-323">Ein Array von Freiform-Zeichen folgen, das Ausführlichere Erläuterungen für jede der aktivierten Funktionen bereitstellt, die als "Other" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="36d43-323">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as "Other".</span></span> <span data-ttu-id="36d43-324">Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="36d43-324">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="36d43-325">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="36d43-325">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-326">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="36d43-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-327">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-328">Der aktivierte oder deaktivierte Status des Elements, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="36d43-328">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="36d43-329">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-329">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-330">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="36d43-330">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-331">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="36d43-331">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="36d43-332">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-333">Alle Daten, zusätzlich zu den Informationen zur Geräte-ID, die zum Identifizieren eines logischen Geräts verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="36d43-333">Any data, in addition to device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="36d43-334">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="36d43-334">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="36d43-335">**Otherlinktechnology**</span><span class="sxs-lookup"><span data-stu-id="36d43-335">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-336">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="36d43-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-337">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-338">Ein Zeichen folgen Wert, der **linktechnology** beschreibt, wenn es auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="36d43-338">A string value that describes **LinkTechnology** when it is set to 1 (Other).</span></span> <span data-ttu-id="36d43-339">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-339">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-340">**Othernetworkporttype**</span><span class="sxs-lookup"><span data-stu-id="36d43-340">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-341">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="36d43-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-342">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-343">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) geerbt und auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="36d43-343">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) and is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="36d43-344">**Otherporttype**</span><span class="sxs-lookup"><span data-stu-id="36d43-344">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-345">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="36d43-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-346">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-347">Der Modultyp, wenn **portType** auf 1 (Other) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="36d43-347">The type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="36d43-348">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-348">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-349">**Permanent Address**</span><span class="sxs-lookup"><span data-stu-id="36d43-349">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-350">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="36d43-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-351">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-352">Die Netzwerkadresse, die in den Port hart codiert ist.</span><span class="sxs-lookup"><span data-stu-id="36d43-352">The network address that is hardcoded into the port.</span></span> <span data-ttu-id="36d43-353">Diese hart codierte Adresse kann mithilfe eines Firmwareupdates oder einer Softwarekonfiguration geändert werden.</span><span class="sxs-lookup"><span data-stu-id="36d43-353">This hardcoded address can be changed using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="36d43-354">Wenn diese Änderung vorgenommen wird, sollte das Feld gleichzeitig aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="36d43-354">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="36d43-355">Die **permanentaddress** -Eigenschaft sollte leer gelassen werden, wenn keine hart codierte Adresse für den Netzwerkadapter vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="36d43-355">The **PermanentAddress** property should be left blank if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="36d43-356">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-356">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-357">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="36d43-357">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-358">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="36d43-358">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-359">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-360">Netzwerkports sind häufig in Bezug auf ein logisches Modul oder ein Netzwerkelement nummeriert.</span><span class="sxs-lookup"><span data-stu-id="36d43-360">Network ports are often numbered relative to either a logical module or a network element.</span></span> <span data-ttu-id="36d43-361">Dieser Wert ist 1 für emulierten NICs, 0 für alle anderen.</span><span class="sxs-lookup"><span data-stu-id="36d43-361">This value is 1 for emulated NICs, 0 for all others.</span></span> <span data-ttu-id="36d43-362">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-362">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-363">**PortType**</span><span class="sxs-lookup"><span data-stu-id="36d43-363">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-364">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="36d43-364">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-365">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-366">Der bestimmte Modus, der derzeit für den Port aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="36d43-366">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="36d43-367">Wenn der Wert auf 1 (Sonstiges) festgelegt ist, enthält die zugehörige Eigenschaft **otherporttype** eine Zeichen folgen Beschreibung für den Porttyp.</span><span class="sxs-lookup"><span data-stu-id="36d43-367">When set to 1 (Other), the related property **OtherPortType** contains a string description of the type of port.</span></span> <span data-ttu-id="36d43-368">Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-368">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-369">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="36d43-369">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-370">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="36d43-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="36d43-371">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-372">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="36d43-372">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="36d43-373">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="36d43-373">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-374">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="36d43-374">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-375">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-376">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="36d43-376">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="36d43-377">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="36d43-377">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-378">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="36d43-378">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-379">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-380">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="36d43-380">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="36d43-381">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="36d43-381">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-382">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="36d43-382">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-383">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-384">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="36d43-384">Provides high level status information.</span></span> <span data-ttu-id="36d43-385">Diese Eigenschaft sollte in Verbindung mit der **detailedstatus** -Eigenschaft verwendet werden, um allgemeine und ausführliche Integritäts Statusinformationen für das-Element und seine unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="36d43-385">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="36d43-386">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="36d43-386">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="36d43-387">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-387">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-388">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="36d43-388">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-389">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="36d43-389">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-390">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36d43-391">Qualifizierer: **Einheiten** ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="36d43-391">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="36d43-392">Die angeforderte Bandbreite des Ports (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="36d43-392">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="36d43-393">Die tatsächliche Bandbreite wird in der Eigenschaft **Geschwindigkeit** gemeldet.</span><span class="sxs-lookup"><span data-stu-id="36d43-393">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="36d43-394">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-394">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-395">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="36d43-395">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-396">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="36d43-396">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-397">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-398">Der zuletzt angeforderte oder gewünschte Status für den Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="36d43-398">The last requested or desired state for the management service.</span></span> <span data-ttu-id="36d43-399">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-399">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-400">**Geschwindigkeit**</span><span class="sxs-lookup"><span data-stu-id="36d43-400">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-401">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="36d43-401">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-402">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36d43-403">Qualifizierer: **Einheiten** ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="36d43-403">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="36d43-404">Die aktuelle Bandbreite des Ports (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="36d43-404">The current bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="36d43-405">Für Ports, die die Bandbreite variieren, oder für diejenigen, bei denen keine genaue Schätzung vorgenommen werden kann, sollte diese Eigenschaft die nominale Bandbreite enthalten.</span><span class="sxs-lookup"><span data-stu-id="36d43-405">For ports that vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span> <span data-ttu-id="36d43-406">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-406">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-407">**Status**</span><span class="sxs-lookup"><span data-stu-id="36d43-407">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-408">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="36d43-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-409">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-410">Der aktuelle Status des Elements.</span><span class="sxs-lookup"><span data-stu-id="36d43-410">The current status of the element.</span></span> <span data-ttu-id="36d43-411">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-411">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-412">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="36d43-412">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-413">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="36d43-413">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="36d43-414">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-415">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="36d43-415">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="36d43-416">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-416">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-417">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="36d43-417">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-418">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="36d43-418">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-419">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-420">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="36d43-420">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="36d43-421">**Supportedmaximumtransmissionunit**</span><span class="sxs-lookup"><span data-stu-id="36d43-421">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-422">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="36d43-422">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-423">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-423">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36d43-424">Qualifizierer: **Einheiten** ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="36d43-424">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="36d43-425">Die maximale Übertragungseinheit (MTU), die unterstützt werden kann.</span><span class="sxs-lookup"><span data-stu-id="36d43-425">The maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="36d43-426">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-426">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-427">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="36d43-427">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-428">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="36d43-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-429">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-430">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="36d43-430">The creation class name of the scoping system.</span></span> <span data-ttu-id="36d43-431">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-431">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-432">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="36d43-432">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-433">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="36d43-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-434">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-435">Der NetBIOS-Name des hostingcomputersystems.</span><span class="sxs-lookup"><span data-stu-id="36d43-435">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="36d43-436">Diese Eigenschaft enthält die ID der virtuellen Maschine im **GUID** -Format.</span><span class="sxs-lookup"><span data-stu-id="36d43-436">This property will contain the virtual machine ID in **GUID** form.</span></span> <span data-ttu-id="36d43-437">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-437">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-438">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="36d43-438">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-439">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="36d43-439">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-440">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-441">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="36d43-441">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="36d43-442">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-442">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-443">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="36d43-443">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-444">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="36d43-444">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-445">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-446">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="36d43-446">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="36d43-447">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="36d43-447">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-448">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="36d43-448">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-449">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-450">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="36d43-450">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="36d43-451">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-451">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="36d43-452">**Einsatz Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="36d43-452">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d43-453">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="36d43-453">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="36d43-454">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36d43-454">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36d43-455">Unter bestimmten Umständen kann ein logischer Port als Front-End-oder Back-End-Port identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="36d43-455">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="36d43-456">Wenn keine Einschränkung für die Verwendung des Ports vorliegt, sollte der Wert auf 4 (nicht eingeschränkt) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="36d43-456">If there is no restriction on the use of the port, then the value should be set to 4 (Not Restricted).</span></span> <span data-ttu-id="36d43-457">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="36d43-457">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="36d43-458">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="36d43-458">Remarks</span></span>

<span data-ttu-id="36d43-459">Der Zugriff auf die **MSVM \_ syntheticethernetport** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="36d43-459">Access to the **Msvm\_SyntheticEthernetPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="36d43-460">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="36d43-460">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="36d43-461">Beispiele</span><span class="sxs-lookup"><span data-stu-id="36d43-461">Examples</span></span>

<span data-ttu-id="36d43-462">Weitere Informationen finden Sie unter [Abfragen von Netzwerk Objekten](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="36d43-462">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="36d43-463">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="36d43-463">Requirements</span></span>



| <span data-ttu-id="36d43-464">Anforderung</span><span class="sxs-lookup"><span data-stu-id="36d43-464">Requirement</span></span> | <span data-ttu-id="36d43-465">Wert</span><span class="sxs-lookup"><span data-stu-id="36d43-465">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36d43-466">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="36d43-466">Minimum supported client</span></span><br/> | <span data-ttu-id="36d43-467">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36d43-467">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="36d43-468">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="36d43-468">Minimum supported server</span></span><br/> | <span data-ttu-id="36d43-469">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36d43-469">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="36d43-470">Namespace</span><span class="sxs-lookup"><span data-stu-id="36d43-470">Namespace</span></span><br/>                | <span data-ttu-id="36d43-471">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="36d43-471">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="36d43-472">MOF</span><span class="sxs-lookup"><span data-stu-id="36d43-472">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36d43-473"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="36d43-473"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="36d43-474">DLL</span><span class="sxs-lookup"><span data-stu-id="36d43-474">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36d43-475"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="36d43-475"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="36d43-476">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36d43-476">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36d43-477">**CIM- \_ Ethernetport**</span><span class="sxs-lookup"><span data-stu-id="36d43-477">**CIM\_EthernetPort**</span></span>](cim-ethernetport.md)
</dt> <dt>

[<span data-ttu-id="36d43-478">**CIM- \_ Ethernetport**</span><span class="sxs-lookup"><span data-stu-id="36d43-478">**CIM\_EthernetPort**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 

