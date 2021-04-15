---
description: Stellt einen externen Ethernet-Port (Netzwerkadapter) dar.
ms.assetid: 70901587-641D-46F5-8A35-FEA483D336DE
title: Msvm_ExternalEthernetPort-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ExternalEthernetPort
- Msvm_ExternalEthernetPort.SetPowerState
- Msvm_ExternalEthernetPort.EnableDevice
- Msvm_ExternalEthernetPort.OnlineDevice
- Msvm_ExternalEthernetPort.QuiesceDevice
- Msvm_ExternalEthernetPort.SaveProperties
- Msvm_ExternalEthernetPort.RestoreProperties
- Msvm_ExternalEthernetPort.InstanceID
- Msvm_ExternalEthernetPort.Caption
- Msvm_ExternalEthernetPort.Description
- Msvm_ExternalEthernetPort.ElementName
- Msvm_ExternalEthernetPort.InstallDate
- Msvm_ExternalEthernetPort.Name
- Msvm_ExternalEthernetPort.OperationalStatus
- Msvm_ExternalEthernetPort.StatusDescriptions
- Msvm_ExternalEthernetPort.Status
- Msvm_ExternalEthernetPort.HealthState
- Msvm_ExternalEthernetPort.CommunicationStatus
- Msvm_ExternalEthernetPort.DetailedStatus
- Msvm_ExternalEthernetPort.OperatingStatus
- Msvm_ExternalEthernetPort.PrimaryStatus
- Msvm_ExternalEthernetPort.EnabledState
- Msvm_ExternalEthernetPort.OtherEnabledState
- Msvm_ExternalEthernetPort.RequestedState
- Msvm_ExternalEthernetPort.EnabledDefault
- Msvm_ExternalEthernetPort.TimeOfLastStateChange
- Msvm_ExternalEthernetPort.AvailableRequestedStates
- Msvm_ExternalEthernetPort.TransitioningToState
- Msvm_ExternalEthernetPort.SystemCreationClassName
- Msvm_ExternalEthernetPort.SystemName
- Msvm_ExternalEthernetPort.CreationClassName
- Msvm_ExternalEthernetPort.DeviceID
- Msvm_ExternalEthernetPort.PowerManagementSupported
- Msvm_ExternalEthernetPort.PowerManagementCapabilities
- Msvm_ExternalEthernetPort.Availability
- Msvm_ExternalEthernetPort.StatusInfo
- Msvm_ExternalEthernetPort.LastErrorCode
- Msvm_ExternalEthernetPort.ErrorDescription
- Msvm_ExternalEthernetPort.ErrorCleared
- Msvm_ExternalEthernetPort.OtherIdentifyingInfo
- Msvm_ExternalEthernetPort.PowerOnHours
- Msvm_ExternalEthernetPort.TotalPowerOnHours
- Msvm_ExternalEthernetPort.IdentifyingDescriptions
- Msvm_ExternalEthernetPort.AdditionalAvailability
- Msvm_ExternalEthernetPort.MaxQuiesceTime
- Msvm_ExternalEthernetPort.Speed
- Msvm_ExternalEthernetPort.MaxSpeed
- Msvm_ExternalEthernetPort.RequestedSpeed
- Msvm_ExternalEthernetPort.UsageRestriction
- Msvm_ExternalEthernetPort.PortType
- Msvm_ExternalEthernetPort.OtherPortType
- Msvm_ExternalEthernetPort.OtherNetworkPortType
- Msvm_ExternalEthernetPort.PortNumber
- Msvm_ExternalEthernetPort.LinkTechnology
- Msvm_ExternalEthernetPort.OtherLinkTechnology
- Msvm_ExternalEthernetPort.PermanentAddress
- Msvm_ExternalEthernetPort.NetworkAddresses
- Msvm_ExternalEthernetPort.FullDuplex
- Msvm_ExternalEthernetPort.AutoSense
- Msvm_ExternalEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_ExternalEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_ExternalEthernetPort.MaxDataSize
- Msvm_ExternalEthernetPort.Capabilities
- Msvm_ExternalEthernetPort.CapabilityDescriptions
- Msvm_ExternalEthernetPort.EnabledCapabilities
- Msvm_ExternalEthernetPort.OtherEnabledCapabilities
- Msvm_ExternalEthernetPort.IsBound
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 507c2235c1fda5f43ba025172e276b30e2f0aa85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526852"
---
# <a name="msvm_externalethernetport-class"></a><span data-ttu-id="074b4-103">MSVM \_ externalethernetport-Klasse</span><span class="sxs-lookup"><span data-stu-id="074b4-103">Msvm\_ExternalEthernetPort class</span></span>

<span data-ttu-id="074b4-104">Stellt einen externen Ethernet-Port (Netzwerkadapter) dar.</span><span class="sxs-lookup"><span data-stu-id="074b4-104">Represents an external Ethernet port (network adapter).</span></span> <span data-ttu-id="074b4-105">Diese Art von Ethernet-Ports ermöglicht virtuellen Computern den Zugriff auf das externe Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="074b4-105">These types of Ethernet ports give virtual machines access to the external network.</span></span>

<span data-ttu-id="074b4-106">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="074b4-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="074b4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="074b4-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ExternalEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Port";
  string   Description = "Microsoft External Ethernet Port";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status = "OK";
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
  string   CreationClassName = "Msvm_ExternalEthernetPort";
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
  string   AdditionalAvailability[];
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
  boolean  IsBound;
};
```

## <a name="members"></a><span data-ttu-id="074b4-108">Member</span><span class="sxs-lookup"><span data-stu-id="074b4-108">Members</span></span>

<span data-ttu-id="074b4-109">Die **MSVM \_ externalethernetport** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="074b4-109">The **Msvm\_ExternalEthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="074b4-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="074b4-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="074b4-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="074b4-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="074b4-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="074b4-112">Methods</span></span>

<span data-ttu-id="074b4-113">Die **MSVM \_ externalethernetport** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="074b4-113">The **Msvm\_ExternalEthernetPort** class has these methods.</span></span>



| <span data-ttu-id="074b4-114">Methode</span><span class="sxs-lookup"><span data-stu-id="074b4-114">Method</span></span>                                                                     | <span data-ttu-id="074b4-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="074b4-115">Description</span></span>                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="074b4-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="074b4-116">**EnableDevice**</span></span>                                                           | <span data-ttu-id="074b4-117">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="074b4-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="074b4-118">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="074b4-118">**OnlineDevice**</span></span>                                                           | <span data-ttu-id="074b4-119">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="074b4-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="074b4-120">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="074b4-120">**QuiesceDevice**</span></span>                                                          | <span data-ttu-id="074b4-121">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="074b4-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="074b4-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="074b4-122">**RequestStateChange**</span></span>](msvm-externalethernetport-requeststatechange.md) | <span data-ttu-id="074b4-123">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="074b4-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="074b4-124">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="074b4-124">**Reset**</span></span>](msvm-externalethernetport-reset.md)                           | <span data-ttu-id="074b4-125">Setzt das virtuelle Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="074b4-125">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="074b4-126">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="074b4-126">**RestoreProperties**</span></span>                                                      | <span data-ttu-id="074b4-127">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="074b4-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="074b4-128">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="074b4-128">**SaveProperties**</span></span>                                                         | <span data-ttu-id="074b4-129">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="074b4-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="074b4-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="074b4-130">**SetPowerState**</span></span>                                                          | <span data-ttu-id="074b4-131">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="074b4-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="074b4-132">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="074b4-132">Properties</span></span>

<span data-ttu-id="074b4-133">Die **MSVM \_ externalethernetport** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="074b4-133">The **Msvm\_ExternalEthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="074b4-134">**Activemaximumtransmissionunit**</span><span class="sxs-lookup"><span data-stu-id="074b4-134">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-135">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="074b4-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="074b4-137">Qualifizierer: **Einheiten** ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="074b4-137">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="074b4-138">Die aktive oder ausgehandelte maximale Übertragungseinheit (Maximum Transmission Unit, MTU), die unterstützt werden kann, in Bytes.</span><span class="sxs-lookup"><span data-stu-id="074b4-138">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="074b4-139">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-139">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="074b4-140">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="074b4-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-141">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="074b4-141">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="074b4-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-143">Alle zusätzlichen Verfügbarkeit und den Status des Geräts, außer den in der **Availability** -Eigenschaft angegebenen.</span><span class="sxs-lookup"><span data-stu-id="074b4-143">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="074b4-144">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="074b4-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="074b4-145">**AutoSense**</span><span class="sxs-lookup"><span data-stu-id="074b4-145">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-146">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="074b4-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-148">Gibt an, ob der Netzwerkport die Geschwindigkeit oder andere Kommunikationsmerkmale der angeschlossenen Netzwerk Medien automatisch bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="074b4-148">Indicates whether the network port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="074b4-149">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-149">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="074b4-150">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="074b4-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-151">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="074b4-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-153">Die primäre Verfügbarkeit und den Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="074b4-153">The primary availability and status of the device.</span></span> <span data-ttu-id="074b4-154">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="074b4-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="074b4-155">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="074b4-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-156">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="074b4-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="074b4-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-158">Gibt die möglichen Werte für den *requestedstate* -Parameter der [**requestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) -Methode an, die zum Initiieren einer Zustandsänderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="074b4-158">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="074b4-159">Bei den aufgelisteten Werten handelt es sich um eine Teilmenge der Werte in der **requestedstaatsupported** -Eigenschaft der zugeordneten Instanz von **CIM \_ enabledlogicalelementfunctions**, bei der die ausgewählten Werte eine Funktion des aktuellen Zustands des [**CIM- \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))sind.</span><span class="sxs-lookup"><span data-stu-id="074b4-159">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="074b4-160">Diese Eigenschaft darf nicht **null** sein, wenn eine Implementierung den Satz möglicher Werte als Funktion des aktuellen Zustands ankündigen kann.</span><span class="sxs-lookup"><span data-stu-id="074b4-160">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="074b4-161">Diese Eigenschaft ist **null** , wenn eine Implementierung den Satz möglicher Werte nicht als Funktion des aktuellen Zustands bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="074b4-161">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="074b4-162">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-162">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="074b4-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="074b4-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="074b4-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Herunter** fahren (4)</span><span class="sxs-lookup"><span data-stu-id="074b4-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="074b4-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="074b4-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>Zurück **stellen (8** )</span><span class="sxs-lookup"><span data-stu-id="074b4-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Still **legung (9** )</span><span class="sxs-lookup"><span data-stu-id="074b4-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Neustart** (10)</span><span class="sxs-lookup"><span data-stu-id="074b4-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Zurücksetzen** (11)</span><span class="sxs-lookup"><span data-stu-id="074b4-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reserviert** (..</span><span class="sxs-lookup"><span data-stu-id="074b4-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="074b4-173">)</span><span class="sxs-lookup"><span data-stu-id="074b4-173">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="074b4-174">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="074b4-174">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-175">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="074b4-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="074b4-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-177">Ein Array, das die Funktionen des Ports angibt.</span><span class="sxs-lookup"><span data-stu-id="074b4-177">An array that specifies the capabilities of the port.</span></span> <span data-ttu-id="074b4-178">Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-178">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="074b4-179"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="074b4-179"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-180"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="074b4-180"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-181"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**Alertonlan** (2)</span><span class="sxs-lookup"><span data-stu-id="074b4-181"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-182"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**Wake-on-LAN** (3)</span><span class="sxs-lookup"><span data-stu-id="074b4-182"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-183"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Failover** (4)</span><span class="sxs-lookup"><span data-stu-id="074b4-183"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-184"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**Loadbalancing** (5)</span><span class="sxs-lookup"><span data-stu-id="074b4-184"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="074b4-185">**Capabilitybeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="074b4-185">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-186">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="074b4-186">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="074b4-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-188">Ein Array von Freiform-Zeichen folgen, das Ausführlichere Erläuterungen für die Port Funktionen enthält **, die im Funktions Array enthalten** sind.</span><span class="sxs-lookup"><span data-stu-id="074b4-188">An array of free-form strings that provides more detailed explanations for the port features that are contained in the **Capabilities** array.</span></span> <span data-ttu-id="074b4-189">Jeder Eintrag dieses Arrays bezieht sich auf den entsprechenden Eintrag im **Funktions Array, der sich** am selben Index befindet.</span><span class="sxs-lookup"><span data-stu-id="074b4-189">Each entry of this array is related to the corresponding entry in the **Capabilities** array that is located at the same index.</span></span> <span data-ttu-id="074b4-190">Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-190">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="074b4-191">**Caption**</span><span class="sxs-lookup"><span data-stu-id="074b4-191">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-192">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="074b4-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="074b4-194">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="074b4-194">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="074b4-195">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="074b4-195">A short description of the object.</span></span> <span data-ttu-id="074b4-196">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ethernet-Port" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="074b4-196">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="074b4-197">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="074b4-197">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-198">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="074b4-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-200">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="074b4-200">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="074b4-201">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="074b4-201">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="074b4-202">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-202">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="074b4-203">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="074b4-203">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-204">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="074b4-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-205">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-206">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="074b4-206">The scoping system's creation class name.</span></span> <span data-ttu-id="074b4-207">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf "MSVM \_ externalethernetport" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="074b4-207">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ExternalEthernetPort".</span></span>

</dd> <dt>

<span data-ttu-id="074b4-208">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="074b4-208">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-209">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="074b4-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-210">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-211">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="074b4-211">A description of the object.</span></span> <span data-ttu-id="074b4-212">Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Microsoft externer Ethernet-Port" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="074b4-212">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft External Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="074b4-213">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="074b4-213">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-214">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="074b4-214">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-215">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-216">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="074b4-216">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="074b4-217">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="074b4-217">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="074b4-218">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-218">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="074b4-219">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="074b4-219">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-220">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="074b4-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-221">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-222">Eine Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="074b4-222">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="074b4-223">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-223">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="074b4-224">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="074b4-224">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-225">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="074b4-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-226">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-227">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="074b4-227">A display name for the object.</span></span> <span data-ttu-id="074b4-228">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-228">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="074b4-229">**Enabled-Funktionen**</span><span class="sxs-lookup"><span data-stu-id="074b4-229">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-230">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="074b4-230">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="074b4-231">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-232">Gibt an, welche Funktionen aus der Liste aller unter **stützten Funktionen im Funktions Array aktiviert** werden.</span><span class="sxs-lookup"><span data-stu-id="074b4-232">Specifies which capabilities are enabled from the list of all supported capabilities in the **Capabilities** array.</span></span> <span data-ttu-id="074b4-233">Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-233">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="074b4-234"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="074b4-234"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-235"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="074b4-235"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-236"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**Alertonlan** (2)</span><span class="sxs-lookup"><span data-stu-id="074b4-236"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-237"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**Wake-on-LAN** (3)</span><span class="sxs-lookup"><span data-stu-id="074b4-237"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-238"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Failover** (4)</span><span class="sxs-lookup"><span data-stu-id="074b4-238"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-239"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**Loadbalancing** (5)</span><span class="sxs-lookup"><span data-stu-id="074b4-239"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="074b4-240">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="074b4-240">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-241">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="074b4-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-242">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-243">Die Standard-oder Startkonfiguration eines Administrators für die **enabledstate** -Eigenschaft eines Elements.</span><span class="sxs-lookup"><span data-stu-id="074b4-243">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="074b4-244">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 2 (aktiviert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="074b4-244">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="074b4-245">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="074b4-245">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-246">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="074b4-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-247">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-248">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="074b4-248">The enabled and disabled states of an element.</span></span> <span data-ttu-id="074b4-249">Sie kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben.</span><span class="sxs-lookup"><span data-stu-id="074b4-249">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="074b4-250">Das Herunterfahren (4) und das Starten (10) sind z. b. vorübergehende Zustände zwischen aktiviertem und deaktiviertem Zustand.</span><span class="sxs-lookup"><span data-stu-id="074b4-250">For example, shutting down (4) and starting (10) are transient states between enabled and disabled.</span></span> <span data-ttu-id="074b4-251">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-251">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="074b4-252">Wert</span><span class="sxs-lookup"><span data-stu-id="074b4-252">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="074b4-253">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="074b4-253">Meaning</span></span>                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="074b4-254"><dt>**Unbekannter**</dt> Wert <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="074b4-254"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 |                                                                                                                                                                                                             |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="074b4-255"><dt>**Sonstige**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="074b4-255"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                             |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="074b4-256"><dt>**Aktiviert**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="074b4-256"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="074b4-257">Das-Element ist oder kann Befehle ausführen, verarbeitet alle in der Warteschlange befindlichen Befehle und fügt neue Anforderungen in die Warteschlange ein.</span><span class="sxs-lookup"><span data-stu-id="074b4-257">The element is or could be executing commands, will process any queued commands, and queues new requests.</span></span><br/>                                                                                        |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="074b4-258"><dt>**Deaktiviert**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="074b4-258"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="074b4-259">Das-Element führt keine Befehle aus und löscht alle neuen Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="074b4-259">The element will not execute commands and will drop any new requests.</span></span><br/>                                                                                                                            |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="074b4-260"><dt>4</dt> wird <dt>**heruntergefahren**</dt></span><span class="sxs-lookup"><span data-stu-id="074b4-260"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="074b4-261">Das Element wird gerade in den deaktivierten Zustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="074b4-261">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                      |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="074b4-262"><dt>**Nicht zutreffend**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="074b4-262"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="074b4-263">Das Element unterstützt das Aktivieren oder Deaktivieren des Elements nicht.</span><span class="sxs-lookup"><span data-stu-id="074b4-263">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                          |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="074b4-264"><dt>**Aktiviert, aber offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="074b4-264"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="074b4-265">Das Element kann Befehle abschließen und löscht alle neuen Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="074b4-265">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                     |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="074b4-266"><dt>**In Test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="074b4-266"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="074b4-267">Das-Element befindet sich in einem Testzustand.</span><span class="sxs-lookup"><span data-stu-id="074b4-267">The element is in a test state.</span></span><br/>                                                                                                                                                                  |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="074b4-268"><dt></dt> Verzögert <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="074b4-268"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="074b4-269">Das Element kann Befehle abschließen, aber alle neuen Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="074b4-269">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                    |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="074b4-270"><dt>**Inesce**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="074b4-270"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="074b4-271">Das Element ist aktiviert, jedoch in einem eingeschränkten Modus.</span><span class="sxs-lookup"><span data-stu-id="074b4-271">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="074b4-272">Das Verhalten des-Elements ähnelt dem aktivierten Zustand, verarbeitet aber nur einen eingeschränkten Satz von Befehlen.</span><span class="sxs-lookup"><span data-stu-id="074b4-272">The behavior of the element is similar to the Enabled state, but it processes only a restricted set of commands.</span></span> <span data-ttu-id="074b4-273">Alle anderen Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="074b4-273">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="074b4-274"><dt>**Start**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="074b4-274"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="074b4-275">Das Element wechselt in den Zustand "aktiviert".</span><span class="sxs-lookup"><span data-stu-id="074b4-275">The element is in the process of going to an Enabled state.</span></span> <span data-ttu-id="074b4-276">Neue Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="074b4-276">New requests are queued.</span></span><br/>                                                                                                             |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="074b4-277"><dt>**DMTF reserviert**</dt> <dt>11 32767</dt></span><span class="sxs-lookup"><span data-stu-id="074b4-277"><dt>**DMTF Reserved**</dt> <dt>11 32767</dt></span></span> </dl>                  | <span data-ttu-id="074b4-278">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="074b4-278">Reserved.</span></span><br/>                                                                                                                                                                                        |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="074b4-279"><dt>**Anbieter reserviert**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="074b4-279"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl>       | <span data-ttu-id="074b4-280">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="074b4-280">Reserved.</span></span><br/>                                                                                                                                                                                        |



 

</dd> <dt>

<span data-ttu-id="074b4-281">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="074b4-281">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-282">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="074b4-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-283">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-284">Gibt an, ob der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="074b4-284">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="074b4-285">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="074b4-285">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="074b4-286">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="074b4-286">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-287">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="074b4-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-288">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-289">Eine Zeichenfolge, die weitere Informationen über den Fehler enthält, der in **LastErrorCode** aufgezeichnet wurde, sowie Informationen über alle Maßnahmen, die ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="074b4-289">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="074b4-290">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="074b4-290">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="074b4-291">**Vollduplex**</span><span class="sxs-lookup"><span data-stu-id="074b4-291">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-292">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="074b4-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-293">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-294">Gibt an, ob der Port im Vollduplex Modus betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="074b4-294">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="074b4-295">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-295">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="074b4-296">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="074b4-296">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-297">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="074b4-297">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-298">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-299">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="074b4-299">The current health of the element.</span></span> <span data-ttu-id="074b4-300">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="074b4-300">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="074b4-301">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="074b4-301">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="074b4-302">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 5 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="074b4-302">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="074b4-303">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="074b4-303">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-304">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="074b4-304">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="074b4-305">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-306">Ein Array von Freiform-Zeichen folgen, die Erklärungen und Details hinter den Einträgen im Eigenschafts Array " **OtherIdentifyingInfo** " bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="074b4-306">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="074b4-307">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="074b4-307">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="074b4-308">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="074b4-308">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-309">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="074b4-309">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-310">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-311">Das Datum und die Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="074b4-311">The date and time when the object was installed.</span></span> <span data-ttu-id="074b4-312">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="074b4-312">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="074b4-313">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-313">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="074b4-314">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="074b4-314">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-315">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="074b4-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-316">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="074b4-317">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="074b4-317">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="074b4-318">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="074b4-318">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="074b4-319">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-319">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="074b4-320">**IsBound**</span><span class="sxs-lookup"><span data-stu-id="074b4-320">**IsBound**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-321">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="074b4-321">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-322">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-323">Wenn diese Eigenschaft **true** ist, kann dieser Ethernet-Port mit den Switches verbunden werden und somit die Konnektivität zu einem virtuellen Computer bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="074b4-323">If this property is **True**, then this Ethernet port can be connected to the switches and thus can provide connectivity to a virtual machine.</span></span> <span data-ttu-id="074b4-324">Wenn diese Eigenschaft den Wert **false** hat, wird dieser Ethernet-Port nicht von der Netzwerkarchitektur des virtuellen Computers verwendet.</span><span class="sxs-lookup"><span data-stu-id="074b4-324">If this property is **False**, then this Ethernet port is not being used by the virtual machine networking architecture.</span></span>

</dd> <dt>

<span data-ttu-id="074b4-325">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="074b4-325">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-326">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="074b4-326">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-327">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-328">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="074b4-328">The last error code reported by the logical device.</span></span> <span data-ttu-id="074b4-329">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="074b4-329">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="074b4-330">**Linktechnology**</span><span class="sxs-lookup"><span data-stu-id="074b4-330">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-331">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="074b4-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-332">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-333">Gibt den Typ der Link Technologie für den Port an.</span><span class="sxs-lookup"><span data-stu-id="074b4-333">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="074b4-334">Wenn der Wert auf 1 (Sonstiges) festgelegt ist, enthält die **otherlinktechnology** -Eigenschaft eine Zeichen folgen Beschreibung des linktyps.</span><span class="sxs-lookup"><span data-stu-id="074b4-334">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="074b4-335">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-335">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="074b4-336"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="074b4-336"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-337"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="074b4-337"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-338"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="074b4-338"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-339"><span id="IB"></span><span id="ib"></span>**IB** (3)</span><span class="sxs-lookup"><span data-stu-id="074b4-339"><span id="IB"></span><span id="ib"></span>**IB** (3)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-340"><span id="FC"></span><span id="fc"></span>**FC** (4)</span><span class="sxs-lookup"><span data-stu-id="074b4-340"><span id="FC"></span><span id="fc"></span>**FC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-341"><span id="FDDI"></span><span id="fddi"></span>**F-di** (5)</span><span class="sxs-lookup"><span data-stu-id="074b4-341"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-342"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span><span class="sxs-lookup"><span data-stu-id="074b4-342"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-343"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**TokenRing** (7)</span><span class="sxs-lookup"><span data-stu-id="074b4-343"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-344"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span><span class="sxs-lookup"><span data-stu-id="074b4-344"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-345"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrarot** (9)</span><span class="sxs-lookup"><span data-stu-id="074b4-345"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (9)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-346"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**Bluetooth** (10)</span><span class="sxs-lookup"><span data-stu-id="074b4-346"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**BlueTooth** (10)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-347"><span id="Wireless_LAN"></span><span id="wireless_lan"></span><span id="WIRELESS_LAN"></span>**Drahtlos LAN** (11)</span><span class="sxs-lookup"><span data-stu-id="074b4-347"><span id="Wireless_LAN"></span><span id="wireless_lan"></span><span id="WIRELESS_LAN"></span>**Wireless LAN** (11)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="074b4-348">**Maxdatasize**</span><span class="sxs-lookup"><span data-stu-id="074b4-348">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-349">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="074b4-349">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-350">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-351">Die maximale Größe des Felds Info (nicht-Mac), das empfangen oder übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="074b4-351">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="074b4-352">Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)geerbt und ist immer auf 1500 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="074b4-352">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="074b4-353">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="074b4-353">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-354">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="074b4-354">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-355">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-356">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="074b4-356">This property has been deprecated.</span></span> <span data-ttu-id="074b4-357">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="074b4-357">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="074b4-358">**MAXSPEED**</span><span class="sxs-lookup"><span data-stu-id="074b4-358">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-359">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="074b4-359">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-360">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="074b4-361">Qualifizierer: **Einheiten** ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="074b4-361">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="074b4-362">Die maximale Bandbreite des Ports (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="074b4-362">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="074b4-363">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-363">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="074b4-364">**Name**</span><span class="sxs-lookup"><span data-stu-id="074b4-364">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-365">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="074b4-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-366">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-367">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="074b4-367">The label by which the object is known.</span></span> <span data-ttu-id="074b4-368">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-368">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="074b4-369">**"Networkaddresses"**</span><span class="sxs-lookup"><span data-stu-id="074b4-369">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-370">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="074b4-370">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="074b4-371">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="074b4-372">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="074b4-372">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="074b4-373">Ein Array von Zeichen folgen, die die Mac-Adressen für den Port enthalten.</span><span class="sxs-lookup"><span data-stu-id="074b4-373">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="074b4-374">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-374">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="074b4-375">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="074b4-375">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-376">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="074b4-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-377">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-378">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="074b4-378">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="074b4-379">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="074b4-379">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="074b4-380">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-380">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="074b4-381">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="074b4-381">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-382">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="074b4-382">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="074b4-383">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-384">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="074b4-384">The current statuses of the object.</span></span> <span data-ttu-id="074b4-385">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf 2 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="074b4-385">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="074b4-386">**Otherenabled-Funktionen**</span><span class="sxs-lookup"><span data-stu-id="074b4-386">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-387">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="074b4-387">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="074b4-388">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-389">Ein Array von Freiform-Zeichen folgen, das Ausführlichere Erläuterungen für jede der aktivierten Funktionen bereitstellt, die als 1 (sonstige) angegeben sind. Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-389">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as 1 (Other.) This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="074b4-390">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="074b4-390">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-391">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="074b4-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-392">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-393">Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="074b4-393">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="074b4-394">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="074b4-394">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="074b4-395">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-395">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="074b4-396">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="074b4-396">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-397">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="074b4-397">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="074b4-398">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-399">Alle zusätzlichen Daten über Geräte-ID-Informationen, die zur Identifizierung eines logischen Geräts verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="074b4-399">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="074b4-400">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="074b4-400">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="074b4-401">**Otherlinktechnology**</span><span class="sxs-lookup"><span data-stu-id="074b4-401">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-402">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="074b4-402">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-403">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-403">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-404">Ein Zeichen folgen Wert, der **linktechnology** beschreibt, wenn es auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="074b4-404">A string value that describes **LinkTechnology** when it is set to 1 (Other).</span></span> <span data-ttu-id="074b4-405">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-405">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="074b4-406">**Othernetworkporttype**</span><span class="sxs-lookup"><span data-stu-id="074b4-406">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-407">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="074b4-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-408">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-409">Die Verwendung dieser Eigenschaft wird anstelle der **portType** -Eigenschaft als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="074b4-409">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="074b4-410">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-410">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="074b4-411">**Otherporttype**</span><span class="sxs-lookup"><span data-stu-id="074b4-411">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-412">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="074b4-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-413">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-414">Der Modultyp, wenn **portType** auf 1 ("Other") festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="074b4-414">The type of module, when **PortType** is set to 1 ("Other").</span></span> <span data-ttu-id="074b4-415">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-415">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="074b4-416">**Permanent Address**</span><span class="sxs-lookup"><span data-stu-id="074b4-416">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-417">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="074b4-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-418">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="074b4-419">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="074b4-419">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="074b4-420">Die Netzwerkadresse, die in einem Port hart codiert ist.</span><span class="sxs-lookup"><span data-stu-id="074b4-420">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="074b4-421">Diese hart codierte Adresse kann mithilfe eines Firmware-Upgrades oder einer Softwarekonfiguration geändert werden.</span><span class="sxs-lookup"><span data-stu-id="074b4-421">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="074b4-422">Wenn diese Änderung vorgenommen wird, sollte das Feld gleichzeitig aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="074b4-422">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="074b4-423">Diese Eigenschaft sollte **null** sein, wenn keine hart codierte Adresse für den Netzwerkadapter vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="074b4-423">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="074b4-424">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-424">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="074b4-425">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="074b4-425">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-426">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="074b4-426">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-427">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-427">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-428">Die Portnummer.</span><span class="sxs-lookup"><span data-stu-id="074b4-428">The port number.</span></span> <span data-ttu-id="074b4-429">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-429">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="074b4-430">**PortType**</span><span class="sxs-lookup"><span data-stu-id="074b4-430">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-431">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="074b4-431">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-432">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-433">Der bestimmte Modus, der derzeit für den Port aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="074b4-433">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="074b4-434">Wenn der Wert auf 1 ("Other") festgelegt ist, enthält die zugehörige Eigenschaft " **otherporttype** " eine Zeichen folgen Beschreibung für den Porttyp.</span><span class="sxs-lookup"><span data-stu-id="074b4-434">When set to 1 ("Other"), the related property **OtherPortType** contains a string description of the type of port.</span></span> <span data-ttu-id="074b4-435">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-435">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="074b4-436"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="074b4-436"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-437"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="074b4-437"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-438"><span id="__50_Copper_10BaseT"></span><span id="__50_copper_10baset"></span><span id="__50_COPPER_10BASET"></span>**50 Kupfer 10BaseT** (50)</span><span class="sxs-lookup"><span data-stu-id="074b4-438"><span id="__50_Copper_10BaseT"></span><span id="__50_copper_10baset"></span><span id="__50_COPPER_10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-439"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100-BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="074b4-439"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-440"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100 BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="074b4-440"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-441"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000 BaseT** (53)</span><span class="sxs-lookup"><span data-stu-id="074b4-441"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-442"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500baset** (54)</span><span class="sxs-lookup"><span data-stu-id="074b4-442"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-443"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10gbaset** (55)</span><span class="sxs-lookup"><span data-stu-id="074b4-443"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-444"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="074b4-444"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-445"><span id="__100_Fibre_100Base-FX"></span><span id="__100_fibre_100base-fx"></span><span id="__100_FIBRE_100BASE-FX"></span>**100 Fibre 100Base-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="074b4-445"><span id="__100_Fibre_100Base-FX"></span><span id="__100_fibre_100base-fx"></span><span id="__100_FIBRE_100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-446"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100BASE-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="074b4-446"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-447"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000 Base-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="074b4-447"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-448"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000 Base-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="074b4-448"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-449"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000 Base-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="074b4-449"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-450"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="074b4-450"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-451"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="074b4-451"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-452"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="074b4-452"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-453"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="074b4-453"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-454"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="074b4-454"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-455"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-er** (110)</span><span class="sxs-lookup"><span data-stu-id="074b4-455"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-456"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span><span class="sxs-lookup"><span data-stu-id="074b4-456"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-457"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (16000 65535)</span><span class="sxs-lookup"><span data-stu-id="074b4-457"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (16000 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="074b4-458">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="074b4-458">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-459">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="074b4-459">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="074b4-460">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-461">Die Energie Verwaltungsfunktionen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="074b4-461">The power management capabilities of the device.</span></span> <span data-ttu-id="074b4-462">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="074b4-462">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="074b4-463">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="074b4-463">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-464">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="074b4-464">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-465">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-466">Gibt an, ob das Gerät Energie gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="074b4-466">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="074b4-467">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="074b4-467">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="074b4-468">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="074b4-468">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-469">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="074b4-469">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-470">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-471">Gibt an, wie viele aufeinanderfolgende Stunden dieses Gerät seit dem letzten Strom Umgebung eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="074b4-471">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="074b4-472">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="074b4-472">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="074b4-473">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="074b4-473">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-474">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="074b4-474">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-475">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-476">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="074b4-476">Provides high level status information.</span></span> <span data-ttu-id="074b4-477">Diese Eigenschaft sollte in Verbindung mit der **detailedstatus** -Eigenschaft verwendet werden, um allgemeine und ausführliche Integritäts Statusinformationen für das-Element und seine unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="074b4-477">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="074b4-478">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="074b4-478">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="074b4-479">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-479">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="074b4-480">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="074b4-480">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-481">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="074b4-481">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-482">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="074b4-483">Qualifizierer: **Einheiten** ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="074b4-483">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="074b4-484">Die angeforderte Bandbreite des Ports in Bits pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="074b4-484">The requested bandwidth of the port in bits per second.</span></span> <span data-ttu-id="074b4-485">Die tatsächliche Bandbreite wird in der Eigenschaft **Geschwindigkeit** gemeldet.</span><span class="sxs-lookup"><span data-stu-id="074b4-485">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="074b4-486">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-486">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="074b4-487">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="074b4-487">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-488">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="074b4-488">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-489">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-489">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-490">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="074b4-490">The last requested or desired state for the element.</span></span> <span data-ttu-id="074b4-491">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 12 (nicht zutreffend) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="074b4-491">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="074b4-492">**Geschwindigkeit**</span><span class="sxs-lookup"><span data-stu-id="074b4-492">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-493">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="074b4-493">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-494">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="074b4-495">Qualifizierer: **Einheiten** ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="074b4-495">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="074b4-496">Die Bandbreite des Ports (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="074b4-496">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="074b4-497">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-497">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="074b4-498">**Status**</span><span class="sxs-lookup"><span data-stu-id="074b4-498">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-499">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="074b4-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-500">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-500">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-501">Der aktuelle Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="074b4-501">The current status of the object.</span></span> <span data-ttu-id="074b4-502">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-502">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="074b4-503">Okay</span><span class="sxs-lookup"><span data-stu-id="074b4-503">"OK"</span></span>
</dt> <dt>

<span data-ttu-id="074b4-504"><span id="OK"></span><span id="ok"></span>**Okay**</span><span class="sxs-lookup"><span data-stu-id="074b4-504"><span id="OK"></span><span id="ok"></span>**OK**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-505"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Zeit**</span><span class="sxs-lookup"><span data-stu-id="074b4-505"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-506"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Zerstört**</span><span class="sxs-lookup"><span data-stu-id="074b4-506"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-507"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannter**</span><span class="sxs-lookup"><span data-stu-id="074b4-507"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-508"><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>**Pred-Fehler**</span><span class="sxs-lookup"><span data-stu-id="074b4-508"><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>**Pred Fail**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-509"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Fahren**</span><span class="sxs-lookup"><span data-stu-id="074b4-509"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-510"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Hindern**</span><span class="sxs-lookup"><span data-stu-id="074b4-510"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-511"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Leistungs**</span><span class="sxs-lookup"><span data-stu-id="074b4-511"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-512"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Gestresst**</span><span class="sxs-lookup"><span data-stu-id="074b4-512"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-513"><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>**Nicht wiederherstellen**</span><span class="sxs-lookup"><span data-stu-id="074b4-513"><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>**NonRecover**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-514"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt**</span><span class="sxs-lookup"><span data-stu-id="074b4-514"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-515"><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>**Verlorene Kommunikations-**</span><span class="sxs-lookup"><span data-stu-id="074b4-515"><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>**Lost Comm**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="074b4-516">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="074b4-516">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-517">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="074b4-517">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="074b4-518">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-518">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-519">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="074b4-519">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="074b4-520">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf "OK" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="074b4-520">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="074b4-521">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="074b4-521">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-522">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="074b4-522">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-523">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-523">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-524">Der aktuelle Zustand des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="074b4-524">The current state of the logical device.</span></span> <span data-ttu-id="074b4-525">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="074b4-525">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="074b4-526">**Supportedmaximumtransmissionunit**</span><span class="sxs-lookup"><span data-stu-id="074b4-526">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-527">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="074b4-527">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-528">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-528">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="074b4-529">Qualifizierer: **Einheiten** ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="074b4-529">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="074b4-530">Die maximale Anzahl von Übertragungs Einheiten (MTU), die unterstützt werden können, in Byte.</span><span class="sxs-lookup"><span data-stu-id="074b4-530">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="074b4-531">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-531">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="074b4-532">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="074b4-532">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-533">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="074b4-533">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-534">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-534">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-535">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="074b4-535">The scoping system's creation class name.</span></span> <span data-ttu-id="074b4-536">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf "MSVM \_ Computersystem" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="074b4-536">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="074b4-537">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="074b4-537">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-538">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="074b4-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-539">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-539">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-540">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="074b4-540">The name of the scoping system.</span></span> <span data-ttu-id="074b4-541">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-541">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="074b4-542">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="074b4-542">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-543">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="074b4-543">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-544">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-544">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-545">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="074b4-545">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="074b4-546">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="074b4-546">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="074b4-547">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="074b4-547">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-548">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="074b4-548">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-549">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-549">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-550">Die Gesamtanzahl der Stunden, für die dieses Gerät eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="074b4-550">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="074b4-551">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="074b4-551">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="074b4-552">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="074b4-552">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-553">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="074b4-553">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-554">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-554">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-555">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="074b4-555">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="074b4-556">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="074b4-556">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="074b4-557">**Einsatz Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="074b4-557">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="074b4-558">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="074b4-558">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="074b4-559">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="074b4-559">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="074b4-560">Unter bestimmten Umständen kann ein logischer Port als Front-End-oder Back-End-Port identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="074b4-560">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="074b4-561">Ein Beispiel für diese Situation wäre ein Speicher Array, das Back-End-Ports für die Kommunikation mit Datenträgern und Front-End-Ports für die Kommunikation mit Hosts aufweisen könnte.</span><span class="sxs-lookup"><span data-stu-id="074b4-561">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="074b4-562">Wenn die Verwendung des Ports nicht eingeschränkt ist, sollte der Wert auf "nicht eingeschränkt" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="074b4-562">If there is no restriction on the use of the port, then the value should be set to "Not restricted".</span></span> <span data-ttu-id="074b4-563">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="074b4-563">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="074b4-564"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="074b4-564"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-565"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Nur Front-End** (2)</span><span class="sxs-lookup"><span data-stu-id="074b4-565"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-566"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Nur Back-End** (3)</span><span class="sxs-lookup"><span data-stu-id="074b4-566"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="074b4-567"><span id="Not_restricted"></span><span id="not_restricted"></span><span id="NOT_RESTRICTED"></span>**Nicht eingeschränkt** (4)</span><span class="sxs-lookup"><span data-stu-id="074b4-567"><span id="Not_restricted"></span><span id="not_restricted"></span><span id="NOT_RESTRICTED"></span>**Not restricted** (4)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="074b4-568">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="074b4-568">Remarks</span></span>

<span data-ttu-id="074b4-569">Der Zugriff auf die **MSVM \_ externalethernetport** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="074b4-569">Access to the **Msvm\_ExternalEthernetPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="074b4-570">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="074b4-570">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="074b4-571">Beispiele</span><span class="sxs-lookup"><span data-stu-id="074b4-571">Examples</span></span>

<span data-ttu-id="074b4-572">Weitere Informationen finden Sie unter [Abfragen von Netzwerk Objekten](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="074b4-572">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="074b4-573">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="074b4-573">Requirements</span></span>



| <span data-ttu-id="074b4-574">Anforderung</span><span class="sxs-lookup"><span data-stu-id="074b4-574">Requirement</span></span> | <span data-ttu-id="074b4-575">Wert</span><span class="sxs-lookup"><span data-stu-id="074b4-575">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="074b4-576">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="074b4-576">Minimum supported client</span></span><br/> | <span data-ttu-id="074b4-577">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="074b4-577">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="074b4-578">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="074b4-578">Minimum supported server</span></span><br/> | <span data-ttu-id="074b4-579">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="074b4-579">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="074b4-580">Namespace</span><span class="sxs-lookup"><span data-stu-id="074b4-580">Namespace</span></span><br/>                | <span data-ttu-id="074b4-581">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="074b4-581">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="074b4-582">MOF</span><span class="sxs-lookup"><span data-stu-id="074b4-582">MOF</span></span><br/>                      | <dl> <span data-ttu-id="074b4-583"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="074b4-583"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="074b4-584">DLL</span><span class="sxs-lookup"><span data-stu-id="074b4-584">DLL</span></span><br/>                      | <dl> <span data-ttu-id="074b4-585"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="074b4-585"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="074b4-586">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="074b4-586">See also</span></span>

<dl> <dt>

[<span data-ttu-id="074b4-587">**CIM- \_ Ethernetport**</span><span class="sxs-lookup"><span data-stu-id="074b4-587">**CIM\_EthernetPort**</span></span>](cim-ethernetport.md)
</dt> <dt>

[<span data-ttu-id="074b4-588">**CIM- \_ Ethernetport**</span><span class="sxs-lookup"><span data-stu-id="074b4-588">**CIM\_EthernetPort**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 

