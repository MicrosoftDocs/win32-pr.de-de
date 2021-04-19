---
description: Stellt eine Instanz einer Erweiterungs Komponente dar, die an einen virtuellen Ethernet-Switch gebunden ist.
ms.assetid: 5b3e26e3-4cb9-47c9-865e-2f3232bbfc8e
title: Msvm_EthernetSwitchExtension-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchExtension
- Msvm_EthernetSwitchExtension.InstanceID
- Msvm_EthernetSwitchExtension.Caption
- Msvm_EthernetSwitchExtension.Description
- Msvm_EthernetSwitchExtension.ElementName
- Msvm_EthernetSwitchExtension.InstallDate
- Msvm_EthernetSwitchExtension.OperationalStatus
- Msvm_EthernetSwitchExtension.StatusDescriptions
- Msvm_EthernetSwitchExtension.Status
- Msvm_EthernetSwitchExtension.HealthState
- Msvm_EthernetSwitchExtension.CommunicationStatus
- Msvm_EthernetSwitchExtension.DetailedStatus
- Msvm_EthernetSwitchExtension.OperatingStatus
- Msvm_EthernetSwitchExtension.PrimaryStatus
- Msvm_EthernetSwitchExtension.EnabledState
- Msvm_EthernetSwitchExtension.OtherEnabledState
- Msvm_EthernetSwitchExtension.RequestedState
- Msvm_EthernetSwitchExtension.EnabledDefault
- Msvm_EthernetSwitchExtension.TimeOfLastStateChange
- Msvm_EthernetSwitchExtension.AvailableRequestedStates
- Msvm_EthernetSwitchExtension.TransitioningToState
- Msvm_EthernetSwitchExtension.SystemCreationClassName
- Msvm_EthernetSwitchExtension.SystemName
- Msvm_EthernetSwitchExtension.CreationClassName
- Msvm_EthernetSwitchExtension.Name
- Msvm_EthernetSwitchExtension.ExtensionType
- Msvm_EthernetSwitchExtension.Vendor
- Msvm_EthernetSwitchExtension.Version
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a6d760737ded1a12cf369ccb3a46595627d8e38e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362795"
---
# <a name="msvm_ethernetswitchextension-class"></a><span data-ttu-id="da19a-103">MSVM \_ ethernetzwitchextension-Klasse</span><span class="sxs-lookup"><span data-stu-id="da19a-103">Msvm\_EthernetSwitchExtension class</span></span>

<span data-ttu-id="da19a-104">Stellt eine Instanz einer Erweiterungs Komponente dar, die an einen virtuellen Ethernet-Switch gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="da19a-104">Represents an instance of an extension component bound to a virtual Ethernet switch.</span></span>

<span data-ttu-id="da19a-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="da19a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="da19a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="da19a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchExtension : CIM_EnabledLogicalElement
{
  string   InstanceID;
  string   Caption = "Virtual Switch Extension";
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
  string   SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string   SystemName;
  string   CreationClassName = "Msvm_EthernetSwitchExtension";
  string   Name;
  uint8    ExtensionType;
  string   Vendor;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="da19a-107">Member</span><span class="sxs-lookup"><span data-stu-id="da19a-107">Members</span></span>

<span data-ttu-id="da19a-108">Die **MSVM-Klasse " \_ ethernetzwitchextension** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="da19a-108">The **Msvm\_EthernetSwitchExtension** class has these types of members:</span></span>

-   [<span data-ttu-id="da19a-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="da19a-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="da19a-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="da19a-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="da19a-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="da19a-111">Methods</span></span>

<span data-ttu-id="da19a-112">Die **MSVM-Klasse " \_ ethernetzwitchextension** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="da19a-112">The **Msvm\_EthernetSwitchExtension** class has these methods.</span></span>



| <span data-ttu-id="da19a-113">Methode</span><span class="sxs-lookup"><span data-stu-id="da19a-113">Method</span></span>                                                                        | <span data-ttu-id="da19a-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="da19a-114">Description</span></span>                         |
|:------------------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="da19a-115">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="da19a-115">**RequestStateChange**</span></span>](msvm-ethernetswitchextension-requeststatechange.md) | <span data-ttu-id="da19a-116">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="da19a-116">Requests a state change.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="da19a-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="da19a-117">Properties</span></span>

<span data-ttu-id="da19a-118">Die **MSVM-Klasse " \_ ethernetzwitchextension** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="da19a-118">The **Msvm\_EthernetSwitchExtension** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="da19a-119">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="da19a-119">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da19a-120">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="da19a-120">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="da19a-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da19a-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da19a-122">Gibt die möglichen Werte für den *requestedstate* -Parameter der [**requestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) -Methode an, die zum Initiieren einer Zustandsänderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="da19a-122">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="da19a-123">Bei den aufgelisteten Werten handelt es sich um eine Teilmenge der Werte in der **requestedstaatsupported** -Eigenschaft der zugeordneten Instanz von **CIM \_ enabledlogicalelementfunctions**, bei der die ausgewählten Werte eine Funktion des aktuellen Zustands des [**CIM- \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))sind.</span><span class="sxs-lookup"><span data-stu-id="da19a-123">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="da19a-124">Diese Eigenschaft darf nicht **null** sein, wenn eine Implementierung den Satz möglicher Werte als Funktion des aktuellen Zustands ankündigen kann.</span><span class="sxs-lookup"><span data-stu-id="da19a-124">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="da19a-125">Diese Eigenschaft ist **null** , wenn eine Implementierung den Satz möglicher Werte nicht als Funktion des aktuellen Zustands bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="da19a-125">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="da19a-126">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="da19a-126">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="da19a-127"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="da19a-127"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="da19a-128"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="da19a-128"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="da19a-129"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Herunter** fahren (4)</span><span class="sxs-lookup"><span data-stu-id="da19a-129"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="da19a-130"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="da19a-130"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="da19a-131"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="da19a-131"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="da19a-132"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>Zurück **stellen (8** )</span><span class="sxs-lookup"><span data-stu-id="da19a-132"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="da19a-133"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Still **legung (9** )</span><span class="sxs-lookup"><span data-stu-id="da19a-133"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="da19a-134"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Neustart** (10)</span><span class="sxs-lookup"><span data-stu-id="da19a-134"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="da19a-135"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Zurücksetzen** (11)</span><span class="sxs-lookup"><span data-stu-id="da19a-135"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="da19a-136"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reserviert** (..</span><span class="sxs-lookup"><span data-stu-id="da19a-136"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="da19a-137">)</span><span class="sxs-lookup"><span data-stu-id="da19a-137">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="da19a-138">**Caption**</span><span class="sxs-lookup"><span data-stu-id="da19a-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da19a-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="da19a-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da19a-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da19a-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da19a-141">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="da19a-141">A short description of the object.</span></span> <span data-ttu-id="da19a-142">Diese Eigenschaft wird vom [**CIM \_ managedelta-Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Virtual Switch extension" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="da19a-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Switch Extension".</span></span>

</dd> <dt>

<span data-ttu-id="da19a-143">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="da19a-143">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da19a-144">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da19a-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="da19a-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da19a-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da19a-146">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="da19a-146">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="da19a-147">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="da19a-147">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="da19a-148">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="da19a-148">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="da19a-149">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="da19a-149">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da19a-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="da19a-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da19a-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da19a-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da19a-152">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="da19a-152">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="da19a-153">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="da19a-153">The name of the class or subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="da19a-154">Diese Eigenschaft ist immer auf "MSVM \_ ethernetzwitchextension" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="da19a-154">This property is always set to "Msvm\_EthernetSwitchExtension".</span></span>

</dd> <dt>

<span data-ttu-id="da19a-155">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="da19a-155">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da19a-156">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="da19a-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da19a-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da19a-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da19a-158">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="da19a-158">A description of the object.</span></span> <span data-ttu-id="da19a-159">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="da19a-159">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="da19a-160">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="da19a-160">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da19a-161">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da19a-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="da19a-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da19a-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da19a-163">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="da19a-163">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="da19a-164">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="da19a-164">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="da19a-165">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="da19a-165">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="da19a-166">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="da19a-166">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da19a-167">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="da19a-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da19a-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da19a-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da19a-169">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="da19a-169">A display name for the object.</span></span> <span data-ttu-id="da19a-170">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="da19a-170">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="da19a-171">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="da19a-171">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da19a-172">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da19a-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="da19a-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da19a-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da19a-174">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="da19a-174">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="da19a-175">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) geerbt und ist einer der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="da19a-175">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="da19a-176"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="da19a-176"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="da19a-177"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="da19a-177"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="da19a-178"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Aktiviert, aber offline** (6)</span><span class="sxs-lookup"><span data-stu-id="da19a-178"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="da19a-179">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="da19a-179">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da19a-180">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da19a-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="da19a-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da19a-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da19a-182">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="da19a-182">The enabled and disabled states of an element.</span></span> <span data-ttu-id="da19a-183">Diese Eigenschaft kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben.</span><span class="sxs-lookup"><span data-stu-id="da19a-183">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="da19a-184">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="da19a-184">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="da19a-185">Wert</span><span class="sxs-lookup"><span data-stu-id="da19a-185">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="da19a-186">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="da19a-186">Meaning</span></span>                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="da19a-187"><dt>**Unbekannter**</dt> Wert <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="da19a-187"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 |                                                                                                                                                                                                             |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="da19a-188"><dt>**Sonstige**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="da19a-188"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                             |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="da19a-189"><dt>**Aktiviert**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="da19a-189"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="da19a-190">Das-Element ist oder kann Befehle ausführen, verarbeitet alle in der Warteschlange befindlichen Befehle und fügt neue Anforderungen in die Warteschlange ein.</span><span class="sxs-lookup"><span data-stu-id="da19a-190">The element is or could be executing commands, will process any queued commands, and queues new requests.</span></span><br/>                                                                                        |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="da19a-191"><dt>**Deaktiviert**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="da19a-191"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="da19a-192">Das-Element führt keine Befehle aus und löscht alle neuen Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="da19a-192">The element will not execute commands and will drop any new requests.</span></span><br/>                                                                                                                            |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="da19a-193"><dt>4</dt> wird <dt>**heruntergefahren**</dt></span><span class="sxs-lookup"><span data-stu-id="da19a-193"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="da19a-194">Das Element wird gerade in den deaktivierten Zustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="da19a-194">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                      |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="da19a-195"><dt>**Nicht zutreffend**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="da19a-195"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="da19a-196">Das Element unterstützt das Aktivieren oder Deaktivieren des Elements nicht.</span><span class="sxs-lookup"><span data-stu-id="da19a-196">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                          |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="da19a-197"><dt>**Aktiviert, aber offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="da19a-197"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="da19a-198">Das Element kann Befehle abschließen und löscht alle neuen Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="da19a-198">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                     |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="da19a-199"><dt>**In Test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="da19a-199"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="da19a-200">Das-Element befindet sich in einem Testzustand.</span><span class="sxs-lookup"><span data-stu-id="da19a-200">The element is in a test state.</span></span><br/>                                                                                                                                                                  |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="da19a-201"><dt></dt> Verzögert <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="da19a-201"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="da19a-202">Das Element kann Befehle abschließen, aber alle neuen Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="da19a-202">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                    |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="da19a-203"><dt>**Inesce**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="da19a-203"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="da19a-204">Das Element ist aktiviert, jedoch in einem eingeschränkten Modus.</span><span class="sxs-lookup"><span data-stu-id="da19a-204">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="da19a-205">Das Verhalten des-Elements ähnelt dem aktivierten Zustand, verarbeitet aber nur einen eingeschränkten Satz von Befehlen.</span><span class="sxs-lookup"><span data-stu-id="da19a-205">The behavior of the element is similar to the Enabled state, but it processes only a restricted set of commands.</span></span> <span data-ttu-id="da19a-206">Alle anderen Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="da19a-206">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="da19a-207"><dt>**Start**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="da19a-207"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="da19a-208">Das Element wechselt in den Zustand "aktiviert".</span><span class="sxs-lookup"><span data-stu-id="da19a-208">The element is in the process of going to an Enabled state.</span></span> <span data-ttu-id="da19a-209">Neue Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="da19a-209">New requests are queued.</span></span><br/>                                                                                                             |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="da19a-210"><dt>**DMTF reserviert**</dt> <dt>11 32767</dt></span><span class="sxs-lookup"><span data-stu-id="da19a-210"><dt>**DMTF Reserved**</dt> <dt>11 32767</dt></span></span> </dl>                  | <span data-ttu-id="da19a-211">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="da19a-211">Reserved.</span></span><br/>                                                                                                                                                                                        |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="da19a-212"><dt>**Anbieter reserviert**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="da19a-212"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl>       | <span data-ttu-id="da19a-213">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="da19a-213">Reserved.</span></span><br/>                                                                                                                                                                                        |



 

</dd> <dt>

<span data-ttu-id="da19a-214">**ExtensionType**</span><span class="sxs-lookup"><span data-stu-id="da19a-214">**ExtensionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da19a-215">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="da19a-215">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="da19a-216">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da19a-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da19a-217">Gibt den Typ der Erweiterungs Komponente an.</span><span class="sxs-lookup"><span data-stu-id="da19a-217">Indicates the type of the extension component.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="da19a-218">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="da19a-218">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Capture"></span><span id="capture"></span><span id="CAPTURE"></span>

<span data-ttu-id="da19a-219">**Erfassung** (1)</span><span class="sxs-lookup"><span data-stu-id="da19a-219">**Capture** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>

<span data-ttu-id="da19a-220">**Filter** (2)</span><span class="sxs-lookup"><span data-stu-id="da19a-220">**Filter** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Forwarding"></span><span id="forwarding"></span><span id="FORWARDING"></span>

<span data-ttu-id="da19a-221">**Weiterleitung** (3)</span><span class="sxs-lookup"><span data-stu-id="da19a-221">**Forwarding** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Monitoring"></span><span id="monitoring"></span><span id="MONITORING"></span>

<span data-ttu-id="da19a-222">**Überwachung** (4)</span><span class="sxs-lookup"><span data-stu-id="da19a-222">**Monitoring** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Native"></span><span id="native"></span><span id="NATIVE"></span>

<span data-ttu-id="da19a-223">**Native** (5)</span><span class="sxs-lookup"><span data-stu-id="da19a-223">**Native** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="da19a-224">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="da19a-224">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da19a-225">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da19a-225">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="da19a-226">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da19a-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da19a-227">Gibt den aktuellen Zustand des Elements an.</span><span class="sxs-lookup"><span data-stu-id="da19a-227">Specifies the current health of the element.</span></span> <span data-ttu-id="da19a-228">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="da19a-228">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="da19a-229">Wenn ein kritischer Fehler auftritt, finden Sie im Ereignisprotokoll weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="da19a-229">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="da19a-230">Die **enabledstate** -Eigenschaft kann auch weitere Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="da19a-230">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="da19a-231">Wenn z. b. der Speicherplatz kritisch ist, ist **healthstate** auf 25 festgelegt, der virtuelle Computer wird angehalten, und **enabledstate** wird auf 32768 (angehalten) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="da19a-231">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="da19a-232">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="da19a-232">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="da19a-233">Wert</span><span class="sxs-lookup"><span data-stu-id="da19a-233">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="da19a-234">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="da19a-234">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="da19a-235"><dt>**OK**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="da19a-235"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="da19a-236">Das-Element ist voll funktionsfähig und wird in normalen Betriebsparametern und ohne Fehler ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="da19a-236">The element is fully functional and is operating within normal operational parameters and without error.</span></span><br/> |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="da19a-237"><dt>**Hauptfehler**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="da19a-237"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="da19a-238">Das-Element hat einen schwerwiegenden Fehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="da19a-238">The element has suffered a major failure.</span></span><br/>                                                                |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="da19a-239"><dt>**Kritischer Fehler**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="da19a-239"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="da19a-240">Das Element ist nicht funktionsfähig, und die Wiederherstellung ist möglicherweise nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="da19a-240">The element is nonfunctional, and recovery might not be possible.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="da19a-241">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="da19a-241">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da19a-242">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="da19a-242">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="da19a-243">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da19a-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da19a-244">Das Datum und die Uhrzeit, zu der die Konfiguration der virtuellen Maschine für eine virtuelle Maschine oder **null** für ein Verwaltungs Betriebssystem erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="da19a-244">The date and time the virtual machine configuration was created for a virtual machine, or **Null**, for a management operating system.</span></span> <span data-ttu-id="da19a-245">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="da19a-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="da19a-246">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="da19a-246">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da19a-247">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="da19a-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da19a-248">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da19a-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da19a-249">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="da19a-249">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="da19a-250">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="da19a-250">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="da19a-251">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="da19a-251">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="da19a-252">**Name**</span><span class="sxs-lookup"><span data-stu-id="da19a-252">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da19a-253">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="da19a-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da19a-254">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da19a-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da19a-255">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="da19a-255">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="da19a-256">Der eindeutige Name der Erweiterungs Komponente.</span><span class="sxs-lookup"><span data-stu-id="da19a-256">The unique name of the extension component.</span></span>

</dd> <dt>

<span data-ttu-id="da19a-257">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="da19a-257">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da19a-258">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da19a-258">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="da19a-259">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da19a-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da19a-260">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="da19a-260">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="da19a-261">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="da19a-261">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="da19a-262">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="da19a-262">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="da19a-263">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="da19a-263">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da19a-264">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="da19a-264">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="da19a-265">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da19a-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da19a-266">Ein Array, das die aktuellen Status des-Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="da19a-266">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="da19a-267">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="da19a-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="da19a-268">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="da19a-268">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da19a-269">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="da19a-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da19a-270">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da19a-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da19a-271">Der aktivierte oder deaktivierte Status des Elements, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="da19a-271">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="da19a-272">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="da19a-272">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="da19a-273">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="da19a-273">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="da19a-274">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="da19a-274">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da19a-275">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da19a-275">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="da19a-276">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da19a-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da19a-277">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="da19a-277">Provides high level status information.</span></span> <span data-ttu-id="da19a-278">Diese Eigenschaft sollte in Verbindung mit der **detailedstatus** -Eigenschaft verwendet werden, um allgemeine und ausführliche Integritäts Statusinformationen für das-Element und seine unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="da19a-278">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="da19a-279">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="da19a-279">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="da19a-280">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="da19a-280">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="da19a-281">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="da19a-281">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da19a-282">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da19a-282">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="da19a-283">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da19a-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da19a-284">Der zuletzt angeforderte oder gewünschte Zustand für das Element, das an die **requestStateChange** -Methode weitergegeben wird, oder 12 (nicht zutreffend), wenn keine Zustandsänderung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="da19a-284">The last requested or desired state for the element as passed to the **RequestStateChange** method, or 12 (Not Applicable) if no state change is in progress.</span></span> <span data-ttu-id="da19a-285">Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="da19a-285">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="da19a-286">Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuell aktivierten oder deaktivierten Zustände zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="da19a-286">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="da19a-287">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="da19a-287">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="da19a-288">**Status**</span><span class="sxs-lookup"><span data-stu-id="da19a-288">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da19a-289">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="da19a-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da19a-290">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da19a-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da19a-291">Eine Zeichenfolge, die den Status des Elements angibt.</span><span class="sxs-lookup"><span data-stu-id="da19a-291">A string that specifies the status of the element.</span></span> <span data-ttu-id="da19a-292">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="da19a-292">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="da19a-293">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="da19a-293">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da19a-294">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="da19a-294">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="da19a-295">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da19a-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da19a-296">Qualifizierer: **arrayType** ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="da19a-296">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="da19a-297">Ein Array, das Zeichen folgen enthält, die die entsprechenden **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="da19a-297">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="da19a-298">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="da19a-298">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="da19a-299">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="da19a-299">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da19a-300">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="da19a-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da19a-301">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da19a-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da19a-302">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="da19a-302">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="da19a-303">Der Name der System Erstellungs Klasse.</span><span class="sxs-lookup"><span data-stu-id="da19a-303">The system creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="da19a-304">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="da19a-304">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da19a-305">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="da19a-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da19a-306">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da19a-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da19a-307">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ System**](cim-system.md).**Name**"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="da19a-307">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="da19a-308">Der Name des virtuellen Switchs, an den die Erweiterungs Instanz gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="da19a-308">The name of the virtual switch to which the extension instance is bound to.</span></span>

</dd> <dt>

<span data-ttu-id="da19a-309">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="da19a-309">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da19a-310">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="da19a-310">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="da19a-311">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da19a-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da19a-312">Das Datum und die Uhrzeit der letzten Änderung des aktivierten Zustands des Elements.</span><span class="sxs-lookup"><span data-stu-id="da19a-312">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="da19a-313">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="da19a-313">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="da19a-314">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="da19a-314">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da19a-315">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da19a-315">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="da19a-316">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da19a-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da19a-317">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="da19a-317">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="da19a-318">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="da19a-318">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="da19a-319">**Hersteller**</span><span class="sxs-lookup"><span data-stu-id="da19a-319">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da19a-320">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="da19a-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da19a-321">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da19a-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da19a-322">Gibt den Anbieter an, der die Erweiterung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="da19a-322">Indicates the vendor providing the extension.</span></span>

</dd> <dt>

<span data-ttu-id="da19a-323">**Version**</span><span class="sxs-lookup"><span data-stu-id="da19a-323">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da19a-324">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="da19a-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da19a-325">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da19a-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da19a-326">Die Version der Erweiterung im Format "*Major*". *neben* Version ", z. b." 2,0 ".</span><span class="sxs-lookup"><span data-stu-id="da19a-326">The version of the extension in a format of "*major*.*minor*", for example "2.0".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="da19a-327">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da19a-327">Requirements</span></span>



| <span data-ttu-id="da19a-328">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da19a-328">Requirement</span></span> | <span data-ttu-id="da19a-329">Wert</span><span class="sxs-lookup"><span data-stu-id="da19a-329">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da19a-330">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="da19a-330">Minimum supported client</span></span><br/> | <span data-ttu-id="da19a-331">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da19a-331">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="da19a-332">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="da19a-332">Minimum supported server</span></span><br/> | <span data-ttu-id="da19a-333">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da19a-333">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="da19a-334">Namespace</span><span class="sxs-lookup"><span data-stu-id="da19a-334">Namespace</span></span><br/>                | <span data-ttu-id="da19a-335">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="da19a-335">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="da19a-336">MOF</span><span class="sxs-lookup"><span data-stu-id="da19a-336">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da19a-337"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="da19a-337"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="da19a-338">DLL</span><span class="sxs-lookup"><span data-stu-id="da19a-338">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da19a-339"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="da19a-339"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

