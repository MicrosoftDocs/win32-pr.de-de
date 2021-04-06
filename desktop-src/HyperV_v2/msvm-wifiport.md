---
description: Stellt einen physischen Wi-Fi (802,11) Netzwerkadapter dar, der an einen virtuellen Switch gebunden werden kann, um externe Netzwerkverbindungen mit virtuellen Maschinen bereitzustellen.
ms.assetid: c6dae491-607c-4f17-aea9-162d910120c2
title: Msvm_WiFiPort-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_WiFiPort
- Msvm_WiFiPort.RequestStateChange
- Msvm_WiFiPort.SetPowerState
- Msvm_WiFiPort.Reset
- Msvm_WiFiPort.EnableDevice
- Msvm_WiFiPort.OnlineDevice
- Msvm_WiFiPort.QuiesceDevice
- Msvm_WiFiPort.SaveProperties
- Msvm_WiFiPort.RestoreProperties
- Msvm_WiFiPort.InstanceID
- Msvm_WiFiPort.Caption
- Msvm_WiFiPort.Description
- Msvm_WiFiPort.ElementName
- Msvm_WiFiPort.InstallDate
- Msvm_WiFiPort.Name
- Msvm_WiFiPort.OperationalStatus
- Msvm_WiFiPort.StatusDescriptions
- Msvm_WiFiPort.Status
- Msvm_WiFiPort.HealthState
- Msvm_WiFiPort.CommunicationStatus
- Msvm_WiFiPort.DetailedStatus
- Msvm_WiFiPort.OperatingStatus
- Msvm_WiFiPort.PrimaryStatus
- Msvm_WiFiPort.EnabledState
- Msvm_WiFiPort.OtherEnabledState
- Msvm_WiFiPort.RequestedState
- Msvm_WiFiPort.EnabledDefault
- Msvm_WiFiPort.TimeOfLastStateChange
- Msvm_WiFiPort.AvailableRequestedStates
- Msvm_WiFiPort.TransitioningToState
- Msvm_WiFiPort.SystemCreationClassName
- Msvm_WiFiPort.SystemName
- Msvm_WiFiPort.CreationClassName
- Msvm_WiFiPort.DeviceID
- Msvm_WiFiPort.PowerManagementSupported
- Msvm_WiFiPort.PowerManagementCapabilities
- Msvm_WiFiPort.Availability
- Msvm_WiFiPort.StatusInfo
- Msvm_WiFiPort.LastErrorCode
- Msvm_WiFiPort.ErrorDescription
- Msvm_WiFiPort.ErrorCleared
- Msvm_WiFiPort.OtherIdentifyingInfo
- Msvm_WiFiPort.PowerOnHours
- Msvm_WiFiPort.TotalPowerOnHours
- Msvm_WiFiPort.IdentifyingDescriptions
- Msvm_WiFiPort.AdditionalAvailability
- Msvm_WiFiPort.MaxQuiesceTime
- Msvm_WiFiPort.Speed
- Msvm_WiFiPort.MaxSpeed
- Msvm_WiFiPort.RequestedSpeed
- Msvm_WiFiPort.UsageRestriction
- Msvm_WiFiPort.PortType
- Msvm_WiFiPort.OtherPortType
- Msvm_WiFiPort.OtherNetworkPortType
- Msvm_WiFiPort.PortNumber
- Msvm_WiFiPort.LinkTechnology
- Msvm_WiFiPort.OtherLinkTechnology
- Msvm_WiFiPort.PermanentAddress
- Msvm_WiFiPort.NetworkAddresses
- Msvm_WiFiPort.FullDuplex
- Msvm_WiFiPort.AutoSense
- Msvm_WiFiPort.SupportedMaximumTransmissionUnit
- Msvm_WiFiPort.ActiveMaximumTransmissionUnit
- Msvm_WiFiPort.IsBound
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 47ec33236c55d281755b50449a8f33a56152a07a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960932"
---
# <a name="msvm_wifiport-class"></a><span data-ttu-id="93f05-103">MSVM- \_ wifiport-Klasse</span><span class="sxs-lookup"><span data-stu-id="93f05-103">Msvm\_WiFiPort class</span></span>

<span data-ttu-id="93f05-104">Stellt einen physischen Wi-Fi (802,11) Netzwerkadapter dar, der an einen virtuellen Switch gebunden werden kann, um externe Netzwerkverbindungen mit virtuellen Maschinen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="93f05-104">Represents a physical Wi-Fi (802.11) network adapter that can be bound to a virtual switch to provide external network connectivity to virtual machines.</span></span>

<span data-ttu-id="93f05-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="93f05-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="93f05-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="93f05-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiPort : CIM_WiFiPort
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
  uint16   HealthState;
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
  boolean  IsBound;
};
```

## <a name="members"></a><span data-ttu-id="93f05-107">Member</span><span class="sxs-lookup"><span data-stu-id="93f05-107">Members</span></span>

<span data-ttu-id="93f05-108">Die **MSVM- \_ wifiport** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="93f05-108">The **Msvm\_WiFiPort** class has these types of members:</span></span>

-   [<span data-ttu-id="93f05-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="93f05-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="93f05-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="93f05-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="93f05-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="93f05-111">Methods</span></span>

<span data-ttu-id="93f05-112">Die **MSVM- \_ wifiport** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="93f05-112">The **Msvm\_WiFiPort** class has these methods.</span></span>



| <span data-ttu-id="93f05-113">Methode</span><span class="sxs-lookup"><span data-stu-id="93f05-113">Method</span></span>                 | <span data-ttu-id="93f05-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="93f05-114">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="93f05-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="93f05-115">**EnableDevice**</span></span>       | <span data-ttu-id="93f05-116">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="93f05-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="93f05-117">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="93f05-117">**OnlineDevice**</span></span>       | <span data-ttu-id="93f05-118">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="93f05-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="93f05-119">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="93f05-119">**QuiesceDevice**</span></span>      | <span data-ttu-id="93f05-120">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="93f05-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="93f05-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="93f05-121">**RequestStateChange**</span></span> | <span data-ttu-id="93f05-122">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="93f05-122">This method is not supported.</span></span><br/> |
| <span data-ttu-id="93f05-123">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="93f05-123">**Reset**</span></span>              | <span data-ttu-id="93f05-124">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="93f05-124">This method is not supported.</span></span><br/> |
| <span data-ttu-id="93f05-125">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="93f05-125">**RestoreProperties**</span></span>  | <span data-ttu-id="93f05-126">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="93f05-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="93f05-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="93f05-127">**SaveProperties**</span></span>     | <span data-ttu-id="93f05-128">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="93f05-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="93f05-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="93f05-129">**SetPowerState**</span></span>      | <span data-ttu-id="93f05-130">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="93f05-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="93f05-131">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="93f05-131">Properties</span></span>

<span data-ttu-id="93f05-132">Die **MSVM- \_ wifiport** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="93f05-132">The **Msvm\_WiFiPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="93f05-133">**Activemaximumtransmissionunit**</span><span class="sxs-lookup"><span data-stu-id="93f05-133">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-134">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93f05-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93f05-136">Qualifizierer: **Einheiten** ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="93f05-136">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="93f05-137">Die aktive oder ausgehandelte maximale Übertragungseinheit (Maximum Transmission Unit, MTU), die unterstützt werden kann, in Bytes.</span><span class="sxs-lookup"><span data-stu-id="93f05-137">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="93f05-138">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-138">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-139">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="93f05-139">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-140">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="93f05-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="93f05-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-142">Alle zusätzlichen Verfügbarkeit und der Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="93f05-142">Any additional availability and status of the device.</span></span> <span data-ttu-id="93f05-143">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-143">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-144">**AutoSense**</span><span class="sxs-lookup"><span data-stu-id="93f05-144">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-145">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="93f05-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-147">Gibt an, ob der Port die Geschwindigkeit oder andere Kommunikationsmerkmale der angeschlossenen Netzwerk Medien automatisch bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="93f05-147">Indicates whether the port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="93f05-148">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-148">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-149">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="93f05-149">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-150">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93f05-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-152">Die primäre Verfügbarkeit und den Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="93f05-152">The primary availability and status of the device.</span></span> <span data-ttu-id="93f05-153">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-153">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-154">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="93f05-154">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-155">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="93f05-155">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="93f05-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-157">Gibt die möglichen Werte für den *requestedstate* -Parameter der [**requestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) -Methode an, die zum Initiieren einer Zustandsänderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="93f05-157">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="93f05-158">Bei den aufgelisteten Werten handelt es sich um eine Teilmenge der Werte in der **requestedstaatsupported** -Eigenschaft der zugeordneten Instanz von **CIM \_ enabledlogicalelementfunctions**, bei der die ausgewählten Werte eine Funktion des aktuellen Zustands des [**CIM- \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))sind.</span><span class="sxs-lookup"><span data-stu-id="93f05-158">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="93f05-159">Diese Eigenschaft darf nicht **null** sein, wenn eine Implementierung den Satz möglicher Werte als Funktion des aktuellen Zustands ankündigen kann.</span><span class="sxs-lookup"><span data-stu-id="93f05-159">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="93f05-160">Diese Eigenschaft ist **null** , wenn eine Implementierung den Satz möglicher Werte nicht als Funktion des aktuellen Zustands bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="93f05-160">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="93f05-161">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-161">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="93f05-162"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="93f05-162"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-163"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="93f05-163"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-164"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Herunter** fahren (4)</span><span class="sxs-lookup"><span data-stu-id="93f05-164"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-165"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="93f05-165"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-166"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="93f05-166"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-167"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>Zurück **stellen (8** )</span><span class="sxs-lookup"><span data-stu-id="93f05-167"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-168"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Still **legung (9** )</span><span class="sxs-lookup"><span data-stu-id="93f05-168"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-169"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Neustart** (10)</span><span class="sxs-lookup"><span data-stu-id="93f05-169"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-170"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Zurücksetzen** (11)</span><span class="sxs-lookup"><span data-stu-id="93f05-170"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-171"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reserviert** (..</span><span class="sxs-lookup"><span data-stu-id="93f05-171"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="93f05-172">)</span><span class="sxs-lookup"><span data-stu-id="93f05-172">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="93f05-173">**Caption**</span><span class="sxs-lookup"><span data-stu-id="93f05-173">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93f05-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-176">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="93f05-176">A short description of the object.</span></span> <span data-ttu-id="93f05-177">Diese Eigenschaft wird von der [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) -Klasse geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-177">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class.</span></span>

</dd> <dt>

<span data-ttu-id="93f05-178">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="93f05-178">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-179">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93f05-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-181">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="93f05-181">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="93f05-182">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="93f05-182">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="93f05-183">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-183">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-184">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="93f05-184">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-185">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93f05-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-187">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="93f05-187">The scoping system's creation class name.</span></span> <span data-ttu-id="93f05-188">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-188">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-189">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="93f05-189">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-190">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93f05-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-192">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="93f05-192">A description of the object.</span></span> <span data-ttu-id="93f05-193">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-193">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-194">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="93f05-194">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-195">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93f05-195">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-196">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-197">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="93f05-197">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="93f05-198">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="93f05-198">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="93f05-199">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-200">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="93f05-200">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-201">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93f05-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-202">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-203">Eine Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="93f05-203">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="93f05-204">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-204">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-205">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="93f05-205">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-206">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93f05-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-207">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-208">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="93f05-208">A display name for the object.</span></span> <span data-ttu-id="93f05-209">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-209">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-210">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="93f05-210">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-211">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93f05-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-212">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-213">Die Standard-oder Startkonfiguration eines Administrators für die **enabledstate** -Eigenschaft eines Elements.</span><span class="sxs-lookup"><span data-stu-id="93f05-213">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="93f05-214">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-214">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-215">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="93f05-215">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-216">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93f05-216">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-217">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-218">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="93f05-218">The enabled and disabled states of an element.</span></span> <span data-ttu-id="93f05-219">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, und es handelt sich um einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="93f05-219">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="93f05-220">Wert</span><span class="sxs-lookup"><span data-stu-id="93f05-220">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="93f05-221">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="93f05-221">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="93f05-222"><dt>**Aktiviert**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="93f05-222"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="93f05-223">Das-Element wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="93f05-223">The element is running.</span></span><br/>    |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="93f05-224"><dt>**Deaktiviert**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="93f05-224"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="93f05-225">Das Element ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="93f05-225">The element is turned off.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="93f05-226">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="93f05-226">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-227">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="93f05-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-228">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-229">Gibt an, ob der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="93f05-229">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="93f05-230">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-231">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="93f05-231">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-232">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93f05-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-233">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-234">Eine Zeichenfolge, die weitere Informationen über den Fehler enthält, der in **LastErrorCode** aufgezeichnet wurde, sowie Informationen über alle Maßnahmen, die ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="93f05-234">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="93f05-235">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-235">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-236">**Vollduplex**</span><span class="sxs-lookup"><span data-stu-id="93f05-236">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-237">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="93f05-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-238">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-239">Gibt an, ob der Port im Vollduplex Modus betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="93f05-239">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="93f05-240">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-240">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-241">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="93f05-241">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-242">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93f05-242">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-243">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-244">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="93f05-244">The current health of the element.</span></span> <span data-ttu-id="93f05-245">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-246">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="93f05-246">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-247">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="93f05-247">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="93f05-248">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-249">Ein Array von Freiform-Zeichen folgen, die Erklärungen und Details hinter den Einträgen im Eigenschafts Array " **OtherIdentifyingInfo** " bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="93f05-249">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="93f05-250">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-251">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="93f05-251">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-252">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="93f05-252">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-253">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-254">Das Datum und die Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="93f05-254">The date and time when the object was installed.</span></span> <span data-ttu-id="93f05-255">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="93f05-255">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="93f05-256">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-257">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="93f05-257">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-258">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93f05-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-259">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93f05-260">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="93f05-260">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="93f05-261">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="93f05-261">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="93f05-262">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-262">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-263">**IsBound**</span><span class="sxs-lookup"><span data-stu-id="93f05-263">**IsBound**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-264">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="93f05-264">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-265">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-266">Gibt an, ob der Wi-Fi Port an die Netzwerkarchitektur des virtuellen Computers gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="93f05-266">Specifies if the Wi-Fi port is bound to the virtual machine networking architecture.</span></span> <span data-ttu-id="93f05-267">Dabei handelt es sich um einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="93f05-267">This will be one of the following values.</span></span>



| <span data-ttu-id="93f05-268">Wert</span><span class="sxs-lookup"><span data-stu-id="93f05-268">Value</span></span>                                                                                                                                                        | <span data-ttu-id="93f05-269">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="93f05-269">Meaning</span></span>                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="True"></span><span id="true"></span><span id="TRUE"></span><dl> <span data-ttu-id="93f05-270"><dt>**Fall**</dt></span><span class="sxs-lookup"><span data-stu-id="93f05-270"><dt>**True**</dt></span></span> </dl>     | <span data-ttu-id="93f05-271">Der Wi-Fi Port ist an die Netzwerkarchitektur des virtuellen Computers gebunden.</span><span class="sxs-lookup"><span data-stu-id="93f05-271">The Wi-Fi port is bound to the virtual machine networking architecture.</span></span> <br/>     |
| <span id="False"></span><span id="false"></span><span id="FALSE"></span><dl> <span data-ttu-id="93f05-272"><dt>**False**</dt></span><span class="sxs-lookup"><span data-stu-id="93f05-272"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="93f05-273">Der Wi-Fi Port ist nicht an die Netzwerkarchitektur des virtuellen Computers gebunden.</span><span class="sxs-lookup"><span data-stu-id="93f05-273">The Wi-Fi port is not bound to the virtual machine networking architecture.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="93f05-274">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="93f05-274">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-275">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93f05-275">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-276">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-277">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="93f05-277">The last error code reported by the logical device.</span></span> <span data-ttu-id="93f05-278">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-278">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-279">**Linktechnology**</span><span class="sxs-lookup"><span data-stu-id="93f05-279">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-280">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93f05-280">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-281">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-282">Gibt den Typ der Link Technologie für den Port an.</span><span class="sxs-lookup"><span data-stu-id="93f05-282">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="93f05-283">Wenn der Wert auf 1 (Sonstiges) festgelegt ist, enthält die **otherlinktechnology** -Eigenschaft eine Zeichen folgen Beschreibung des linktyps.</span><span class="sxs-lookup"><span data-stu-id="93f05-283">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="93f05-284">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-284">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="93f05-285"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="93f05-285"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-286"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="93f05-286"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-287"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="93f05-287"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-288"><span id="IB"></span><span id="ib"></span>**IB** (3)</span><span class="sxs-lookup"><span data-stu-id="93f05-288"><span id="IB"></span><span id="ib"></span>**IB** (3)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-289"><span id="FC"></span><span id="fc"></span>**FC** (4)</span><span class="sxs-lookup"><span data-stu-id="93f05-289"><span id="FC"></span><span id="fc"></span>**FC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-290"><span id="FDDI"></span><span id="fddi"></span>**F-di** (5)</span><span class="sxs-lookup"><span data-stu-id="93f05-290"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-291"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span><span class="sxs-lookup"><span data-stu-id="93f05-291"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-292"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**TokenRing** (7)</span><span class="sxs-lookup"><span data-stu-id="93f05-292"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-293"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span><span class="sxs-lookup"><span data-stu-id="93f05-293"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-294"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrarot** (9)</span><span class="sxs-lookup"><span data-stu-id="93f05-294"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (9)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-295"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**Bluetooth** (10)</span><span class="sxs-lookup"><span data-stu-id="93f05-295"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**BlueTooth** (10)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-296"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Drahtlos LAN** (11)</span><span class="sxs-lookup"><span data-stu-id="93f05-296"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Wireless LAN** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="93f05-297">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="93f05-297">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-298">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93f05-298">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-299">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-300">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="93f05-300">This property has been deprecated.</span></span> <span data-ttu-id="93f05-301">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-301">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-302">**MAXSPEED**</span><span class="sxs-lookup"><span data-stu-id="93f05-302">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-303">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93f05-303">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-304">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93f05-305">Qualifizierer: **Einheiten** ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="93f05-305">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="93f05-306">Die maximale Bandbreite des Ports (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="93f05-306">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="93f05-307">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-307">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-308">**Name**</span><span class="sxs-lookup"><span data-stu-id="93f05-308">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-309">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93f05-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-310">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-311">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="93f05-311">The label by which the object is known.</span></span> <span data-ttu-id="93f05-312">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-313">**"Networkaddresses"**</span><span class="sxs-lookup"><span data-stu-id="93f05-313">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-314">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="93f05-314">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="93f05-315">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93f05-316">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="93f05-316">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="93f05-317">Ein Array von Zeichen folgen, die die Mac-Adressen für den Port enthalten.</span><span class="sxs-lookup"><span data-stu-id="93f05-317">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="93f05-318">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-318">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-319">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="93f05-319">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-320">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93f05-320">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-321">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-322">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="93f05-322">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="93f05-323">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="93f05-323">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="93f05-324">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-324">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-325">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="93f05-325">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-326">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="93f05-326">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="93f05-327">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-328">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="93f05-328">The current statuses of the object.</span></span> <span data-ttu-id="93f05-329">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-329">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-330">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="93f05-330">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-331">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93f05-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-332">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-333">Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="93f05-333">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="93f05-334">Diese Eigenschaft muss auf **null** festgelegt werden, wenn die **enabledstate** -Eigenschaft einen anderen Wert als 1 hat.</span><span class="sxs-lookup"><span data-stu-id="93f05-334">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="93f05-335">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-335">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-336">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="93f05-336">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-337">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="93f05-337">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="93f05-338">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-339">Alle zusätzlichen Daten über Geräte-ID-Informationen, die zur Identifizierung eines logischen Geräts verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="93f05-339">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="93f05-340">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-341">**Otherlinktechnology**</span><span class="sxs-lookup"><span data-stu-id="93f05-341">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-342">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93f05-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-343">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-344">Ein Zeichen folgen Wert, der **linktechnology** beschreibt, wenn er auf 1 festgelegt ist (andere).</span><span class="sxs-lookup"><span data-stu-id="93f05-344">A string value that describes **LinkTechnology** when it is set to 1, (Other).</span></span> <span data-ttu-id="93f05-345">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-345">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-346">**Othernetworkporttype**</span><span class="sxs-lookup"><span data-stu-id="93f05-346">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-347">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93f05-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-348">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-349">Die Verwendung dieser Eigenschaft wird anstelle der **portType** -Eigenschaft als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="93f05-349">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="93f05-350">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-350">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-351">**Otherporttype**</span><span class="sxs-lookup"><span data-stu-id="93f05-351">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-352">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93f05-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-353">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-354">Beschreibt den Modultyp, wenn **portType** auf 1 (Other) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="93f05-354">Describes the type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="93f05-355">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-355">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-356">**Permanent Address**</span><span class="sxs-lookup"><span data-stu-id="93f05-356">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-357">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93f05-357">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-358">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93f05-359">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="93f05-359">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="93f05-360">Die Netzwerkadresse, die in einem Port hart codiert ist.</span><span class="sxs-lookup"><span data-stu-id="93f05-360">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="93f05-361">Diese hart codierte Adresse kann mithilfe eines Firmware-Upgrades oder einer Softwarekonfiguration geändert werden.</span><span class="sxs-lookup"><span data-stu-id="93f05-361">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="93f05-362">Wenn diese Änderung vorgenommen wird, sollte das Feld gleichzeitig aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="93f05-362">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="93f05-363">Diese Eigenschaft sollte **null** sein, wenn keine hart codierte Adresse für den Netzwerkadapter vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="93f05-363">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="93f05-364">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-364">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-365">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="93f05-365">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-366">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93f05-366">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-367">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-368">Die Portnummer.</span><span class="sxs-lookup"><span data-stu-id="93f05-368">The port number.</span></span> <span data-ttu-id="93f05-369">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-369">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-370">**PortType**</span><span class="sxs-lookup"><span data-stu-id="93f05-370">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-371">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93f05-371">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-372">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-373">Der bestimmte Modus, der derzeit für den Port aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="93f05-373">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="93f05-374">Wenn der Wert auf 1 (Sonstiges) festgelegt ist, enthält die zugehörige **otherporttype** -Eigenschaft eine Zeichen folgen Beschreibung des Port Typs.</span><span class="sxs-lookup"><span data-stu-id="93f05-374">When set to 1 (Other), the related **OtherPortType** property contains a string description of the type of port.</span></span> <span data-ttu-id="93f05-375">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-375">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="93f05-376"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="93f05-376"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-377"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="93f05-377"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-378"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**50 Kupfer 10BaseT** (50)</span><span class="sxs-lookup"><span data-stu-id="93f05-378"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-379"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100-BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="93f05-379"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-380"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100 BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="93f05-380"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-381"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000 BaseT** (53)</span><span class="sxs-lookup"><span data-stu-id="93f05-381"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-382"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500baset** (54)</span><span class="sxs-lookup"><span data-stu-id="93f05-382"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-383"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10gbaset** (55)</span><span class="sxs-lookup"><span data-stu-id="93f05-383"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-384"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="93f05-384"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-385"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**100 Fibre 100Base-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="93f05-385"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-386"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100BASE-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="93f05-386"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-387"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000 Base-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="93f05-387"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-388"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000 Base-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="93f05-388"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-389"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000 Base-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="93f05-389"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-390"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="93f05-390"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-391"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="93f05-391"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-392"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="93f05-392"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-393"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="93f05-393"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-394"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="93f05-394"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-395"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-er** (110)</span><span class="sxs-lookup"><span data-stu-id="93f05-395"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-396"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span><span class="sxs-lookup"><span data-stu-id="93f05-396"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-397"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (16000.65535)</span><span class="sxs-lookup"><span data-stu-id="93f05-397"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (16000..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="93f05-398">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="93f05-398">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-399">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="93f05-399">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="93f05-400">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-401">Die Energie Verwaltungsfunktionen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="93f05-401">The power management capabilities of the device.</span></span> <span data-ttu-id="93f05-402">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-402">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-403">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="93f05-403">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-404">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="93f05-404">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-405">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-406">Gibt an, ob das Gerät Energie gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="93f05-406">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="93f05-407">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-407">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-408">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="93f05-408">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-409">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93f05-409">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-410">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-411">Gibt an, wie viele aufeinanderfolgende Stunden dieses Gerät seit dem letzten Strom Umgebung eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="93f05-411">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="93f05-412">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-412">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-413">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="93f05-413">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-414">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93f05-414">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-415">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-416">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="93f05-416">Provides high level status information.</span></span> <span data-ttu-id="93f05-417">Diese Eigenschaft sollte in Verbindung mit der **detailedstatus** -Eigenschaft verwendet werden, um allgemeine und ausführliche Integritäts Statusinformationen für das-Element und seine unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="93f05-417">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="93f05-418">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="93f05-418">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="93f05-419">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-419">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-420">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="93f05-420">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-421">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93f05-421">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-422">Zugriffstyp: schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-422">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="93f05-423">Qualifizierer: **Einheiten** ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="93f05-423">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="93f05-424">Die angeforderte Bandbreite des Ports (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="93f05-424">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="93f05-425">Die tatsächliche Bandbreite wird in der Eigenschaft **Geschwindigkeit** gemeldet.</span><span class="sxs-lookup"><span data-stu-id="93f05-425">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="93f05-426">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-426">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-427">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="93f05-427">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-428">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93f05-428">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-429">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-430">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="93f05-430">The last requested or desired state for the element.</span></span> <span data-ttu-id="93f05-431">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-431">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-432">**Geschwindigkeit**</span><span class="sxs-lookup"><span data-stu-id="93f05-432">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-433">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93f05-433">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-434">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93f05-435">Qualifizierer: **Einheiten** ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="93f05-435">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="93f05-436">Die Bandbreite des Ports (in Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="93f05-436">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="93f05-437">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-437">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-438">**Status**</span><span class="sxs-lookup"><span data-stu-id="93f05-438">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-439">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93f05-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-440">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-441">Der aktuelle Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="93f05-441">The current status of the object.</span></span> <span data-ttu-id="93f05-442">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-442">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-443">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="93f05-443">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-444">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="93f05-444">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="93f05-445">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-446">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="93f05-446">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="93f05-447">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-447">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-448">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="93f05-448">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-449">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93f05-449">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-450">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-451">Der aktuelle Zustand des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="93f05-451">The current state of the logical device.</span></span> <span data-ttu-id="93f05-452">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-452">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-453">**Supportedmaximumtransmissionunit**</span><span class="sxs-lookup"><span data-stu-id="93f05-453">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-454">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93f05-454">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-455">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93f05-456">Qualifizierer: **Einheiten** ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="93f05-456">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="93f05-457">Die maximale Anzahl von Übertragungs Einheiten (MTU), die unterstützt werden können, in Byte.</span><span class="sxs-lookup"><span data-stu-id="93f05-457">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="93f05-458">Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-458">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-459">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="93f05-459">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-460">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93f05-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-461">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-461">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-462">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="93f05-462">The scoping system's creation class name.</span></span> <span data-ttu-id="93f05-463">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-463">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-464">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="93f05-464">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-465">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="93f05-465">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-466">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-466">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-467">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="93f05-467">The scoping system's name.</span></span> <span data-ttu-id="93f05-468">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-468">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-469">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="93f05-469">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-470">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="93f05-470">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-471">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-471">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-472">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="93f05-472">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="93f05-473">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-473">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-474">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="93f05-474">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-475">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93f05-475">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-476">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-476">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-477">Die Gesamtanzahl der Stunden, die dieses Gerät eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="93f05-477">The total number of hours that this device has been powered on.</span></span> <span data-ttu-id="93f05-478">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-478">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="93f05-479">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="93f05-479">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-480">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93f05-480">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-481">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-481">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-482">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="93f05-482">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="93f05-483">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="93f05-483">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="93f05-484">**Einsatz Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="93f05-484">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f05-485">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93f05-485">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93f05-486">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="93f05-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93f05-487">Unter bestimmten Umständen kann ein logischer Port als Front-End-oder Back-End-Port identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="93f05-487">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="93f05-488">Ein Beispiel für diese Situation wäre ein Speicher Array, das Back-End-Ports für die Kommunikation mit Datenträgern und Front-End-Ports für die Kommunikation mit Hosts aufweisen könnte.</span><span class="sxs-lookup"><span data-stu-id="93f05-488">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="93f05-489">Wenn keine Einschränkung für die Verwendung des Ports vorliegt, sollte der Wert auf 4 (nicht eingeschränkt) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="93f05-489">If there is no restriction on the use of the port, then the value should be set to 4 (Not restricted).</span></span> <span data-ttu-id="93f05-490">Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="93f05-490">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="93f05-491"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="93f05-491"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-492"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Nur Front-End** (2)</span><span class="sxs-lookup"><span data-stu-id="93f05-492"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-493"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Nur Back-End** (3)</span><span class="sxs-lookup"><span data-stu-id="93f05-493"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="93f05-494"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Nicht eingeschränkt** (4)</span><span class="sxs-lookup"><span data-stu-id="93f05-494"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Not restricted** (4 )</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="93f05-495">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93f05-495">Requirements</span></span>



| <span data-ttu-id="93f05-496">Anforderung</span><span class="sxs-lookup"><span data-stu-id="93f05-496">Requirement</span></span> | <span data-ttu-id="93f05-497">Wert</span><span class="sxs-lookup"><span data-stu-id="93f05-497">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93f05-498">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="93f05-498">Minimum supported client</span></span><br/> | <span data-ttu-id="93f05-499">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="93f05-499">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="93f05-500">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="93f05-500">Minimum supported server</span></span><br/> | <span data-ttu-id="93f05-501">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="93f05-501">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="93f05-502">Namespace</span><span class="sxs-lookup"><span data-stu-id="93f05-502">Namespace</span></span><br/>                | <span data-ttu-id="93f05-503">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="93f05-503">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="93f05-504">MOF</span><span class="sxs-lookup"><span data-stu-id="93f05-504">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93f05-505"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="93f05-505"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="93f05-506">DLL</span><span class="sxs-lookup"><span data-stu-id="93f05-506">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93f05-507"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="93f05-507"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

