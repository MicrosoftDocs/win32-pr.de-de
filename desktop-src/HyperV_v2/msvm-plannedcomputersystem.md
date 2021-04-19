---
description: Stellt einen geplanten virtuellen Computer dar.
ms.assetid: 4ce6d34c-66fb-4f4f-bf52-26d19bab6d4a
title: Msvm_PlannedComputerSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PlannedComputerSystem
- Msvm_PlannedComputerSystem.SetPowerState
- Msvm_PlannedComputerSystem.InstanceID
- Msvm_PlannedComputerSystem.Caption
- Msvm_PlannedComputerSystem.Description
- Msvm_PlannedComputerSystem.ElementName
- Msvm_PlannedComputerSystem.InstallDate
- Msvm_PlannedComputerSystem.OperationalStatus
- Msvm_PlannedComputerSystem.StatusDescriptions
- Msvm_PlannedComputerSystem.Status
- Msvm_PlannedComputerSystem.HealthState
- Msvm_PlannedComputerSystem.CommunicationStatus
- Msvm_PlannedComputerSystem.DetailedStatus
- Msvm_PlannedComputerSystem.OperatingStatus
- Msvm_PlannedComputerSystem.PrimaryStatus
- Msvm_PlannedComputerSystem.EnabledState
- Msvm_PlannedComputerSystem.OtherEnabledState
- Msvm_PlannedComputerSystem.RequestedState
- Msvm_PlannedComputerSystem.EnabledDefault
- Msvm_PlannedComputerSystem.TimeOfLastStateChange
- Msvm_PlannedComputerSystem.AvailableRequestedStates
- Msvm_PlannedComputerSystem.TransitioningToState
- Msvm_PlannedComputerSystem.CreationClassName
- Msvm_PlannedComputerSystem.Name
- Msvm_PlannedComputerSystem.NameFormat
- Msvm_PlannedComputerSystem.PrimaryOwnerName
- Msvm_PlannedComputerSystem.PrimaryOwnerContact
- Msvm_PlannedComputerSystem.Roles
- Msvm_PlannedComputerSystem.OtherIdentifyingInfo
- Msvm_PlannedComputerSystem.IdentifyingDescriptions
- Msvm_PlannedComputerSystem.Dedicated
- Msvm_PlannedComputerSystem.OtherDedicatedDescriptions
- Msvm_PlannedComputerSystem.ResetCapability
- Msvm_PlannedComputerSystem.PowerManagementCapabilities
- Msvm_PlannedComputerSystem.AssignedNumaNodeList
- Msvm_PlannedComputerSystem.OnTimeInMilliseconds
- Msvm_PlannedComputerSystem.ProcessID
- Msvm_PlannedComputerSystem.TimeOfLastConfigurationChange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 54bd72567880e97ece02936348d5a091a11d8ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366274"
---
# <a name="msvm_plannedcomputersystem-class"></a><span data-ttu-id="90e9b-103">MSVM \_ plannedcomputersystem-Klasse</span><span class="sxs-lookup"><span data-stu-id="90e9b-103">Msvm\_PlannedComputerSystem class</span></span>

<span data-ttu-id="90e9b-104">Stellt einen geplanten virtuellen Computer dar.</span><span class="sxs-lookup"><span data-stu-id="90e9b-104">Represents a planned virtual machine.</span></span>

<span data-ttu-id="90e9b-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="90e9b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="90e9b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="90e9b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PlannedComputerSystem : CIM_ComputerSystem
{
  string   InstanceID;
  string   Caption = "Planned Virtual Machine";
  string   Description = "Microsoft Planned Virtual Machine";
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The service is running normally" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState = 12;
  string   CreationClassName;
  string   Name;
  string   NameFormat;
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability;
  uint16   PowerManagementCapabilities[];
  uint16   AssignedNumaNodeList[];
  uint64   OnTimeInMilliseconds;
  uint32   ProcessID;
  datetime TimeOfLastConfigurationChange;
};
```

## <a name="members"></a><span data-ttu-id="90e9b-107">Member</span><span class="sxs-lookup"><span data-stu-id="90e9b-107">Members</span></span>

<span data-ttu-id="90e9b-108">Die **MSVM \_ plannedcomputersystem** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="90e9b-108">The **Msvm\_PlannedComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="90e9b-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="90e9b-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="90e9b-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="90e9b-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="90e9b-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="90e9b-111">Methods</span></span>

<span data-ttu-id="90e9b-112">Die **MSVM- \_ plannedcomputersystem** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="90e9b-112">The **Msvm\_PlannedComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="90e9b-113">Methode</span><span class="sxs-lookup"><span data-stu-id="90e9b-113">Method</span></span>                                                                      | <span data-ttu-id="90e9b-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="90e9b-114">Description</span></span>                                                                                 |
|:----------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90e9b-115">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="90e9b-115">**RequestStateChange**</span></span>](requeststatechange-msvm-plannedcomputersystem.md) | <span data-ttu-id="90e9b-116">Fordert an, dass der Status des geplanten Systems in den angegebenen Wert geändert wird.</span><span class="sxs-lookup"><span data-stu-id="90e9b-116">Requests that the state of the planned system be changed to the value specified.</span></span><br/> |
| <span data-ttu-id="90e9b-117">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="90e9b-117">**SetPowerState**</span></span>                                                           | <span data-ttu-id="90e9b-118">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-118">This method is not supported.</span></span><br/>                                                    |



 

### <a name="properties"></a><span data-ttu-id="90e9b-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="90e9b-119">Properties</span></span>

<span data-ttu-id="90e9b-120">Die **MSVM- \_ plannedcomputersystem** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="90e9b-120">The **Msvm\_PlannedComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="90e9b-121">**Assignednumanodelist**</span><span class="sxs-lookup"><span data-stu-id="90e9b-121">**AssignedNumaNodeList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-122">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="90e9b-122">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90e9b-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-124">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="90e9b-124">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-125">Ein Array von NUMA-Knoten (nicht einheitlicher Speicherzugriff), die dem virtuellen Computer derzeit zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="90e9b-125">An array of nonuniform memory access (NUMA) nodes that are currently assigned to the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="90e9b-126">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="90e9b-126">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-127">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="90e9b-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90e9b-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-129">Gibt die möglichen Werte für den *requestedstate* -Parameter der [**requestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) -Methode an, die zum Initiieren einer Zustandsänderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="90e9b-129">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="90e9b-130">Bei den aufgelisteten Werten handelt es sich um eine Teilmenge der Werte, die in der **requestedstaatsupported** -Eigenschaft der zugeordneten Instanz von **CIM \_ enabledlogicalelementfunctions** enthalten sind, wobei die ausgewählten Werte eine Funktion des aktuellen Zustands des [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) -Objekts sind.</span><span class="sxs-lookup"><span data-stu-id="90e9b-130">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="90e9b-131">Diese Eigenschaft darf nicht **null** sein, wenn eine Implementierung den Satz möglicher Werte als Funktion des aktuellen Zustands ankündigen kann.</span><span class="sxs-lookup"><span data-stu-id="90e9b-131">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="90e9b-132">Diese Eigenschaft ist **null** , wenn eine Implementierung den Satz möglicher Werte nicht als Funktion des aktuellen Zustands bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="90e9b-132">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="90e9b-133">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-133">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="90e9b-134"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="90e9b-134"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-135"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="90e9b-135"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-136"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Herunter** fahren (4)</span><span class="sxs-lookup"><span data-stu-id="90e9b-136"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-137"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="90e9b-137"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-138"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="90e9b-138"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-139"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>Zurück **stellen (8** )</span><span class="sxs-lookup"><span data-stu-id="90e9b-139"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-140"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Still **legung (9** )</span><span class="sxs-lookup"><span data-stu-id="90e9b-140"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-141"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Neustart** (10)</span><span class="sxs-lookup"><span data-stu-id="90e9b-141"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-142"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Zurücksetzen** (11)</span><span class="sxs-lookup"><span data-stu-id="90e9b-142"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-143"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reserviert** (..</span><span class="sxs-lookup"><span data-stu-id="90e9b-143"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="90e9b-144">)</span><span class="sxs-lookup"><span data-stu-id="90e9b-144">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="90e9b-145">**Caption**</span><span class="sxs-lookup"><span data-stu-id="90e9b-145">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="90e9b-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90e9b-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-148">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="90e9b-148">A short description of the object.</span></span> <span data-ttu-id="90e9b-149">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "geplanter virtueller Computer" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-149">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Planned Virtual Machine".</span></span>

</dd> <dt>

<span data-ttu-id="90e9b-150">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="90e9b-150">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-151">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="90e9b-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90e9b-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-153">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="90e9b-153">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="90e9b-154">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="90e9b-154">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="90e9b-155">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-155">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="90e9b-156">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="90e9b-156">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-157">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="90e9b-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90e9b-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-159">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="90e9b-159">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-160">Gibt den Namen der Klasse oder der Unterklasse an, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="90e9b-160">Indicates the name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="90e9b-161">Wenn diese Eigenschaft mit den anderen Schlüsseleigenschaften dieser Klasse verwendet wird, können alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="90e9b-161">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="90e9b-162">Diese Eigenschaft wird von der [**CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system) Klasse geerbt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-162">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="90e9b-163">**Dediziert**</span><span class="sxs-lookup"><span data-stu-id="90e9b-163">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-164">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="90e9b-164">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90e9b-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-166">Ein Array von Werten, die angeben, zu welchem Zweck das geplante System reserviert ist, und welche Funktionen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="90e9b-166">An array of values that indicate the purposes to which the planned system is dedicated, if any, and what functionality is provided.</span></span> <span data-ttu-id="90e9b-167">Beispielsweise können Sie angeben, dass das System für "Print" (Wert = 11) vorgesehen ist oder als "Hub" (Wert = 8) fungiert.</span><span class="sxs-lookup"><span data-stu-id="90e9b-167">For example, one could specify that the System is dedicated to "Print" (value=11) or acts as a "Hub" (value=8).</span></span> <span data-ttu-id="90e9b-168">Es können auch mehrere Zwecke angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="90e9b-168">Multiple purposes can also be indicated.</span></span> <span data-ttu-id="90e9b-169">Dies ist z. b. ein allgemeines System, das "nicht dediziert" (Wert = 0) angibt, aber auch "Print" (Value = 11) oder "Mobile User Device"-Dienste (Value = 17) hostet.</span><span class="sxs-lookup"><span data-stu-id="90e9b-169">For example, this is a general purpose system indicating "Not Dedicated" (value=0) but that it also hosts "Print" (value=11) or "Mobile User Device" (value=17) services.</span></span>

<span data-ttu-id="90e9b-170">Diese Eigenschaft wird von der [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Klasse geerbt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-170">This property is inherited from the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class.</span></span>



| <span data-ttu-id="90e9b-171">Wert</span><span class="sxs-lookup"><span data-stu-id="90e9b-171">Value</span></span>                                                                                                                                                                                                                                                                                                    | <span data-ttu-id="90e9b-172">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="90e9b-172">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span><dl> <span data-ttu-id="90e9b-173"><dt>**Nicht dediziert**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-173"><dt>**Not Dedicated**</dt> <dt>0</dt></span></span> </dl>                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="90e9b-174"><dt>**Unbekannt**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-174"><dt>**Unknown**</dt> <dt>1</dt></span></span> </dl>                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="90e9b-175"><dt>**Weitere**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-175"><dt>**Other**</dt> <dt>2</dt></span></span> </dl>                                                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span><dl> <span data-ttu-id="90e9b-176"><dt>**Speicher**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-176"><dt>**Storage**</dt> <dt>3</dt></span></span> </dl>                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Router"></span><span id="router"></span><span id="ROUTER"></span><dl> <span data-ttu-id="90e9b-177"><dt>**Router**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-177"><dt>**Router**</dt> <dt>4</dt></span></span> </dl>                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span><dl> <span data-ttu-id="90e9b-178"><dt>**Switch**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-178"><dt>**Switch**</dt> <dt>5</dt></span></span> </dl>                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span><dl> <span data-ttu-id="90e9b-179"><dt>**Layer 3-Switch**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-179"><dt>**Layer 3 Switch**</dt> <dt>6</dt></span></span> </dl>                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span><dl> <span data-ttu-id="90e9b-180"><dt>**Zentrale Niederlassung, Switch**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-180"><dt>**Central Office Switch**</dt> <dt>7</dt></span></span> </dl>                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Hub"></span><span id="hub"></span><span id="HUB"></span><dl> <span data-ttu-id="90e9b-181"><dt>**Hub**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-181"><dt>**Hub**</dt> <dt>8</dt></span></span> </dl>                                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span><dl> <span data-ttu-id="90e9b-182"><dt>**Access Server**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-182"><dt>**Access Server**</dt> <dt>9</dt></span></span> </dl>                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span><dl> <span data-ttu-id="90e9b-183"><dt>**Firewall**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-183"><dt>**Firewall**</dt> <dt>10</dt></span></span> </dl>                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Print"></span><span id="print"></span><span id="PRINT"></span><dl> <span data-ttu-id="90e9b-184"><dt>**Drucken**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-184"><dt>**Print**</dt> <dt>11</dt></span></span> </dl>                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="I_O"></span><span id="i_o"></span><dl> <span data-ttu-id="90e9b-185">E <dt>**/**</dt> a <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-185"><dt>**I/O**</dt> <dt>12</dt></span></span> </dl>                                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span><dl> <span data-ttu-id="90e9b-186"><dt>**Webcaching**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-186"><dt>**Web Caching**</dt> <dt>13</dt></span></span> </dl>                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span><dl> <span data-ttu-id="90e9b-187"><dt>**Verwaltung**</dt> <dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-187"><dt>**Management**</dt> <dt>14</dt></span></span> </dl>                                                                 | <span data-ttu-id="90e9b-188">Gibt an, dass diese Instanz für das Hosting der System Verwaltungssoftware reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="90e9b-188">Indicates this instance is dedicated to hosting system management software.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span><dl> <span data-ttu-id="90e9b-189"><dt>**Blockieren von Server**</dt> <dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-189"><dt>**Block Server**</dt> <dt>15</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span><dl> <span data-ttu-id="90e9b-190"><dt>**Datei Server**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-190"><dt>**File Server**</dt> <dt>16</dt></span></span> </dl>                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span><dl> <span data-ttu-id="90e9b-191"><dt>**Mobiles Benutzergerät**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-191"><dt>**Mobile User Device**</dt> <dt>17</dt></span></span> </dl>                                 | <span data-ttu-id="90e9b-192">Ein Beispiel für ein dediziertes mobiles Benutzergerät ist ein Mobiltelefon oder ein Barcode Scanner in einem Geschäft, der über eine Funkfrequenz kommuniziert.</span><span class="sxs-lookup"><span data-stu-id="90e9b-192">An example of a dedicated mobile user device is a mobile phone or a bar code scanner in a store that communicates through radio frequency.</span></span> <span data-ttu-id="90e9b-193">Diese Systeme sind in der Funktionalität und Programmierbarkeit sehr eingeschränkt und werden nicht als universelle Computerplattformen angesehen.</span><span class="sxs-lookup"><span data-stu-id="90e9b-193">These systems are quite limited in functionality and programmability, and are not considered general purpose computing platforms.</span></span> <span data-ttu-id="90e9b-194">Ein Beispiel für ein mobiles System, bei dem es sich um einen allgemeinen Zweck handelt (d. h. nicht dediziert), ist ein Hand gehalteter Computer.</span><span class="sxs-lookup"><span data-stu-id="90e9b-194">Alternately, an example of a mobile system that is general purpose (that is, is NOT dedicated) is a hand-held computer.</span></span> <span data-ttu-id="90e9b-195">Obwohl die Programmierbarkeit eingeschränkt ist, kann neue Software heruntergeladen und ihre Funktionalität vom Benutzer erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="90e9b-195">Although limited in its programmability, new software can be downloaded and its functionality expanded by the user.</span></span> <br/> |
| <span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span><dl> <span data-ttu-id="90e9b-196"><dt>**Wiederholung**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-196"><dt>**Repeater**</dt> <dt>18</dt></span></span> </dl>                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span><dl> <span data-ttu-id="90e9b-197"><dt>**Bridge/Extender**</dt> <dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-197"><dt>**Bridge/Extender**</dt> <dt>19</dt></span></span> </dl>                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span><dl> <span data-ttu-id="90e9b-198"><dt>**Gateway**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-198"><dt>**Gateway**</dt> <dt>20</dt></span></span> </dl>                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span><dl> <span data-ttu-id="90e9b-199"><dt>**Speichervirtualisierer**</dt> <dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-199"><dt>**Storage Virtualizer**</dt> <dt>21</dt></span></span> </dl>                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span><dl> <span data-ttu-id="90e9b-200"><dt>**Medienbibliothek**</dt> <dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-200"><dt>**Media Library**</dt> <dt>22</dt></span></span> </dl>                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span><dl> <span data-ttu-id="90e9b-201"><dt>**Erweiterderknoten**</dt> <dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-201"><dt>**ExtenderNode**</dt> <dt>23</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span><dl> <span data-ttu-id="90e9b-202"><dt>**NAS-Head**</dt> <dt>24</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-202"><dt>**NAS Head**</dt> <dt>24</dt></span></span> </dl>                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span><dl> <span data-ttu-id="90e9b-203"><dt>**Eigenständiges NAS**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-203"><dt>**Self-contained NAS**</dt> <dt>25</dt></span></span> </dl>                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="UPS"></span><span id="ups"></span><dl> <span data-ttu-id="90e9b-204"><dt>**UPS**</dt> <dt>26</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-204"><dt>**UPS**</dt> <dt>26</dt></span></span> </dl>                                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span><dl> <span data-ttu-id="90e9b-205"><dt>**IP-Telefon**</dt> <dt>27</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-205"><dt>**IP Phone**</dt> <dt>27</dt></span></span> </dl>                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span><dl> <span data-ttu-id="90e9b-206"><dt>**Verwaltungs Controller**</dt> <dt>28</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-206"><dt>**Management Controller**</dt> <dt>28</dt></span></span> </dl>                     | <span data-ttu-id="90e9b-207">Gibt an, dass diese Instanz spezielle Hardware für die Systemverwaltung darstellt (d. h. einen Baseboard-Verwaltungs Controller (BMC) oder einen Dienst Prozessor).</span><span class="sxs-lookup"><span data-stu-id="90e9b-207">Indicates this instance represents specialized hardware dedicated to systems management (that is, a Baseboard Management Controller (BMC) or service processor).</span></span> <span data-ttu-id="90e9b-208">Der Verwaltungsbereich eines Verwaltungs Controllers ist in der Regel ein einzelnes verwaltetes System, in dem es enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="90e9b-208">The management scope of a Management Controller is typically a single managed system in which it is contained.</span></span><br/>                                                                                                                                                                                                                                           |
| <span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span><dl> <span data-ttu-id="90e9b-209"><dt>**Chassis Manager**</dt> <dt>29</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-209"><dt>**Chassis Manager**</dt> <dt>29</dt></span></span> </dl>                                             | <span data-ttu-id="90e9b-210">Gibt an, dass diese Instanz ein System darstellt, das für die Verwaltung eines Blade Chassis und der darin enthaltenen Geräte vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="90e9b-210">Indicates this instance represents a system dedicated to management of a blade chassis and its contained devices.</span></span> <span data-ttu-id="90e9b-211">Dieser Wert wird verwendet, um einen Regal Controller darzustellen.</span><span class="sxs-lookup"><span data-stu-id="90e9b-211">This value would be used to represent a Shelf Controller.</span></span> <span data-ttu-id="90e9b-212">Ein Chassis-Manager ist ein Aggregations Punkt für die Verwaltung und kann für die Verwaltung von Bestandteilen auf untergeordneten Verwaltungs Controllern basieren</span><span class="sxs-lookup"><span data-stu-id="90e9b-212">A Chassis Manager is an aggregation point for management and may rely on subordinate management controllers for the management of constituent parts.</span></span> <br/>                                                                                                                                                                                         |
| <span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span><dl> <span data-ttu-id="90e9b-213"><dt>**Host basierter RAID-Controller**</dt> <dt>30</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-213"><dt>**Host-based RAID controller**</dt> <dt>30</dt></span></span> </dl> | <span data-ttu-id="90e9b-214">Gibt an, dass diese Instanz einen in einem Host Computer enthaltenen RAID-Speichercontroller darstellt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-214">Indicates this instance represents a RAID storage controller contained within a host computer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span><dl> <span data-ttu-id="90e9b-215"><dt>**Speichergeräte Gehäuse**</dt> <dt>31</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-215"><dt>**Storage Device Enclosure**</dt> <dt>31</dt></span></span> </dl>         | <span data-ttu-id="90e9b-216">Gibt an, dass diese Instanz ein Gehäuse darstellt, das Speichergeräte enthält.</span><span class="sxs-lookup"><span data-stu-id="90e9b-216">Indicates this instance represents an enclosure that contains storage devices.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span><dl> <span data-ttu-id="90e9b-217"><dt>**Desktop**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-217"><dt>**Desktop**</dt> <dt>32</dt></span></span> </dl>                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span><dl> <span data-ttu-id="90e9b-218"><dt>**Laptop**</dt> <dt>33</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-218"><dt>**Laptop**</dt> <dt>33</dt></span></span> </dl>                                                                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span><dl> <span data-ttu-id="90e9b-219"><dt>**Bibliothek für virtuelle Bänder**</dt> <dt>34</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-219"><dt>**Virtual Tape Library**</dt> <dt>34</dt></span></span> </dl>                         | <span data-ttu-id="90e9b-220">Die Emulation einer Band Bibliothek durch ein virtuelles Bibliotheks System.</span><span class="sxs-lookup"><span data-stu-id="90e9b-220">The emulation of a tape library by a Virtual Library System.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span><dl> <span data-ttu-id="90e9b-221"><dt>**Virtuelles Bibliotheks System**</dt> <dt>35</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-221"><dt>**Virtual Library System**</dt> <dt>35</dt></span></span> </dl>                 | <span data-ttu-id="90e9b-222">Verwendet Datenträger Speicher zum Emulieren von Bandbibliotheken.</span><span class="sxs-lookup"><span data-stu-id="90e9b-222">Uses disk storage to emulate tape libraries.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span><dl> <span data-ttu-id="90e9b-223"><dt>**Netzwerk-PC/Thin Client**</dt> <dt>36</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-223"><dt>**Network PC/Thin Client**</dt> <dt>36</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span><dl> <span data-ttu-id="90e9b-224"><dt>**FC-Switch**</dt> <dt>37</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-224"><dt>**FC Switch**</dt> <dt>37</dt></span></span> </dl>                                                                     | <span data-ttu-id="90e9b-225">Gibt an, dass diese Instanz dediziert ist, um Schicht 2 Fibre Channel Frames zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="90e9b-225">Indicates this instance is dedicated to switching layer 2 Fibre Channel frames.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span><dl> <span data-ttu-id="90e9b-226"><dt>**Ethernet-Switch**</dt> <dt>38</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-226"><dt>**Ethernet Switch**</dt> <dt>38</dt></span></span> </dl>                                             | <span data-ttu-id="90e9b-227">Gibt an, dass diese Instanz für das Wechseln von Layer 2-Ethernet-Frames reserviert ist</span><span class="sxs-lookup"><span data-stu-id="90e9b-227">Indicates this instance is dedicated to switching layer 2 Ethernet frames.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="90e9b-228"><dt>**DMTF reserviert**</dt> <dt>39.. 32567</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-228"><dt>**DMTF Reserved**</dt> <dt>39..32567</dt></span></span> </dl>                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="90e9b-229"><dt> **Anbieter reserviert**</dt> <dt>32568.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-229"><dt>**Vendor Reserved** </dt> <dt>32568..65535</dt></span></span> </dl>                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="90e9b-230">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="90e9b-230">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-231">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="90e9b-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-232">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90e9b-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-233">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="90e9b-233">A description of the object.</span></span> <span data-ttu-id="90e9b-234">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Microsoft geplanter virtueller Computer" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-234">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Planned Virtual Machine".</span></span>

</dd> <dt>

<span data-ttu-id="90e9b-235">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="90e9b-235">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-236">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="90e9b-236">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-237">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90e9b-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-238">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="90e9b-238">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="90e9b-239">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="90e9b-239">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="90e9b-240">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-240">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="90e9b-241">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="90e9b-241">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-242">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="90e9b-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-243">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90e9b-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-244">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-244">A display name for the object.</span></span> <span data-ttu-id="90e9b-245">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-245">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="90e9b-246">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="90e9b-246">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-247">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="90e9b-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-248">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90e9b-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-249">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="90e9b-249">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="90e9b-250">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="90e9b-250">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and can be one of the following values.</span></span>



| <span data-ttu-id="90e9b-251">Wert</span><span class="sxs-lookup"><span data-stu-id="90e9b-251">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="90e9b-252">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="90e9b-252">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="90e9b-253"><dt>**Deaktiviert**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-253"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="90e9b-254">Das System ist ausgeschaltet.</span><span class="sxs-lookup"><span data-stu-id="90e9b-254">The system is turned off.</span></span><br/>                                             |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="90e9b-255"><dt>**Aktiviert, aber offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-255"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="90e9b-256">Das System ist aktiviert, aber offline.</span><span class="sxs-lookup"><span data-stu-id="90e9b-256">The system is enabled, but offline.</span></span> <span data-ttu-id="90e9b-257">Alle neuen Anforderungen werden gelöscht.</span><span class="sxs-lookup"><span data-stu-id="90e9b-257">Any new requests will be dropped.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="90e9b-258">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="90e9b-258">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-259">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="90e9b-259">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-260">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90e9b-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-261">Gibt den aktivierten Zustand des geplanten Systems an.</span><span class="sxs-lookup"><span data-stu-id="90e9b-261">Specifies the enabled state of the planned system.</span></span> <span data-ttu-id="90e9b-262">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="90e9b-262">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it can be one of the following values.</span></span>



| <span data-ttu-id="90e9b-263">Wert</span><span class="sxs-lookup"><span data-stu-id="90e9b-263">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="90e9b-264">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="90e9b-264">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="90e9b-265"><dt>**Deaktiviert**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-265"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="90e9b-266">Das System ist ausgeschaltet.</span><span class="sxs-lookup"><span data-stu-id="90e9b-266">The system is turned off.</span></span><br/>                                             |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="90e9b-267"><dt>**Aktiviert, aber offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-267"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="90e9b-268">Das System ist aktiviert, aber offline.</span><span class="sxs-lookup"><span data-stu-id="90e9b-268">The system is enabled, but offline.</span></span> <span data-ttu-id="90e9b-269">Alle neuen Anforderungen werden gelöscht.</span><span class="sxs-lookup"><span data-stu-id="90e9b-269">Any new requests will be dropped.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="90e9b-270">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="90e9b-270">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-271">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="90e9b-271">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-272">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90e9b-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-273">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="90e9b-273">The current health of the element.</span></span> <span data-ttu-id="90e9b-274">Diese Eigenschaft drückt die Integrität dieses Elements aus, aber nicht notwendigerweise die seiner unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="90e9b-274">This property expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="90e9b-275">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="90e9b-275">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="90e9b-276">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 5 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="90e9b-277">Wert</span><span class="sxs-lookup"><span data-stu-id="90e9b-277">Value</span></span>                                                                        | <span data-ttu-id="90e9b-278">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="90e9b-278">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="90e9b-279"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-279"><dt>5</dt></span></span> </dl> | <span data-ttu-id="90e9b-280">Der Integritäts Status ist "Normal".</span><span class="sxs-lookup"><span data-stu-id="90e9b-280">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="90e9b-281">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="90e9b-281">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-282">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="90e9b-282">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-283">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90e9b-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-284">Ein Array von Zeichen folgen, das Erläuterungen und Details hinter den Einträgen im " **OtherIdentifyingInfo** "-Array bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-284">An array of strings providing explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="90e9b-285">Jeder Eintrag dieses Arrays bezieht sich auf den Eintrag in " **OtherIdentifyingInfo** ", der sich im gleichen Index befindet.</span><span class="sxs-lookup"><span data-stu-id="90e9b-285">Each entry of this array is related to the entry in **OtherIdentifyingInfo** that is located at the same index.</span></span> <span data-ttu-id="90e9b-286">Diese Eigenschaft wird von der [**CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system) Klasse geerbt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-286">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="90e9b-287">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="90e9b-287">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-288">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="90e9b-288">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-289">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90e9b-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-290">Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="90e9b-290">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="90e9b-291">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-291">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="90e9b-292">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="90e9b-292">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-293">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="90e9b-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-294">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90e9b-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-295">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="90e9b-295">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-296">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="90e9b-296">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="90e9b-297">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-297">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="90e9b-298">**Name**</span><span class="sxs-lookup"><span data-stu-id="90e9b-298">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-299">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="90e9b-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-300">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90e9b-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-301">Qualifizierer: **Key**, **override**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="90e9b-301">Qualifiers: **Key**, **Override**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-302">Der geerbte Name dient als Schlüssel für eine System Instanz in einer Unternehmensumgebung.</span><span class="sxs-lookup"><span data-stu-id="90e9b-302">The inherited name serves as the key of a system instance in an enterprise environment.</span></span> <span data-ttu-id="90e9b-303">Diese Eigenschaft wird von der [**CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system) Klasse geerbt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-303">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="90e9b-304">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="90e9b-304">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-305">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="90e9b-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-306">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90e9b-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-307">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="90e9b-307">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-308">Gibt an, wie der Systemname mithilfe der Heuristik der Unterklasse generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="90e9b-308">Identifies how the system name was generated, using the heuristic of the subclass.</span></span> <span data-ttu-id="90e9b-309">Das Systemobjekt und seine Ableitungen sind Objekte der obersten Ebene von CIM.</span><span class="sxs-lookup"><span data-stu-id="90e9b-309">The system object and its derivatives are top-level objects of CIM.</span></span> <span data-ttu-id="90e9b-310">Sie stellen den Bereich für zahlreiche Komponenten bereit.</span><span class="sxs-lookup"><span data-stu-id="90e9b-310">They provide the scope for numerous components.</span></span> <span data-ttu-id="90e9b-311">Eindeutige Systemschlüssel sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="90e9b-311">Having unique system keys is required.</span></span> <span data-ttu-id="90e9b-312">Eine Heuristik kann in einzelnen System Unterklassen definiert werden, um immer denselben Systemnamen Schlüssel zu generieren.</span><span class="sxs-lookup"><span data-stu-id="90e9b-312">A heuristic can be defined in individual system subclasses to attempt to always generate the same system name key.</span></span> <span data-ttu-id="90e9b-313">Diese Eigenschaft wird von der [**CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system) Klasse geerbt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-313">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="90e9b-314">**Ontimeinmilliseconds**</span><span class="sxs-lookup"><span data-stu-id="90e9b-314">**OnTimeInMilliseconds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-315">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="90e9b-315">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-316">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90e9b-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-317">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Millisekunden")</span><span class="sxs-lookup"><span data-stu-id="90e9b-317">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds")</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-318">Die Gesamtzeit (in Millisekunden), seit der die virtuelle Maschine zuletzt eingeschaltet, zurückgesetzt oder wieder hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="90e9b-318">The total time, in milliseconds, since the virtual machine was last turned on, reset, or restored.</span></span> <span data-ttu-id="90e9b-319">Diese Zeit schließt die Zeit aus, zu der sich der virtuelle Computer im angehaltenen Zustand befunden hat.</span><span class="sxs-lookup"><span data-stu-id="90e9b-319">This time excludes the time the virtual machine was in the paused state.</span></span>

</dd> <dt>

<span data-ttu-id="90e9b-320">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="90e9b-320">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-321">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="90e9b-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-322">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90e9b-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-323">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="90e9b-323">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="90e9b-324">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="90e9b-324">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="90e9b-325">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="90e9b-326">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="90e9b-326">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-327">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="90e9b-327">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-328">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90e9b-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-329">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="90e9b-329">The current statuses of the object.</span></span> <span data-ttu-id="90e9b-330">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf 2 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-330">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="90e9b-331">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="90e9b-331">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-332">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="90e9b-332">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-333">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90e9b-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-334">Eine Zeichenfolge, die beschreibt, wie oder warum das System dediziert ist, wenn das dedizierte Array den Wert 2 ("Other") enthält.</span><span class="sxs-lookup"><span data-stu-id="90e9b-334">A string describing how or why the system is dedicated when the Dedicated array includes the value 2, "Other".</span></span> <span data-ttu-id="90e9b-335">Diese Eigenschaft wird von der [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Klasse geerbt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-335">This property is inherited from the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class.</span></span>

</dd> <dt>

<span data-ttu-id="90e9b-336">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="90e9b-336">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-337">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="90e9b-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-338">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90e9b-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-339">Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 ("Other") festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="90e9b-339">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="90e9b-340">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="90e9b-340">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="90e9b-341">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-341">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="90e9b-342">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="90e9b-342">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-343">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="90e9b-343">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-344">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90e9b-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-345">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="90e9b-345">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-346">Enthält zusätzliche Daten über Systemnamen Informationen hinaus, die zur Identifizierung eines Computer Systems verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="90e9b-346">Contains additional data, beyond system name information, that can be used to identify a ComputerSystem.</span></span> <span data-ttu-id="90e9b-347">Ein Beispiel wäre die Fibre Channel World Wide Name (WWN) eines Knotens.</span><span class="sxs-lookup"><span data-stu-id="90e9b-347">One example would be to hold the Fibre Channel World-Wide Name (WWN) of a node.</span></span> <span data-ttu-id="90e9b-348">Wenn nur der Fibre Channel Name verfügbar ist und eindeutig (als Systemschlüssel verwendet werden kann), ist diese Eigenschaft **null** , und der WWN würde zum Systemschlüssel werden, dessen Daten in die **Name** -Eigenschaft eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="90e9b-348">If only the Fibre Channel name is available and is unique (able to be used as the system key), then this property would be **Null** and the WWN would become the system key, its data placed in the **Name** property.</span></span> <span data-ttu-id="90e9b-349">Diese Eigenschaft wird von der [**CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system) Klasse geerbt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-349">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="90e9b-350">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="90e9b-350">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-351">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="90e9b-351">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-352">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90e9b-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-353">Diese Eigenschaft wird von der [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Klasse geerbt, aber Sie wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-353">This property is inherited from the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class, but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="90e9b-354">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="90e9b-354">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-355">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="90e9b-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-356">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="90e9b-356">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-357">Qualifizierer: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="90e9b-357">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-358">Eine Zeichenfolge, die Informationen darüber bereitstellt, wie der primäre Systembesitzer erreicht werden kann (z. b. Telefonnummer, e-Mail-Adresse usw.).</span><span class="sxs-lookup"><span data-stu-id="90e9b-358">A string that provides information on how the primary system owner can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="90e9b-359">Diese Eigenschaft wird von der [**CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system) Klasse geerbt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-359">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="90e9b-360">**Primaryownername**</span><span class="sxs-lookup"><span data-stu-id="90e9b-360">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-361">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="90e9b-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-362">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="90e9b-362">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-363">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="90e9b-363">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-364">Der Name des primären System Besitzers.</span><span class="sxs-lookup"><span data-stu-id="90e9b-364">The name of the primary system owner.</span></span> <span data-ttu-id="90e9b-365">Der Systembesitzer ist der primäre Benutzer des Systems.</span><span class="sxs-lookup"><span data-stu-id="90e9b-365">The system owner is the primary user of the system.</span></span> <span data-ttu-id="90e9b-366">Diese Eigenschaft wird von der [**CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system) Klasse geerbt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-366">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="90e9b-367">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="90e9b-367">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-368">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="90e9b-368">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-369">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90e9b-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-370">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="90e9b-370">Provides high level status information.</span></span> <span data-ttu-id="90e9b-371">Diese Eigenschaft sollte in Verbindung mit der **detailedstatus** -Eigenschaft verwendet werden, um allgemeine und ausführliche Integritäts Statusinformationen für das-Element und seine unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="90e9b-371">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="90e9b-372">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="90e9b-372">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="90e9b-373">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-373">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="90e9b-374">**ProcessID**</span><span class="sxs-lookup"><span data-stu-id="90e9b-374">**ProcessID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-375">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="90e9b-375">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-376">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90e9b-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-377">Der Bezeichner des Prozesses, unter dem dieser virtuelle Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="90e9b-377">The identifier of the process under which this virtual machine is running.</span></span> <span data-ttu-id="90e9b-378">Dieser Wert kann verwendet werden, um die Instanz von Vmwp.exe auf dem System, auf dem der virtuelle Computer ausgeführt wird, eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="90e9b-378">This value can be used to uniquely identify the instance of Vmwp.exe on the system that is running the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="90e9b-379">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="90e9b-379">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-380">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="90e9b-380">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-381">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90e9b-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-382">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="90e9b-382">The last requested or desired state for the element.</span></span> <span data-ttu-id="90e9b-383">Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-383">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="90e9b-384">Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuellen Zustände für ein Element zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="90e9b-384">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="90e9b-385">Eine bestimmte Instanz der [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) -Klasse unterstützt die **requestedstate** -Eigenschaft möglicherweise nicht.</span><span class="sxs-lookup"><span data-stu-id="90e9b-385">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="90e9b-386">Wenn dies auftritt, wird der Wert 12 ("nicht zutreffend") verwendet.</span><span class="sxs-lookup"><span data-stu-id="90e9b-386">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="90e9b-387">Diese Eigenschaft wird von **CIM \_ enabledlogicalelement** geerbt und ist immer auf 12 (nicht zutreffend) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-387">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="90e9b-388">Wert</span><span class="sxs-lookup"><span data-stu-id="90e9b-388">Value</span></span>                                                                         | <span data-ttu-id="90e9b-389">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="90e9b-389">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="90e9b-390"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-390"><dt>12</dt></span></span> </dl> | <span data-ttu-id="90e9b-391">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="90e9b-391">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="90e9b-392">**Resetcapability**</span><span class="sxs-lookup"><span data-stu-id="90e9b-392">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-393">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="90e9b-393">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-394">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90e9b-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-395">Gibt die Zurücksetzungs Funktionen des Computer Systems an.</span><span class="sxs-lookup"><span data-stu-id="90e9b-395">Specifies the reset capabilities of the computer system.</span></span> <span data-ttu-id="90e9b-396">Diese Eigenschaft wird von der [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Klasse geerbt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-396">This property is inherited from the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class.</span></span>



| <span data-ttu-id="90e9b-397">Wert</span><span class="sxs-lookup"><span data-stu-id="90e9b-397">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="90e9b-398">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="90e9b-398">Meaning</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="90e9b-399"><dt>**Sonstige**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-399"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                              |                                                                                                            |
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="90e9b-400"><dt>**Unbekannt**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-400"><dt>**Unknown**</dt> <dt>2</dt></span></span> </dl>                                      |                                                                                                            |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="90e9b-401"><dt>**Deaktiviert**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-401"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                  | <span data-ttu-id="90e9b-402">Das Zurücksetzen von Hardware ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="90e9b-402">Hardware reset is not allowed.</span></span> <br/>                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="90e9b-403"><dt></dt> <dt>4</dt> aktiviert</span><span class="sxs-lookup"><span data-stu-id="90e9b-403"><dt>**Enabled**</dt> <dt>4</dt></span></span> </dl>                                      | <span data-ttu-id="90e9b-404">Das Computersystem kann mit Hardware zurückgesetzt werden (z. b. die Schaltflächen Strom und zurücksetzen).</span><span class="sxs-lookup"><span data-stu-id="90e9b-404">The computer system can be reset by using hardware (for example, the power and reset buttons).</span></span> <br/> |
| <span id="Not_Implemented_"></span><span id="not_implemented_"></span><span id="NOT_IMPLEMENTED_"></span><dl> <span data-ttu-id="90e9b-405"><dt> **Nicht implementiert**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-405"><dt>**Not Implemented** </dt> <dt>5 </dt></span></span> </dl> |                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="90e9b-406">**Rollen**</span><span class="sxs-lookup"><span data-stu-id="90e9b-406">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-407">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="90e9b-407">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-408">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="90e9b-408">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-409">Ein Array von Zeichen folgen, das die vom Administrator definierten Rollen angibt, die dieses System in der verwalteten Umgebung spielt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-409">An array of strings that specifies the administrator-defined roles this system plays in the managed environment.</span></span> <span data-ttu-id="90e9b-410">Beispiele hierfür sind "Building 8 Printserver" oder "Boise User Directories".</span><span class="sxs-lookup"><span data-stu-id="90e9b-410">Examples might be "Building 8 print server" or "Boise user directories".</span></span> <span data-ttu-id="90e9b-411">Ein einzelnes System kann mehrere Rollen ausführen.</span><span class="sxs-lookup"><span data-stu-id="90e9b-411">A single system may perform multiple roles.</span></span> <span data-ttu-id="90e9b-412">Die Instrumentations Ansicht der Rollen eines Systems wird definiert, indem eine bestimmte Unterklasse von System oder durch Eigenschaften in einer Unterklasse oder beides instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="90e9b-412">The instrumentation view of the roles of a system is defined by instantiating a specific subclass of system, or by properties in a subclass, or both.</span></span> <span data-ttu-id="90e9b-413">Beispielsweise wird der Zweck eines Computer Systems mithilfe der **dedizierten** Eigenschaften und der **otherdedigendescription-Eigenschaft** definiert.</span><span class="sxs-lookup"><span data-stu-id="90e9b-413">For example, the purpose of a ComputerSystem is defined using the **Dedicated** and **OtherDedicatedDescription** properties.</span></span> <span data-ttu-id="90e9b-414">Diese Eigenschaft wird von der [**CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system) Klasse geerbt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-414">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="90e9b-415">**Status**</span><span class="sxs-lookup"><span data-stu-id="90e9b-415">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-416">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="90e9b-416">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-417">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90e9b-417">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-418">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="90e9b-418">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="90e9b-419">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="90e9b-419">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-420">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="90e9b-420">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-421">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90e9b-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-422">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="90e9b-422">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="90e9b-423">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf "der Dienst wird normal ausgeführt" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-423">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "The service is running normally".</span></span>

</dd> <dt>

<span data-ttu-id="90e9b-424">**Timeoflastconfigurationchange**</span><span class="sxs-lookup"><span data-stu-id="90e9b-424">**TimeOfLastConfigurationChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-425">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="90e9b-425">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-426">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90e9b-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-427">Das Datum und die Uhrzeit der letzten Änderung der Konfigurationsdatei des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="90e9b-427">The date and time when the virtual machine configuration file was last modified.</span></span> <span data-ttu-id="90e9b-428">Die Konfigurationsdatei wird bei bestimmten virtuellen Maschinen Vorgängen geändert, sowie beim Hinzufügen, ändern oder Entfernen von virtuellen Computern oder Geräteeinstellungen.</span><span class="sxs-lookup"><span data-stu-id="90e9b-428">The configuration file is modified during certain virtual machine operations, as well as when any of the virtual machine or device settings are added, modified, or removed.</span></span>

</dd> <dt>

<span data-ttu-id="90e9b-429">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="90e9b-429">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-430">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="90e9b-430">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-431">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90e9b-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-432">Das Datum und die Uhrzeit der letzten Änderung des aktivierten Zustands des Elements.</span><span class="sxs-lookup"><span data-stu-id="90e9b-432">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="90e9b-433">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, wird jedoch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-433">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="90e9b-434">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="90e9b-434">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e9b-435">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="90e9b-435">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="90e9b-436">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90e9b-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90e9b-437">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="90e9b-437">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="90e9b-438">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-438">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="90e9b-439">Wert</span><span class="sxs-lookup"><span data-stu-id="90e9b-439">Value</span></span>                                                                                                                                                                                                                                                     | <span data-ttu-id="90e9b-440">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="90e9b-440">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="90e9b-441"><dt>**Unbekannter**</dt> Wert <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-441"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                               |                                                                                  |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="90e9b-442"><dt>**Aktiviert**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-442"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                               |                                                                                  |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="90e9b-443"><dt>**Deaktiviert**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-443"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                           |                                                                                  |
| <span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span><dl> <span data-ttu-id="90e9b-444"><dt>**Herunterfahren**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-444"><dt>**Shut Down**</dt> <dt>4</dt></span></span> </dl>                       |                                                                                  |
| <span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span><dl> <span data-ttu-id="90e9b-445"><dt>**Keine Änderung**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-445"><dt>**No Change**</dt> <dt>5</dt></span></span> </dl>                       | <span data-ttu-id="90e9b-446">Es wird kein Übergang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="90e9b-446">No transition is in progress.</span></span><br/>                                         |
| <span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span><dl> <span data-ttu-id="90e9b-447"><dt>**Offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-447"><dt>**Offline**</dt> <dt>6</dt></span></span> </dl>                               |                                                                                  |
| <span id="Test"></span><span id="test"></span><span id="TEST"></span><dl> <span data-ttu-id="90e9b-448"><dt>**Test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-448"><dt>**Test**</dt> <dt>7</dt></span></span> </dl>                                           |                                                                                  |
| <span id="Defer"></span><span id="defer"></span><span id="DEFER"></span><dl> <span data-ttu-id="90e9b-449"><dt></dt> Zurückstellen <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-449"><dt>**Defer**</dt> <dt>8</dt></span></span> </dl>                                       |                                                                                  |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="90e9b-450"><dt>**Inesce**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-450"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                               |                                                                                  |
| <span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span><dl> <span data-ttu-id="90e9b-451"><dt>**Neustart**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-451"><dt>**Reboot**</dt> <dt>10</dt></span></span> </dl>                                  |                                                                                  |
| <span id="Reset"></span><span id="reset"></span><span id="RESET"></span><dl> <span data-ttu-id="90e9b-452"><dt>11</dt> <dt>**Zurücksetzen**</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-452"><dt>**Reset**</dt> <dt>11</dt></span></span> </dl>                                      |                                                                                  |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="90e9b-453"><dt>**Nicht zutreffend**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-453"><dt>**Not Applicable**</dt> <dt>12</dt></span></span> </dl>  | <span data-ttu-id="90e9b-454">Die-Implementierung unterstützt das darstellen von laufenden Übergängen nicht.</span><span class="sxs-lookup"><span data-stu-id="90e9b-454">The implementation does not support representing ongoing transitions.</span></span><br/> |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <span data-ttu-id="90e9b-455"><dt> **DMTF reserviert**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-455"><dt>**DMTF Reserved** </dt> <dt>.. </dt></span></span> </dl> |                                                                                  |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="90e9b-456">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90e9b-456">Requirements</span></span>



| <span data-ttu-id="90e9b-457">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90e9b-457">Requirement</span></span> | <span data-ttu-id="90e9b-458">Wert</span><span class="sxs-lookup"><span data-stu-id="90e9b-458">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90e9b-459">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="90e9b-459">Minimum supported client</span></span><br/> | <span data-ttu-id="90e9b-460">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90e9b-460">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="90e9b-461">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="90e9b-461">Minimum supported server</span></span><br/> | <span data-ttu-id="90e9b-462">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90e9b-462">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="90e9b-463">Namespace</span><span class="sxs-lookup"><span data-stu-id="90e9b-463">Namespace</span></span><br/>                | <span data-ttu-id="90e9b-464">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="90e9b-464">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="90e9b-465">MOF</span><span class="sxs-lookup"><span data-stu-id="90e9b-465">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90e9b-466"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-466"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="90e9b-467">DLL</span><span class="sxs-lookup"><span data-stu-id="90e9b-467">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90e9b-468"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="90e9b-468"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="90e9b-469">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90e9b-469">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90e9b-470">**CIM- \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="90e9b-470">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> <dt>

[<span data-ttu-id="90e9b-471">**MSVM \_ virtualsystemmanagementservice. Importsystemdefinition-Methode**</span><span class="sxs-lookup"><span data-stu-id="90e9b-471">**Msvm\_VirtualSystemManagementService .ImportSystemDefinition method**</span></span>](importsystemdefinition-msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

