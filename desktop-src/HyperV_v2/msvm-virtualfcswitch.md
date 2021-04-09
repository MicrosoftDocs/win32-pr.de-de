---
description: Stellt einen virtuellen Fibre Channel Switch dar.
ms.assetid: 4300747b-3ffc-4caf-8f0b-76cab6d2294e
title: Msvm_VirtualFcSwitch-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualFcSwitch
- Msvm_VirtualFcSwitch.SetPowerState
- Msvm_VirtualFcSwitch.InstanceID
- Msvm_VirtualFcSwitch.Caption
- Msvm_VirtualFcSwitch.Description
- Msvm_VirtualFcSwitch.ElementName
- Msvm_VirtualFcSwitch.InstallDate
- Msvm_VirtualFcSwitch.OperationalStatus
- Msvm_VirtualFcSwitch.StatusDescriptions
- Msvm_VirtualFcSwitch.Status
- Msvm_VirtualFcSwitch.HealthState
- Msvm_VirtualFcSwitch.CommunicationStatus
- Msvm_VirtualFcSwitch.DetailedStatus
- Msvm_VirtualFcSwitch.OperatingStatus
- Msvm_VirtualFcSwitch.PrimaryStatus
- Msvm_VirtualFcSwitch.EnabledState
- Msvm_VirtualFcSwitch.OtherEnabledState
- Msvm_VirtualFcSwitch.RequestedState
- Msvm_VirtualFcSwitch.EnabledDefault
- Msvm_VirtualFcSwitch.TimeOfLastStateChange
- Msvm_VirtualFcSwitch.AvailableRequestedStates
- Msvm_VirtualFcSwitch.TransitioningToState
- Msvm_VirtualFcSwitch.CreationClassName
- Msvm_VirtualFcSwitch.Name
- Msvm_VirtualFcSwitch.PrimaryOwnerName
- Msvm_VirtualFcSwitch.PrimaryOwnerContact
- Msvm_VirtualFcSwitch.Roles
- Msvm_VirtualFcSwitch.NameFormat
- Msvm_VirtualFcSwitch.OtherIdentifyingInfo
- Msvm_VirtualFcSwitch.IdentifyingDescriptions
- Msvm_VirtualFcSwitch.Dedicated
- Msvm_VirtualFcSwitch.OtherDedicatedDescriptions
- Msvm_VirtualFcSwitch.ResetCapability
- Msvm_VirtualFcSwitch.PowerManagementCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 66c6b7a284a2751b1c9b664428a9c90db9f468a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128408"
---
# <a name="msvm_virtualfcswitch-class"></a><span data-ttu-id="327b1-103">MSVM \_ virtualfcswitch-Klasse</span><span class="sxs-lookup"><span data-stu-id="327b1-103">Msvm\_VirtualFcSwitch class</span></span>

<span data-ttu-id="327b1-104">Stellt einen virtuellen Fibre Channel Switch dar.</span><span class="sxs-lookup"><span data-stu-id="327b1-104">Represents a virtual Fibre Channel switch.</span></span> <span data-ttu-id="327b1-105">Jeder Switch ist einem physischen Fibre Channel Port zugeordnet, mit dem viele synthetische Fibre Channel Ports verbunden werden können.</span><span class="sxs-lookup"><span data-stu-id="327b1-105">Each switch is associated with one physical Fibre Channel port to which many synthetic Fibre Channel ports can be connected.</span></span> <span data-ttu-id="327b1-106">Der Switch selbst ist nicht hochgradig konfigurierbar und fungiert hauptsächlich als Platzhalter.</span><span class="sxs-lookup"><span data-stu-id="327b1-106">The switch itself is not highly configurable and acts mostly as a placeholder.</span></span>

<span data-ttu-id="327b1-107">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="327b1-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="327b1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="327b1-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualFcSwitch : CIM_ComputerSystem
{
  string   InstanceID;
  string   Caption;
  string   Description;
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
  string   CreationClassName;
  string   Name;
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   NameFormat;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability;
  uint16   PowerManagementCapabilities[];
};
```

## <a name="members"></a><span data-ttu-id="327b1-109">Member</span><span class="sxs-lookup"><span data-stu-id="327b1-109">Members</span></span>

<span data-ttu-id="327b1-110">Die Klasse " **MSVM \_ virtualfcswitch** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="327b1-110">The **Msvm\_VirtualFcSwitch** class has these types of members:</span></span>

-   [<span data-ttu-id="327b1-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="327b1-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="327b1-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="327b1-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="327b1-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="327b1-113">Methods</span></span>

<span data-ttu-id="327b1-114">Die Klasse **MSVM \_ virtualfcswitch** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="327b1-114">The **Msvm\_VirtualFcSwitch** class has these methods.</span></span>



| <span data-ttu-id="327b1-115">Methode</span><span class="sxs-lookup"><span data-stu-id="327b1-115">Method</span></span>                                                                | <span data-ttu-id="327b1-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="327b1-116">Description</span></span>                              |
|:----------------------------------------------------------------------|:-----------------------------------------|
| [<span data-ttu-id="327b1-117">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="327b1-117">**RequestStateChange**</span></span>](msvm-virtualfcswitch-requeststatechange.md) | <span data-ttu-id="327b1-118">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="327b1-118">Requests a state change.</span></span><br/>      |
| <span data-ttu-id="327b1-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="327b1-119">**SetPowerState**</span></span>                                                     | <span data-ttu-id="327b1-120">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="327b1-120">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="327b1-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="327b1-121">Properties</span></span>

<span data-ttu-id="327b1-122">Die **MSVM \_ virtualfcswitch** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="327b1-122">The **Msvm\_VirtualFcSwitch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="327b1-123">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="327b1-123">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327b1-124">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="327b1-124">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="327b1-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="327b1-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="327b1-126">Gibt die möglichen Werte für den *requestedstate* -Parameter der [**requestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) -Methode an, die zum Initiieren einer Zustandsänderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="327b1-126">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="327b1-127">Bei den aufgelisteten Werten handelt es sich um eine Teilmenge der Werte, die in der **requestedstaatsupported** -Eigenschaft der zugeordneten Instanz von **CIM \_ enabledlogicalelementfunctions** enthalten sind, wobei die ausgewählten Werte eine Funktion des aktuellen Zustands des [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) -Objekts sind.</span><span class="sxs-lookup"><span data-stu-id="327b1-127">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="327b1-128">Diese Eigenschaft darf nicht **null** sein, wenn eine Implementierung den Satz möglicher Werte als Funktion des aktuellen Zustands ankündigen kann.</span><span class="sxs-lookup"><span data-stu-id="327b1-128">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="327b1-129">Diese Eigenschaft ist **null** , wenn eine Implementierung den Satz möglicher Werte nicht als Funktion des aktuellen Zustands bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="327b1-129">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="327b1-130">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="327b1-130">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="327b1-131"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="327b1-131"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-132"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="327b1-132"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-133"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Herunter** fahren (4)</span><span class="sxs-lookup"><span data-stu-id="327b1-133"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-134"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="327b1-134"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-135"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="327b1-135"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-136"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>Zurück **stellen (8** )</span><span class="sxs-lookup"><span data-stu-id="327b1-136"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-137"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Still **legung (9** )</span><span class="sxs-lookup"><span data-stu-id="327b1-137"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-138"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Neustart** (10)</span><span class="sxs-lookup"><span data-stu-id="327b1-138"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-139"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Zurücksetzen** (11)</span><span class="sxs-lookup"><span data-stu-id="327b1-139"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-140"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reserviert** (..</span><span class="sxs-lookup"><span data-stu-id="327b1-140"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="327b1-141">)</span><span class="sxs-lookup"><span data-stu-id="327b1-141">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="327b1-142">**Caption**</span><span class="sxs-lookup"><span data-stu-id="327b1-142">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327b1-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="327b1-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="327b1-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="327b1-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="327b1-145">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="327b1-145">A short description of the object.</span></span> <span data-ttu-id="327b1-146">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="327b1-146">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="327b1-147">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="327b1-147">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327b1-148">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="327b1-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="327b1-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="327b1-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="327b1-150">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="327b1-150">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="327b1-151">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="327b1-151">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="327b1-152">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="327b1-152">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="327b1-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="327b1-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-154"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="327b1-154"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-155"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="327b1-155"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-156"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="327b1-156"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-157"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="327b1-157"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="327b1-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-159"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="327b1-159"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="327b1-160">)</span><span class="sxs-lookup"><span data-stu-id="327b1-160">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="327b1-161">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="327b1-161">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327b1-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="327b1-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="327b1-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="327b1-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="327b1-164">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="327b1-164">The name of the class or subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="327b1-165">Diese Eigenschaft wird vom [**CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system)geerbt.</span><span class="sxs-lookup"><span data-stu-id="327b1-165">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system).</span></span>

</dd> <dt>

<span data-ttu-id="327b1-166">**Dediziert**</span><span class="sxs-lookup"><span data-stu-id="327b1-166">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327b1-167">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="327b1-167">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="327b1-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="327b1-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="327b1-169">Gibt an, ob es sich bei dem Computersystem um ein spezielles System handelt (dediziert für eine bestimmte Verwendung) und ob es sich um ein allgemeines System handelt.</span><span class="sxs-lookup"><span data-stu-id="327b1-169">Indicates whether the computer system is a special-purpose system (dedicated to a particular use), versus being a general-purpose system.</span></span> <span data-ttu-id="327b1-170">Diese Eigenschaft wird von [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)geerbt und ist immer auf 0 (nicht dediziert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="327b1-170">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 0 (Not Dedicated).</span></span>

</dd> <dt>

<span data-ttu-id="327b1-171">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="327b1-171">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327b1-172">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="327b1-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="327b1-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="327b1-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="327b1-174">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="327b1-174">A description of the object.</span></span> <span data-ttu-id="327b1-175">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="327b1-175">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="327b1-176">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="327b1-176">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327b1-177">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="327b1-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="327b1-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="327b1-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="327b1-179">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="327b1-179">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="327b1-180">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="327b1-180">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="327b1-181">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="327b1-181">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="327b1-182"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="327b1-182"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-183"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="327b1-183"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-184"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="327b1-184"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-185"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="327b1-185"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-186"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="327b1-186"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-187"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="327b1-187"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="327b1-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="327b1-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="327b1-190">)</span><span class="sxs-lookup"><span data-stu-id="327b1-190">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="327b1-191">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="327b1-191">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327b1-192">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="327b1-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="327b1-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="327b1-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="327b1-194">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="327b1-194">A display name for the object.</span></span> <span data-ttu-id="327b1-195">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="327b1-195">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="327b1-196">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="327b1-196">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327b1-197">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="327b1-197">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="327b1-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="327b1-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="327b1-199">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="327b1-199">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="327b1-200">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) geerbt und ist einer der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="327b1-200">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="327b1-201"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="327b1-201"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-202"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="327b1-202"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-203"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Aktiviert, aber offline** (6)</span><span class="sxs-lookup"><span data-stu-id="327b1-203"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="327b1-204">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="327b1-204">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327b1-205">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="327b1-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="327b1-206">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="327b1-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="327b1-207">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="327b1-207">The enabled and disabled states of an element.</span></span> <span data-ttu-id="327b1-208">Diese Eigenschaft kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben.</span><span class="sxs-lookup"><span data-stu-id="327b1-208">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="327b1-209">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 5 festgelegt (nicht zutreffend).</span><span class="sxs-lookup"><span data-stu-id="327b1-209">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="327b1-210">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="327b1-210">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327b1-211">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="327b1-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="327b1-212">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="327b1-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="327b1-213">Gibt den aktuellen Zustand des Elements an.</span><span class="sxs-lookup"><span data-stu-id="327b1-213">Specifies the current health of the element.</span></span> <span data-ttu-id="327b1-214">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="327b1-214">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="327b1-215">Wenn ein kritischer Fehler auftritt, finden Sie im Ereignisprotokoll weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="327b1-215">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="327b1-216">Die **enabledstate** -Eigenschaft kann auch weitere Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="327b1-216">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="327b1-217">Wenn z. b. der Speicherplatz kritisch ist, ist **healthstate** auf 25 festgelegt, der virtuelle Computer wird angehalten, und **enabledstate** wird auf 32768 (angehalten) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="327b1-217">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="327b1-218">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="327b1-218">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="327b1-219">Wert</span><span class="sxs-lookup"><span data-stu-id="327b1-219">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="327b1-220">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="327b1-220">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="327b1-221"><dt>**OK**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="327b1-221"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="327b1-222">Das-Element ist voll funktionsfähig und wird in normalen Betriebsparametern und ohne Fehler ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="327b1-222">The element is fully functional and is operating within normal operational parameters and without error.</span></span><br/> |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="327b1-223"><dt>**Hauptfehler**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="327b1-223"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="327b1-224">Das-Element hat einen schwerwiegenden Fehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="327b1-224">The element has suffered a major failure.</span></span><br/>                                                                |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="327b1-225"><dt>**Kritischer Fehler**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="327b1-225"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="327b1-226">Das Element ist nicht funktionsfähig, und die Wiederherstellung ist möglicherweise nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="327b1-226">The element is nonfunctional and recovery might not be possible.</span></span><br/>                                         |



 

</dd> <dt>

<span data-ttu-id="327b1-227">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="327b1-227">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327b1-228">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="327b1-228">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="327b1-229">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="327b1-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="327b1-230">Diese Eigenschaft wird von [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="327b1-230">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="327b1-231">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="327b1-231">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327b1-232">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="327b1-232">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="327b1-233">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="327b1-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="327b1-234">Das Datum und die Uhrzeit, zu der die Konfiguration der virtuellen Maschine für eine virtuelle Maschine oder **null** für ein Verwaltungs Betriebssystem erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="327b1-234">The date and time the virtual machine configuration was created for a virtual machine, or **Null**, for a management operating system.</span></span> <span data-ttu-id="327b1-235">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="327b1-235">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="327b1-236">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="327b1-236">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327b1-237">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="327b1-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="327b1-238">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="327b1-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="327b1-239">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="327b1-239">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="327b1-240">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="327b1-240">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="327b1-241">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="327b1-241">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="327b1-242">**Name**</span><span class="sxs-lookup"><span data-stu-id="327b1-242">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327b1-243">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="327b1-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="327b1-244">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="327b1-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="327b1-245">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="327b1-245">The label by which the object is known.</span></span> <span data-ttu-id="327b1-246">Diese Eigenschaft wird vom [**CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system)geerbt.</span><span class="sxs-lookup"><span data-stu-id="327b1-246">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system).</span></span>

</dd> <dt>

<span data-ttu-id="327b1-247">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="327b1-247">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327b1-248">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="327b1-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="327b1-249">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="327b1-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="327b1-250">Eine Zeichenfolge, die angibt, wie der Systemname mithilfe der Unterklasse heuristic generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="327b1-250">A string that identifies how the system name was generated, using the subclass heuristic.</span></span> <span data-ttu-id="327b1-251">Diese Eigenschaft wird von [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="327b1-251">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="327b1-252">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="327b1-252">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327b1-253">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="327b1-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="327b1-254">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="327b1-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="327b1-255">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="327b1-255">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="327b1-256">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="327b1-256">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="327b1-257">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="327b1-257">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="327b1-258"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="327b1-258"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-259"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="327b1-259"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-260"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="327b1-260"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-261"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="327b1-261"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-262"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="327b1-262"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-263"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="327b1-263"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-264"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="327b1-264"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-265"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="327b1-265"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-266"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="327b1-266"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-267"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="327b1-267"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-268"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="327b1-268"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-269"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="327b1-269"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-270"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="327b1-270"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-271"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="327b1-271"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-272"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="327b1-272"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-273"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="327b1-273"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-274"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="327b1-274"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-275"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="327b1-275"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-276"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="327b1-276"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="327b1-277">)</span><span class="sxs-lookup"><span data-stu-id="327b1-277">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="327b1-278">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="327b1-278">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327b1-279">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="327b1-279">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="327b1-280">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="327b1-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="327b1-281">Ein Array, das die aktuellen Status des-Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="327b1-281">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="327b1-282">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="327b1-282">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="327b1-283">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="327b1-283">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327b1-284">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="327b1-284">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="327b1-285">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="327b1-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="327b1-286">Eine Zeichenfolge, die beschreibt, wie oder warum das System dediziert ist, wenn das **dedizierte** Array den Wert 2 (Sonstiges) enthält.</span><span class="sxs-lookup"><span data-stu-id="327b1-286">A string that describes how or why the system is dedicated when the **Dedicated** array includes the value 2 (Other).</span></span> <span data-ttu-id="327b1-287">Diese Eigenschaft wird von [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="327b1-287">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="327b1-288">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="327b1-288">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327b1-289">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="327b1-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="327b1-290">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="327b1-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="327b1-291">Der aktivierte oder deaktivierte Status des Elements, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="327b1-291">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="327b1-292">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="327b1-292">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="327b1-293">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="327b1-293">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="327b1-294">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="327b1-294">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327b1-295">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="327b1-295">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="327b1-296">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="327b1-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="327b1-297">Diese Eigenschaft wird von [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="327b1-297">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="327b1-298">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="327b1-298">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327b1-299">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="327b1-299">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="327b1-300">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="327b1-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="327b1-301">Diese Eigenschaft wird von [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="327b1-301">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="327b1-302">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="327b1-302">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327b1-303">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="327b1-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="327b1-304">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="327b1-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="327b1-305">Eine Zeichenfolge, die angibt, wie der primäre Systembesitzer erreicht werden kann (z. b. eine Telefonnummer oder eine e-Mail-Adresse).</span><span class="sxs-lookup"><span data-stu-id="327b1-305">A string that indicates how the primary system owner can be reached (for example, a phone number or an email address).</span></span> <span data-ttu-id="327b1-306">Diese Eigenschaft wird vom [**CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="327b1-306">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="327b1-307">**Primaryownername**</span><span class="sxs-lookup"><span data-stu-id="327b1-307">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327b1-308">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="327b1-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="327b1-309">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="327b1-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="327b1-310">Der Name des primären System Besitzers.</span><span class="sxs-lookup"><span data-stu-id="327b1-310">The name of the primary system owner.</span></span> <span data-ttu-id="327b1-311">Diese Eigenschaft wird vom [**CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="327b1-311">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="327b1-312">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="327b1-312">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327b1-313">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="327b1-313">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="327b1-314">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="327b1-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="327b1-315">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="327b1-315">Provides high level status information.</span></span> <span data-ttu-id="327b1-316">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="327b1-316">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="327b1-317">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="327b1-317">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="327b1-318">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="327b1-318">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="327b1-319"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="327b1-319"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-320"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="327b1-320"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-321"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="327b1-321"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-322"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="327b1-322"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-323"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="327b1-323"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="327b1-324"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="327b1-324"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="327b1-325">)</span><span class="sxs-lookup"><span data-stu-id="327b1-325">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="327b1-326">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="327b1-326">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327b1-327">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="327b1-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="327b1-328">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="327b1-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="327b1-329">Der zuletzt angeforderte oder gewünschte Zustand für das Element, das an die **requestStateChange** -Methode weitergegeben wird, oder 12 (nicht zutreffend), wenn keine Zustandsänderung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="327b1-329">The last requested or desired state for the element as passed to the **RequestStateChange** method, or 12 (Not Applicable) if no state change is in progress.</span></span> <span data-ttu-id="327b1-330">Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="327b1-330">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="327b1-331">Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuell aktivierten oder deaktivierten Zustände zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="327b1-331">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="327b1-332">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="327b1-332">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="327b1-333">**Resetcapability**</span><span class="sxs-lookup"><span data-stu-id="327b1-333">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327b1-334">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="327b1-334">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="327b1-335">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="327b1-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="327b1-336">Diese Eigenschaft wird von [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)geerbt.</span><span class="sxs-lookup"><span data-stu-id="327b1-336">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem).</span></span>

</dd> <dt>

<span data-ttu-id="327b1-337">**Rollen**</span><span class="sxs-lookup"><span data-stu-id="327b1-337">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327b1-338">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="327b1-338">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="327b1-339">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="327b1-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="327b1-340">Ein Array von Zeichen folgen, das die Rollen beschreibt, die das System in der Informationstechnologie Umgebung spielt.</span><span class="sxs-lookup"><span data-stu-id="327b1-340">An array of strings that describe the roles the system plays in the information technology environment.</span></span> <span data-ttu-id="327b1-341">Diese Eigenschaft wird vom [**CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="327b1-341">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="327b1-342">**Status**</span><span class="sxs-lookup"><span data-stu-id="327b1-342">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327b1-343">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="327b1-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="327b1-344">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="327b1-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="327b1-345">Eine Zeichenfolge, die den Status des Elements angibt.</span><span class="sxs-lookup"><span data-stu-id="327b1-345">A string that specifies the status of the element.</span></span> <span data-ttu-id="327b1-346">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="327b1-346">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="327b1-347">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="327b1-347">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327b1-348">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="327b1-348">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="327b1-349">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="327b1-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="327b1-350">Qualifizierer: **arrayType** ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="327b1-350">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="327b1-351">Ein Array, das Zeichen folgen enthält, die die entsprechenden **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="327b1-351">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="327b1-352">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="327b1-352">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="327b1-353">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="327b1-353">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327b1-354">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="327b1-354">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="327b1-355">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="327b1-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="327b1-356">Das Datum und die Uhrzeit der letzten Änderung des aktivierten Zustands des Elements.</span><span class="sxs-lookup"><span data-stu-id="327b1-356">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="327b1-357">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="327b1-357">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="327b1-358">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="327b1-358">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="327b1-359">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="327b1-359">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="327b1-360">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="327b1-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="327b1-361">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="327b1-361">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="327b1-362">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="327b1-362">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="327b1-363">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="327b1-363">Requirements</span></span>



| <span data-ttu-id="327b1-364">Anforderung</span><span class="sxs-lookup"><span data-stu-id="327b1-364">Requirement</span></span> | <span data-ttu-id="327b1-365">Wert</span><span class="sxs-lookup"><span data-stu-id="327b1-365">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="327b1-366">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="327b1-366">Minimum supported client</span></span><br/> | <span data-ttu-id="327b1-367">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="327b1-367">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="327b1-368">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="327b1-368">Minimum supported server</span></span><br/> | <span data-ttu-id="327b1-369">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="327b1-369">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="327b1-370">Namespace</span><span class="sxs-lookup"><span data-stu-id="327b1-370">Namespace</span></span><br/>                | <span data-ttu-id="327b1-371">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="327b1-371">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="327b1-372">MOF</span><span class="sxs-lookup"><span data-stu-id="327b1-372">MOF</span></span><br/>                      | <dl> <span data-ttu-id="327b1-373"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="327b1-373"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="327b1-374">DLL</span><span class="sxs-lookup"><span data-stu-id="327b1-374">DLL</span></span><br/>                      | <dl> <span data-ttu-id="327b1-375"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="327b1-375"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

