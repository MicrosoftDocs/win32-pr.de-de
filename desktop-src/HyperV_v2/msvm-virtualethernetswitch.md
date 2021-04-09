---
description: Stellt einen virtuellen Ethernet-Switch dar. Jeder Switch verfügt über viele verschiedene Ports, an die Netzwerkadapter angefügt werden können. Der Switch selbst ist nicht hochgradig konfigurierbar und fungiert hauptsächlich als Platzhalter.
ms.assetid: 9415477a-9423-40fa-a887-3a93da1374af
title: Msvm_VirtualEthernetSwitch-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitch
- Msvm_VirtualEthernetSwitch.SetPowerState
- Msvm_VirtualEthernetSwitch.InstanceID
- Msvm_VirtualEthernetSwitch.Caption
- Msvm_VirtualEthernetSwitch.Description
- Msvm_VirtualEthernetSwitch.ElementName
- Msvm_VirtualEthernetSwitch.InstallDate
- Msvm_VirtualEthernetSwitch.OperationalStatus
- Msvm_VirtualEthernetSwitch.StatusDescriptions
- Msvm_VirtualEthernetSwitch.Status
- Msvm_VirtualEthernetSwitch.HealthState
- Msvm_VirtualEthernetSwitch.CommunicationStatus
- Msvm_VirtualEthernetSwitch.DetailedStatus
- Msvm_VirtualEthernetSwitch.OperatingStatus
- Msvm_VirtualEthernetSwitch.PrimaryStatus
- Msvm_VirtualEthernetSwitch.EnabledState
- Msvm_VirtualEthernetSwitch.OtherEnabledState
- Msvm_VirtualEthernetSwitch.RequestedState
- Msvm_VirtualEthernetSwitch.EnabledDefault
- Msvm_VirtualEthernetSwitch.TimeOfLastStateChange
- Msvm_VirtualEthernetSwitch.AvailableRequestedStates
- Msvm_VirtualEthernetSwitch.TransitioningToState
- Msvm_VirtualEthernetSwitch.CreationClassName
- Msvm_VirtualEthernetSwitch.Name
- Msvm_VirtualEthernetSwitch.PrimaryOwnerName
- Msvm_VirtualEthernetSwitch.PrimaryOwnerContact
- Msvm_VirtualEthernetSwitch.Roles
- Msvm_VirtualEthernetSwitch.NameFormat
- Msvm_VirtualEthernetSwitch.OtherIdentifyingInfo
- Msvm_VirtualEthernetSwitch.IdentifyingDescriptions
- Msvm_VirtualEthernetSwitch.Dedicated
- Msvm_VirtualEthernetSwitch.OtherDedicatedDescriptions
- Msvm_VirtualEthernetSwitch.ResetCapability
- Msvm_VirtualEthernetSwitch.PowerManagementCapabilities
- Msvm_VirtualEthernetSwitch.MaxVMQOffloads
- Msvm_VirtualEthernetSwitch.MaxIOVOffloads
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1cd916e24a6e34ed6a70002c4988f55810050c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866392"
---
# <a name="msvm_virtualethernetswitch-class"></a><span data-ttu-id="6e0d4-105">MSVM \_ virtualethernetzwitch-Klasse</span><span class="sxs-lookup"><span data-stu-id="6e0d4-105">Msvm\_VirtualEthernetSwitch class</span></span>

<span data-ttu-id="6e0d4-106">Stellt einen virtuellen Ethernet-Switch dar.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-106">Represents a virtual Ethernet switch.</span></span> <span data-ttu-id="6e0d4-107">Jeder Switch verfügt über viele verschiedene Ports, an die Netzwerkadapter angefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-107">Each switch has many different ports to which network adapters can be attached.</span></span> <span data-ttu-id="6e0d4-108">Der Switch selbst ist nicht hochgradig konfigurierbar und fungiert hauptsächlich als Platzhalter.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-108">The switch itself is not highly configurable and acts mostly as a placeholder.</span></span>

<span data-ttu-id="6e0d4-109">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-109">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e0d4-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e0d4-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitch : CIM_ComputerSystem
{
  string   InstanceID;
  string   Caption = "Virtual Switch";
  string   Description = "Microsoft Virtual Switch";
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   CreationClassName = "Msvm_VirtualEthernetSwitch";
  string   Name = "GUID";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   NameFormat;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability = 5;
  uint16   PowerManagementCapabilities[];
  uint32   MaxVMQOffloads;
  uint32   MaxIOVOffloads;
};
```

## <a name="members"></a><span data-ttu-id="6e0d4-111">Member</span><span class="sxs-lookup"><span data-stu-id="6e0d4-111">Members</span></span>

<span data-ttu-id="6e0d4-112">Die **MSVM-Klasse \_ virtualethernetzwitch** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6e0d4-112">The **Msvm\_VirtualEthernetSwitch** class has these types of members:</span></span>

-   [<span data-ttu-id="6e0d4-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="6e0d4-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="6e0d4-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6e0d4-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6e0d4-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="6e0d4-115">Methods</span></span>

<span data-ttu-id="6e0d4-116">Die **MSVM-Klasse \_ virtualethernetzwitch** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-116">The **Msvm\_VirtualEthernetSwitch** class has these methods.</span></span>



| <span data-ttu-id="6e0d4-117">Methode</span><span class="sxs-lookup"><span data-stu-id="6e0d4-117">Method</span></span>                                                                      | <span data-ttu-id="6e0d4-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6e0d4-118">Description</span></span>                              |
|:----------------------------------------------------------------------------|:-----------------------------------------|
| [<span data-ttu-id="6e0d4-119">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-119">**RequestStateChange**</span></span>](msvm-virtualethernetswitch-requeststatechange.md) | <span data-ttu-id="6e0d4-120">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-120">Requests a state change.</span></span><br/>      |
| <span data-ttu-id="6e0d4-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-121">**SetPowerState**</span></span>                                                           | <span data-ttu-id="6e0d4-122">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-122">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6e0d4-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6e0d4-123">Properties</span></span>

<span data-ttu-id="6e0d4-124">Die **MSVM- \_ virtualethernetzwitch** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-124">The **Msvm\_VirtualEthernetSwitch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6e0d4-125">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-125">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-126">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="6e0d4-126">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e0d4-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-128">Gibt die möglichen Werte für den *requestedstate* -Parameter der [**requestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) -Methode an, die zum Initiieren einer Zustandsänderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-128">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="6e0d4-129">Bei den aufgelisteten Werten handelt es sich um eine Teilmenge der Werte, die in der **requestedstaatsupported** -Eigenschaft der zugeordneten Instanz von **CIM \_ enabledlogicalelementfunctions** enthalten sind, wobei die ausgewählten Werte eine Funktion des aktuellen Zustands des [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) -Objekts sind.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-129">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="6e0d4-130">Diese Eigenschaft darf nicht **null** sein, wenn eine Implementierung den Satz möglicher Werte als Funktion des aktuellen Zustands ankündigen kann.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-130">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="6e0d4-131">Diese Eigenschaft ist **null** , wenn eine Implementierung den Satz möglicher Werte nicht als Funktion des aktuellen Zustands bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-131">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="6e0d4-132">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-132">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="6e0d4-133"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-133"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-134"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-134"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-135"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Herunter** fahren (4)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-135"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-136"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-136"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-137"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-137"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-138"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>Zurück **stellen (8** )</span><span class="sxs-lookup"><span data-stu-id="6e0d4-138"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-139"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Still **legung (9** )</span><span class="sxs-lookup"><span data-stu-id="6e0d4-139"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-140"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Neustart** (10)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-140"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-141"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Zurücksetzen** (11)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-141"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-142"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reserviert** (..</span><span class="sxs-lookup"><span data-stu-id="6e0d4-142"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="6e0d4-143">)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-143">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6e0d4-144">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-144">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e0d4-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-147">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-147">A short description of the object.</span></span> <span data-ttu-id="6e0d4-148">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "virtueller Switch" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-148">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Switch".</span></span>

</dd> <dt>

<span data-ttu-id="6e0d4-149">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-149">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-150">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e0d4-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-152">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-152">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="6e0d4-153">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-153">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6e0d4-154">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-154">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="6e0d4-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-156"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-156"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-157"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-157"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-158"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-158"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-159"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-159"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-160"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-160"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-161"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="6e0d4-161"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="6e0d4-162">)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-162">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6e0d4-163">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-163">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e0d4-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-166">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-166">The name of the class or subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="6e0d4-167">Diese Eigenschaft wird vom [**CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system)geerbt und ist immer auf "MSVM \_ virtualethernwitch" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-167">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to "Msvm\_VirtualEthernetSwitch".</span></span>

</dd> <dt>

<span data-ttu-id="6e0d4-168">**Dediziert**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-168">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-169">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="6e0d4-169">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e0d4-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-171">Gibt an, ob es sich bei dem Computersystem um ein spezielles System handelt (dediziert für eine bestimmte Verwendung) und ob es sich um ein allgemeines System handelt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-171">Indicates whether the computer system is a special-purpose system (dedicated to a particular use), versus being a general-purpose system.</span></span> <span data-ttu-id="6e0d4-172">Diese Eigenschaft wird von [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)geerbt und ist immer auf 0 (nicht dediziert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-172">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 0 (Not Dedicated).</span></span>

</dd> <dt>

<span data-ttu-id="6e0d4-173">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-173">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e0d4-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-176">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-176">A description of the object.</span></span> <span data-ttu-id="6e0d4-177">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Microsoft Virtual Switch" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-177">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Virtual Switch".</span></span>

</dd> <dt>

<span data-ttu-id="6e0d4-178">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-178">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-179">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e0d4-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-181">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-181">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="6e0d4-182">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-182">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6e0d4-183">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-183">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="6e0d4-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-185"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-185"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-186"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-186"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-187"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-187"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-188"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-188"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-189"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-189"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-191"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="6e0d4-191"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="6e0d4-192">)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-192">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6e0d4-193">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-193">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-194">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e0d4-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-196">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-196">A display name for the object.</span></span> <span data-ttu-id="6e0d4-197">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-197">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6e0d4-198">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-198">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-199">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-200">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e0d4-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-201">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-201">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="6e0d4-202">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) geerbt und ist einer der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-202">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="6e0d4-203"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-203"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-204"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-204"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-205"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Aktiviert, aber offline** (6)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-205"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6e0d4-206">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-206">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-207">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-208">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e0d4-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-209">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-209">The enabled and disabled states of an element.</span></span> <span data-ttu-id="6e0d4-210">Diese Eigenschaft kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-210">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="6e0d4-211">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 5 festgelegt (nicht zutreffend).</span><span class="sxs-lookup"><span data-stu-id="6e0d4-211">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="6e0d4-212">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-212">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-213">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-214">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e0d4-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-215">Gibt den aktuellen Zustand des Elements an.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-215">Specifies the current health of the element.</span></span> <span data-ttu-id="6e0d4-216">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-216">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="6e0d4-217">Wenn ein kritischer Fehler auftritt, finden Sie im Ereignisprotokoll weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-217">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="6e0d4-218">Die **enabledstate** -Eigenschaft kann auch weitere Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-218">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="6e0d4-219">Wenn z. b. der Speicherplatz kritisch ist, ist **healthstate** auf 25 festgelegt, der virtuelle Computer wird angehalten, und **enabledstate** wird auf 32768 (angehalten) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-219">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="6e0d4-220">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-220">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="6e0d4-221">Wert</span><span class="sxs-lookup"><span data-stu-id="6e0d4-221">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="6e0d4-222">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6e0d4-222">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="6e0d4-223"><dt>**OK**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="6e0d4-223"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="6e0d4-224">Das-Element ist voll funktionsfähig und wird in normalen Betriebsparametern und ohne Fehler ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-224">The element is fully functional and is operating within normal operational parameters and without error.</span></span><br/> |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="6e0d4-225"><dt>**Hauptfehler**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="6e0d4-225"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="6e0d4-226">Das-Element hat einen schwerwiegenden Fehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-226">The element has suffered a major failure.</span></span><br/>                                                                |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="6e0d4-227"><dt>**Kritischer Fehler**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="6e0d4-227"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="6e0d4-228">Das Element ist nicht funktionsfähig, und die Wiederherstellung ist möglicherweise nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-228">The element is nonfunctional, and recovery might not be possible.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="6e0d4-229">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-229">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-230">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="6e0d4-230">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-231">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e0d4-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-232">Diese Eigenschaft wird von [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-232">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6e0d4-233">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-233">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-234">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-234">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-235">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e0d4-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-236">Das Datum und die Uhrzeit, zu der die Konfiguration der virtuellen Maschine für eine virtuelle Maschine oder **null** für ein Verwaltungs Betriebssystem erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-236">The date and time the virtual machine configuration was created for a virtual machine, or **Null**, for a management operating system.</span></span> <span data-ttu-id="6e0d4-237">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-237">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6e0d4-238">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-238">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-239">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-239">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-240">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e0d4-240">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-241">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-241">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-242">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-242">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="6e0d4-243">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-243">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6e0d4-244">**Maxiovoffloads**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-244">**MaxIOVOffloads**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-245">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-245">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-246">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e0d4-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-247">Die maximale Anzahl von virtuellen SR-IOV-Funktions Abladungen (Single root IO Virtualization), die auf diesem Switch verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-247">The maximum number of single root IO virtualization (SR-IOV) virtual function offloads available on this switch.</span></span>

</dd> <dt>

<span data-ttu-id="6e0d4-248">**Maxvmqoffloads**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-248">**MaxVMQOffloads**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-249">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-249">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-250">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6e0d4-250">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-251">Die maximale Anzahl von VMQ-Abladungen (Virtual Machine Queue), die für einen Port auf diesem Switch zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-251">The maximum number of virtual machine queue (VMQ) offloads allowed for a port on this switch.</span></span>

</dd> <dt>

<span data-ttu-id="6e0d4-252">**Name**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-252">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-253">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-254">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e0d4-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-255">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-255">The label by which the object is known.</span></span> <span data-ttu-id="6e0d4-256">Diese Eigenschaft wird vom [**CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system)geerbt und ist immer auf "*GUID*" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-256">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to "*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="6e0d4-257">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-257">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-258">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-259">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e0d4-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-260">Eine Zeichenfolge, die angibt, wie der Systemname mithilfe der Unterklasse heuristic generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-260">A string that identifies how the system name was generated, using the subclass heuristic.</span></span> <span data-ttu-id="6e0d4-261">Diese Eigenschaft wird von [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-261">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6e0d4-262">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-262">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-263">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-263">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-264">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e0d4-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-265">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-265">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="6e0d4-266">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-266">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6e0d4-267">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="6e0d4-268"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-268"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-269"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-269"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-270"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-270"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-271"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-271"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-272"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="6e0d4-272"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-273"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-273"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-274"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-274"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-275"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-275"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-276"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-276"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-277"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-277"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-278"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-278"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-279"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-279"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-280"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-280"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-281"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-281"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-282"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-282"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-283"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-283"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-284"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-284"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-285"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-285"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-286"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="6e0d4-286"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="6e0d4-287">)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-287">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6e0d4-288">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-288">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-289">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="6e0d4-289">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-290">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e0d4-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-291">Ein Array, das die aktuellen Status des-Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-291">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="6e0d4-292">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-292">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6e0d4-293">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-293">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-294">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="6e0d4-294">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-295">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e0d4-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-296">Eine Zeichenfolge, die beschreibt, wie oder warum das System dediziert ist, wenn das **dedizierte** Array den Wert 2 (Sonstiges) enthält.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-296">A string that describes how or why the system is dedicated when the **Dedicated** array includes the value 2 (Other).</span></span> <span data-ttu-id="6e0d4-297">Diese Eigenschaft wird von [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-297">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6e0d4-298">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-298">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-299">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-300">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e0d4-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-301">Der aktivierte oder deaktivierte Status des Elements, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-301">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="6e0d4-302">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-302">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="6e0d4-303">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-303">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6e0d4-304">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-304">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-305">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="6e0d4-305">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-306">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e0d4-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-307">Diese Eigenschaft wird von [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-307">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6e0d4-308">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-308">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-309">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="6e0d4-309">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-310">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e0d4-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-311">Diese Eigenschaft wird von [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-311">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6e0d4-312">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-312">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-313">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-314">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e0d4-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-315">Eine Zeichenfolge, die angibt, wie der primäre Systembesitzer erreicht werden kann (z. b. eine Telefonnummer oder eine e-Mail-Adresse).</span><span class="sxs-lookup"><span data-stu-id="6e0d4-315">A string that indicates how the primary system owner can be reached (for example, a phone number or an email address).</span></span> <span data-ttu-id="6e0d4-316">Diese Eigenschaft wird vom [**CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-316">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6e0d4-317">**Primaryownername**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-317">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-318">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-319">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e0d4-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-320">Der Name des primären System Besitzers.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-320">The name of the primary system owner.</span></span> <span data-ttu-id="6e0d4-321">Diese Eigenschaft wird vom [**CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-321">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6e0d4-322">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-322">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-323">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-323">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-324">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e0d4-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-325">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-325">Provides high level status information.</span></span> <span data-ttu-id="6e0d4-326">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-326">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="6e0d4-327">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-327">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6e0d4-328">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-328">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="6e0d4-329"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-329"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-330"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-330"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-331"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="6e0d4-331"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-332"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-332"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-333"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-333"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-334"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="6e0d4-334"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="6e0d4-335">)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-335">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6e0d4-336">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-336">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-337">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-337">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-338">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e0d4-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-339">Der zuletzt angeforderte oder gewünschte Zustand für das Element, das an die **requestStateChange** -Methode weitergegeben wird, oder 12 (nicht zutreffend), wenn keine Zustandsänderung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-339">The last requested or desired state for the element as passed to the **RequestStateChange** method, or 12 (Not Applicable) if no state change is in progress.</span></span> <span data-ttu-id="6e0d4-340">Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-340">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="6e0d4-341">Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuell aktivierten oder deaktivierten Zustände zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-341">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="6e0d4-342">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-342">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="6e0d4-343">**Resetcapability**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-343">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-344">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-345">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e0d4-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-346">Diese Eigenschaft wird von [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)geerbt und ist immer auf 5 (nicht implementiert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-346">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 5 (Not implemented).</span></span>

</dd> <dt>

<span data-ttu-id="6e0d4-347">**Rollen**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-347">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-348">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="6e0d4-348">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-349">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e0d4-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-350">Ein Array von Zeichen folgen, das die Rollen beschreibt, die das System in der Informationstechnologie Umgebung spielt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-350">An array of strings that describe the roles the system plays in the information technology environment.</span></span> <span data-ttu-id="6e0d4-351">Diese Eigenschaft wird vom [**CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-351">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6e0d4-352">**Status**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-352">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-353">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-354">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e0d4-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-355">Eine Zeichenfolge, die den Status des Elements angibt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-355">A string that specifies the status of the element.</span></span> <span data-ttu-id="6e0d4-356">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-356">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6e0d4-357">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-357">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-358">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="6e0d4-358">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-359">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e0d4-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-360">Qualifizierer: **arrayType** ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="6e0d4-360">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-361">Ein Array, das Zeichen folgen enthält, die die entsprechenden **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-361">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="6e0d4-362">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-362">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6e0d4-363">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-363">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-364">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-364">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-365">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e0d4-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-366">Das Datum und die Uhrzeit der letzten Änderung des aktivierten Zustands des Elements.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-366">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="6e0d4-367">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-367">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="6e0d4-368">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-368">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e0d4-369">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6e0d4-369">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6e0d4-370">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e0d4-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e0d4-371">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-371">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="6e0d4-372">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="6e0d4-372">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6e0d4-373">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6e0d4-373">Requirements</span></span>



| <span data-ttu-id="6e0d4-374">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6e0d4-374">Requirement</span></span> | <span data-ttu-id="6e0d4-375">Wert</span><span class="sxs-lookup"><span data-stu-id="6e0d4-375">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e0d4-376">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-376">Minimum supported client</span></span><br/> | <span data-ttu-id="6e0d4-377">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6e0d4-377">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6e0d4-378">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6e0d4-378">Minimum supported server</span></span><br/> | <span data-ttu-id="6e0d4-379">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6e0d4-379">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6e0d4-380">Namespace</span><span class="sxs-lookup"><span data-stu-id="6e0d4-380">Namespace</span></span><br/>                | <span data-ttu-id="6e0d4-381">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="6e0d4-381">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6e0d4-382">MOF</span><span class="sxs-lookup"><span data-stu-id="6e0d4-382">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e0d4-383"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6e0d4-383"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6e0d4-384">DLL</span><span class="sxs-lookup"><span data-stu-id="6e0d4-384">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e0d4-385"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6e0d4-385"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

