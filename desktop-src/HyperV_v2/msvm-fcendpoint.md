---
description: Stellt den logischen Verbindungspunkt für einen Fibre Channel-Port dar.
ms.assetid: 54e9cb76-04f2-417b-b250-1b3156772694
title: Msvm_FcEndpoint-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcEndpoint
- Msvm_FcEndpoint.InstanceID
- Msvm_FcEndpoint.Caption
- Msvm_FcEndpoint.Description
- Msvm_FcEndpoint.ElementName
- Msvm_FcEndpoint.InstallDate
- Msvm_FcEndpoint.Name
- Msvm_FcEndpoint.OperationalStatus
- Msvm_FcEndpoint.StatusDescriptions
- Msvm_FcEndpoint.Status
- Msvm_FcEndpoint.HealthState
- Msvm_FcEndpoint.CommunicationStatus
- Msvm_FcEndpoint.DetailedStatus
- Msvm_FcEndpoint.OperatingStatus
- Msvm_FcEndpoint.PrimaryStatus
- Msvm_FcEndpoint.EnabledState
- Msvm_FcEndpoint.OtherEnabledState
- Msvm_FcEndpoint.RequestedState
- Msvm_FcEndpoint.EnabledDefault
- Msvm_FcEndpoint.TimeOfLastStateChange
- Msvm_FcEndpoint.AvailableRequestedStates
- Msvm_FcEndpoint.TransitioningToState
- Msvm_FcEndpoint.SystemCreationClassName
- Msvm_FcEndpoint.SystemName
- Msvm_FcEndpoint.CreationClassName
- Msvm_FcEndpoint.NameFormat
- Msvm_FcEndpoint.ProtocolType
- Msvm_FcEndpoint.ProtocolIFType
- Msvm_FcEndpoint.OtherTypeDescription
- Msvm_FcEndpoint.Connected
- Msvm_FcEndpoint.WWPN
- Msvm_FcEndpoint.WWNN
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b28136cfc4f0afcf84b5f53ade4976760c997e36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526843"
---
# <a name="msvm_fcendpoint-class"></a><span data-ttu-id="e2315-103">MSVM \_ fcendpoint-Klasse</span><span class="sxs-lookup"><span data-stu-id="e2315-103">Msvm\_FcEndpoint class</span></span>

<span data-ttu-id="e2315-104">Stellt den logischen Verbindungspunkt für einen Fibre Channel-Port dar.</span><span class="sxs-lookup"><span data-stu-id="e2315-104">Represents the logical connection point for a Fibre Channel port.</span></span> <span data-ttu-id="e2315-105">Wenn der Fibre Channel-Endpunkt mit einem Switchport verbunden ist, verfügt der Fibre Channel Port, der mit dem Fibre Channel-Endpunkt verbunden ist, über Fibre Channel Konnektivität.</span><span class="sxs-lookup"><span data-stu-id="e2315-105">When the Fibre Channel endpoint is connected to a switch port, the Fibre Channel port connected to the Fibre Channel endpoint has Fibre Channel connectivity.</span></span>

<span data-ttu-id="e2315-106">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e2315-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2315-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2315-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcEndpoint : CIM_ProtocolEndpoint
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
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   NameFormat;
  uint16   ProtocolType;
  uint16   ProtocolIFType;
  string   OtherTypeDescription;
  boolean  Connected;
  string   WWPN;
  string   WWNN;
};
```

## <a name="members"></a><span data-ttu-id="e2315-108">Member</span><span class="sxs-lookup"><span data-stu-id="e2315-108">Members</span></span>

<span data-ttu-id="e2315-109">Die **MSVM \_ fcendpoint** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e2315-109">The **Msvm\_FcEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="e2315-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="e2315-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="e2315-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e2315-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e2315-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="e2315-112">Methods</span></span>

<span data-ttu-id="e2315-113">Die **MSVM \_ fcendpoint** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="e2315-113">The **Msvm\_FcEndpoint** class has these methods.</span></span>



| <span data-ttu-id="e2315-114">Methode</span><span class="sxs-lookup"><span data-stu-id="e2315-114">Method</span></span>                                                           | <span data-ttu-id="e2315-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e2315-115">Description</span></span>                         |
|:-----------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="e2315-116">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="e2315-116">**RequestStateChange**</span></span>](msvm-fcendpoint-requeststatechange.md) | <span data-ttu-id="e2315-117">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="e2315-117">Requests a state change.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e2315-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e2315-118">Properties</span></span>

<span data-ttu-id="e2315-119">Die **MSVM \_ fcendpoint** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e2315-119">The **Msvm\_FcEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e2315-120">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="e2315-120">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2315-121">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="e2315-121">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e2315-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2315-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2315-123">Gibt die möglichen Werte für den *requestedstate* -Parameter der [**requestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) -Methode an, die zum Initiieren einer Zustandsänderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e2315-123">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="e2315-124">Bei den aufgelisteten Werten handelt es sich um eine Teilmenge der Werte in der **requestedstaatsupported** -Eigenschaft der zugeordneten Instanz von **CIM \_ enabledlogicalelementfunctions**, bei der die ausgewählten Werte eine Funktion des aktuellen Zustands der [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) -Klasse sind.</span><span class="sxs-lookup"><span data-stu-id="e2315-124">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class.</span></span> <span data-ttu-id="e2315-125">Diese Eigenschaft darf nicht **null** sein, wenn eine Implementierung den Satz möglicher Werte als Funktion des aktuellen Zustands ankündigen kann.</span><span class="sxs-lookup"><span data-stu-id="e2315-125">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="e2315-126">Diese Eigenschaft ist **null** , wenn eine Implementierung den Satz möglicher Werte nicht als Funktion des aktuellen Zustands bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="e2315-126">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="e2315-127">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="e2315-127">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="e2315-128"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="e2315-128"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-129"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="e2315-129"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-130"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Herunter** fahren (4)</span><span class="sxs-lookup"><span data-stu-id="e2315-130"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-131"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="e2315-131"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-132"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="e2315-132"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-133"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>Zurück **stellen (8** )</span><span class="sxs-lookup"><span data-stu-id="e2315-133"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-134"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Still **legung (9** )</span><span class="sxs-lookup"><span data-stu-id="e2315-134"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-135"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Neustart** (10)</span><span class="sxs-lookup"><span data-stu-id="e2315-135"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-136"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Zurücksetzen** (11)</span><span class="sxs-lookup"><span data-stu-id="e2315-136"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-137"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reserviert** (..</span><span class="sxs-lookup"><span data-stu-id="e2315-137"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="e2315-138">)</span><span class="sxs-lookup"><span data-stu-id="e2315-138">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e2315-139">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e2315-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2315-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2315-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2315-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2315-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2315-142">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="e2315-142">A short description of the object.</span></span> <span data-ttu-id="e2315-143">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e2315-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2315-144">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="e2315-144">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2315-145">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2315-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2315-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2315-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2315-147">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="e2315-147">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="e2315-148">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="e2315-148">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e2315-149">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e2315-149">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2315-150">**Verbunden**</span><span class="sxs-lookup"><span data-stu-id="e2315-150">**Connected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2315-151">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="e2315-151">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2315-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2315-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2315-153">Diese Eigenschaft ist auf **true** festgelegt, wenn dieser Fibre Channel Endpunkt aktiv mit einem anderen Fibre Channel Endpunkt verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="e2315-153">This property is set to **True** if this Fibre Channel endpoint is actively connected to another Fibre Channel endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="e2315-154">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="e2315-154">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2315-155">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2315-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2315-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2315-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2315-157">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="e2315-157">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="e2315-158">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e2315-158">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="e2315-159">Diese Eigenschaft wird von [**CIM \_ serviceaccesspoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e2315-159">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="e2315-160">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e2315-160">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2315-161">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2315-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2315-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2315-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2315-163">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="e2315-163">A description of the object.</span></span> <span data-ttu-id="e2315-164">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e2315-164">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2315-165">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="e2315-165">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2315-166">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2315-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2315-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2315-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2315-168">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="e2315-168">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="e2315-169">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="e2315-169">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e2315-170">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e2315-170">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2315-171">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e2315-171">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2315-172">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2315-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2315-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2315-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2315-174">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e2315-174">A display name for the object.</span></span> <span data-ttu-id="e2315-175">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e2315-175">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2315-176">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="e2315-176">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2315-177">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2315-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2315-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2315-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2315-179">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="e2315-179">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="e2315-180">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, und es handelt sich um einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="e2315-180">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e2315-181"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="e2315-181"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-182"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="e2315-182"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-183"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Aktiviert, aber offline** (6)</span><span class="sxs-lookup"><span data-stu-id="e2315-183"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e2315-184">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="e2315-184">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2315-185">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2315-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2315-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2315-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2315-187">Gibt den aktivierten Zustand des geplanten Systems an.</span><span class="sxs-lookup"><span data-stu-id="e2315-187">Specifies the enabled state of the planned system.</span></span> <span data-ttu-id="e2315-188">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e2315-188">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it can be one of the following values.</span></span>



| <span data-ttu-id="e2315-189">Wert</span><span class="sxs-lookup"><span data-stu-id="e2315-189">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="e2315-190">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e2315-190">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="e2315-191"><dt>**Deaktiviert**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e2315-191"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="e2315-192">Das System ist ausgeschaltet.</span><span class="sxs-lookup"><span data-stu-id="e2315-192">The system is turned off.</span></span><br/>                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="e2315-193"><dt>**Nicht zutreffend**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="e2315-193"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="e2315-194">Das Element unterstützt das Aktivieren oder Deaktivieren des Elements nicht.</span><span class="sxs-lookup"><span data-stu-id="e2315-194">The element does not support being enabled or disabled.</span></span><br/>               |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="e2315-195"><dt>**Aktiviert, aber offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="e2315-195"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="e2315-196">Das System ist aktiviert, aber offline.</span><span class="sxs-lookup"><span data-stu-id="e2315-196">The system is enabled, but offline.</span></span> <span data-ttu-id="e2315-197">Alle neuen Anforderungen werden gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e2315-197">Any new requests will be dropped.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e2315-198">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="e2315-198">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2315-199">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2315-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2315-200">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2315-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2315-201">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="e2315-201">The current health of the element.</span></span> <span data-ttu-id="e2315-202">Diese Eigenschaft drückt die Integrität dieses Elements aus, aber nicht notwendigerweise die seiner unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="e2315-202">This property expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="e2315-203">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="e2315-203">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="e2315-204">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e2315-204">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2315-205">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e2315-205">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2315-206">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="e2315-206">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e2315-207">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2315-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2315-208">Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="e2315-208">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="e2315-209">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e2315-209">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2315-210">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e2315-210">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2315-211">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2315-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2315-212">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2315-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2315-213">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="e2315-213">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e2315-214">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="e2315-214">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e2315-215">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e2315-215">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2315-216">**Name**</span><span class="sxs-lookup"><span data-stu-id="e2315-216">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2315-217">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2315-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2315-218">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2315-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2315-219">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="e2315-219">The label by which the object is known.</span></span> <span data-ttu-id="e2315-220">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e2315-220">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2315-221">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="e2315-221">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2315-222">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2315-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2315-223">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2315-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2315-224">Qualifizierer: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="e2315-224">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="e2315-225">Enthält die Namensheuristik, die ausgewählt wird, um sicherzustellen, dass der Wert der **Name** -Eigenschaft eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="e2315-225">Contains the naming heuristic that is selected to ensure that the value of the **Name** property is unique.</span></span> <span data-ttu-id="e2315-226">Diese Eigenschaft wird von [**CIM \_ protocolendpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e2315-226">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="e2315-227">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="e2315-227">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2315-228">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2315-228">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2315-229">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2315-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2315-230">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e2315-230">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="e2315-231">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="e2315-231">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e2315-232">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e2315-232">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2315-233">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="e2315-233">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2315-234">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="e2315-234">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e2315-235">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2315-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2315-236">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="e2315-236">The current statuses of the object.</span></span> <span data-ttu-id="e2315-237">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e2315-237">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2315-238">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="e2315-238">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2315-239">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2315-239">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2315-240">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2315-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2315-241">Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 ("Other") festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e2315-241">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="e2315-242">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="e2315-242">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="e2315-243">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e2315-243">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e2315-244">**OtherTypeDescription**</span><span class="sxs-lookup"><span data-stu-id="e2315-244">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2315-245">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2315-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2315-246">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2315-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2315-247">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="e2315-247">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="e2315-248">Eine Zeichenfolge, die den Typ des Protokoll Endpunkts beschreibt, wenn die **protocoliftype** -Eigenschaft dieser Klasse (oder eine ihrer Unterklassen) auf 1 (sonstige) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e2315-248">A string that describes the type of protocol endpoint when the **ProtocolIFType** property of this class (or any of its subclasses) is set to 1 (Other).</span></span> <span data-ttu-id="e2315-249">Diese Eigenschaft sollte auf **null** festgelegt werden, wenn die **protocoliftype** -Eigenschaft einen anderen Wert als 1 hat.</span><span class="sxs-lookup"><span data-stu-id="e2315-249">This property should be set to **Null** when the **ProtocolIFType** property is any value other than 1.</span></span> <span data-ttu-id="e2315-250">Diese Eigenschaft wird von [**CIM \_ protocolendpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e2315-250">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="e2315-251">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="e2315-251">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2315-252">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2315-252">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2315-253">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2315-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2315-254">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="e2315-254">Provides high level status information.</span></span> <span data-ttu-id="e2315-255">Diese Eigenschaft sollte in Verbindung mit der **detailedstatus** -Eigenschaft verwendet werden, um allgemeine und ausführliche Integritäts Statusinformationen für das-Element und seine unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e2315-255">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="e2315-256">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="e2315-256">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e2315-257">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e2315-257">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2315-258">**Protocoliftype**</span><span class="sxs-lookup"><span data-stu-id="e2315-258">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2315-259">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2315-259">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2315-260">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2315-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2315-261">Die-Eigenschaft wird verwendet, um Instanzen dieser Klasse zu kategorisieren und zu klassifizieren.</span><span class="sxs-lookup"><span data-stu-id="e2315-261">The property is used to categorize and classify instances of this class.</span></span> <span data-ttu-id="e2315-262">Wenn **protocoliftype** auf 1 (Sonstiges) festgelegt ist, sollten die Typinformationen in der **OtherTypeDescription** -Eigenschaft bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e2315-262">If the **ProtocolIFType** is set to 1 (Other), then the type information should be provided in the **OtherTypeDescription** property.</span></span> <span data-ttu-id="e2315-263">Diese Eigenschaft wird von [**CIM \_ protocolendpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e2315-263">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

> [!Note]  
> <span data-ttu-id="e2315-264">**Protocoliftype** ist eine Enumeration, die mit der [IANA iftype-MIB](https://www.iana.org/assignments/ianaiftype-mib)synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="e2315-264">**ProtocolIFType** is an enumeration that is synchronized with the [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <span data-ttu-id="e2315-265">Weitere Werte, die von der DMTF definiert werden, sind ebenfalls enthalten.</span><span class="sxs-lookup"><span data-stu-id="e2315-265">Additional values defined by the DMTF are also included.</span></span>

 

<dl> <dt>

<span data-ttu-id="e2315-266"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="e2315-266"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-267"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="e2315-267"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-268"><span id="Regular_1822"></span><span id="regular_1822"></span><span id="REGULAR_1822"></span>**Regulär 1822** (2)</span><span class="sxs-lookup"><span data-stu-id="e2315-268"><span id="Regular_1822"></span><span id="regular_1822"></span><span id="REGULAR_1822"></span>**Regular 1822** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-269"><span id="HDH_1822"></span><span id="hdh_1822"></span>**HDH 1822** (3)</span><span class="sxs-lookup"><span data-stu-id="e2315-269"><span id="HDH_1822"></span><span id="hdh_1822"></span>**HDH 1822** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-270"><span id="DDN_X.25"></span><span id="ddn_x.25"></span>**DDN X. 25** (4)</span><span class="sxs-lookup"><span data-stu-id="e2315-270"><span id="DDN_X.25"></span><span id="ddn_x.25"></span>**DDN X.25** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-271"><span id="RFC877_X.25"></span><span id="rfc877_x.25"></span>**RFC877 X. 25** (5)</span><span class="sxs-lookup"><span data-stu-id="e2315-271"><span id="RFC877_X.25"></span><span id="rfc877_x.25"></span>**RFC877 X.25** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-272"><span id="Ethernet_CSMA_CD"></span><span id="ethernet_csma_cd"></span><span id="ETHERNET_CSMA_CD"></span>**Ethernet-CSMA/CD** (6)</span><span class="sxs-lookup"><span data-stu-id="e2315-272"><span id="Ethernet_CSMA_CD"></span><span id="ethernet_csma_cd"></span><span id="ETHERNET_CSMA_CD"></span>**Ethernet CSMA/CD** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-273"><span id="ISO_802.3_CSMA_CD"></span><span id="iso_802.3_csma_cd"></span>**ISO 802,3 CSMA/CD** (7)</span><span class="sxs-lookup"><span data-stu-id="e2315-273"><span id="ISO_802.3_CSMA_CD"></span><span id="iso_802.3_csma_cd"></span>**ISO 802.3 CSMA/CD** (7)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-274"><span id="ISO_802.4_Token_Bus"></span><span id="iso_802.4_token_bus"></span><span id="ISO_802.4_TOKEN_BUS"></span>**ISO 802,4-tokbus** (8)</span><span class="sxs-lookup"><span data-stu-id="e2315-274"><span id="ISO_802.4_Token_Bus"></span><span id="iso_802.4_token_bus"></span><span id="ISO_802.4_TOKEN_BUS"></span>**ISO 802.4 Token Bus** (8)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-275"><span id="ISO_802.5_Token_Ring"></span><span id="iso_802.5_token_ring"></span><span id="ISO_802.5_TOKEN_RING"></span>**ISO 802,5-TokenRing** (9)</span><span class="sxs-lookup"><span data-stu-id="e2315-275"><span id="ISO_802.5_Token_Ring"></span><span id="iso_802.5_token_ring"></span><span id="ISO_802.5_TOKEN_RING"></span>**ISO 802.5 Token Ring** (9)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-276"><span id="ISO_802.6_MAN"></span><span id="iso_802.6_man"></span>**ISO 802,6 Mann** (10)</span><span class="sxs-lookup"><span data-stu-id="e2315-276"><span id="ISO_802.6_MAN"></span><span id="iso_802.6_man"></span>**ISO 802.6 MAN** (10)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-277"><span id="StarLAN"></span><span id="starlan"></span><span id="STARLAN"></span>**StarLAN** (11)</span><span class="sxs-lookup"><span data-stu-id="e2315-277"><span id="StarLAN"></span><span id="starlan"></span><span id="STARLAN"></span>**StarLAN** (11)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-278"><span id="Proteon_10Mbit"></span><span id="proteon_10mbit"></span><span id="PROTEON_10MBIT"></span>**Schützfür 10Mbit** (12)</span><span class="sxs-lookup"><span data-stu-id="e2315-278"><span id="Proteon_10Mbit"></span><span id="proteon_10mbit"></span><span id="PROTEON_10MBIT"></span>**Proteon 10Mbit** (12)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-279"><span id="Proteon_80Mbit"></span><span id="proteon_80mbit"></span><span id="PROTEON_80MBIT"></span>**Schützlos** (13)</span><span class="sxs-lookup"><span data-stu-id="e2315-279"><span id="Proteon_80Mbit"></span><span id="proteon_80mbit"></span><span id="PROTEON_80MBIT"></span>**Proteon 80Mbit** (13)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-280"><span id="HyperChannel"></span><span id="hyperchannel"></span><span id="HYPERCHANNEL"></span>**Hyperchannel** (14)</span><span class="sxs-lookup"><span data-stu-id="e2315-280"><span id="HyperChannel"></span><span id="hyperchannel"></span><span id="HYPERCHANNEL"></span>**HyperChannel** (14)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-281"><span id="FDDI"></span><span id="fddi"></span>**F-di** (15)</span><span class="sxs-lookup"><span data-stu-id="e2315-281"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (15)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-282"><span id="LAP-B"></span><span id="lap-b"></span>**Lap-B** (16)</span><span class="sxs-lookup"><span data-stu-id="e2315-282"><span id="LAP-B"></span><span id="lap-b"></span>**LAP-B** (16)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-283"><span id="SDLC"></span><span id="sdlc"></span>**SDLC** (17)</span><span class="sxs-lookup"><span data-stu-id="e2315-283"><span id="SDLC"></span><span id="sdlc"></span>**SDLC** (17)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-284"><span id="DS1"></span><span id="ds1"></span>**Ds1** (18)</span><span class="sxs-lookup"><span data-stu-id="e2315-284"><span id="DS1"></span><span id="ds1"></span>**DS1** (18)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-285"><span id="E1"></span><span id="e1"></span>**E1** (19)</span><span class="sxs-lookup"><span data-stu-id="e2315-285"><span id="E1"></span><span id="e1"></span>**E1** (19)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-286"><span id="Basic_ISDN"></span><span id="basic_isdn"></span><span id="BASIC_ISDN"></span>**Basis-ISDN** (20)</span><span class="sxs-lookup"><span data-stu-id="e2315-286"><span id="Basic_ISDN"></span><span id="basic_isdn"></span><span id="BASIC_ISDN"></span>**Basic ISDN** (20)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-287"><span id="Primary_ISDN"></span><span id="primary_isdn"></span><span id="PRIMARY_ISDN"></span>**Primärer ISDN** (21)</span><span class="sxs-lookup"><span data-stu-id="e2315-287"><span id="Primary_ISDN"></span><span id="primary_isdn"></span><span id="PRIMARY_ISDN"></span>**Primary ISDN** (21)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-288"><span id="Proprietary_Point-to-Point_Serial"></span><span id="proprietary_point-to-point_serial"></span><span id="PROPRIETARY_POINT-TO-POINT_SERIAL"></span>**Proprietäre Punkt-zu-Punkt-seriell** (22)</span><span class="sxs-lookup"><span data-stu-id="e2315-288"><span id="Proprietary_Point-to-Point_Serial"></span><span id="proprietary_point-to-point_serial"></span><span id="PROPRIETARY_POINT-TO-POINT_SERIAL"></span>**Proprietary Point-to-Point Serial** (22)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-289"><span id="PPP"></span><span id="ppp"></span>**PPP** (23)</span><span class="sxs-lookup"><span data-stu-id="e2315-289"><span id="PPP"></span><span id="ppp"></span>**PPP** (23)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-290"><span id="Software_Loopback"></span><span id="software_loopback"></span><span id="SOFTWARE_LOOPBACK"></span>**Software Loopback** (24)</span><span class="sxs-lookup"><span data-stu-id="e2315-290"><span id="Software_Loopback"></span><span id="software_loopback"></span><span id="SOFTWARE_LOOPBACK"></span>**Software Loopback** (24)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-291"><span id="EON"></span><span id="eon"></span>**EON** (25)</span><span class="sxs-lookup"><span data-stu-id="e2315-291"><span id="EON"></span><span id="eon"></span>**EON** (25)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-292"><span id="Ethernet_3Mbit"></span><span id="ethernet_3mbit"></span><span id="ETHERNET_3MBIT"></span>**Ethernet 3Mbit** (26)</span><span class="sxs-lookup"><span data-stu-id="e2315-292"><span id="Ethernet_3Mbit"></span><span id="ethernet_3mbit"></span><span id="ETHERNET_3MBIT"></span>**Ethernet 3Mbit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-293"><span id="NSIP"></span><span id="nsip"></span>**NSIP** (27)</span><span class="sxs-lookup"><span data-stu-id="e2315-293"><span id="NSIP"></span><span id="nsip"></span>**NSIP** (27)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-294"><span id="SLIP"></span><span id="slip"></span>**Slip** (28)</span><span class="sxs-lookup"><span data-stu-id="e2315-294"><span id="SLIP"></span><span id="slip"></span>**SLIP** (28)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-295"><span id="Ultra"></span><span id="ultra"></span><span id="ULTRA"></span>**Ultra** (29)</span><span class="sxs-lookup"><span data-stu-id="e2315-295"><span id="Ultra"></span><span id="ultra"></span><span id="ULTRA"></span>**Ultra** (29)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-296"><span id="DS3"></span><span id="ds3"></span>**DS3** (30)</span><span class="sxs-lookup"><span data-stu-id="e2315-296"><span id="DS3"></span><span id="ds3"></span>**DS3** (30)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-297"><span id="SIP"></span><span id="sip"></span>**SIP** (31)</span><span class="sxs-lookup"><span data-stu-id="e2315-297"><span id="SIP"></span><span id="sip"></span>**SIP** (31)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-298"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (32)</span><span class="sxs-lookup"><span data-stu-id="e2315-298"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (32)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-299"><span id="RS-232"></span><span id="rs-232"></span>**RS-232** (33)</span><span class="sxs-lookup"><span data-stu-id="e2315-299"><span id="RS-232"></span><span id="rs-232"></span>**RS-232** (33)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-300"><span id="Parallel"></span><span id="parallel"></span><span id="PARALLEL"></span>**Parallel** (34)</span><span class="sxs-lookup"><span data-stu-id="e2315-300"><span id="Parallel"></span><span id="parallel"></span><span id="PARALLEL"></span>**Parallel** (34)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-301"><span id="ARCNet"></span><span id="arcnet"></span><span id="ARCNET"></span>**ARCNET** (35)</span><span class="sxs-lookup"><span data-stu-id="e2315-301"><span id="ARCNet"></span><span id="arcnet"></span><span id="ARCNET"></span>**ARCNet** (35)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-302"><span id="ARCNet_Plus"></span><span id="arcnet_plus"></span><span id="ARCNET_PLUS"></span>**ARCNET Plus** (36)</span><span class="sxs-lookup"><span data-stu-id="e2315-302"><span id="ARCNet_Plus"></span><span id="arcnet_plus"></span><span id="ARCNET_PLUS"></span>**ARCNet Plus** (36)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-303"><span id="ATM"></span><span id="atm"></span>**ATM** (37)</span><span class="sxs-lookup"><span data-stu-id="e2315-303"><span id="ATM"></span><span id="atm"></span>**ATM** (37)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-304"><span id="MIO_X.25"></span><span id="mio_x.25"></span>**Mio. 25** (38)</span><span class="sxs-lookup"><span data-stu-id="e2315-304"><span id="MIO_X.25"></span><span id="mio_x.25"></span>**MIO X.25** (38)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-305"><span id="SONET"></span><span id="sonet"></span>**SONET** (39)</span><span class="sxs-lookup"><span data-stu-id="e2315-305"><span id="SONET"></span><span id="sonet"></span>**SONET** (39)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-306"><span id="X.25_PLE"></span><span id="x.25_ple"></span>**X. 25 PLE** (40)</span><span class="sxs-lookup"><span data-stu-id="e2315-306"><span id="X.25_PLE"></span><span id="x.25_ple"></span>**X.25 PLE** (40)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-307"><span id="ISO_802.211c"></span><span id="iso_802.211c"></span><span id="ISO_802.211C"></span>**ISO 802.211 c** (41)</span><span class="sxs-lookup"><span data-stu-id="e2315-307"><span id="ISO_802.211c"></span><span id="iso_802.211c"></span><span id="ISO_802.211C"></span>**ISO 802.211c** (41)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-308"><span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>**LocalTalk** (42)</span><span class="sxs-lookup"><span data-stu-id="e2315-308"><span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>**LocalTalk** (42)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-309"><span id="SMDS_DXI"></span><span id="smds_dxi"></span>**SMDS DXI** (43)</span><span class="sxs-lookup"><span data-stu-id="e2315-309"><span id="SMDS_DXI"></span><span id="smds_dxi"></span>**SMDS DXI** (43)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-310"><span id="Frame_Relay_Service"></span><span id="frame_relay_service"></span><span id="FRAME_RELAY_SERVICE"></span>**Frame Relay-Dienst** (44)</span><span class="sxs-lookup"><span data-stu-id="e2315-310"><span id="Frame_Relay_Service"></span><span id="frame_relay_service"></span><span id="FRAME_RELAY_SERVICE"></span>**Frame Relay Service** (44)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-311"><span id="V.35"></span><span id="v.35"></span>**V. 35** (45)</span><span class="sxs-lookup"><span data-stu-id="e2315-311"><span id="V.35"></span><span id="v.35"></span>**V.35** (45)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-312"><span id="HSSI"></span><span id="hssi"></span>**HSSI** (46)</span><span class="sxs-lookup"><span data-stu-id="e2315-312"><span id="HSSI"></span><span id="hssi"></span>**HSSI** (46)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-313"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (47)</span><span class="sxs-lookup"><span data-stu-id="e2315-313"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (47)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-314"><span id="Modem"></span><span id="modem"></span><span id="MODEM"></span>**Modem** (48)</span><span class="sxs-lookup"><span data-stu-id="e2315-314"><span id="Modem"></span><span id="modem"></span><span id="MODEM"></span>**Modem** (48)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-315"><span id="AAL5"></span><span id="aal5"></span>**AAL5** (49)</span><span class="sxs-lookup"><span data-stu-id="e2315-315"><span id="AAL5"></span><span id="aal5"></span>**AAL5** (49)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-316"><span id="SONET_Path"></span><span id="sonet_path"></span><span id="SONET_PATH"></span>**Sonetpfad** (50)</span><span class="sxs-lookup"><span data-stu-id="e2315-316"><span id="SONET_Path"></span><span id="sonet_path"></span><span id="SONET_PATH"></span>**SONET Path** (50)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-317"><span id="SONET_VT"></span><span id="sonet_vt"></span>**SONET VT** (51)</span><span class="sxs-lookup"><span data-stu-id="e2315-317"><span id="SONET_VT"></span><span id="sonet_vt"></span>**SONET VT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-318"><span id="SMDS_ICIP"></span><span id="smds_icip"></span>**SMDS ICIP** (52)</span><span class="sxs-lookup"><span data-stu-id="e2315-318"><span id="SMDS_ICIP"></span><span id="smds_icip"></span>**SMDS ICIP** (52)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-319"><span id="Proprietary_Virtual_Internal"></span><span id="proprietary_virtual_internal"></span><span id="PROPRIETARY_VIRTUAL_INTERNAL"></span>**Proprietäre virtuell/intern** (53)</span><span class="sxs-lookup"><span data-stu-id="e2315-319"><span id="Proprietary_Virtual_Internal"></span><span id="proprietary_virtual_internal"></span><span id="PROPRIETARY_VIRTUAL_INTERNAL"></span>**Proprietary Virtual/Internal** (53)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-320"><span id="Proprietary_Multiplexor"></span><span id="proprietary_multiplexor"></span><span id="PROPRIETARY_MULTIPLEXOR"></span>**Proprietäres Multiplexor** (54)</span><span class="sxs-lookup"><span data-stu-id="e2315-320"><span id="Proprietary_Multiplexor"></span><span id="proprietary_multiplexor"></span><span id="PROPRIETARY_MULTIPLEXOR"></span>**Proprietary Multiplexor** (54)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-321"><span id="IEEE_802.12"></span><span id="ieee_802.12"></span>**IEEE 802,12** (55)</span><span class="sxs-lookup"><span data-stu-id="e2315-321"><span id="IEEE_802.12"></span><span id="ieee_802.12"></span>**IEEE 802.12** (55)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-322"><span id="Fibre_Channel"></span><span id="fibre_channel"></span><span id="FIBRE_CHANNEL"></span>**Fibre Channel** (56)</span><span class="sxs-lookup"><span data-stu-id="e2315-322"><span id="Fibre_Channel"></span><span id="fibre_channel"></span><span id="FIBRE_CHANNEL"></span>**Fibre Channel** (56)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-323"><span id="HIPPI_Interface"></span><span id="hippi_interface"></span><span id="HIPPI_INTERFACE"></span>**HIPPI-Schnittstelle** (57)</span><span class="sxs-lookup"><span data-stu-id="e2315-323"><span id="HIPPI_Interface"></span><span id="hippi_interface"></span><span id="HIPPI_INTERFACE"></span>**HIPPI Interface** (57)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-324"><span id="Frame_Relay_Interconnect"></span><span id="frame_relay_interconnect"></span><span id="FRAME_RELAY_INTERCONNECT"></span>**Frame Relay-Interconnect** (58)</span><span class="sxs-lookup"><span data-stu-id="e2315-324"><span id="Frame_Relay_Interconnect"></span><span id="frame_relay_interconnect"></span><span id="FRAME_RELAY_INTERCONNECT"></span>**Frame Relay Interconnect** (58)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-325"><span id="ATM_Emulated_LAN_for_802.3"></span><span id="atm_emulated_lan_for_802.3"></span><span id="ATM_EMULATED_LAN_FOR_802.3"></span>Mit **ATM emulierten LAN für 802,3** (59)</span><span class="sxs-lookup"><span data-stu-id="e2315-325"><span id="ATM_Emulated_LAN_for_802.3"></span><span id="atm_emulated_lan_for_802.3"></span><span id="ATM_EMULATED_LAN_FOR_802.3"></span>**ATM Emulated LAN for 802.3** (59)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-326"><span id="ATM_Emulated_LAN_for_802.5"></span><span id="atm_emulated_lan_for_802.5"></span><span id="ATM_EMULATED_LAN_FOR_802.5"></span>Mit **ATM emulierten LAN für 802,5** (60)</span><span class="sxs-lookup"><span data-stu-id="e2315-326"><span id="ATM_Emulated_LAN_for_802.5"></span><span id="atm_emulated_lan_for_802.5"></span><span id="ATM_EMULATED_LAN_FOR_802.5"></span>**ATM Emulated LAN for 802.5** (60)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-327"><span id="ATM_Emulated_Circuit"></span><span id="atm_emulated_circuit"></span><span id="ATM_EMULATED_CIRCUIT"></span>Verbindung mit " **ATM-emuliert** " (61)</span><span class="sxs-lookup"><span data-stu-id="e2315-327"><span id="ATM_Emulated_Circuit"></span><span id="atm_emulated_circuit"></span><span id="ATM_EMULATED_CIRCUIT"></span>**ATM Emulated Circuit** (61)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-328"><span id="Fast_Ethernet__100BaseT_"></span><span id="fast_ethernet__100baset_"></span><span id="FAST_ETHERNET__100BASET_"></span>**Schnelles Ethernet (100BaseT)** (62)</span><span class="sxs-lookup"><span data-stu-id="e2315-328"><span id="Fast_Ethernet__100BaseT_"></span><span id="fast_ethernet__100baset_"></span><span id="FAST_ETHERNET__100BASET_"></span>**Fast Ethernet (100BaseT)** (62)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-329"><span id="ISDN"></span><span id="isdn"></span>**ISDN** (63)</span><span class="sxs-lookup"><span data-stu-id="e2315-329"><span id="ISDN"></span><span id="isdn"></span>**ISDN** (63)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-330"><span id="V.11"></span><span id="v.11"></span>**V. 11** (64)</span><span class="sxs-lookup"><span data-stu-id="e2315-330"><span id="V.11"></span><span id="v.11"></span>**V.11** (64)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-331"><span id="V.36"></span><span id="v.36"></span>**V. 36** (65)</span><span class="sxs-lookup"><span data-stu-id="e2315-331"><span id="V.36"></span><span id="v.36"></span>**V.36** (65)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-332"><span id="G703_at_64K"></span><span id="g703_at_64k"></span><span id="G703_AT_64K"></span>**G703 bei 64K** (66)</span><span class="sxs-lookup"><span data-stu-id="e2315-332"><span id="G703_at_64K"></span><span id="g703_at_64k"></span><span id="G703_AT_64K"></span>**G703 at 64K** (66)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-333"><span id="G703_at_2Mb"></span><span id="g703_at_2mb"></span><span id="G703_AT_2MB"></span>**G703 bei 2 MB** (67)</span><span class="sxs-lookup"><span data-stu-id="e2315-333"><span id="G703_at_2Mb"></span><span id="g703_at_2mb"></span><span id="G703_AT_2MB"></span>**G703 at 2Mb** (67)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-334"><span id="QLLC"></span><span id="qllc"></span>**QLLC** (68)</span><span class="sxs-lookup"><span data-stu-id="e2315-334"><span id="QLLC"></span><span id="qllc"></span>**QLLC** (68)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-335"><span id="Fast_Ethernet_100BaseFX"></span><span id="fast_ethernet_100basefx"></span><span id="FAST_ETHERNET_100BASEFX"></span>**Schnelles Ethernet 100BaseFX** (69)</span><span class="sxs-lookup"><span data-stu-id="e2315-335"><span id="Fast_Ethernet_100BaseFX"></span><span id="fast_ethernet_100basefx"></span><span id="FAST_ETHERNET_100BASEFX"></span>**Fast Ethernet 100BaseFX** (69)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-336"><span id="Channel"></span><span id="channel"></span><span id="CHANNEL"></span>**Channel** (70)</span><span class="sxs-lookup"><span data-stu-id="e2315-336"><span id="Channel"></span><span id="channel"></span><span id="CHANNEL"></span>**Channel** (70)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-337"><span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802,11** (71)</span><span class="sxs-lookup"><span data-stu-id="e2315-337"><span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802.11** (71)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-338"><span id="IBM_260_370_OEMI_Channel"></span><span id="ibm_260_370_oemi_channel"></span><span id="IBM_260_370_OEMI_CHANNEL"></span>**IBM 260/370-Kanal (oemi** ) (72)</span><span class="sxs-lookup"><span data-stu-id="e2315-338"><span id="IBM_260_370_OEMI_Channel"></span><span id="ibm_260_370_oemi_channel"></span><span id="IBM_260_370_OEMI_CHANNEL"></span>**IBM 260/370 OEMI Channel** (72)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-339"><span id="ESCON"></span><span id="escon"></span>**ESCON** (73)</span><span class="sxs-lookup"><span data-stu-id="e2315-339"><span id="ESCON"></span><span id="escon"></span>**ESCON** (73)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-340"><span id="Data_Link_Switching"></span><span id="data_link_switching"></span><span id="DATA_LINK_SWITCHING"></span>**Daten Link Wechsel** (74)</span><span class="sxs-lookup"><span data-stu-id="e2315-340"><span id="Data_Link_Switching"></span><span id="data_link_switching"></span><span id="DATA_LINK_SWITCHING"></span>**Data Link Switching** (74)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-341"><span id="ISDN_S_T_Interface"></span><span id="isdn_s_t_interface"></span><span id="ISDN_S_T_INTERFACE"></span>**ISDN S/T-Schnittstelle** (75)</span><span class="sxs-lookup"><span data-stu-id="e2315-341"><span id="ISDN_S_T_Interface"></span><span id="isdn_s_t_interface"></span><span id="ISDN_S_T_INTERFACE"></span>**ISDN S/T Interface** (75)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-342"><span id="ISDN_U_Interface"></span><span id="isdn_u_interface"></span><span id="ISDN_U_INTERFACE"></span>**ISDN-U-Schnittstelle** (76)</span><span class="sxs-lookup"><span data-stu-id="e2315-342"><span id="ISDN_U_Interface"></span><span id="isdn_u_interface"></span><span id="ISDN_U_INTERFACE"></span>**ISDN U Interface** (76)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-343"><span id="LAP-D"></span><span id="lap-d"></span>**Lap-D** (77)</span><span class="sxs-lookup"><span data-stu-id="e2315-343"><span id="LAP-D"></span><span id="lap-d"></span>**LAP-D** (77)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-344"><span id="IP_Switch"></span><span id="ip_switch"></span><span id="IP_SWITCH"></span>**IP-Switch** (78)</span><span class="sxs-lookup"><span data-stu-id="e2315-344"><span id="IP_Switch"></span><span id="ip_switch"></span><span id="IP_SWITCH"></span>**IP Switch** (78)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-345"><span id="Remote_Source_Route_Bridging"></span><span id="remote_source_route_bridging"></span><span id="REMOTE_SOURCE_ROUTE_BRIDGING"></span>**Remote-Quell Routen Überbrückung** (79)</span><span class="sxs-lookup"><span data-stu-id="e2315-345"><span id="Remote_Source_Route_Bridging"></span><span id="remote_source_route_bridging"></span><span id="REMOTE_SOURCE_ROUTE_BRIDGING"></span>**Remote Source Route Bridging** (79)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-346"><span id="ATM_Logical"></span><span id="atm_logical"></span><span id="ATM_LOGICAL"></span>**ATM logisch** (80)</span><span class="sxs-lookup"><span data-stu-id="e2315-346"><span id="ATM_Logical"></span><span id="atm_logical"></span><span id="ATM_LOGICAL"></span>**ATM Logical** (80)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-347"><span id="DS0"></span><span id="ds0"></span>**DS0** (81)</span><span class="sxs-lookup"><span data-stu-id="e2315-347"><span id="DS0"></span><span id="ds0"></span>**DS0** (81)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-348"><span id="DS0_Bundle"></span><span id="ds0_bundle"></span><span id="DS0_BUNDLE"></span>**DS0 Bundle** (82)</span><span class="sxs-lookup"><span data-stu-id="e2315-348"><span id="DS0_Bundle"></span><span id="ds0_bundle"></span><span id="DS0_BUNDLE"></span>**DS0 Bundle** (82)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-349"><span id="BSC"></span><span id="bsc"></span>**BSC** (83)</span><span class="sxs-lookup"><span data-stu-id="e2315-349"><span id="BSC"></span><span id="bsc"></span>**BSC** (83)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-350"><span id="Async"></span><span id="async"></span><span id="ASYNC"></span>**Async** (84)</span><span class="sxs-lookup"><span data-stu-id="e2315-350"><span id="Async"></span><span id="async"></span><span id="ASYNC"></span>**Async** (84)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-351"><span id="Combat_Net_Radio"></span><span id="combat_net_radio"></span><span id="COMBAT_NET_RADIO"></span>**Netzwerk Radio** (85)</span><span class="sxs-lookup"><span data-stu-id="e2315-351"><span id="Combat_Net_Radio"></span><span id="combat_net_radio"></span><span id="COMBAT_NET_RADIO"></span>**Combat Net Radio** (85)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-352"><span id="ISO_802.5r_DTR"></span><span id="iso_802.5r_dtr"></span><span id="ISO_802.5R_DTR"></span>**ISO 802.5 definiert r DTR** (86)</span><span class="sxs-lookup"><span data-stu-id="e2315-352"><span id="ISO_802.5r_DTR"></span><span id="iso_802.5r_dtr"></span><span id="ISO_802.5R_DTR"></span>**ISO 802.5r DTR** (86)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-353"><span id="Ext_Pos_Loc_Report_System"></span><span id="ext_pos_loc_report_system"></span><span id="EXT_POS_LOC_REPORT_SYSTEM"></span>**Ext POS Loc-Berichts System** (87)</span><span class="sxs-lookup"><span data-stu-id="e2315-353"><span id="Ext_Pos_Loc_Report_System"></span><span id="ext_pos_loc_report_system"></span><span id="EXT_POS_LOC_REPORT_SYSTEM"></span>**Ext Pos Loc Report System** (87)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-354"><span id="AppleTalk_Remote_Access_Protocol"></span><span id="appletalk_remote_access_protocol"></span><span id="APPLETALK_REMOTE_ACCESS_PROTOCOL"></span>**AppleTalk-Remote Zugriffsprotokoll** (88)</span><span class="sxs-lookup"><span data-stu-id="e2315-354"><span id="AppleTalk_Remote_Access_Protocol"></span><span id="appletalk_remote_access_protocol"></span><span id="APPLETALK_REMOTE_ACCESS_PROTOCOL"></span>**AppleTalk Remote Access Protocol** (88)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-355"><span id="Proprietary_Connectionless"></span><span id="proprietary_connectionless"></span><span id="PROPRIETARY_CONNECTIONLESS"></span>**Proprietäre Connectionless** (89)</span><span class="sxs-lookup"><span data-stu-id="e2315-355"><span id="Proprietary_Connectionless"></span><span id="proprietary_connectionless"></span><span id="PROPRIETARY_CONNECTIONLESS"></span>**Proprietary Connectionless** (89)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-356"><span id="ITU_X.29_Host_PAD"></span><span id="itu_x.29_host_pad"></span><span id="ITU_X.29_HOST_PAD"></span>**ITU X. 29-hostpad** (90)</span><span class="sxs-lookup"><span data-stu-id="e2315-356"><span id="ITU_X.29_Host_PAD"></span><span id="itu_x.29_host_pad"></span><span id="ITU_X.29_HOST_PAD"></span>**ITU X.29 Host PAD** (90)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-357"><span id="ITU_X.3_Terminal_PAD"></span><span id="itu_x.3_terminal_pad"></span><span id="ITU_X.3_TERMINAL_PAD"></span>**ITU X. 3-Terminal Pad** (91)</span><span class="sxs-lookup"><span data-stu-id="e2315-357"><span id="ITU_X.3_Terminal_PAD"></span><span id="itu_x.3_terminal_pad"></span><span id="ITU_X.3_TERMINAL_PAD"></span>**ITU X.3 Terminal PAD** (91)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-358"><span id="Frame_Relay_MPI"></span><span id="frame_relay_mpi"></span><span id="FRAME_RELAY_MPI"></span>**Frame Relay MPI** (92)</span><span class="sxs-lookup"><span data-stu-id="e2315-358"><span id="Frame_Relay_MPI"></span><span id="frame_relay_mpi"></span><span id="FRAME_RELAY_MPI"></span>**Frame Relay MPI** (92)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-359"><span id="ITU_X.213"></span><span id="itu_x.213"></span>**ITU X. 213** (93)</span><span class="sxs-lookup"><span data-stu-id="e2315-359"><span id="ITU_X.213"></span><span id="itu_x.213"></span>**ITU X.213** (93)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-360"><span id="ADSL"></span><span id="adsl"></span>**ADSL** (94)</span><span class="sxs-lookup"><span data-stu-id="e2315-360"><span id="ADSL"></span><span id="adsl"></span>**ADSL** (94)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-361"><span id="RADSL"></span><span id="radsl"></span>**RADSL** (95)</span><span class="sxs-lookup"><span data-stu-id="e2315-361"><span id="RADSL"></span><span id="radsl"></span>**RADSL** (95)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-362"><span id="SDSL"></span><span id="sdsl"></span>**SDSL** (96)</span><span class="sxs-lookup"><span data-stu-id="e2315-362"><span id="SDSL"></span><span id="sdsl"></span>**SDSL** (96)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-363"><span id="VDSL"></span><span id="vdsl"></span>**VDSL** (97)</span><span class="sxs-lookup"><span data-stu-id="e2315-363"><span id="VDSL"></span><span id="vdsl"></span>**VDSL** (97)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-364"><span id="ISO_802.5_CRFP"></span><span id="iso_802.5_crfp"></span>**ISO 802,5 crfp** (98)</span><span class="sxs-lookup"><span data-stu-id="e2315-364"><span id="ISO_802.5_CRFP"></span><span id="iso_802.5_crfp"></span>**ISO 802.5 CRFP** (98)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-365"><span id="Myrinet"></span><span id="myrinet"></span><span id="MYRINET"></span>**Myrinet** (99)</span><span class="sxs-lookup"><span data-stu-id="e2315-365"><span id="Myrinet"></span><span id="myrinet"></span><span id="MYRINET"></span>**Myrinet** (99)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-366"><span id="Voice_Receive_and_Transmit"></span><span id="voice_receive_and_transmit"></span><span id="VOICE_RECEIVE_AND_TRANSMIT"></span>**Sprach Empfang und-Übertragung** (100)</span><span class="sxs-lookup"><span data-stu-id="e2315-366"><span id="Voice_Receive_and_Transmit"></span><span id="voice_receive_and_transmit"></span><span id="VOICE_RECEIVE_AND_TRANSMIT"></span>**Voice Receive and Transmit** (100)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-367"><span id="Voice_Foreign_Exchange_Office"></span><span id="voice_foreign_exchange_office"></span><span id="VOICE_FOREIGN_EXCHANGE_OFFICE"></span>**Sprach fremde Exchange-Niederlassung** (101)</span><span class="sxs-lookup"><span data-stu-id="e2315-367"><span id="Voice_Foreign_Exchange_Office"></span><span id="voice_foreign_exchange_office"></span><span id="VOICE_FOREIGN_EXCHANGE_OFFICE"></span>**Voice Foreign Exchange Office** (101)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-368"><span id="Voice_Foreign_Exchange_Service"></span><span id="voice_foreign_exchange_service"></span><span id="VOICE_FOREIGN_EXCHANGE_SERVICE"></span>**Sprachnachrichten Austauschdienst** (102)</span><span class="sxs-lookup"><span data-stu-id="e2315-368"><span id="Voice_Foreign_Exchange_Service"></span><span id="voice_foreign_exchange_service"></span><span id="VOICE_FOREIGN_EXCHANGE_SERVICE"></span>**Voice Foreign Exchange Service** (102)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-369"><span id="Voice_Encapsulation"></span><span id="voice_encapsulation"></span><span id="VOICE_ENCAPSULATION"></span>**Sprach Kapselung** (103)</span><span class="sxs-lookup"><span data-stu-id="e2315-369"><span id="Voice_Encapsulation"></span><span id="voice_encapsulation"></span><span id="VOICE_ENCAPSULATION"></span>**Voice Encapsulation** (103)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-370"><span id="Voice_over_IP"></span><span id="voice_over_ip"></span><span id="VOICE_OVER_IP"></span>**Voice-over-IP** (104)</span><span class="sxs-lookup"><span data-stu-id="e2315-370"><span id="Voice_over_IP"></span><span id="voice_over_ip"></span><span id="VOICE_OVER_IP"></span>**Voice over IP** (104)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-371"><span id="ATM_DXI"></span><span id="atm_dxi"></span>**ATM DXI** (105)</span><span class="sxs-lookup"><span data-stu-id="e2315-371"><span id="ATM_DXI"></span><span id="atm_dxi"></span>**ATM DXI** (105)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-372"><span id="ATM_FUNI"></span><span id="atm_funi"></span>**ATM Funi** (106)</span><span class="sxs-lookup"><span data-stu-id="e2315-372"><span id="ATM_FUNI"></span><span id="atm_funi"></span>**ATM FUNI** (106)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-373"><span id="ATM_IMA"></span><span id="atm_ima"></span>**ATM IMA** (107)</span><span class="sxs-lookup"><span data-stu-id="e2315-373"><span id="ATM_IMA"></span><span id="atm_ima"></span>**ATM IMA** (107)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-374"><span id="PPP_Multilink_Bundle"></span><span id="ppp_multilink_bundle"></span><span id="PPP_MULTILINK_BUNDLE"></span>**PPP-multilinkbündel** (108)</span><span class="sxs-lookup"><span data-stu-id="e2315-374"><span id="PPP_Multilink_Bundle"></span><span id="ppp_multilink_bundle"></span><span id="PPP_MULTILINK_BUNDLE"></span>**PPP Multilink Bundle** (108)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-375"><span id="IP_over_CDLC"></span><span id="ip_over_cdlc"></span><span id="IP_OVER_CDLC"></span>**IP über CDLC** (109)</span><span class="sxs-lookup"><span data-stu-id="e2315-375"><span id="IP_over_CDLC"></span><span id="ip_over_cdlc"></span><span id="IP_OVER_CDLC"></span>**IP over CDLC** (109)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-376"><span id="IP_over_CLAW"></span><span id="ip_over_claw"></span><span id="IP_OVER_CLAW"></span>**IP-over-Claw** (110)</span><span class="sxs-lookup"><span data-stu-id="e2315-376"><span id="IP_over_CLAW"></span><span id="ip_over_claw"></span><span id="IP_OVER_CLAW"></span>**IP over CLAW** (110)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-377"><span id="Stack_to_Stack"></span><span id="stack_to_stack"></span><span id="STACK_TO_STACK"></span>**Stapel zu Stapel** (111)</span><span class="sxs-lookup"><span data-stu-id="e2315-377"><span id="Stack_to_Stack"></span><span id="stack_to_stack"></span><span id="STACK_TO_STACK"></span>**Stack to Stack** (111)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-378"><span id="Virtual_IP_Address"></span><span id="virtual_ip_address"></span><span id="VIRTUAL_IP_ADDRESS"></span>**Virtuelle IP-Adresse** (112)</span><span class="sxs-lookup"><span data-stu-id="e2315-378"><span id="Virtual_IP_Address"></span><span id="virtual_ip_address"></span><span id="VIRTUAL_IP_ADDRESS"></span>**Virtual IP Address** (112)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-379"><span id="MPC"></span><span id="mpc"></span>**MPC** (113)</span><span class="sxs-lookup"><span data-stu-id="e2315-379"><span id="MPC"></span><span id="mpc"></span>**MPC** (113)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-380"><span id="IP_over_ATM"></span><span id="ip_over_atm"></span><span id="IP_OVER_ATM"></span>**IP über ATM** (114)</span><span class="sxs-lookup"><span data-stu-id="e2315-380"><span id="IP_over_ATM"></span><span id="ip_over_atm"></span><span id="IP_OVER_ATM"></span>**IP over ATM** (114)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-381"><span id="ISO_802.5j_Fibre_Token_Ring"></span><span id="iso_802.5j_fibre_token_ring"></span><span id="ISO_802.5J_FIBRE_TOKEN_RING"></span>**ISO 802.5 definiert j Fibre Token Ring** (115)</span><span class="sxs-lookup"><span data-stu-id="e2315-381"><span id="ISO_802.5j_Fibre_Token_Ring"></span><span id="iso_802.5j_fibre_token_ring"></span><span id="ISO_802.5J_FIBRE_TOKEN_RING"></span>**ISO 802.5j Fibre Token Ring** (115)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-382"><span id="TDLC"></span><span id="tdlc"></span>**Tdlc** (116)</span><span class="sxs-lookup"><span data-stu-id="e2315-382"><span id="TDLC"></span><span id="tdlc"></span>**TDLC** (116)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-383"><span id="Gigabit_Ethernet"></span><span id="gigabit_ethernet"></span><span id="GIGABIT_ETHERNET"></span>**Gigabit-Ethernet** (117)</span><span class="sxs-lookup"><span data-stu-id="e2315-383"><span id="Gigabit_Ethernet"></span><span id="gigabit_ethernet"></span><span id="GIGABIT_ETHERNET"></span>**Gigabit Ethernet** (117)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-384"><span id="HDLC"></span><span id="hdlc"></span>**HDLC** (118)</span><span class="sxs-lookup"><span data-stu-id="e2315-384"><span id="HDLC"></span><span id="hdlc"></span>**HDLC** (118)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-385"><span id="LAP-F"></span><span id="lap-f"></span>**Lap-F** (119)</span><span class="sxs-lookup"><span data-stu-id="e2315-385"><span id="LAP-F"></span><span id="lap-f"></span>**LAP-F** (119)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-386"><span id="V.37"></span><span id="v.37"></span>**V. 37** (120)</span><span class="sxs-lookup"><span data-stu-id="e2315-386"><span id="V.37"></span><span id="v.37"></span>**V.37** (120)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-387"><span id="X.25_MLP"></span><span id="x.25_mlp"></span>**X. 25 MLP** (121)</span><span class="sxs-lookup"><span data-stu-id="e2315-387"><span id="X.25_MLP"></span><span id="x.25_mlp"></span>**X.25 MLP** (121)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-388"><span id="X.25_Hunt_Group"></span><span id="x.25_hunt_group"></span><span id="X.25_HUNT_GROUP"></span>**X. 25-Jagdgruppe** (122)</span><span class="sxs-lookup"><span data-stu-id="e2315-388"><span id="X.25_Hunt_Group"></span><span id="x.25_hunt_group"></span><span id="X.25_HUNT_GROUP"></span>**X.25 Hunt Group** (122)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-389"><span id="Transp_HDLC"></span><span id="transp_hdlc"></span><span id="TRANSP_HDLC"></span>**Transp HDLC** (123)</span><span class="sxs-lookup"><span data-stu-id="e2315-389"><span id="Transp_HDLC"></span><span id="transp_hdlc"></span><span id="TRANSP_HDLC"></span>**Transp HDLC** (123)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-390"><span id="Interleave_Channel"></span><span id="interleave_channel"></span><span id="INTERLEAVE_CHANNEL"></span>**Interleave-Kanal** (124)</span><span class="sxs-lookup"><span data-stu-id="e2315-390"><span id="Interleave_Channel"></span><span id="interleave_channel"></span><span id="INTERLEAVE_CHANNEL"></span>**Interleave Channel** (124)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-391"><span id="FAST_Channel"></span><span id="fast_channel"></span><span id="FAST_CHANNEL"></span>**Schneller Kanal** (125)</span><span class="sxs-lookup"><span data-stu-id="e2315-391"><span id="FAST_Channel"></span><span id="fast_channel"></span><span id="FAST_CHANNEL"></span>**FAST Channel** (125)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-392"><span id="IP__for_APPN_HPR_in_IP_Networks_"></span><span id="ip__for_appn_hpr_in_ip_networks_"></span><span id="IP__FOR_APPN_HPR_IN_IP_NETWORKS_"></span>**IP (für APPN HPR in IP-Netzwerken)** (126)</span><span class="sxs-lookup"><span data-stu-id="e2315-392"><span id="IP__for_APPN_HPR_in_IP_Networks_"></span><span id="ip__for_appn_hpr_in_ip_networks_"></span><span id="IP__FOR_APPN_HPR_IN_IP_NETWORKS_"></span>**IP (for APPN HPR in IP Networks)** (126)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-393"><span id="CATV_MAC_Layer"></span><span id="catv_mac_layer"></span><span id="CATV_MAC_LAYER"></span>Hyper- **v-Mac-Ebene** (127)</span><span class="sxs-lookup"><span data-stu-id="e2315-393"><span id="CATV_MAC_Layer"></span><span id="catv_mac_layer"></span><span id="CATV_MAC_LAYER"></span>**CATV MAC Layer** (127)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-394"><span id="CATV_Downstream"></span><span id="catv_downstream"></span><span id="CATV_DOWNSTREAM"></span>**Streamv Downstream** (128)</span><span class="sxs-lookup"><span data-stu-id="e2315-394"><span id="CATV_Downstream"></span><span id="catv_downstream"></span><span id="CATV_DOWNSTREAM"></span>**CATV Downstream** (128)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-395"><span id="CATV_Upstream"></span><span id="catv_upstream"></span><span id="CATV_UPSTREAM"></span>**Streamv Upstream** (129)</span><span class="sxs-lookup"><span data-stu-id="e2315-395"><span id="CATV_Upstream"></span><span id="catv_upstream"></span><span id="CATV_UPSTREAM"></span>**CATV Upstream** (129)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-396"><span id="Avalon_12MPP_Switch"></span><span id="avalon_12mpp_switch"></span><span id="AVALON_12MPP_SWITCH"></span>**Schalter "Avalon 12mpp** " (130)</span><span class="sxs-lookup"><span data-stu-id="e2315-396"><span id="Avalon_12MPP_Switch"></span><span id="avalon_12mpp_switch"></span><span id="AVALON_12MPP_SWITCH"></span>**Avalon 12MPP Switch** (130)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-397"><span id="Tunnel"></span><span id="tunnel"></span><span id="TUNNEL"></span>**Tunnel** (131)</span><span class="sxs-lookup"><span data-stu-id="e2315-397"><span id="Tunnel"></span><span id="tunnel"></span><span id="TUNNEL"></span>**Tunnel** (131)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-398"><span id="Coffee"></span><span id="coffee"></span><span id="COFFEE"></span>**Kaffee** (132)</span><span class="sxs-lookup"><span data-stu-id="e2315-398"><span id="Coffee"></span><span id="coffee"></span><span id="COFFEE"></span>**Coffee** (132)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-399"><span id="Circuit_Emulation_Service"></span><span id="circuit_emulation_service"></span><span id="CIRCUIT_EMULATION_SERVICE"></span>**Circuit Emulation-Dienst** (133)</span><span class="sxs-lookup"><span data-stu-id="e2315-399"><span id="Circuit_Emulation_Service"></span><span id="circuit_emulation_service"></span><span id="CIRCUIT_EMULATION_SERVICE"></span>**Circuit Emulation Service** (133)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-400"><span id="ATM_SubInterface"></span><span id="atm_subinterface"></span><span id="ATM_SUBINTERFACE"></span>**ATM-Unterschnittstelle** (134)</span><span class="sxs-lookup"><span data-stu-id="e2315-400"><span id="ATM_SubInterface"></span><span id="atm_subinterface"></span><span id="ATM_SUBINTERFACE"></span>**ATM SubInterface** (134)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-401"><span id="Layer_2_VLAN_using_802.1Q"></span><span id="layer_2_vlan_using_802.1q"></span><span id="LAYER_2_VLAN_USING_802.1Q"></span>**Layer 2-VLAN mit 802.1 q** (135)</span><span class="sxs-lookup"><span data-stu-id="e2315-401"><span id="Layer_2_VLAN_using_802.1Q"></span><span id="layer_2_vlan_using_802.1q"></span><span id="LAYER_2_VLAN_USING_802.1Q"></span>**Layer 2 VLAN using 802.1Q** (135)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-402"><span id="Layer_3_VLAN_using_IP"></span><span id="layer_3_vlan_using_ip"></span><span id="LAYER_3_VLAN_USING_IP"></span>**Layer 3-VLAN mit IP** (136)</span><span class="sxs-lookup"><span data-stu-id="e2315-402"><span id="Layer_3_VLAN_using_IP"></span><span id="layer_3_vlan_using_ip"></span><span id="LAYER_3_VLAN_USING_IP"></span>**Layer 3 VLAN using IP** (136)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-403"><span id="Layer_3_VLAN_using_IPX"></span><span id="layer_3_vlan_using_ipx"></span><span id="LAYER_3_VLAN_USING_IPX"></span>**Layer 3-VLAN mit IPX** (137)</span><span class="sxs-lookup"><span data-stu-id="e2315-403"><span id="Layer_3_VLAN_using_IPX"></span><span id="layer_3_vlan_using_ipx"></span><span id="LAYER_3_VLAN_USING_IPX"></span>**Layer 3 VLAN using IPX** (137)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-404"><span id="Digital_Power_Line"></span><span id="digital_power_line"></span><span id="DIGITAL_POWER_LINE"></span>**Digitale Stromversorgung** (138)</span><span class="sxs-lookup"><span data-stu-id="e2315-404"><span id="Digital_Power_Line"></span><span id="digital_power_line"></span><span id="DIGITAL_POWER_LINE"></span>**Digital Power Line** (138)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-405"><span id="Multimedia_Mail_over_IP"></span><span id="multimedia_mail_over_ip"></span><span id="MULTIMEDIA_MAIL_OVER_IP"></span>**Multimedia-e-Mail über IP** (139)</span><span class="sxs-lookup"><span data-stu-id="e2315-405"><span id="Multimedia_Mail_over_IP"></span><span id="multimedia_mail_over_ip"></span><span id="MULTIMEDIA_MAIL_OVER_IP"></span>**Multimedia Mail over IP** (139)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-406"><span id="DTM"></span><span id="dtm"></span>**DTM** (140)</span><span class="sxs-lookup"><span data-stu-id="e2315-406"><span id="DTM"></span><span id="dtm"></span>**DTM** (140)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-407"><span id="DCN"></span><span id="dcn"></span>**DCN** (141)</span><span class="sxs-lookup"><span data-stu-id="e2315-407"><span id="DCN"></span><span id="dcn"></span>**DCN** (141)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-408"><span id="IP_Forwarding"></span><span id="ip_forwarding"></span><span id="IP_FORWARDING"></span>**IP-Weiterleitung** (142)</span><span class="sxs-lookup"><span data-stu-id="e2315-408"><span id="IP_Forwarding"></span><span id="ip_forwarding"></span><span id="IP_FORWARDING"></span>**IP Forwarding** (142)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-409"><span id="MSDSL"></span><span id="msdsl"></span>**Msdsl** (143)</span><span class="sxs-lookup"><span data-stu-id="e2315-409"><span id="MSDSL"></span><span id="msdsl"></span>**MSDSL** (143)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-410"><span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (144)</span><span class="sxs-lookup"><span data-stu-id="e2315-410"><span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (144)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-411"><span id="IF-GSN_HIPPI-6400"></span><span id="if-gsn_hippi-6400"></span>**If-GSN/HIPPI-6400** (145)</span><span class="sxs-lookup"><span data-stu-id="e2315-411"><span id="IF-GSN_HIPPI-6400"></span><span id="if-gsn_hippi-6400"></span>**IF-GSN/HIPPI-6400** (145)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-412"><span id="DVB-RCC_MAC_Layer"></span><span id="dvb-rcc_mac_layer"></span><span id="DVB-RCC_MAC_LAYER"></span>**DVB-RCC Mac-Ebene** (146)</span><span class="sxs-lookup"><span data-stu-id="e2315-412"><span id="DVB-RCC_MAC_Layer"></span><span id="dvb-rcc_mac_layer"></span><span id="DVB-RCC_MAC_LAYER"></span>**DVB-RCC MAC Layer** (146)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-413"><span id="DVB-RCC_Downstream"></span><span id="dvb-rcc_downstream"></span><span id="DVB-RCC_DOWNSTREAM"></span>**DVB-RCC Downstream** (147)</span><span class="sxs-lookup"><span data-stu-id="e2315-413"><span id="DVB-RCC_Downstream"></span><span id="dvb-rcc_downstream"></span><span id="DVB-RCC_DOWNSTREAM"></span>**DVB-RCC Downstream** (147)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-414"><span id="DVB-RCC_Upstream"></span><span id="dvb-rcc_upstream"></span><span id="DVB-RCC_UPSTREAM"></span>**DVB-RCC Upstream** (148)</span><span class="sxs-lookup"><span data-stu-id="e2315-414"><span id="DVB-RCC_Upstream"></span><span id="dvb-rcc_upstream"></span><span id="DVB-RCC_UPSTREAM"></span>**DVB-RCC Upstream** (148)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-415"><span id="ATM_Virtual"></span><span id="atm_virtual"></span><span id="ATM_VIRTUAL"></span>**ATM virtuell** (149)</span><span class="sxs-lookup"><span data-stu-id="e2315-415"><span id="ATM_Virtual"></span><span id="atm_virtual"></span><span id="ATM_VIRTUAL"></span>**ATM Virtual** (149)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-416"><span id="MPLS_Tunnel"></span><span id="mpls_tunnel"></span><span id="MPLS_TUNNEL"></span>**MPLS-Tunnel** (150)</span><span class="sxs-lookup"><span data-stu-id="e2315-416"><span id="MPLS_Tunnel"></span><span id="mpls_tunnel"></span><span id="MPLS_TUNNEL"></span>**MPLS Tunnel** (150)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-417"><span id="SRP"></span><span id="srp"></span>**SRP** (151)</span><span class="sxs-lookup"><span data-stu-id="e2315-417"><span id="SRP"></span><span id="srp"></span>**SRP** (151)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-418"><span id="Voice_over_ATM"></span><span id="voice_over_atm"></span><span id="VOICE_OVER_ATM"></span>**Voice over ATM** (152)</span><span class="sxs-lookup"><span data-stu-id="e2315-418"><span id="Voice_over_ATM"></span><span id="voice_over_atm"></span><span id="VOICE_OVER_ATM"></span>**Voice over ATM** (152)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-419"><span id="Voice_over_Frame_Relay"></span><span id="voice_over_frame_relay"></span><span id="VOICE_OVER_FRAME_RELAY"></span>**Voice over Frame Relay** (153)</span><span class="sxs-lookup"><span data-stu-id="e2315-419"><span id="Voice_over_Frame_Relay"></span><span id="voice_over_frame_relay"></span><span id="VOICE_OVER_FRAME_RELAY"></span>**Voice over Frame Relay** (153)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-420"><span id="ISDL"></span><span id="isdl"></span>**Isdl** (154)</span><span class="sxs-lookup"><span data-stu-id="e2315-420"><span id="ISDL"></span><span id="isdl"></span>**ISDL** (154)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-421"><span id="Composite_Link"></span><span id="composite_link"></span><span id="COMPOSITE_LINK"></span>**Zusammengesetzter Link** (155)</span><span class="sxs-lookup"><span data-stu-id="e2315-421"><span id="Composite_Link"></span><span id="composite_link"></span><span id="COMPOSITE_LINK"></span>**Composite Link** (155)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-422"><span id="SS7_Signaling_Link"></span><span id="ss7_signaling_link"></span><span id="SS7_SIGNALING_LINK"></span>**SS7 Signalisierungs Link** (156)</span><span class="sxs-lookup"><span data-stu-id="e2315-422"><span id="SS7_Signaling_Link"></span><span id="ss7_signaling_link"></span><span id="SS7_SIGNALING_LINK"></span>**SS7 Signaling Link** (156)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-423"><span id="Proprietary_P2P_Wireless"></span><span id="proprietary_p2p_wireless"></span><span id="PROPRIETARY_P2P_WIRELESS"></span>**Proprietäre P2P Wireless** (157)</span><span class="sxs-lookup"><span data-stu-id="e2315-423"><span id="Proprietary_P2P_Wireless"></span><span id="proprietary_p2p_wireless"></span><span id="PROPRIETARY_P2P_WIRELESS"></span>**Proprietary P2P Wireless** (157)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-424"><span id="Frame_Forward"></span><span id="frame_forward"></span><span id="FRAME_FORWARD"></span>**Frame vorwärts** (158)</span><span class="sxs-lookup"><span data-stu-id="e2315-424"><span id="Frame_Forward"></span><span id="frame_forward"></span><span id="FRAME_FORWARD"></span>**Frame Forward** (158)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-425"><span id="RFC1483_Multiprotocol_over_ATM"></span><span id="rfc1483_multiprotocol_over_atm"></span><span id="RFC1483_MULTIPROTOCOL_OVER_ATM"></span>**RFC1483 MultiProtocol über ATM** (159)</span><span class="sxs-lookup"><span data-stu-id="e2315-425"><span id="RFC1483_Multiprotocol_over_ATM"></span><span id="rfc1483_multiprotocol_over_atm"></span><span id="RFC1483_MULTIPROTOCOL_OVER_ATM"></span>**RFC1483 Multiprotocol over ATM** (159)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-426"><span id="USB"></span><span id="usb"></span>**USB** (160)</span><span class="sxs-lookup"><span data-stu-id="e2315-426"><span id="USB"></span><span id="usb"></span>**USB** (160)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-427"><span id="IEEE_802.3ad_Link_Aggregate"></span><span id="ieee_802.3ad_link_aggregate"></span><span id="IEEE_802.3AD_LINK_AGGREGATE"></span>**IEEE 802.3 Ad-Link Aggregat** (161)</span><span class="sxs-lookup"><span data-stu-id="e2315-427"><span id="IEEE_802.3ad_Link_Aggregate"></span><span id="ieee_802.3ad_link_aggregate"></span><span id="IEEE_802.3AD_LINK_AGGREGATE"></span>**IEEE 802.3ad Link Aggregate** (161)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-428"><span id="BGP_Policy_Accounting"></span><span id="bgp_policy_accounting"></span><span id="BGP_POLICY_ACCOUNTING"></span>**BGP-Richtlinien Abrechnung** (162)</span><span class="sxs-lookup"><span data-stu-id="e2315-428"><span id="BGP_Policy_Accounting"></span><span id="bgp_policy_accounting"></span><span id="BGP_POLICY_ACCOUNTING"></span>**BGP Policy Accounting** (162)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-429"><span id="FRF_.16_Multilink_FR"></span><span id="frf_.16_multilink_fr"></span><span id="FRF_.16_MULTILINK_FR"></span>**FRF .16 Multilink fr** (163)</span><span class="sxs-lookup"><span data-stu-id="e2315-429"><span id="FRF_.16_Multilink_FR"></span><span id="frf_.16_multilink_fr"></span><span id="FRF_.16_MULTILINK_FR"></span>**FRF .16 Multilink FR** (163)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-430"><span id="H.323_Gatekeeper"></span><span id="h.323_gatekeeper"></span><span id="H.323_GATEKEEPER"></span>**H. 323 Gatekeeper** (164)</span><span class="sxs-lookup"><span data-stu-id="e2315-430"><span id="H.323_Gatekeeper"></span><span id="h.323_gatekeeper"></span><span id="H.323_GATEKEEPER"></span>**H.323 Gatekeeper** (164)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-431"><span id="H.323_Proxy"></span><span id="h.323_proxy"></span><span id="H.323_PROXY"></span>**H. 323-Proxy** (165)</span><span class="sxs-lookup"><span data-stu-id="e2315-431"><span id="H.323_Proxy"></span><span id="h.323_proxy"></span><span id="H.323_PROXY"></span>**H.323 Proxy** (165)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-432"><span id="MPLS"></span><span id="mpls"></span>**MPLS** (166)</span><span class="sxs-lookup"><span data-stu-id="e2315-432"><span id="MPLS"></span><span id="mpls"></span>**MPLS** (166)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-433"><span id="Multi-Frequency_Signaling_Link"></span><span id="multi-frequency_signaling_link"></span><span id="MULTI-FREQUENCY_SIGNALING_LINK"></span>**Mehrfach Frequenz-Signal Verknüpfung** (167)</span><span class="sxs-lookup"><span data-stu-id="e2315-433"><span id="Multi-Frequency_Signaling_Link"></span><span id="multi-frequency_signaling_link"></span><span id="MULTI-FREQUENCY_SIGNALING_LINK"></span>**Multi-Frequency Signaling Link** (167)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-434"><span id="HDSL-2"></span><span id="hdsl-2"></span>**HDSL-2** (168)</span><span class="sxs-lookup"><span data-stu-id="e2315-434"><span id="HDSL-2"></span><span id="hdsl-2"></span>**HDSL-2** (168)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-435"><span id="S-HDSL"></span><span id="s-hdsl"></span>**S-HDSL** (169)</span><span class="sxs-lookup"><span data-stu-id="e2315-435"><span id="S-HDSL"></span><span id="s-hdsl"></span>**S-HDSL** (169)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-436"><span id="DS1_Facility_Data_Link"></span><span id="ds1_facility_data_link"></span><span id="DS1_FACILITY_DATA_LINK"></span>**Ds1-Anlagedaten Link** (170)</span><span class="sxs-lookup"><span data-stu-id="e2315-436"><span id="DS1_Facility_Data_Link"></span><span id="ds1_facility_data_link"></span><span id="DS1_FACILITY_DATA_LINK"></span>**DS1 Facility Data Link** (170)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-437"><span id="Packet_over_SONET_SDH"></span><span id="packet_over_sonet_sdh"></span><span id="PACKET_OVER_SONET_SDH"></span>**Paket über SONET/SDH** (171)</span><span class="sxs-lookup"><span data-stu-id="e2315-437"><span id="Packet_over_SONET_SDH"></span><span id="packet_over_sonet_sdh"></span><span id="PACKET_OVER_SONET_SDH"></span>**Packet over SONET/SDH** (171)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-438"><span id="DVB-ASI_Input"></span><span id="dvb-asi_input"></span><span id="DVB-ASI_INPUT"></span>**DVB-ASI-Eingabe** (172)</span><span class="sxs-lookup"><span data-stu-id="e2315-438"><span id="DVB-ASI_Input"></span><span id="dvb-asi_input"></span><span id="DVB-ASI_INPUT"></span>**DVB-ASI Input** (172)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-439"><span id="DVB-ASI_Output"></span><span id="dvb-asi_output"></span><span id="DVB-ASI_OUTPUT"></span>**DVB-ASI-Ausgabe** (173)</span><span class="sxs-lookup"><span data-stu-id="e2315-439"><span id="DVB-ASI_Output"></span><span id="dvb-asi_output"></span><span id="DVB-ASI_OUTPUT"></span>**DVB-ASI Output** (173)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-440"><span id="Power_Line"></span><span id="power_line"></span><span id="POWER_LINE"></span>**Stromversorgung** (174)</span><span class="sxs-lookup"><span data-stu-id="e2315-440"><span id="Power_Line"></span><span id="power_line"></span><span id="POWER_LINE"></span>**Power Line** (174)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-441"><span id="Non_Facility_Associated_Signaling"></span><span id="non_facility_associated_signaling"></span><span id="NON_FACILITY_ASSOCIATED_SIGNALING"></span>**Nicht der Anlage zugeordnete Signalisierung** (175)</span><span class="sxs-lookup"><span data-stu-id="e2315-441"><span id="Non_Facility_Associated_Signaling"></span><span id="non_facility_associated_signaling"></span><span id="NON_FACILITY_ASSOCIATED_SIGNALING"></span>**Non Facility Associated Signaling** (175)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-442"><span id="TR008"></span><span id="tr008"></span>**TR008** (176)</span><span class="sxs-lookup"><span data-stu-id="e2315-442"><span id="TR008"></span><span id="tr008"></span>**TR008** (176)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-443"><span id="GR303_RDT"></span><span id="gr303_rdt"></span>**GR303 RDT** (177)</span><span class="sxs-lookup"><span data-stu-id="e2315-443"><span id="GR303_RDT"></span><span id="gr303_rdt"></span>**GR303 RDT** (177)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-444"><span id="GR303_IDT"></span><span id="gr303_idt"></span>**GR303 IDT** (178)</span><span class="sxs-lookup"><span data-stu-id="e2315-444"><span id="GR303_IDT"></span><span id="gr303_idt"></span>**GR303 IDT** (178)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-445"><span id="ISUP"></span><span id="isup"></span>**IsUp** (179)</span><span class="sxs-lookup"><span data-stu-id="e2315-445"><span id="ISUP"></span><span id="isup"></span>**ISUP** (179)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-446"><span id="Proprietary_Wireless_MAC_Layer"></span><span id="proprietary_wireless_mac_layer"></span><span id="PROPRIETARY_WIRELESS_MAC_LAYER"></span>**Proprietäre drahtlose Mac-Ebene** (180)</span><span class="sxs-lookup"><span data-stu-id="e2315-446"><span id="Proprietary_Wireless_MAC_Layer"></span><span id="proprietary_wireless_mac_layer"></span><span id="PROPRIETARY_WIRELESS_MAC_LAYER"></span>**Proprietary Wireless MAC Layer** (180)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-447"><span id="Proprietary_Wireless_Downstream"></span><span id="proprietary_wireless_downstream"></span><span id="PROPRIETARY_WIRELESS_DOWNSTREAM"></span>**Proprietäre drahtlos, Downstream** (181)</span><span class="sxs-lookup"><span data-stu-id="e2315-447"><span id="Proprietary_Wireless_Downstream"></span><span id="proprietary_wireless_downstream"></span><span id="PROPRIETARY_WIRELESS_DOWNSTREAM"></span>**Proprietary Wireless Downstream** (181)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-448"><span id="Proprietary_Wireless_Upstream"></span><span id="proprietary_wireless_upstream"></span><span id="PROPRIETARY_WIRELESS_UPSTREAM"></span>**Proprietäre drahtlos Upstream** (182)</span><span class="sxs-lookup"><span data-stu-id="e2315-448"><span id="Proprietary_Wireless_Upstream"></span><span id="proprietary_wireless_upstream"></span><span id="PROPRIETARY_WIRELESS_UPSTREAM"></span>**Proprietary Wireless Upstream** (182)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-449"><span id="HIPERLAN_Type_2"></span><span id="hiperlan_type_2"></span><span id="HIPERLAN_TYPE_2"></span>**HIPERLAN-Typ 2** (183)</span><span class="sxs-lookup"><span data-stu-id="e2315-449"><span id="HIPERLAN_Type_2"></span><span id="hiperlan_type_2"></span><span id="HIPERLAN_TYPE_2"></span>**HIPERLAN Type 2** (183)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-450"><span id="Proprietary_Broadband_Wireless_Access_Point_to_Multipoint"></span><span id="proprietary_broadband_wireless_access_point_to_multipoint"></span><span id="PROPRIETARY_BROADBAND_WIRELESS_ACCESS_POINT_TO_MULTIPOINT"></span>Geschützter **Breitband-drahtlos Zugriffspunkt auf Multipoint** (184)</span><span class="sxs-lookup"><span data-stu-id="e2315-450"><span id="Proprietary_Broadband_Wireless_Access_Point_to_Multipoint"></span><span id="proprietary_broadband_wireless_access_point_to_multipoint"></span><span id="PROPRIETARY_BROADBAND_WIRELESS_ACCESS_POINT_TO_MULTIPOINT"></span>**Proprietary Broadband Wireless Access Point to Multipoint** (184)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-451"><span id="SONET_Overhead_Channel"></span><span id="sonet_overhead_channel"></span><span id="SONET_OVERHEAD_CHANNEL"></span>**SONET-Overhead-Kanal** (185)</span><span class="sxs-lookup"><span data-stu-id="e2315-451"><span id="SONET_Overhead_Channel"></span><span id="sonet_overhead_channel"></span><span id="SONET_OVERHEAD_CHANNEL"></span>**SONET Overhead Channel** (185)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-452"><span id="Digital_Wrapper_Overhead_Channel"></span><span id="digital_wrapper_overhead_channel"></span><span id="DIGITAL_WRAPPER_OVERHEAD_CHANNEL"></span>Verwaltungs Kanal für den **digitalen Wrapper** (186)</span><span class="sxs-lookup"><span data-stu-id="e2315-452"><span id="Digital_Wrapper_Overhead_Channel"></span><span id="digital_wrapper_overhead_channel"></span><span id="DIGITAL_WRAPPER_OVERHEAD_CHANNEL"></span>**Digital Wrapper Overhead Channel** (186)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-453"><span id="ATM_Adaptation_Layer_2"></span><span id="atm_adaptation_layer_2"></span><span id="ATM_ADAPTATION_LAYER_2"></span>**ATM-Anpassungs Schicht 2** (187)</span><span class="sxs-lookup"><span data-stu-id="e2315-453"><span id="ATM_Adaptation_Layer_2"></span><span id="atm_adaptation_layer_2"></span><span id="ATM_ADAPTATION_LAYER_2"></span>**ATM Adaptation Layer 2** (187)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-454"><span id="Radio_MAC"></span><span id="radio_mac"></span><span id="RADIO_MAC"></span>**Radio Mac** (188)</span><span class="sxs-lookup"><span data-stu-id="e2315-454"><span id="Radio_MAC"></span><span id="radio_mac"></span><span id="RADIO_MAC"></span>**Radio MAC** (188)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-455"><span id="ATM_Radio"></span><span id="atm_radio"></span><span id="ATM_RADIO"></span>**ATM Radio** (189)</span><span class="sxs-lookup"><span data-stu-id="e2315-455"><span id="ATM_Radio"></span><span id="atm_radio"></span><span id="ATM_RADIO"></span>**ATM Radio** (189)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-456"><span id="Inter_Machine_Trunk"></span><span id="inter_machine_trunk"></span><span id="INTER_MACHINE_TRUNK"></span>**Trunk zwischen Computer** (190)</span><span class="sxs-lookup"><span data-stu-id="e2315-456"><span id="Inter_Machine_Trunk"></span><span id="inter_machine_trunk"></span><span id="INTER_MACHINE_TRUNK"></span>**Inter Machine Trunk** (190)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-457"><span id="MVL_DSL"></span><span id="mvl_dsl"></span>**Mvl-DSL** (191)</span><span class="sxs-lookup"><span data-stu-id="e2315-457"><span id="MVL_DSL"></span><span id="mvl_dsl"></span>**MVL DSL** (191)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-458"><span id="Long_Read_DSL"></span><span id="long_read_dsl"></span><span id="LONG_READ_DSL"></span>**Lange Lese-DSL** (192)</span><span class="sxs-lookup"><span data-stu-id="e2315-458"><span id="Long_Read_DSL"></span><span id="long_read_dsl"></span><span id="LONG_READ_DSL"></span>**Long Read DSL** (192)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-459"><span id="Frame_Relay_DLCI_Endpoint"></span><span id="frame_relay_dlci_endpoint"></span><span id="FRAME_RELAY_DLCI_ENDPOINT"></span>**Rahmen Relay-DLCI-Endpunkt** (193)</span><span class="sxs-lookup"><span data-stu-id="e2315-459"><span id="Frame_Relay_DLCI_Endpoint"></span><span id="frame_relay_dlci_endpoint"></span><span id="FRAME_RELAY_DLCI_ENDPOINT"></span>**Frame Relay DLCI Endpoint** (193)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-460"><span id="ATM_VCI_Endpoint"></span><span id="atm_vci_endpoint"></span><span id="ATM_VCI_ENDPOINT"></span>**ATM-VCI-Endpunkt** (194)</span><span class="sxs-lookup"><span data-stu-id="e2315-460"><span id="ATM_VCI_Endpoint"></span><span id="atm_vci_endpoint"></span><span id="ATM_VCI_ENDPOINT"></span>**ATM VCI Endpoint** (194)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-461"><span id="Optical_Channel"></span><span id="optical_channel"></span><span id="OPTICAL_CHANNEL"></span>**Optischer Kanal** (195)</span><span class="sxs-lookup"><span data-stu-id="e2315-461"><span id="Optical_Channel"></span><span id="optical_channel"></span><span id="OPTICAL_CHANNEL"></span>**Optical Channel** (195)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-462"><span id="Optical_Transport"></span><span id="optical_transport"></span><span id="OPTICAL_TRANSPORT"></span>**Optischer Transport** (196)</span><span class="sxs-lookup"><span data-stu-id="e2315-462"><span id="Optical_Transport"></span><span id="optical_transport"></span><span id="OPTICAL_TRANSPORT"></span>**Optical Transport** (196)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-463"><span id="Proprietary_ATM"></span><span id="proprietary_atm"></span><span id="PROPRIETARY_ATM"></span>**Proprietäre ATM** (197)</span><span class="sxs-lookup"><span data-stu-id="e2315-463"><span id="Proprietary_ATM"></span><span id="proprietary_atm"></span><span id="PROPRIETARY_ATM"></span>**Proprietary ATM** (197)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-464"><span id="Voice_over_Cable"></span><span id="voice_over_cable"></span><span id="VOICE_OVER_CABLE"></span>**Voice-over-Kabel** (198)</span><span class="sxs-lookup"><span data-stu-id="e2315-464"><span id="Voice_over_Cable"></span><span id="voice_over_cable"></span><span id="VOICE_OVER_CABLE"></span>**Voice over Cable** (198)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-465"><span id="Infiniband"></span><span id="infiniband"></span><span id="INFINIBAND"></span>**InfiniBand** (199)</span><span class="sxs-lookup"><span data-stu-id="e2315-465"><span id="Infiniband"></span><span id="infiniband"></span><span id="INFINIBAND"></span>**Infiniband** (199)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-466"><span id="TE_Link"></span><span id="te_link"></span><span id="TE_LINK"></span>**Te-Verknüpfung** (200)</span><span class="sxs-lookup"><span data-stu-id="e2315-466"><span id="TE_Link"></span><span id="te_link"></span><span id="TE_LINK"></span>**TE Link** (200)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-467"><span id="Q.2931"></span><span id="q.2931"></span>**Q. 2931** (201)</span><span class="sxs-lookup"><span data-stu-id="e2315-467"><span id="Q.2931"></span><span id="q.2931"></span>**Q.2931** (201)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-468"><span id="Virtual_Trunk_Group"></span><span id="virtual_trunk_group"></span><span id="VIRTUAL_TRUNK_GROUP"></span>**Virtuelle Trunk Gruppe** (202)</span><span class="sxs-lookup"><span data-stu-id="e2315-468"><span id="Virtual_Trunk_Group"></span><span id="virtual_trunk_group"></span><span id="VIRTUAL_TRUNK_GROUP"></span>**Virtual Trunk Group** (202)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-469"><span id="SIP_Trunk_Group"></span><span id="sip_trunk_group"></span><span id="SIP_TRUNK_GROUP"></span>**SIP-Trunk Gruppe** (203)</span><span class="sxs-lookup"><span data-stu-id="e2315-469"><span id="SIP_Trunk_Group"></span><span id="sip_trunk_group"></span><span id="SIP_TRUNK_GROUP"></span>**SIP Trunk Group** (203)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-470"><span id="SIP_Signaling"></span><span id="sip_signaling"></span><span id="SIP_SIGNALING"></span>**SIP-Signalisierung** (204)</span><span class="sxs-lookup"><span data-stu-id="e2315-470"><span id="SIP_Signaling"></span><span id="sip_signaling"></span><span id="SIP_SIGNALING"></span>**SIP Signaling** (204)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-471"><span id="CATV_Upstream_Channel"></span><span id="catv_upstream_channel"></span><span id="CATV_UPSTREAM_CHANNEL"></span>**Streamv-upstreamchannel** (205)</span><span class="sxs-lookup"><span data-stu-id="e2315-471"><span id="CATV_Upstream_Channel"></span><span id="catv_upstream_channel"></span><span id="CATV_UPSTREAM_CHANNEL"></span>**CATV Upstream Channel** (205)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-472"><span id="Econet"></span><span id="econet"></span><span id="ECONET"></span>**Econet** (206)</span><span class="sxs-lookup"><span data-stu-id="e2315-472"><span id="Econet"></span><span id="econet"></span><span id="ECONET"></span>**Econet** (206)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-473"><span id="FSAN_155Mb_PON"></span><span id="fsan_155mb_pon"></span><span id="FSAN_155MB_PON"></span>**F** -5-MB-Pon (207)</span><span class="sxs-lookup"><span data-stu-id="e2315-473"><span id="FSAN_155Mb_PON"></span><span id="fsan_155mb_pon"></span><span id="FSAN_155MB_PON"></span>**FSAN 155Mb PON** (207)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-474"><span id="FSAN_622Mb_PON"></span><span id="fsan_622mb_pon"></span><span id="FSAN_622MB_PON"></span>**F 622mb Pon** (208)</span><span class="sxs-lookup"><span data-stu-id="e2315-474"><span id="FSAN_622Mb_PON"></span><span id="fsan_622mb_pon"></span><span id="FSAN_622MB_PON"></span>**FSAN 622Mb PON** (208)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-475"><span id="Transparent_Bridge"></span><span id="transparent_bridge"></span><span id="TRANSPARENT_BRIDGE"></span>**Transparente Brücke** (209)</span><span class="sxs-lookup"><span data-stu-id="e2315-475"><span id="Transparent_Bridge"></span><span id="transparent_bridge"></span><span id="TRANSPARENT_BRIDGE"></span>**Transparent Bridge** (209)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-476"><span id="Line_Group"></span><span id="line_group"></span><span id="LINE_GROUP"></span>**Zeilen Gruppe** (210)</span><span class="sxs-lookup"><span data-stu-id="e2315-476"><span id="Line_Group"></span><span id="line_group"></span><span id="LINE_GROUP"></span>**Line Group** (210)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-477"><span id="Voice___Feature_Group"></span><span id="voice___feature_group"></span><span id="VOICE___FEATURE_GROUP"></span>**Sprach & Featuregruppe** (211)</span><span class="sxs-lookup"><span data-stu-id="e2315-477"><span id="Voice___Feature_Group"></span><span id="voice___feature_group"></span><span id="VOICE___FEATURE_GROUP"></span>**Voice & Feature Group** (211)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-478"><span id="Voice_FGD_EANA"></span><span id="voice_fgd_eana"></span><span id="VOICE_FGD_EANA"></span>**Sprach-f-Eana** (212)</span><span class="sxs-lookup"><span data-stu-id="e2315-478"><span id="Voice_FGD_EANA"></span><span id="voice_fgd_eana"></span><span id="VOICE_FGD_EANA"></span>**Voice FGD EANA** (212)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-479"><span id="Voice_DID"></span><span id="voice_did"></span><span id="VOICE_DID"></span>**Stimme** an (213)</span><span class="sxs-lookup"><span data-stu-id="e2315-479"><span id="Voice_DID"></span><span id="voice_did"></span><span id="VOICE_DID"></span>**Voice DID** (213)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-480"><span id="MPEG_Transport"></span><span id="mpeg_transport"></span><span id="MPEG_TRANSPORT"></span>**MPEG-Transport** (214)</span><span class="sxs-lookup"><span data-stu-id="e2315-480"><span id="MPEG_Transport"></span><span id="mpeg_transport"></span><span id="MPEG_TRANSPORT"></span>**MPEG Transport** (214)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-481"><span id="6To4"></span><span id="6to4"></span><span id="6TO4"></span>**6zu 4** (215)</span><span class="sxs-lookup"><span data-stu-id="e2315-481"><span id="6To4"></span><span id="6to4"></span><span id="6TO4"></span>**6To4** (215)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-482"><span id="GTP"></span><span id="gtp"></span>**GTP** (216)</span><span class="sxs-lookup"><span data-stu-id="e2315-482"><span id="GTP"></span><span id="gtp"></span>**GTP** (216)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-483"><span id="Paradyne_EtherLoop_1"></span><span id="paradyne_etherloop_1"></span><span id="PARADYNE_ETHERLOOP_1"></span>**Paradyne etherloop 1** (217)</span><span class="sxs-lookup"><span data-stu-id="e2315-483"><span id="Paradyne_EtherLoop_1"></span><span id="paradyne_etherloop_1"></span><span id="PARADYNE_ETHERLOOP_1"></span>**Paradyne EtherLoop 1** (217)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-484"><span id="Paradyne_EtherLoop_2"></span><span id="paradyne_etherloop_2"></span><span id="PARADYNE_ETHERLOOP_2"></span>**Paradyne etherloop 2** (218)</span><span class="sxs-lookup"><span data-stu-id="e2315-484"><span id="Paradyne_EtherLoop_2"></span><span id="paradyne_etherloop_2"></span><span id="PARADYNE_ETHERLOOP_2"></span>**Paradyne EtherLoop 2** (218)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-485"><span id="Optical_Channel_Group"></span><span id="optical_channel_group"></span><span id="OPTICAL_CHANNEL_GROUP"></span>**Optische Kanal Gruppe** (219)</span><span class="sxs-lookup"><span data-stu-id="e2315-485"><span id="Optical_Channel_Group"></span><span id="optical_channel_group"></span><span id="OPTICAL_CHANNEL_GROUP"></span>**Optical Channel Group** (219)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-486"><span id="HomePNA"></span><span id="homepna"></span><span id="HOMEPNA"></span>**HomePNA** (220)</span><span class="sxs-lookup"><span data-stu-id="e2315-486"><span id="HomePNA"></span><span id="homepna"></span><span id="HOMEPNA"></span>**HomePNA** (220)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-487"><span id="GFP"></span><span id="gfp"></span>**GFP** (221)</span><span class="sxs-lookup"><span data-stu-id="e2315-487"><span id="GFP"></span><span id="gfp"></span>**GFP** (221)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-488"><span id="ciscoISLvlan"></span><span id="ciscoislvlan"></span><span id="CISCOISLVLAN"></span>**ciscoislvlan** (222)</span><span class="sxs-lookup"><span data-stu-id="e2315-488"><span id="ciscoISLvlan"></span><span id="ciscoislvlan"></span><span id="CISCOISLVLAN"></span>**ciscoISLvlan** (222)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-489"><span id="actelisMetaLOOP"></span><span id="actelismetaloop"></span><span id="ACTELISMETALOOP"></span>**actelismetaloop** (223)</span><span class="sxs-lookup"><span data-stu-id="e2315-489"><span id="actelisMetaLOOP"></span><span id="actelismetaloop"></span><span id="ACTELISMETALOOP"></span>**actelisMetaLOOP** (223)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-490"><span id="Fcip"></span><span id="fcip"></span><span id="FCIP"></span>**F** (224)</span><span class="sxs-lookup"><span data-stu-id="e2315-490"><span id="Fcip"></span><span id="fcip"></span><span id="FCIP"></span>**Fcip** (224)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-491"><span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**IANA reserviert** (225.. 4095)</span><span class="sxs-lookup"><span data-stu-id="e2315-491"><span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**IANA Reserved** (225..4095)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-492"><span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096)</span><span class="sxs-lookup"><span data-stu-id="e2315-492"><span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-493"><span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097)</span><span class="sxs-lookup"><span data-stu-id="e2315-493"><span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-494"><span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/V6** (4098)</span><span class="sxs-lookup"><span data-stu-id="e2315-494"><span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/v6** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-495"><span id="IPX"></span><span id="ipx"></span>**IPX** (4099)</span><span class="sxs-lookup"><span data-stu-id="e2315-495"><span id="IPX"></span><span id="ipx"></span>**IPX** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-496"><span id="DECnet"></span><span id="decnet"></span><span id="DECNET"></span>**DECnet** (4100)</span><span class="sxs-lookup"><span data-stu-id="e2315-496"><span id="DECnet"></span><span id="decnet"></span><span id="DECNET"></span>**DECnet** (4100)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-497"><span id="SNA"></span><span id="sna"></span>**SNA** (4101)</span><span class="sxs-lookup"><span data-stu-id="e2315-497"><span id="SNA"></span><span id="sna"></span>**SNA** (4101)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-498"><span id="CONP"></span><span id="conp"></span>Verbindungs- **Manager (4102** )</span><span class="sxs-lookup"><span data-stu-id="e2315-498"><span id="CONP"></span><span id="conp"></span>**CONP** (4102)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-499"><span id="CLNP"></span><span id="clnp"></span>**CLNP** (4103)</span><span class="sxs-lookup"><span data-stu-id="e2315-499"><span id="CLNP"></span><span id="clnp"></span>**CLNP** (4103)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-500"><span id="VINES"></span><span id="vines"></span>**Rebstöcke** (4104)</span><span class="sxs-lookup"><span data-stu-id="e2315-500"><span id="VINES"></span><span id="vines"></span>**VINES** (4104)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-501"><span id="XNS"></span><span id="xns"></span>**XNS** (4105)</span><span class="sxs-lookup"><span data-stu-id="e2315-501"><span id="XNS"></span><span id="xns"></span>**XNS** (4105)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-502"><span id="ISDN_B_Channel_Endpoint"></span><span id="isdn_b_channel_endpoint"></span><span id="ISDN_B_CHANNEL_ENDPOINT"></span>**ISDN-B-Kanal Endpunkt** (4106)</span><span class="sxs-lookup"><span data-stu-id="e2315-502"><span id="ISDN_B_Channel_Endpoint"></span><span id="isdn_b_channel_endpoint"></span><span id="ISDN_B_CHANNEL_ENDPOINT"></span>**ISDN B Channel Endpoint** (4106)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-503"><span id="ISDN_D_Channel_Endpoint"></span><span id="isdn_d_channel_endpoint"></span><span id="ISDN_D_CHANNEL_ENDPOINT"></span>**ISDN-D-Kanal Endpunkt** (4107)</span><span class="sxs-lookup"><span data-stu-id="e2315-503"><span id="ISDN_D_Channel_Endpoint"></span><span id="isdn_d_channel_endpoint"></span><span id="ISDN_D_CHANNEL_ENDPOINT"></span>**ISDN D Channel Endpoint** (4107)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-504"><span id="BGP"></span><span id="bgp"></span>**BGP** (4108)</span><span class="sxs-lookup"><span data-stu-id="e2315-504"><span id="BGP"></span><span id="bgp"></span>**BGP** (4108)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-505"><span id="OSPF"></span><span id="ospf"></span>**OSPF** (4109)</span><span class="sxs-lookup"><span data-stu-id="e2315-505"><span id="OSPF"></span><span id="ospf"></span>**OSPF** (4109)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-506"><span id="UDP"></span><span id="udp"></span>**UDP** (4110)</span><span class="sxs-lookup"><span data-stu-id="e2315-506"><span id="UDP"></span><span id="udp"></span>**UDP** (4110)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-507"><span id="TCP"></span><span id="tcp"></span>**TCP** (4111)</span><span class="sxs-lookup"><span data-stu-id="e2315-507"><span id="TCP"></span><span id="tcp"></span>**TCP** (4111)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-508"><span id="802.11a"></span><span id="802.11A"></span>**802.11 a** (4112)</span><span class="sxs-lookup"><span data-stu-id="e2315-508"><span id="802.11a"></span><span id="802.11A"></span>**802.11a** (4112)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-509"><span id="802.11b"></span><span id="802.11B"></span>**802.11 b** (4113)</span><span class="sxs-lookup"><span data-stu-id="e2315-509"><span id="802.11b"></span><span id="802.11B"></span>**802.11b** (4113)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-510"><span id="802.11g"></span><span id="802.11G"></span>**802.11 g** (4114)</span><span class="sxs-lookup"><span data-stu-id="e2315-510"><span id="802.11g"></span><span id="802.11G"></span>**802.11g** (4114)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-511"><span id="802.11h"></span><span id="802.11H"></span>**802.11 h** (4115)</span><span class="sxs-lookup"><span data-stu-id="e2315-511"><span id="802.11h"></span><span id="802.11H"></span>**802.11h** (4115)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-512"><span id="NFS"></span><span id="nfs"></span>**NFS** (4200)</span><span class="sxs-lookup"><span data-stu-id="e2315-512"><span id="NFS"></span><span id="nfs"></span>**NFS** (4200)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-513"><span id="CIFS"></span><span id="cifs"></span>**CIFS** (4201)</span><span class="sxs-lookup"><span data-stu-id="e2315-513"><span id="CIFS"></span><span id="cifs"></span>**CIFS** (4201)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-514"><span id="DAFS"></span><span id="dafs"></span>**DAFS** (4202)</span><span class="sxs-lookup"><span data-stu-id="e2315-514"><span id="DAFS"></span><span id="dafs"></span>**DAFS** (4202)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-515"><span id="WebDAV"></span><span id="webdav"></span><span id="WEBDAV"></span>**WebDAV** (4203)</span><span class="sxs-lookup"><span data-stu-id="e2315-515"><span id="WebDAV"></span><span id="webdav"></span><span id="WEBDAV"></span>**WebDAV** (4203)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-516"><span id="HTTP"></span><span id="http"></span>**Http** (4204)</span><span class="sxs-lookup"><span data-stu-id="e2315-516"><span id="HTTP"></span><span id="http"></span>**HTTP** (4204)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-517"><span id="FTP"></span><span id="ftp"></span>**FTP** (4205)</span><span class="sxs-lookup"><span data-stu-id="e2315-517"><span id="FTP"></span><span id="ftp"></span>**FTP** (4205)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-518"><span id="NDMP"></span><span id="ndmp"></span>**NDMP** (4300)</span><span class="sxs-lookup"><span data-stu-id="e2315-518"><span id="NDMP"></span><span id="ndmp"></span>**NDMP** (4300)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-519"><span id="Telnet"></span><span id="telnet"></span><span id="TELNET"></span>**Telnet** (4400)</span><span class="sxs-lookup"><span data-stu-id="e2315-519"><span id="Telnet"></span><span id="telnet"></span><span id="TELNET"></span>**Telnet** (4400)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-520"><span id="SSH"></span><span id="ssh"></span>**SSH** (4401)</span><span class="sxs-lookup"><span data-stu-id="e2315-520"><span id="SSH"></span><span id="ssh"></span>**SSH** (4401)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-521"><span id="SM_CLP"></span><span id="sm_clp"></span>**SM CLP** (4402)</span><span class="sxs-lookup"><span data-stu-id="e2315-521"><span id="SM_CLP"></span><span id="sm_clp"></span>**SM CLP** (4402)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-522"><span id="SMTP"></span><span id="smtp"></span>**SMTP** (4403)</span><span class="sxs-lookup"><span data-stu-id="e2315-522"><span id="SMTP"></span><span id="smtp"></span>**SMTP** (4403)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-523"><span id="LDAP"></span><span id="ldap"></span>**LDAP** (4404)</span><span class="sxs-lookup"><span data-stu-id="e2315-523"><span id="LDAP"></span><span id="ldap"></span>**LDAP** (4404)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-524"><span id="RDP"></span><span id="rdp"></span>**RDP** (4405)</span><span class="sxs-lookup"><span data-stu-id="e2315-524"><span id="RDP"></span><span id="rdp"></span>**RDP** (4405)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-525"><span id="HTTPS"></span><span id="https"></span>**Https** (4406)</span><span class="sxs-lookup"><span data-stu-id="e2315-525"><span id="HTTPS"></span><span id="https"></span>**HTTPS** (4406)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-526"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="e2315-526"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e2315-527"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (32768...</span><span class="sxs-lookup"><span data-stu-id="e2315-527"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32768..</span></span> <span data-ttu-id="e2315-528">)</span><span class="sxs-lookup"><span data-stu-id="e2315-528">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e2315-529">**ProtocolType**</span><span class="sxs-lookup"><span data-stu-id="e2315-529">**ProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2315-530">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2315-530">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2315-531">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2315-531">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2315-532">Diese Eigenschaft wird anstelle der **protocoliftype** -Eigenschaft als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="e2315-532">This property is deprecated in lieu of the **ProtocolIFType** property.</span></span> <span data-ttu-id="e2315-533">Diese Eigenschaft wird von [**CIM \_ protocolendpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e2315-533">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="e2315-534">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="e2315-534">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2315-535">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2315-535">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2315-536">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2315-536">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2315-537">Der zuletzt angeforderte oder gewünschte Status für den Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="e2315-537">The last requested or desired state for the management service.</span></span> <span data-ttu-id="e2315-538">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 12 (nicht zutreffend) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e2315-538">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="e2315-539">Wert</span><span class="sxs-lookup"><span data-stu-id="e2315-539">Value</span></span>                                                                         | <span data-ttu-id="e2315-540">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e2315-540">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="e2315-541"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="e2315-541"><dt>12</dt></span></span> </dl> | <span data-ttu-id="e2315-542">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e2315-542">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e2315-543">**Status**</span><span class="sxs-lookup"><span data-stu-id="e2315-543">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2315-544">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2315-544">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2315-545">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2315-545">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2315-546">Beschreibt den Status des Elements.</span><span class="sxs-lookup"><span data-stu-id="e2315-546">Describes the status of the element.</span></span> <span data-ttu-id="e2315-547">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e2315-547">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="e2315-548">Okay</span><span class="sxs-lookup"><span data-stu-id="e2315-548">"OK"</span></span>

<span data-ttu-id="e2315-549">Zeit</span><span class="sxs-lookup"><span data-stu-id="e2315-549">"Error"</span></span>

<span data-ttu-id="e2315-550">Zerstört</span><span class="sxs-lookup"><span data-stu-id="e2315-550">"Degraded"</span></span>

<span data-ttu-id="e2315-551">Unbekannter</span><span class="sxs-lookup"><span data-stu-id="e2315-551">"Unknown"</span></span>

<span data-ttu-id="e2315-552">"Pred Fail"</span><span class="sxs-lookup"><span data-stu-id="e2315-552">"Pred Fail"</span></span>

<span data-ttu-id="e2315-553">Fahren</span><span class="sxs-lookup"><span data-stu-id="e2315-553">"Starting"</span></span>

<span data-ttu-id="e2315-554">Hindern</span><span class="sxs-lookup"><span data-stu-id="e2315-554">"Stopping"</span></span>

<span data-ttu-id="e2315-555">Leistungs</span><span class="sxs-lookup"><span data-stu-id="e2315-555">"Service"</span></span>

<span data-ttu-id="e2315-556">Gestresst</span><span class="sxs-lookup"><span data-stu-id="e2315-556">"Stressed"</span></span>

<span data-ttu-id="e2315-557">"Nicht wiederherstellen"</span><span class="sxs-lookup"><span data-stu-id="e2315-557">"NonRecover"</span></span>

<span data-ttu-id="e2315-558">"Kein Kontakt"</span><span class="sxs-lookup"><span data-stu-id="e2315-558">"No Contact"</span></span>

<span data-ttu-id="e2315-559">"Verlorene comm"</span><span class="sxs-lookup"><span data-stu-id="e2315-559">"Lost Comm"</span></span>

</dd> <dt>

<span data-ttu-id="e2315-560">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="e2315-560">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2315-561">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="e2315-561">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e2315-562">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2315-562">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2315-563">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="e2315-563">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="e2315-564">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e2315-564">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2315-565">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="e2315-565">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2315-566">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2315-566">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2315-567">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2315-567">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2315-568">Der Name der Erstellungs Klasse des hostingsystems.</span><span class="sxs-lookup"><span data-stu-id="e2315-568">The hosting system's creation class name.</span></span> <span data-ttu-id="e2315-569">Diese Eigenschaft wird von [**CIM \_ serviceaccesspoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e2315-569">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="e2315-570">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="e2315-570">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2315-571">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2315-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2315-572">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2315-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2315-573">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="e2315-573">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="e2315-574">Der Name des hostingsystems.</span><span class="sxs-lookup"><span data-stu-id="e2315-574">The name of the hosting system.</span></span> <span data-ttu-id="e2315-575">Diese Eigenschaft wird von [**CIM \_ serviceaccesspoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e2315-575">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="e2315-576">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="e2315-576">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2315-577">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="e2315-577">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e2315-578">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2315-578">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2315-579">Das Datum und die Uhrzeit der letzten Änderung des aktivierten Zustands des Elements.</span><span class="sxs-lookup"><span data-stu-id="e2315-579">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="e2315-580">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, wird jedoch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e2315-580">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="e2315-581">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="e2315-581">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2315-582">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2315-582">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2315-583">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2315-583">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2315-584">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="e2315-584">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="e2315-585">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e2315-585">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e2315-586">**WWNN**</span><span class="sxs-lookup"><span data-stu-id="e2315-586">**WWNN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2315-587">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2315-587">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2315-588">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2315-588">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2315-589">Der World Wide Node Name des Fibre Channel Ports, mit dem dieser Endpunkt verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="e2315-589">The world wide node name of the Fibre Channel port this endpoint is connected to.</span></span>

</dd> <dt>

<span data-ttu-id="e2315-590">**WWPN**</span><span class="sxs-lookup"><span data-stu-id="e2315-590">**WWPN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2315-591">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2315-591">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2315-592">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2315-592">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2315-593">Der World Wide Port Name des Fibre Channel Ports, mit dem dieser Endpunkt verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="e2315-593">The world wide port name of the Fibre Channel port this endpoint is connected to.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e2315-594">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2315-594">Requirements</span></span>



| <span data-ttu-id="e2315-595">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2315-595">Requirement</span></span> | <span data-ttu-id="e2315-596">Wert</span><span class="sxs-lookup"><span data-stu-id="e2315-596">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2315-597">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e2315-597">Minimum supported client</span></span><br/> | <span data-ttu-id="e2315-598">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2315-598">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e2315-599">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e2315-599">Minimum supported server</span></span><br/> | <span data-ttu-id="e2315-600">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2315-600">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e2315-601">Namespace</span><span class="sxs-lookup"><span data-stu-id="e2315-601">Namespace</span></span><br/>                | <span data-ttu-id="e2315-602">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="e2315-602">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e2315-603">MOF</span><span class="sxs-lookup"><span data-stu-id="e2315-603">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2315-604"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e2315-604"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2315-605">DLL</span><span class="sxs-lookup"><span data-stu-id="e2315-605">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2315-606"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e2315-606"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

