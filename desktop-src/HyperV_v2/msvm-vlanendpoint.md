---
description: Stellt den VLAN-Endpunkt eines Switchports dar.
ms.assetid: 82F2EC39-0C9C-4A9D-A6C4-1543A62A341D
title: Msvm_VLANEndpoint-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VLANEndpoint
- Msvm_VLANEndpoint.InstanceID
- Msvm_VLANEndpoint.Caption
- Msvm_VLANEndpoint.Description
- Msvm_VLANEndpoint.ElementName
- Msvm_VLANEndpoint.InstallDate
- Msvm_VLANEndpoint.Name
- Msvm_VLANEndpoint.OperationalStatus
- Msvm_VLANEndpoint.StatusDescriptions
- Msvm_VLANEndpoint.Status
- Msvm_VLANEndpoint.HealthState
- Msvm_VLANEndpoint.CommunicationStatus
- Msvm_VLANEndpoint.DetailedStatus
- Msvm_VLANEndpoint.OperatingStatus
- Msvm_VLANEndpoint.PrimaryStatus
- Msvm_VLANEndpoint.EnabledState
- Msvm_VLANEndpoint.OtherEnabledState
- Msvm_VLANEndpoint.RequestedState
- Msvm_VLANEndpoint.EnabledDefault
- Msvm_VLANEndpoint.TimeOfLastStateChange
- Msvm_VLANEndpoint.AvailableRequestedStates
- Msvm_VLANEndpoint.TransitioningToState
- Msvm_VLANEndpoint.SystemCreationClassName
- Msvm_VLANEndpoint.SystemName
- Msvm_VLANEndpoint.CreationClassName
- Msvm_VLANEndpoint.NameFormat
- Msvm_VLANEndpoint.ProtocolType
- Msvm_VLANEndpoint.ProtocolIFType
- Msvm_VLANEndpoint.OtherTypeDescription
- Msvm_VLANEndpoint.DesiredEndpointMode
- Msvm_VLANEndpoint.OtherEndpointMode
- Msvm_VLANEndpoint.OperationalEndpointMode
- Msvm_VLANEndpoint.DesiredVLANTrunkEncapsulation
- Msvm_VLANEndpoint.OtherTrunkEncapsulation
- Msvm_VLANEndpoint.OperationalVLANTrunkEncapsulation
- Msvm_VLANEndpoint.GVRPStatus
- Msvm_VLANEndpoint.SupportedEndpointModes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5606e18fd1327f17feaac07570e5bf8c0c8eb59d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344043"
---
# <a name="msvm_vlanendpoint-class"></a><span data-ttu-id="7747a-103">MSVM \_ vlanendpoint-Klasse</span><span class="sxs-lookup"><span data-stu-id="7747a-103">Msvm\_VLANEndpoint class</span></span>

<span data-ttu-id="7747a-104">Stellt den VLAN-Endpunkt eines Switchports dar.</span><span class="sxs-lookup"><span data-stu-id="7747a-104">Represents the VLAN endpoint of a switch port.</span></span> <span data-ttu-id="7747a-105">Die Konfiguration dieses Endpunkts ändert die Art und Weise, in der der Switchport VLAN-Pakete über den Switch sendet.</span><span class="sxs-lookup"><span data-stu-id="7747a-105">The configuration of this endpoint will change the way the switch port sends VLAN packets through the switch.</span></span>

<span data-ttu-id="7747a-106">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7747a-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7747a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7747a-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VLANEndpoint : CIM_VLANEndpoint
{
  string   InstanceID;
  String   Caption = "VLAN Endpoint";
  string   Description = "Microsoft VLAN Endpoint";
  String   ElementName;
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
  String   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_VirtualSwitch";
  string   SystemName;
  String   CreationClassName = "Msvm_VLANEndpoint";
  String   NameFormat;
  uint16   ProtocolType;
  uint16   ProtocolIFType = 1;
  String   OtherTypeDescription = "Virtual Ethernet";
  uint16   DesiredEndpointMode;
  string   OtherEndpointMode;
  uint16   OperationalEndpointMode;
  uint16   DesiredVLANTrunkEncapsulation;
  string   OtherTrunkEncapsulation;
  uint16   OperationalVLANTrunkEncapsulation;
  uint16   GVRPStatus;
  uint16   SupportedEndpointModes[];
};
```

## <a name="members"></a><span data-ttu-id="7747a-108">Member</span><span class="sxs-lookup"><span data-stu-id="7747a-108">Members</span></span>

<span data-ttu-id="7747a-109">Die **MSVM \_ vlanendpoint** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7747a-109">The **Msvm\_VLANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="7747a-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="7747a-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="7747a-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7747a-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7747a-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="7747a-112">Methods</span></span>

<span data-ttu-id="7747a-113">Die **MSVM \_ vlanendpoint** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="7747a-113">The **Msvm\_VLANEndpoint** class has these methods.</span></span>



| <span data-ttu-id="7747a-114">Methode</span><span class="sxs-lookup"><span data-stu-id="7747a-114">Method</span></span>                                                             | <span data-ttu-id="7747a-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7747a-115">Description</span></span>                         |
|:-------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="7747a-116">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="7747a-116">**RequestStateChange**</span></span>](msvm-vlanendpoint-requeststatechange.md) | <span data-ttu-id="7747a-117">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="7747a-117">Requests a state change.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7747a-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7747a-118">Properties</span></span>

<span data-ttu-id="7747a-119">Die **MSVM \_ vlanendpoint** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7747a-119">The **Msvm\_VLANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7747a-120">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="7747a-120">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-121">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="7747a-121">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7747a-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-123">Gibt die möglichen Werte für den *requestedstate* -Parameter der [**requestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) -Methode an, die zum Initiieren einer Zustandsänderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7747a-123">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="7747a-124">Bei den aufgelisteten Werten handelt es sich um eine Teilmenge der Werte in der **requestedstaatsupported** -Eigenschaft der zugeordneten Instanz von **CIM \_ enabledlogicalelementfunctions**, bei der die ausgewählten Werte eine Funktion des aktuellen Zustands des [**CIM- \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))sind.</span><span class="sxs-lookup"><span data-stu-id="7747a-124">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="7747a-125">Diese Eigenschaft darf nicht **null** sein, wenn eine Implementierung den Satz möglicher Werte als Funktion des aktuellen Zustands ankündigen kann.</span><span class="sxs-lookup"><span data-stu-id="7747a-125">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="7747a-126">Diese Eigenschaft ist **null** , wenn eine Implementierung den Satz möglicher Werte nicht als Funktion des aktuellen Zustands bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="7747a-126">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="7747a-127">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="7747a-127">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="7747a-128"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="7747a-128"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7747a-129"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="7747a-129"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7747a-130"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Herunter** fahren (4)</span><span class="sxs-lookup"><span data-stu-id="7747a-130"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7747a-131"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="7747a-131"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="7747a-132"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="7747a-132"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="7747a-133"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>Zurück **stellen (8** )</span><span class="sxs-lookup"><span data-stu-id="7747a-133"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="7747a-134"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Still **legung (9** )</span><span class="sxs-lookup"><span data-stu-id="7747a-134"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="7747a-135"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Neustart** (10)</span><span class="sxs-lookup"><span data-stu-id="7747a-135"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="7747a-136"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Zurücksetzen** (11)</span><span class="sxs-lookup"><span data-stu-id="7747a-136"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="7747a-137"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reserviert** (..</span><span class="sxs-lookup"><span data-stu-id="7747a-137"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="7747a-138">)</span><span class="sxs-lookup"><span data-stu-id="7747a-138">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7747a-139">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7747a-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7747a-140">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="7747a-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-142">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="7747a-142">A short description of the object.</span></span> <span data-ttu-id="7747a-143">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "VLAN-Endpunkt" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7747a-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "VLAN Endpoint".</span></span>

</dd> <dt>

<span data-ttu-id="7747a-144">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="7747a-144">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-145">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7747a-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7747a-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-147">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="7747a-147">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="7747a-148">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="7747a-148">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7747a-149">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7747a-149">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7747a-150">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="7747a-150">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-151">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7747a-151">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="7747a-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-153">Der Name der Klasse oder der Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7747a-153">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="7747a-154">Diese Eigenschaft wird von [**CIM \_ serviceaccesspoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)geerbt und ist immer auf "MSVM \_ vlanendpoint" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7747a-154">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint), and it is always set to "Msvm\_VLANEndpoint".</span></span>

</dd> <dt>

<span data-ttu-id="7747a-155">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7747a-155">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-156">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7747a-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7747a-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-158">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="7747a-158">A description of the object.</span></span> <span data-ttu-id="7747a-159">Diese Eigenschaft wird vom [**CIM \_ managedelta-Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Microsoft VLAN Endpoint" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7747a-159">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft VLAN Endpoint".</span></span>

</dd> <dt>

<span data-ttu-id="7747a-160">**"Desiredendpointmode"**</span><span class="sxs-lookup"><span data-stu-id="7747a-160">**DesiredEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-161">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7747a-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7747a-162">Zugriffstyp: schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-162">Access type: Write-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-163">Der gewünschte VLAN-Modus, der zur Verwendung angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="7747a-163">The desired VLAN mode that is requested for use.</span></span> <span data-ttu-id="7747a-164">Der aktuelle Modus wird von der **operationalendpointmode** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="7747a-164">The current mode is given by the **OperationalEndpointMode** property.</span></span> <span data-ttu-id="7747a-165">Diese Eigenschaft wird von [**CIM \_ vlanendpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7747a-165">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>



| <span data-ttu-id="7747a-166">Wert</span><span class="sxs-lookup"><span data-stu-id="7747a-166">Value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="7747a-167">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7747a-167">Meaning</span></span>                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="7747a-168"><dt>**DMTF reserviert**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7747a-168"><dt>**DMTF Reserved**</dt> <dt>0</dt></span></span> </dl>                       |                                                                                                                                                                                                                                                                                  |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="7747a-169"><dt>**Sonstige**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7747a-169"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                       |                                                                                                                                                                                                                                                                                  |
| <span id="Access"></span><span id="access"></span><span id="ACCESS"></span><dl> <span data-ttu-id="7747a-170"><dt>**Zugriff**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7747a-170"><dt>**Access**</dt> <dt>2</dt></span></span> </dl>                                                   | <span data-ttu-id="7747a-171">Versetzt den Endpunkt/Switchport in den permanenten nicht Trunking-Modus und aushandgt, um den Link in einen nicht trunk-Link zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="7747a-171">Puts the endpoint/switch port into permanent nontrunking mode and negotiates to convert the link into a nontrunk link.</span></span> <span data-ttu-id="7747a-172">Der Endpunkt wird zu einer nicht trunk-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7747a-172">The endpoint becomes a nontrunk interface.</span></span><br/>                                                                                                     |
| <span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span><dl> <span data-ttu-id="7747a-173"><dt>**Dynamisches Auto**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="7747a-173"><dt>**Dynamic Auto**</dt> <dt>3</dt></span></span> </dl>                           | <span data-ttu-id="7747a-174">Macht den Endpunkt in der Lage, den Link in einen trunk Link zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="7747a-174">Makes the endpoint able to convert the link to a trunk link.</span></span> <span data-ttu-id="7747a-175">Der Endpunkt wird zu einer trunk Schnittstelle, wenn die benachbarte Schnittstelle auf den trunk Modus oder den gewünschten Modus festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7747a-175">The endpoint becomes a trunk interface if the neighboring interface is set to trunk or desirable mode.</span></span><br/>                                                                                                   |
| <span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span><dl> <span data-ttu-id="7747a-176"><dt>**Dynamisch erwünscht**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="7747a-176"><dt>**Dynamic Desirable**</dt> <dt>4</dt></span></span> </dl>       | <span data-ttu-id="7747a-177">Bewirkt, dass der Endpunkt aktiv versucht, den Link in einen trunk Link zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="7747a-177">Makes the endpoint actively attempt to convert the link to a trunk link.</span></span> <span data-ttu-id="7747a-178">Der Endpunkt wird zu einer trunk Schnittstelle, wenn die benachbarte Schnittstelle auf den trunk-, wünschenswert-oder Auto-Modus festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7747a-178">The endpoint becomes a trunk interface if the neighboring interface is set to trunk, desirable, or auto mode.</span></span> <span data-ttu-id="7747a-179">Der standardmäßige switchportmodus für alle Ethernet-Schnittstellen ist dynamisch erwünscht.</span><span class="sxs-lookup"><span data-stu-id="7747a-179">The default switch-port mode for all Ethernet interfaces is dynamic desirable.</span></span><br/> |
| <span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span><dl> <span data-ttu-id="7747a-180"><dt>**Trunk**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="7747a-180"><dt>**Trunk**</dt> <dt>5</dt></span></span> </dl>                                                       | <span data-ttu-id="7747a-181">Versetzt den Endpunkt in den permanenten trunkingmodus und aushandgt, um den Link in einen trunk Link zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="7747a-181">Puts the endpoint into permanent trunking mode and negotiates to convert the link into a trunk link.</span></span> <span data-ttu-id="7747a-182">Der Endpunkt wird zu einer trunk Schnittstelle, auch wenn die benachbarte Schnittstelle keine trunk Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="7747a-182">The endpoint becomes a trunk interface even if the neighboring interface is not a trunk interface.</span></span><br/>                                                               |
| <span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span><dl> <span data-ttu-id="7747a-183"><dt>**Dot1Q Tunnel**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="7747a-183"><dt>**Dot1Q Tunnel**</dt> <dt>6</dt></span></span> </dl>                           | <span data-ttu-id="7747a-184">Konfiguriert die Schnittstelle als Tunnelendpunkt/-Port (nicht abgeschnitten), der in einer asymmetrischen Verknüpfung mit einem 802.1 q-trunk-Port verbunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="7747a-184">Configures the interface as a tunnel (nontrunking) endpoint/port to be connected in an asymmetric link with an 802.1Q trunk port.</span></span> <span data-ttu-id="7747a-185">802.1 q-Tunnelung wird verwendet, um die Kunden-VLAN-Integrität über ein Dienstanbieter Netzwerk hinweg aufrechtzuerhalten.</span><span class="sxs-lookup"><span data-stu-id="7747a-185">802.1Q tunneling is used to maintain customer VLAN integrity across a service provider network.</span></span><br/>                                     |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="7747a-186"><dt>**DMTF reserviert**</dt> <dt>7 32767</dt></span><span class="sxs-lookup"><span data-stu-id="7747a-186"><dt>**DMTF Reserved**</dt> <dt>7 32767</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                                  |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="7747a-187"><dt> **Anbieter reserviert**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="7747a-187"><dt>**Vendor Reserved** </dt> <dt>32768 65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="7747a-188">**Desiredvlantrunkenkapselung**</span><span class="sxs-lookup"><span data-stu-id="7747a-188">**DesiredVLANTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-189">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7747a-189">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7747a-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-191">Der Typ der für die Verwendung angeforderten VLAN-Kapselung.</span><span class="sxs-lookup"><span data-stu-id="7747a-191">The type of VLAN encapsulation that is requested for use.</span></span> <span data-ttu-id="7747a-192">Die derzeit verwendete Kapselung wird von der **operationalvlantrunkenkapselungs** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="7747a-192">The encapsulation currently in use is given by the **OperationalVLANTrunkEncapsulation** property.</span></span> <span data-ttu-id="7747a-193">Diese Eigenschaft ist nur anwendbar, wenn der Endpunkt in einem trunkingmodus betrieben wird (Weitere Informationen finden Sie unter der **operationalendpointmode** -Eigenschaft).</span><span class="sxs-lookup"><span data-stu-id="7747a-193">This property is only applicable when the endpoint is operating in a trunking mode (see the **OperationalEndpointMode** property for additional details).</span></span> <span data-ttu-id="7747a-194">Diese Eigenschaft ist entweder 2 (nicht zutreffend) (d. h. der Endpunkt wird nie in einem Trunking-Modus abgelegt), ein bestimmter Typ (802.1 q oder Cisco ISL) oder 5 (aushandeln) (das Ergebnis der Aushandlung zwischen dieser Schnittstelle und Ihrem Nachbarn).</span><span class="sxs-lookup"><span data-stu-id="7747a-194">This property is either 2 (Not Applicable) (that is, the endpoint will never be placed in a trunking mode), a particular type (802.1Q or Cisco ISL), or 5 (Negotiate) (that is, the result of the negotiation between this interface and its neighbor).</span></span> <span data-ttu-id="7747a-195">Der Wert 5 (aushandeln) ist nicht zulässig, wenn der Endpunkt keine Aushandlung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7747a-195">The value, 5 (Negotiate) is not allowed if the endpoint does not support negotiation.</span></span> <span data-ttu-id="7747a-196">Diese Funktion ist von Hardware und Hersteller abhängig.</span><span class="sxs-lookup"><span data-stu-id="7747a-196">This capability is hardware and vendor dependent.</span></span> <span data-ttu-id="7747a-197">Diese Eigenschaft wird von [**CIM \_ vlanendpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7747a-197">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

<dl> <dt>

<span data-ttu-id="7747a-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (0)</span><span class="sxs-lookup"><span data-stu-id="7747a-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7747a-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="7747a-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7747a-200"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (2)</span><span class="sxs-lookup"><span data-stu-id="7747a-200"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7747a-201"><span id="802.1Q"></span><span id="802.1q"></span>**802.1 q** (3)</span><span class="sxs-lookup"><span data-stu-id="7747a-201"><span id="802.1Q"></span><span id="802.1q"></span>**802.1Q** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7747a-202"><span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**Cisco ISL** (4)</span><span class="sxs-lookup"><span data-stu-id="7747a-202"><span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**Cisco ISL** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7747a-203"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Aushandeln** (5)</span><span class="sxs-lookup"><span data-stu-id="7747a-203"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negotiate** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7747a-204"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (6 32767)</span><span class="sxs-lookup"><span data-stu-id="7747a-204"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (6 32767)</span></span>
</dt> <dt>

<span data-ttu-id="7747a-205"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="7747a-205"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7747a-206">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="7747a-206">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-207">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7747a-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7747a-208">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-209">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="7747a-209">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="7747a-210">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="7747a-210">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7747a-211">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7747a-211">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7747a-212">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="7747a-212">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-213">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7747a-213">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="7747a-214">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-215">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7747a-215">A display name for the object.</span></span> <span data-ttu-id="7747a-216">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7747a-216">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7747a-217">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="7747a-217">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-218">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7747a-218">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7747a-219">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-220">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="7747a-220">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="7747a-221">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) geerbt und ist immer auf 2 (aktiviert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7747a-221">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="7747a-222">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="7747a-222">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-223">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7747a-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7747a-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-225">Der aktivierte und deaktivierte Status dieses Elements.</span><span class="sxs-lookup"><span data-stu-id="7747a-225">The enabled and disabled states of this element.</span></span> <span data-ttu-id="7747a-226">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 5 festgelegt (nicht zutreffend).</span><span class="sxs-lookup"><span data-stu-id="7747a-226">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="7747a-227">**Gvrpstatus**</span><span class="sxs-lookup"><span data-stu-id="7747a-227">**GVRPStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-228">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7747a-228">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7747a-229">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-230">Gibt an, ob das Garp-VLAN-Registrierungs Protokoll (GVRP) auf dem trunk Endpunkt/-Port aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7747a-230">Indicates whether GARP VLAN Registration Protocol (GVRP) is enabled or disabled on the trunk endpoint/port.</span></span> <span data-ttu-id="7747a-231">Diese Eigenschaft ist 2 (nicht zutreffend), es sei denn, GVRP wird vom Endpunkt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7747a-231">This property is 2 (Not Applicable) unless GVRP is supported by the endpoint.</span></span> <span data-ttu-id="7747a-232">Diese Eigenschaft ist nur anwendbar, wenn der Endpunkt im trunkingmodus ausgeführt wird (Weitere Informationen finden Sie unter der **operationalendpointmode** -Eigenschaft).</span><span class="sxs-lookup"><span data-stu-id="7747a-232">This property is applicable only when the endpoint is operating in trunking mode (see the **OperationalEndpointMode** property for additional details).</span></span> <span data-ttu-id="7747a-233">Diese Eigenschaft wird von [**CIM \_ vlanendpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7747a-233">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

<dl> <dt>

<span data-ttu-id="7747a-234"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="7747a-234"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7747a-235"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (2)</span><span class="sxs-lookup"><span data-stu-id="7747a-235"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7747a-236"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="7747a-236"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7747a-237"><span id="Disabled_"></span><span id="disabled_"></span><span id="DISABLED_"></span>**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="7747a-237"><span id="Disabled_"></span><span id="disabled_"></span><span id="DISABLED_"></span>**Disabled** (4 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7747a-238">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="7747a-238">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-239">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7747a-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7747a-240">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-241">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="7747a-241">The current health of the element.</span></span> <span data-ttu-id="7747a-242">Diese Eigenschaft drückt die Integrität dieses Elements aus, aber nicht notwendigerweise die seiner unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="7747a-242">This property expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="7747a-243">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="7747a-243">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="7747a-244">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 5 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7747a-244">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="7747a-245">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7747a-245">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-246">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="7747a-246">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7747a-247">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-248">Das Datum und die Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="7747a-248">The date and time when the object was installed.</span></span> <span data-ttu-id="7747a-249">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="7747a-249">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7747a-250">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7747a-250">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-251">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7747a-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7747a-252">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7747a-253">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="7747a-253">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="7747a-254">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="7747a-254">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="7747a-255">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7747a-255">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7747a-256">**Name**</span><span class="sxs-lookup"><span data-stu-id="7747a-256">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-257">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7747a-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7747a-258">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-259">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="7747a-259">The label by which the object is known.</span></span> <span data-ttu-id="7747a-260">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7747a-260">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7747a-261">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="7747a-261">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-262">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7747a-262">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="7747a-263">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-264">Die Benennungs-Heuristik, die ausgewählt wird, um sicherzustellen, dass der Wert der **Name** -Eigenschaft eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="7747a-264">The naming heuristic that is selected to ensure that the value of the **Name** property is unique.</span></span> <span data-ttu-id="7747a-265">Diese Eigenschaft wird von [**CIM \_ protocolendpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="7747a-265">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7747a-266">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="7747a-266">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-267">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7747a-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7747a-268">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-269">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7747a-269">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="7747a-270">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="7747a-270">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7747a-271">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7747a-271">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7747a-272">**Operationalendpointmode**</span><span class="sxs-lookup"><span data-stu-id="7747a-272">**OperationalEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-273">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7747a-273">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7747a-274">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-275">Der Konfigurations Modus für den VLAN-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="7747a-275">The configuration mode for the VLAN endpoint.</span></span> <span data-ttu-id="7747a-276">Diese Eigenschaft wird von [**CIM \_ vlanendpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7747a-276">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>



| <span data-ttu-id="7747a-277">Wert</span><span class="sxs-lookup"><span data-stu-id="7747a-277">Value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="7747a-278">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7747a-278">Meaning</span></span>                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="7747a-279"><dt>**DMTF reserviert**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7747a-279"><dt>**DMTF Reserved**</dt> <dt>0</dt></span></span> </dl>                       |                                                                                                                                                                                                                                                                     |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="7747a-280"><dt>**Sonstige**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7747a-280"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                       | <span data-ttu-id="7747a-281">Der Endpunkt ist nicht VLAN-fähig.</span><span class="sxs-lookup"><span data-stu-id="7747a-281">The endpoint is not VLAN aware.</span></span><br/>                                                                                                                                                                                                                          |
| <span id="Access"></span><span id="access"></span><span id="ACCESS"></span><dl> <span data-ttu-id="7747a-282"><dt>**Zugriff**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7747a-282"><dt>**Access**</dt> <dt>2</dt></span></span> </dl>                                                   | <span data-ttu-id="7747a-283">Versetzt den Endpunkt in den permanenten nicht Trunking-Modus und aushandgt, um den Link in einen nicht trunk-Link zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="7747a-283">Puts the endpoint into permanent nontrunking mode and negotiates to convert the link into a nontrunk link.</span></span> <span data-ttu-id="7747a-284">Der Endpunkt wird zu einer nicht trunk-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7747a-284">The endpoint becomes a nontrunk interface.</span></span><br/>                                                                                                    |
| <span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span><dl> <span data-ttu-id="7747a-285"><dt>**Dynamisches Auto**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="7747a-285"><dt>**Dynamic Auto**</dt> <dt>3</dt></span></span> </dl>                           | <span data-ttu-id="7747a-286">Macht den Endpunkt in der Lage, den Link in einen trunk Link zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="7747a-286">Makes the endpoint able to convert the link to a trunk link.</span></span> <span data-ttu-id="7747a-287">Der Endpunkt wird zu einer trunk Schnittstelle, wenn die benachbarte Schnittstelle auf den trunk Modus oder den gewünschten Modus festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7747a-287">The endpoint becomes a trunk interface if the neighboring interface is set to trunk or desirable mode.</span></span><br/>                                                                                      |
| <span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span><dl> <span data-ttu-id="7747a-288"><dt>**Dynamisch erwünscht**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="7747a-288"><dt>**Dynamic Desirable**</dt> <dt>4</dt></span></span> </dl>       | <span data-ttu-id="7747a-289">Bewirkt, dass der Endpunkt aktiv versucht, den Link in einen trunk Link zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="7747a-289">Makes the endpoint actively attempt to convert the link to a trunk link.</span></span> <span data-ttu-id="7747a-290">Der Endpunkt wird zu einer trunk Schnittstelle, wenn die benachbarte Schnittstelle auf den trunk-, wünschenswert-oder Auto-Modus festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7747a-290">The endpoint becomes a trunk interface if the neighboring interface is set to trunk, desirable, or auto mode.</span></span> <span data-ttu-id="7747a-291">Dies ist der standardswitchportmodus für alle Ethernet-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="7747a-291">This is the default switch-port mode for all Ethernet interfaces.</span></span><br/> |
| <span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span><dl> <span data-ttu-id="7747a-292"><dt>**Trunk**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="7747a-292"><dt>**Trunk**</dt> <dt>5</dt></span></span> </dl>                                                       | <span data-ttu-id="7747a-293">Versetzt den Endpunkt in den permanenten trunkingmodus und aushandgt, um den Link in einen trunk Link zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="7747a-293">Puts the endpoint into permanent trunking mode and negotiates to convert the link into a trunk link.</span></span> <span data-ttu-id="7747a-294">Der Endpunkt wird zu einer trunk Schnittstelle, auch wenn die benachbarte Schnittstelle keine trunk Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="7747a-294">The endpoint becomes a trunk interface even if the neighboring interface is not a trunk interface.</span></span><br/>                                                  |
| <span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span><dl> <span data-ttu-id="7747a-295"><dt>**Dot1Q Tunnel**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="7747a-295"><dt>**Dot1Q Tunnel**</dt> <dt>6</dt></span></span> </dl>                           | <span data-ttu-id="7747a-296">Konfiguriert die Schnittstelle als Tunnelendpunkt/-Port (nicht abgeschnitten), der in einer asymmetrischen Verknüpfung mit einem 802.1 q-trunk-Port verbunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="7747a-296">Configures the interface as a tunnel (nontrunking) endpoint/port to be connected in an asymmetric link with an 802.1Q trunk port.</span></span> <span data-ttu-id="7747a-297">802.1 q-Tunnelung wird verwendet, um die Kunden-VLAN-Integrität über ein Dienstanbieter Netzwerk hinweg aufrechtzuerhalten.</span><span class="sxs-lookup"><span data-stu-id="7747a-297">802.1Q tunneling is used to maintain customer VLAN integrity across a service provider network.</span></span><br/>                        |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="7747a-298"><dt>**DMTF reserviert**</dt> <dt>7 32767</dt></span><span class="sxs-lookup"><span data-stu-id="7747a-298"><dt>**DMTF Reserved**</dt> <dt>7 32767</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                     |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="7747a-299"><dt> **Anbieter reserviert**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="7747a-299"><dt>**Vendor Reserved** </dt> <dt>32768 65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="7747a-300">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="7747a-300">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-301">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="7747a-301">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7747a-302">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-303">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="7747a-303">The current statuses of the object.</span></span> <span data-ttu-id="7747a-304">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf 2 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7747a-304">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="7747a-305">**Operationalvlantrunkenkapselung**</span><span class="sxs-lookup"><span data-stu-id="7747a-305">**OperationalVLANTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-306">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7747a-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7747a-307">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-308">Der Typ der VLAN-Kapselung, die auf einem Trunk Endpunkt/-Port verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7747a-308">The type of VLAN encapsulation in use on a trunk endpoint/port.</span></span> <span data-ttu-id="7747a-309">Diese Eigenschaft ist entweder 2 (nicht zutreffend) (d. h. der Endpunkt wird nicht im trunkingmodus betrieben), ein bestimmter Typ (3-802.1 q oder 4-Cisco ISL), 5 (aushandeln) (das heißt, die Endpunkte aushandeln den Kapselungstyp).</span><span class="sxs-lookup"><span data-stu-id="7747a-309">This property is either 2 (Not Applicable) (that is, the endpoint is not operating in trunking mode), a particular type (3 - 802.1Q or 4 - Cisco ISL), 5 (Negotiate) (that is, the endpoints are negotiating the encapsulation type).</span></span> <span data-ttu-id="7747a-310">Diese Eigenschaft ist nur anwendbar, wenn der Endpunkt in einem trunkingmodus betrieben wird (Weitere Informationen finden Sie unter der **operationalendpointmode** -Eigenschaft).</span><span class="sxs-lookup"><span data-stu-id="7747a-310">This property is only applicable when the endpoint is operating in a trunking mode (see the **OperationalEndpointMode** property for additional details).</span></span> <span data-ttu-id="7747a-311">Diese Eigenschaft wird von [**CIM \_ vlanendpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7747a-311">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

<dl> <dt>

<span data-ttu-id="7747a-312"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="7747a-312"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7747a-313"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="7747a-313"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7747a-314"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (2)</span><span class="sxs-lookup"><span data-stu-id="7747a-314"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7747a-315"><span id="802.1Q"></span><span id="802.1q"></span>**802.1 q** (3)</span><span class="sxs-lookup"><span data-stu-id="7747a-315"><span id="802.1Q"></span><span id="802.1q"></span>**802.1Q** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7747a-316"><span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**Cisco ISL** (4)</span><span class="sxs-lookup"><span data-stu-id="7747a-316"><span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**Cisco ISL** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7747a-317"><span id="Negotiating"></span><span id="negotiating"></span><span id="NEGOTIATING"></span>**Aushandlung** (5)</span><span class="sxs-lookup"><span data-stu-id="7747a-317"><span id="Negotiating"></span><span id="negotiating"></span><span id="NEGOTIATING"></span>**Negotiating** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7747a-318"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (6 32767)</span><span class="sxs-lookup"><span data-stu-id="7747a-318"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (6 32767)</span></span>
</dt> <dt>

<span data-ttu-id="7747a-319"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="7747a-319"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7747a-320">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="7747a-320">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-321">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7747a-321">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="7747a-322">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-323">Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 ("Other") festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7747a-323">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="7747a-324">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="7747a-324">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="7747a-325">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7747a-325">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7747a-326">**Otherendpointmode**</span><span class="sxs-lookup"><span data-stu-id="7747a-326">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-327">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7747a-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7747a-328">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-329">Der Typ des VLAN-Endpunkt Modells, das von diesem VLAN-Endpunkt unterstützt wird, wenn der Wert der **operationalendpointmode** -Eigenschaft auf 1 (sonstige) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7747a-329">The type of VLAN endpoint model that is supported by this VLAN endpoint, when the value of the **OperationalEndpointMode** property is set to 1 (Other).</span></span> <span data-ttu-id="7747a-330">Diese Eigenschaft sollte auf **null** festgelegt werden, wenn die **operationalendpointmode** -Eigenschaft einen anderen Wert als 1 hat.</span><span class="sxs-lookup"><span data-stu-id="7747a-330">This property should be set to **Null** when the **OperationalEndpointMode** property is any value other than 1.</span></span> <span data-ttu-id="7747a-331">Diese Eigenschaft wird von [**CIM \_ vlanendpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7747a-331">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="7747a-332">**Othertrunkenkapselung**</span><span class="sxs-lookup"><span data-stu-id="7747a-332">**OtherTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-333">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7747a-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7747a-334">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-335">Der Typ der VLAN-Kapselung, die von diesem VLAN-Endpunkt unterstützt wird, wenn der Wert der Eigenschaft **operationalvlantrunkenkapselung** auf 1 (sonstige) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7747a-335">The type of VLAN encapsulation that is supported by this VLAN endpoint, when the value of the **OperationalVLANTrunkEncapsulation** property is set to 1 (Other).</span></span> <span data-ttu-id="7747a-336">Diese Eigenschaft sollte auf **null** festgelegt werden, wenn die gewünschte Kapselungs Eigenschaft einen anderen Wert als 1 hat.</span><span class="sxs-lookup"><span data-stu-id="7747a-336">This property should be set to **Null** when the desired encapsulation property is any value other than 1.</span></span> <span data-ttu-id="7747a-337">Diese Eigenschaft wird von [**CIM \_ vlanendpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7747a-337">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="7747a-338">**OtherTypeDescription**</span><span class="sxs-lookup"><span data-stu-id="7747a-338">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-339">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7747a-339">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="7747a-340">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-341">Der Typ des Protokoll Endpunkts, wenn die **Type** -Eigenschaft dieser Klasse (oder eine ihrer Unterklassen) auf 1 (sonstige) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7747a-341">The type of protocol endpoint when the **Type** property of this class (or any of its subclasses) is set to 1 (Other).</span></span> <span data-ttu-id="7747a-342">Diese Eigenschaft wird von [**CIM \_ protocolendpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)geerbt und ist immer auf "Virtuelles Ethernet" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7747a-342">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint), and it is always set to "Virtual Ethernet".</span></span>

</dd> <dt>

<span data-ttu-id="7747a-343">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="7747a-343">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-344">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7747a-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7747a-345">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-346">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="7747a-346">Provides high level status information.</span></span> <span data-ttu-id="7747a-347">Diese Eigenschaft sollte in Verbindung mit der **detailedstatus** -Eigenschaft verwendet werden, um allgemeine und ausführliche Integritäts Statusinformationen für das-Element und seine unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7747a-347">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="7747a-348">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="7747a-348">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7747a-349">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7747a-349">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7747a-350">**Protocoliftype**</span><span class="sxs-lookup"><span data-stu-id="7747a-350">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-351">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7747a-351">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7747a-352">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-353">Der [IANA iftype-MIB](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="7747a-353">The [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <span data-ttu-id="7747a-354">Diese Eigenschaft wird von [**CIM \_ protocolendpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)geerbt und ist immer auf 1 (sonstige) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7747a-354">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint), and it is always set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="7747a-355">**ProtocolType**</span><span class="sxs-lookup"><span data-stu-id="7747a-355">**ProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-356">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7747a-356">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7747a-357">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-358">Diese Eigenschaft wird von [**CIM \_ protocolendpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="7747a-358">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7747a-359">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="7747a-359">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-360">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7747a-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7747a-361">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-362">Der zuletzt angeforderte oder gewünschte Status für den Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="7747a-362">The last requested or desired state for the management service.</span></span> <span data-ttu-id="7747a-363">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 12 (nicht zutreffend) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7747a-363">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="7747a-364">Wert</span><span class="sxs-lookup"><span data-stu-id="7747a-364">Value</span></span>                                                                         | <span data-ttu-id="7747a-365">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7747a-365">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="7747a-366"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="7747a-366"><dt>12</dt></span></span> </dl> | <span data-ttu-id="7747a-367">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="7747a-367">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7747a-368">**Status**</span><span class="sxs-lookup"><span data-stu-id="7747a-368">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-369">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7747a-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7747a-370">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-371">Beschreibt den Status des Elements.</span><span class="sxs-lookup"><span data-stu-id="7747a-371">Describes the status of the element.</span></span> <span data-ttu-id="7747a-372">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7747a-372">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="7747a-373">Okay</span><span class="sxs-lookup"><span data-stu-id="7747a-373">"OK"</span></span>

<span data-ttu-id="7747a-374">Zeit</span><span class="sxs-lookup"><span data-stu-id="7747a-374">"Error"</span></span>

<span data-ttu-id="7747a-375">Zerstört</span><span class="sxs-lookup"><span data-stu-id="7747a-375">"Degraded"</span></span>

<span data-ttu-id="7747a-376">Unbekannter</span><span class="sxs-lookup"><span data-stu-id="7747a-376">"Unknown"</span></span>

<span data-ttu-id="7747a-377">"Pred Fail"</span><span class="sxs-lookup"><span data-stu-id="7747a-377">"Pred Fail"</span></span>

<span data-ttu-id="7747a-378">Fahren</span><span class="sxs-lookup"><span data-stu-id="7747a-378">"Starting"</span></span>

<span data-ttu-id="7747a-379">Hindern</span><span class="sxs-lookup"><span data-stu-id="7747a-379">"Stopping"</span></span>

<span data-ttu-id="7747a-380">Leistungs</span><span class="sxs-lookup"><span data-stu-id="7747a-380">"Service"</span></span>

<span data-ttu-id="7747a-381">Gestresst</span><span class="sxs-lookup"><span data-stu-id="7747a-381">"Stressed"</span></span>

<span data-ttu-id="7747a-382">"Nicht wiederherstellen"</span><span class="sxs-lookup"><span data-stu-id="7747a-382">"NonRecover"</span></span>

<span data-ttu-id="7747a-383">"Kein Kontakt"</span><span class="sxs-lookup"><span data-stu-id="7747a-383">"No Contact"</span></span>

<span data-ttu-id="7747a-384">"Verlorene comm"</span><span class="sxs-lookup"><span data-stu-id="7747a-384">"Lost Comm"</span></span>

</dd> <dt>

<span data-ttu-id="7747a-385">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="7747a-385">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-386">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="7747a-386">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7747a-387">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-388">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="7747a-388">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="7747a-389">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf "OK" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7747a-389">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="7747a-390">**Supportedendpointmodes**</span><span class="sxs-lookup"><span data-stu-id="7747a-390">**SupportedEndpointModes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-391">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="7747a-391">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7747a-392">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7747a-393">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="7747a-393">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="7747a-394">Die von diesem Port unterstützten Endpunkt Modi.</span><span class="sxs-lookup"><span data-stu-id="7747a-394">The endpoint modes supported by this port.</span></span>

</dd> <dt>

<span data-ttu-id="7747a-395">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="7747a-395">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-396">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7747a-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7747a-397">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-398">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="7747a-398">The creation class name of the scoping system.</span></span> <span data-ttu-id="7747a-399">Diese Eigenschaft wird von [**CIM \_ serviceaccesspoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)geerbt und ist immer auf "MSVM \_ virtualswitch" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7747a-399">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint), and it is always set to "Msvm\_VirtualSwitch"</span></span>

</dd> <dt>

<span data-ttu-id="7747a-400">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="7747a-400">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-401">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7747a-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7747a-402">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-403">Der Systemname des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="7747a-403">The system name of the scoping system.</span></span> <span data-ttu-id="7747a-404">Diese Eigenschaft wird von [**CIM \_ serviceaccesspoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7747a-404">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="7747a-405">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="7747a-405">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-406">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="7747a-406">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7747a-407">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-408">Das Datum und die Uhrzeit der letzten Änderung des aktivierten Zustands des Elements.</span><span class="sxs-lookup"><span data-stu-id="7747a-408">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="7747a-409">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, wird jedoch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7747a-409">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="7747a-410">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="7747a-410">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7747a-411">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7747a-411">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7747a-412">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7747a-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7747a-413">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="7747a-413">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="7747a-414">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="7747a-414">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7747a-415">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7747a-415">Remarks</span></span>

<span data-ttu-id="7747a-416">Der Zugriff auf die **MSVM \_ vlanendpoint** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="7747a-416">Access to the **Msvm\_VLANEndpoint** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="7747a-417">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="7747a-417">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="7747a-418">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7747a-418">Examples</span></span>

<span data-ttu-id="7747a-419">Weitere Informationen finden Sie unter [Abfragen von Netzwerk Objekten](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="7747a-419">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7747a-420">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7747a-420">Requirements</span></span>



| <span data-ttu-id="7747a-421">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7747a-421">Requirement</span></span> | <span data-ttu-id="7747a-422">Wert</span><span class="sxs-lookup"><span data-stu-id="7747a-422">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7747a-423">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7747a-423">Minimum supported client</span></span><br/> | <span data-ttu-id="7747a-424">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7747a-424">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7747a-425">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7747a-425">Minimum supported server</span></span><br/> | <span data-ttu-id="7747a-426">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7747a-426">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7747a-427">Namespace</span><span class="sxs-lookup"><span data-stu-id="7747a-427">Namespace</span></span><br/>                | <span data-ttu-id="7747a-428">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="7747a-428">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7747a-429">MOF</span><span class="sxs-lookup"><span data-stu-id="7747a-429">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7747a-430"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7747a-430"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7747a-431">DLL</span><span class="sxs-lookup"><span data-stu-id="7747a-431">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7747a-432"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7747a-432"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7747a-433">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7747a-433">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7747a-434">**CIM- \_ vlanendpoint**</span><span class="sxs-lookup"><span data-stu-id="7747a-434">**CIM\_VLANEndpoint**</span></span>](cim-vlanendpoint.md)
</dt> <dt>

[<span data-ttu-id="7747a-435">**CIM- \_ vlanendpoint**</span><span class="sxs-lookup"><span data-stu-id="7747a-435">**CIM\_VLANEndpoint**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)
</dt> </dl>

 

