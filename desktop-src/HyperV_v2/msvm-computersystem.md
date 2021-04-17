---
description: Stellt ein physisches Computersystem oder eine virtuelle Maschine dar.
ms.assetid: 1db9e169-1466-4898-ab95-e9d622fe43cb
title: Msvm_ComputerSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem
- Msvm_ComputerSystem.SetPowerState
- Msvm_ComputerSystem.InstanceID
- Msvm_ComputerSystem.Caption
- Msvm_ComputerSystem.Description
- Msvm_ComputerSystem.ElementName
- Msvm_ComputerSystem.InstallDate
- Msvm_ComputerSystem.OperationalStatus
- Msvm_ComputerSystem.StatusDescriptions
- Msvm_ComputerSystem.Status
- Msvm_ComputerSystem.HealthState
- Msvm_ComputerSystem.CommunicationStatus
- Msvm_ComputerSystem.DetailedStatus
- Msvm_ComputerSystem.OperatingStatus
- Msvm_ComputerSystem.PrimaryStatus
- Msvm_ComputerSystem.EnabledState
- Msvm_ComputerSystem.OtherEnabledState
- Msvm_ComputerSystem.RequestedState
- Msvm_ComputerSystem.EnabledDefault
- Msvm_ComputerSystem.TimeOfLastStateChange
- Msvm_ComputerSystem.AvailableRequestedStates
- Msvm_ComputerSystem.TransitioningToState
- Msvm_ComputerSystem.CreationClassName
- Msvm_ComputerSystem.Name
- Msvm_ComputerSystem.PrimaryOwnerName
- Msvm_ComputerSystem.PrimaryOwnerContact
- Msvm_ComputerSystem.Roles
- Msvm_ComputerSystem.NameFormat
- Msvm_ComputerSystem.OtherIdentifyingInfo
- Msvm_ComputerSystem.IdentifyingDescriptions
- Msvm_ComputerSystem.Dedicated
- Msvm_ComputerSystem.OtherDedicatedDescriptions
- Msvm_ComputerSystem.ResetCapability
- Msvm_ComputerSystem.PowerManagementCapabilities
- Msvm_ComputerSystem.OnTimeInMilliseconds
- Msvm_ComputerSystem.ProcessID
- Msvm_ComputerSystem.TimeOfLastConfigurationChange
- Msvm_ComputerSystem.NumberOfNumaNodes
- Msvm_ComputerSystem.ReplicationState
- Msvm_ComputerSystem.ReplicationHealth
- Msvm_ComputerSystem.ReplicationMode
- Msvm_ComputerSystem.FailedOverReplicationType
- Msvm_ComputerSystem.LastReplicationType
- Msvm_ComputerSystem.LastApplicationConsistentReplicationTime
- Msvm_ComputerSystem.LastReplicationTime
- Msvm_ComputerSystem.LastSuccessfulBackupTime
- Msvm_ComputerSystem.EnhancedSessionModeState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ae36179e14b584bad4e68350e27d485cdc10c42b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104554813"
---
# <a name="msvm_computersystem-class"></a><span data-ttu-id="23673-103">MSVM \_ Computersystem-Klasse</span><span class="sxs-lookup"><span data-stu-id="23673-103">Msvm\_ComputerSystem class</span></span>

<span data-ttu-id="23673-104">Stellt ein physisches Computersystem oder eine virtuelle Maschine dar.</span><span class="sxs-lookup"><span data-stu-id="23673-104">Represents a physical computer system or virtual machine.</span></span>

<span data-ttu-id="23673-105">Verwenden Sie zum Abrufen von Informationen für die VMMS die Klasse [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="23673-105">To retrieve information for the VMMS, use the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="23673-106">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="23673-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="23673-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="23673-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ComputerSystem : CIM_ComputerSystem
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
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   CreationClassName;
  string   Name = "GUID";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   NameFormat;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability = 1;
  uint16   PowerManagementCapabilities[];
  uint64   OnTimeInMilliseconds;
  uint32   ProcessID;
  datetime TimeOfLastConfigurationChange;
  uint16   NumberOfNumaNodes;
  uint16   ReplicationState;
  uint16   ReplicationHealth;
  uint16   ReplicationMode;
  uint16   FailedOverReplicationType;
  uint16   LastReplicationType;
  DateTime LastApplicationConsistentReplicationTime;
  DateTime LastReplicationTime;
  DateTime LastSuccessfulBackupTime;
  uint16   EnhancedSessionModeState;
};
```

## <a name="members"></a><span data-ttu-id="23673-108">Member</span><span class="sxs-lookup"><span data-stu-id="23673-108">Members</span></span>

<span data-ttu-id="23673-109">Die **MSVM \_ Computersystem** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="23673-109">The **Msvm\_ComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="23673-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="23673-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="23673-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="23673-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="23673-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="23673-112">Methods</span></span>

<span data-ttu-id="23673-113">Die **MSVM \_ Computersystem** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="23673-113">The **Msvm\_ComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="23673-114">Methode</span><span class="sxs-lookup"><span data-stu-id="23673-114">Method</span></span>                                                                                         | <span data-ttu-id="23673-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="23673-115">Description</span></span>                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="23673-116">**Injetnonmaskableinterrupt**</span><span class="sxs-lookup"><span data-stu-id="23673-116">**InjectNonMaskableInterrupt**</span></span>](injectnonmaskableinterrupt-msvm-computersystem.md)           | <span data-ttu-id="23673-117">Fügt einen nicht maskierbaren Interrupt in den virtuellen Computer ein.</span><span class="sxs-lookup"><span data-stu-id="23673-117">Injects a non-maskable interrupt into the virtual machine.</span></span> <span data-ttu-id="23673-118">Diese Methode wird nur für Instanzen der **MSVM \_ Computersystem** -Klasse unterstützt, die eine virtuelle Maschine darstellen.</span><span class="sxs-lookup"><span data-stu-id="23673-118">This method is only supported for instances of the **Msvm\_ComputerSystem** class that represent a virtual machine.</span></span><br/> <span data-ttu-id="23673-119">**Windows 8.1:** Diese Methode wird erst Windows 8.1 und Windows Server 2012 R2 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="23673-119">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>                                    |
| [<span data-ttu-id="23673-120">**Requestreplicationstatechange**</span><span class="sxs-lookup"><span data-stu-id="23673-120">**RequestReplicationStateChange**</span></span>](msvm-computersystem-requestreplicationstatechange.md)     | <span data-ttu-id="23673-121">Fordert an, dass der Replikations Status der virtuellen Maschine auf den angegebenen Wert geändert wird.</span><span class="sxs-lookup"><span data-stu-id="23673-121">Requests that the replication state of the virtual machine be changed to the specified value.</span></span> <span data-ttu-id="23673-122">Diese Methode wird nur für Instanzen der **MSVM \_ Computersystem** -Klasse unterstützt, die eine virtuelle Maschine darstellen.</span><span class="sxs-lookup"><span data-stu-id="23673-122">This method is only supported for instances of the **Msvm\_ComputerSystem** class that represent a virtual machine.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="23673-123">**Requestreplicationstatechangeex**</span><span class="sxs-lookup"><span data-stu-id="23673-123">**RequestReplicationStateChangeEx**</span></span>](msvm-requestreplicationstatechangeex-computersystem.md) | <span data-ttu-id="23673-124">Fordert an, dass der Replikations Status der virtuellen Maschine auf den angegebenen Wert geändert wird.</span><span class="sxs-lookup"><span data-stu-id="23673-124">Requests that the replication state of the virtual machine be changed to the specified value.</span></span> <span data-ttu-id="23673-125">Diese Methode wird nur für Instanzen der **MSVM \_ Computersystem** -Klasse unterstützt, die eine virtuelle Maschine darstellen.</span><span class="sxs-lookup"><span data-stu-id="23673-125">This method is only supported for instances of the **Msvm\_ComputerSystem** class that represent a virtual machine.</span></span><br/> <span data-ttu-id="23673-126">**Windows 8.1:** Diese Methode wird erst Windows 8.1 und Windows Server 2012 R2 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="23673-126">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| [<span data-ttu-id="23673-127">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="23673-127">**RequestStateChange**</span></span>](requeststatechange-msvm-computersystem.md)                           | <span data-ttu-id="23673-128">Fordert an, dass der Zustand des virtuellen Computers geändert wird.</span><span class="sxs-lookup"><span data-stu-id="23673-128">Requests that the state of the virtual machine be changed.</span></span> <span data-ttu-id="23673-129">Diese Methode wird nur für Instanzen der **MSVM \_ Computersystem** -Klasse unterstützt, die eine virtuelle Maschine darstellen.</span><span class="sxs-lookup"><span data-stu-id="23673-129">This method is only supported for instances of the **Msvm\_ComputerSystem** class that represent a virtual machine.</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="23673-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="23673-130">**SetPowerState**</span></span>                                                                              | <span data-ttu-id="23673-131">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="23673-131">This method is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                            |



 

### <a name="properties"></a><span data-ttu-id="23673-132">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="23673-132">Properties</span></span>

<span data-ttu-id="23673-133">Die **MSVM \_ Computersystem** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="23673-133">The **Msvm\_ComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="23673-134">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="23673-134">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-135">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="23673-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="23673-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-137">Gibt die möglichen Werte für den *requestedstate* -Parameter der [**requestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) -Methode an, die zum Initiieren einer Zustandsänderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="23673-137">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="23673-138">Bei den aufgelisteten Werten handelt es sich um eine Teilmenge der Werte, die in der **requestedstaatsupported** -Eigenschaft der zugeordneten Instanz von **CIM \_ enabledlogicalelementfunctions** enthalten sind, wobei die ausgewählten Werte eine Funktion des aktuellen Zustands des [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) -Objekts sind.</span><span class="sxs-lookup"><span data-stu-id="23673-138">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="23673-139">Diese Eigenschaft darf nicht **null** sein, wenn eine Implementierung den Satz möglicher Werte als Funktion des aktuellen Zustands ankündigen kann.</span><span class="sxs-lookup"><span data-stu-id="23673-139">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="23673-140">Diese Eigenschaft ist **null** , wenn eine Implementierung den Satz möglicher Werte nicht als Funktion des aktuellen Zustands bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="23673-140">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="23673-141">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="23673-141">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="23673-142"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="23673-142"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="23673-143"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="23673-143"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="23673-144"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Herunter** fahren (4)</span><span class="sxs-lookup"><span data-stu-id="23673-144"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="23673-145"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="23673-145"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="23673-146"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="23673-146"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="23673-147"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>Zurück **stellen (8** )</span><span class="sxs-lookup"><span data-stu-id="23673-147"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="23673-148"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Still **legung (9** )</span><span class="sxs-lookup"><span data-stu-id="23673-148"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="23673-149"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Neustart** (10)</span><span class="sxs-lookup"><span data-stu-id="23673-149"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="23673-150"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Zurücksetzen** (11)</span><span class="sxs-lookup"><span data-stu-id="23673-150"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="23673-151"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reserviert** (..</span><span class="sxs-lookup"><span data-stu-id="23673-151"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="23673-152">)</span><span class="sxs-lookup"><span data-stu-id="23673-152">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="23673-153">**Caption**</span><span class="sxs-lookup"><span data-stu-id="23673-153">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-154">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="23673-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23673-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-156">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="23673-156">A short description of the object.</span></span> <span data-ttu-id="23673-157">Diese Eigenschaft wird von der [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) -Klasse geerbt und enthält einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="23673-157">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class, and it will contain one of the following values.</span></span>



| <span data-ttu-id="23673-158">Wert</span><span class="sxs-lookup"><span data-stu-id="23673-158">Value</span></span>                                                                                                | <span data-ttu-id="23673-159">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="23673-159">Meaning</span></span>                                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="23673-160"><dt>"Virtueller Computer"</dt></span><span class="sxs-lookup"><span data-stu-id="23673-160"><dt>"Virtual Machine"</dt></span></span> </dl>         | <span data-ttu-id="23673-161">Die-Instanz stellt einen virtuellen Computer dar.</span><span class="sxs-lookup"><span data-stu-id="23673-161">The instance represents a virtual machine.</span></span><br/>    |
| <dl> <span data-ttu-id="23673-162"><dt>"Hosting Computer System"</dt></span><span class="sxs-lookup"><span data-stu-id="23673-162"><dt>"Hosting Computer System"</dt></span></span> </dl> | <span data-ttu-id="23673-163">Die-Instanz stellt den hostingcomputer dar.</span><span class="sxs-lookup"><span data-stu-id="23673-163">The instance represents the hosting computer.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="23673-164">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="23673-164">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-165">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23673-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23673-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-167">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="23673-167">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="23673-168">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="23673-168">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="23673-169">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="23673-169">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="23673-170">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="23673-170">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-171">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="23673-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23673-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-173">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="23673-173">The name of the class or subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="23673-174">Diese Eigenschaft wird vom [**CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system)geerbt und ist immer auf "MSVM \_ Computer System" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="23673-174">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="23673-175">**Dediziert**</span><span class="sxs-lookup"><span data-stu-id="23673-175">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-176">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="23673-176">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="23673-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-178">Gibt an, ob es sich bei dem Computersystem um ein spezielles System handelt (dediziert für eine bestimmte Verwendung) und ob es sich um ein allgemeines System handelt.</span><span class="sxs-lookup"><span data-stu-id="23673-178">Indicates whether the computer system is a special-purpose system (dedicated to a particular use), versus being a general-purpose system.</span></span> <span data-ttu-id="23673-179">Diese Eigenschaft wird von [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)geerbt und ist immer auf 0 (nicht dediziert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="23673-179">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 0 (Not Dedicated).</span></span>

</dd> <dt>

<span data-ttu-id="23673-180">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="23673-180">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-181">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="23673-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23673-182">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-183">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="23673-183">A description of the object.</span></span> <span data-ttu-id="23673-184">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und enthält einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="23673-184">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it will contain one of the following values.</span></span>



| <span data-ttu-id="23673-185">Wert</span><span class="sxs-lookup"><span data-stu-id="23673-185">Value</span></span>                                                                                                          | <span data-ttu-id="23673-186">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="23673-186">Meaning</span></span>                                                  |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="23673-187"><dt>"Microsoft Virtual Computer System"</dt></span><span class="sxs-lookup"><span data-stu-id="23673-187"><dt>"Microsoft Virtual Computer System"</dt></span></span> </dl> | <span data-ttu-id="23673-188">Die-Instanz stellt einen virtuellen Computer dar.</span><span class="sxs-lookup"><span data-stu-id="23673-188">The instance represents a virtual machine.</span></span><br/>    |
| <dl> <span data-ttu-id="23673-189"><dt>"Microsoft Hosting Computer System"</dt></span><span class="sxs-lookup"><span data-stu-id="23673-189"><dt>"Microsoft Hosting Computer System"</dt></span></span> </dl> | <span data-ttu-id="23673-190">Die-Instanz stellt den hostingcomputer dar.</span><span class="sxs-lookup"><span data-stu-id="23673-190">The instance represents the hosting computer.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="23673-191">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="23673-191">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-192">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23673-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23673-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-194">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="23673-194">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="23673-195">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="23673-195">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="23673-196">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="23673-196">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="23673-197">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="23673-197">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-198">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="23673-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23673-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-200">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="23673-200">A display name for the object.</span></span> <span data-ttu-id="23673-201">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf den anzeigen amen des Computers für eine virtuelle Maschine oder den NetBIOS-Namen des Verwaltungs Betriebssystems festgelegt.</span><span class="sxs-lookup"><span data-stu-id="23673-201">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to the display name of the computer for a virtual machine or the NetBIOS name of the management operating system.</span></span>

</dd> <dt>

<span data-ttu-id="23673-202">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="23673-202">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-203">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23673-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23673-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-205">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="23673-205">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="23673-206">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) geerbt und ist einer der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="23673-206">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="23673-207"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="23673-207"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="23673-208"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="23673-208"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="23673-209"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Aktiviert, aber offline** (6)</span><span class="sxs-lookup"><span data-stu-id="23673-209"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="23673-210">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="23673-210">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-211">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23673-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23673-212">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-213">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="23673-213">The enabled and disabled states of an element.</span></span> <span data-ttu-id="23673-214">Diese Eigenschaft kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben.</span><span class="sxs-lookup"><span data-stu-id="23673-214">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="23673-215">Diese Eigenschaft wird von der [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) -Klasse geerbt und auf 2 (aktiviert) für einen physischen Computer oder auf einen der folgenden Werte für eine virtuelle Maschine festgelegt.</span><span class="sxs-lookup"><span data-stu-id="23673-215">This property is inherited from the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class, and it is set to 2 (Enabled) for a physical computer or one of the following values for a virtual machine.</span></span> <span data-ttu-id="23673-216">Eine grafische Ansicht dieser Zustände finden Sie unter "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="23673-216">For a graphical view of these states, see Remarks.</span></span>



| <span data-ttu-id="23673-217">Wert</span><span class="sxs-lookup"><span data-stu-id="23673-217">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="23673-218">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="23673-218">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="23673-219"><dt>**Unbekannter**</dt> Wert <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="23673-219"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="23673-220">Der Zustand des Elements konnte nicht bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="23673-220">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="23673-221"><dt>**Sonstige**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="23673-221"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="23673-222"><dt>**Aktiviert**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="23673-222"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="23673-223">Das-Element wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="23673-223">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="23673-224"><dt>**Deaktiviert**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="23673-224"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="23673-225">Das Element ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="23673-225">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="23673-226"><dt>4</dt> wird <dt>**heruntergefahren**</dt></span><span class="sxs-lookup"><span data-stu-id="23673-226"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="23673-227">Das Element wird gerade in den deaktivierten Zustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="23673-227">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="23673-228"><dt>**Nicht zutreffend**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="23673-228"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="23673-229">Das Element unterstützt das Aktivieren oder Deaktivieren des Elements nicht.</span><span class="sxs-lookup"><span data-stu-id="23673-229">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="23673-230"><dt>**Aktiviert, aber offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="23673-230"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="23673-231">Das Element kann Befehle abschließen und löscht alle neuen Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="23673-231">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="23673-232"><dt>**In Test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="23673-232"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="23673-233">Das-Element befindet sich in einem Testzustand.</span><span class="sxs-lookup"><span data-stu-id="23673-233">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="23673-234"><dt></dt> Verzögert <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="23673-234"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="23673-235">Das Element kann Befehle abschließen, aber alle neuen Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="23673-235">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="23673-236"><dt>**Inesce**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="23673-236"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="23673-237">Das Element ist aktiviert, jedoch in einem eingeschränkten Modus.</span><span class="sxs-lookup"><span data-stu-id="23673-237">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="23673-238">Das Verhalten des-Elements ähnelt dem aktivierten Status (2), aber es verarbeitet nur einen eingeschränkten Satz von Befehlen.</span><span class="sxs-lookup"><span data-stu-id="23673-238">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="23673-239">Alle anderen Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="23673-239">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="23673-240"><dt>**Start**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="23673-240"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="23673-241">Das Element wechselt in den Zustand "aktiviert" (2).</span><span class="sxs-lookup"><span data-stu-id="23673-241">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="23673-242">Neue Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="23673-242">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="23673-243">**Enhancedsessionmodestate**</span><span class="sxs-lookup"><span data-stu-id="23673-243">**EnhancedSessionModeState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-244">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23673-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23673-245">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-246">Gibt den aktuellen Status des erweiterten Sitzungs Modus auf dem virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="23673-246">Specifies the current state of enhanced session mode on the virtual machine.</span></span>

<span data-ttu-id="23673-247">Der Hyper-V-WMI-Anbieter löst jedes Mal, wenn sich der **enhancedsessionmodestate** der **MSVM \_ Computersystem** -Klasse ändert, ein [**\_ \_ instancemodificationevent-Ereignis**](/windows/desktop/WmiSdk/--instancemodificationevent) aus.</span><span class="sxs-lookup"><span data-stu-id="23673-247">The Hyper-V WMI provider raises an [**\_\_InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) each time the **EnhancedSessionModeState** of the **Msvm\_ComputerSystem** class changes.</span></span> <span data-ttu-id="23673-248">Wenn eine aktive vmconnection-Sitzung ein **\_ \_ instancemodificationevent-Ereignis** empfängt, wird versucht, in den erweiterten Sitzungs Modus zu wechseln, wenn der Benutzer diese Einstellung aktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="23673-248">If an active vmconnection session receives an **\_\_InstanceModificationEvent**, it attempts to switch to enhanced session mode if the user enabled that setting.</span></span>

<span data-ttu-id="23673-249">**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="23673-249">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<span data-ttu-id="23673-250">**Enhancedsessionmodestate** kann einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="23673-250">**EnhancedSessionModeState** can be one of these values:</span></span>

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

<span data-ttu-id="23673-251"><span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>**Zulässig und verfügbar** (2)</span><span class="sxs-lookup"><span data-stu-id="23673-251"><span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>**Allowed and available** (2)</span></span>


</dt> <dd>

<span data-ttu-id="23673-252">Der erweiterte Modus ist zulässig und auf dem virtuellen Computer verfügbar.</span><span class="sxs-lookup"><span data-stu-id="23673-252">Enhanced mode is allowed and available on the virtual machine.</span></span>

</dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span data-ttu-id="23673-253"><span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**Nicht zulässig** (3)</span><span class="sxs-lookup"><span data-stu-id="23673-253"><span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**Not allowed** (3)</span></span>


</dt> <dd>

<span data-ttu-id="23673-254">Der erweiterte Modus ist auf dem virtuellen Computer nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="23673-254">Enhanced mode is not allowed on the virtual machine.</span></span>

</dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

<span data-ttu-id="23673-255"><span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>**Zulässig, aber nicht verfügbar** (6)</span><span class="sxs-lookup"><span data-stu-id="23673-255"><span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>**Allowed but not available** (6)</span></span>


</dt> <dd>

<span data-ttu-id="23673-256">Der erweiterte Modus ist zulässig, aber zurzeit nicht auf dem virtuellen Computer verfügbar.</span><span class="sxs-lookup"><span data-stu-id="23673-256">Enhanced mode is allowed and but not currently available on the virtual machine.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="23673-257">**Failedoverreplicationtype**</span><span class="sxs-lookup"><span data-stu-id="23673-257">**FailedOverReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-258">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23673-258">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23673-259">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23673-260">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md).**Failedoverreplicationtype**")</span><span class="sxs-lookup"><span data-stu-id="23673-260">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**FailedOverReplicationType**")</span></span>
</dt> </dl>

<span data-ttu-id="23673-261">Der Typ des Wiederherstellungsdaten Punkts, der während des Failovervorgangs angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="23673-261">The type of recovery data point that was applied during the failover operation.</span></span>

> [!Note]  
> <span data-ttu-id="23673-262">Diese Eigenschaft ist ab Windows 8.1 veraltet. Verwenden Sie stattdessen die-Eigenschaft mit demselben Namen in der [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md) -Klasse, um den Wert für die primäre oder erweiterte Beziehung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="23673-262">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

<span data-ttu-id="23673-263">Dabei sind folgende Werte möglich:</span><span class="sxs-lookup"><span data-stu-id="23673-263">Possible values are:</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="23673-264">**Keine** (0)</span><span class="sxs-lookup"><span data-stu-id="23673-264">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="23673-265">**Regulär** (1)</span><span class="sxs-lookup"><span data-stu-id="23673-265">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="23673-266">**Anwendungs konsistent** (2)</span><span class="sxs-lookup"><span data-stu-id="23673-266">**Application consistent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="23673-267">**Geplant** (3)</span><span class="sxs-lookup"><span data-stu-id="23673-267">**Planned** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="23673-268">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="23673-268">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-269">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23673-269">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23673-270">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-271">Gibt den aktuellen Zustand des Elements an.</span><span class="sxs-lookup"><span data-stu-id="23673-271">Specifies the current health of the element.</span></span> <span data-ttu-id="23673-272">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="23673-272">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="23673-273">Wenn ein kritischer Fehler auftritt, finden Sie im Ereignisprotokoll weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="23673-273">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="23673-274">Die **enabledstate** -Eigenschaft kann auch weitere Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="23673-274">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="23673-275">Wenn z. b. der Speicherplatz kritisch ist, ist **healthstate** auf 25 festgelegt, der virtuelle Computer wird angehalten, und **enabledstate** wird auf 32768 (angehalten) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="23673-275">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="23673-276">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="23673-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="23673-277">Wert</span><span class="sxs-lookup"><span data-stu-id="23673-277">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="23673-278">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="23673-278">Meaning</span></span>                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="23673-279"><dt>**OK**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="23673-279"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="23673-280">Der virtuelle Computer ist voll funktionsfähig und wird in normalen Betriebsparametern und ohne Fehler ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="23673-280">The virtual machine is fully functional and is operating within normal operational parameters and without error.</span></span><br/>                                                                                                                                                                                    |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="23673-281"><dt>**Hauptfehler**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="23673-281"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="23673-282">Der virtuelle Computer hat einen schwerwiegenden Fehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="23673-282">The virtual machine has suffered a major failure.</span></span> <span data-ttu-id="23673-283">Dieser Wert wird verwendet, wenn auf einem oder mehreren Datenträgern, die die virtuellen Festplatten des virtuellen Computers enthalten, wenig Speicherplatz auf dem Datenträger und die virtuelle Maschine angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="23673-283">This value is used when one or more disks that contain the virtual machine's VHDs is low on disk space and the virtual machine has been paused.</span></span><br/>                                                                                                   |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="23673-284"><dt>**Kritischer Fehler**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="23673-284"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="23673-285">Das Element ist nicht funktionsfähig, und die Wiederherstellung ist möglicherweise nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="23673-285">The element is nonfunctional, and recovery might not be possible.</span></span> <span data-ttu-id="23673-286">Dies kann darauf hinweisen, dass der Arbeitsprozess für den virtuellen Computer (Vmwp.exe) nicht auf Steuerungs-oder Informationsanforderungen antwortet oder dass auf einem oder mehreren Datenträgern, die die virtuellen Festplatten für die virtuelle Maschine enthalten, wenig Speicherplatz zur Neige ist.</span><span class="sxs-lookup"><span data-stu-id="23673-286">This can indicate that the worker process for the virtual machine (Vmwp.exe) is not responding to control or information requests, or that one or more disks that contain the VHDs for the virtual machine are low on disk space.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="23673-287">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="23673-287">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-288">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="23673-288">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="23673-289">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-290">Diese Eigenschaft wird von [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="23673-290">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="23673-291">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="23673-291">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-292">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="23673-292">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="23673-293">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-294">Das Datum und die Uhrzeit, zu der die Konfiguration der virtuellen Maschine für eine virtuelle Maschine oder **null** für ein Verwaltungs Betriebssystem erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="23673-294">The date and time the virtual machine configuration was created for a virtual machine, or **Null**, for a management operating system.</span></span> <span data-ttu-id="23673-295">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="23673-295">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="23673-296">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="23673-296">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-297">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="23673-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23673-298">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23673-299">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="23673-299">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="23673-300">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="23673-300">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="23673-301">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="23673-301">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="23673-302">In Windows 8 gibt es für jedes Computersystem oder jeden virtuellen Computer eine einzelne Instanz von [**replicationsettingdata**](msvm-replicationsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="23673-302">In Windows 8, there is a single instance of [**ReplicationSettingData**](msvm-replicationsettingdata.md) for every computer system or virtual machine.</span></span> <span data-ttu-id="23673-303">Für Windows 8.1 hat ein virtueller Wiederherstellungs Computer zwei Instanzen von **replicationsettingdata**.</span><span class="sxs-lookup"><span data-stu-id="23673-303">For Windows 8.1, a recovery virtual machine has two instances of **ReplicationSettingData**.</span></span> <span data-ttu-id="23673-304">Diese Änderung unterscheidet und ordnet Einstellungsdaten der Replikations Beziehung zu.</span><span class="sxs-lookup"><span data-stu-id="23673-304">This change differentiates and associates setting data with replication relationship.</span></span>



| <span data-ttu-id="23673-305">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="23673-305">Property name</span></span>  | <span data-ttu-id="23673-306">Windows 8-Wert</span><span class="sxs-lookup"><span data-stu-id="23673-306">Windows 8 value</span></span>               | <span data-ttu-id="23673-307">Windows 8.1 Wert</span><span class="sxs-lookup"><span data-stu-id="23673-307">Windows 8.1 value</span></span>                          |
|----------------|-------------------------------|--------------------------------------------|
| <span data-ttu-id="23673-308">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="23673-308">**InstanceID**</span></span> | <span data-ttu-id="23673-309">Microsoft: <vmguid> \\ HVR</span><span class="sxs-lookup"><span data-stu-id="23673-309">Microsoft:<vmguid>\\HVR</span></span> | <span data-ttu-id="23673-310">Microsoft: <vmguid> \\ HVR \\<0/1></span><span class="sxs-lookup"><span data-stu-id="23673-310">Microsoft:<vmguid>\\HVR\\<0/1></span></span> |



 

<span data-ttu-id="23673-311">Im Windows 8.1 Wert gibt 0 den primär Wert und 1 die erweiterte Replikation an.</span><span class="sxs-lookup"><span data-stu-id="23673-311">In the Windows 8.1 value, 0 indicates primary and 1 indicates extended replication.</span></span> <span data-ttu-id="23673-312">Weitere Informationen zur erweiterten Replikation finden Sie unter [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md).</span><span class="sxs-lookup"><span data-stu-id="23673-312">For more info about extended replication, see [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).</span></span>

</dd> <dt>

<span data-ttu-id="23673-313">**Lastapplicationkonsistentreplicationtime**</span><span class="sxs-lookup"><span data-stu-id="23673-313">**LastApplicationConsistentReplicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-314">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="23673-314">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="23673-315">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23673-316">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md).**Lastapplicationkonsistentreplicationtime**")</span><span class="sxs-lookup"><span data-stu-id="23673-316">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**LastApplicationConsistentReplicationTime**")</span></span>
</dt> </dl>

<span data-ttu-id="23673-317">Der Zeitpunkt, zu dem die letzte Anwendungs konsistente Replikation für den virtuellen Computer empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="23673-317">The time at which the last application-consistent replication was received for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="23673-318">Diese Eigenschaft ist ab Windows 8.1 veraltet. Verwenden Sie stattdessen die-Eigenschaft mit demselben Namen in der [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md) -Klasse, um den Wert für die primäre oder erweiterte Beziehung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="23673-318">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

</dd> <dt>

<span data-ttu-id="23673-319">**Lastreplicationtime**</span><span class="sxs-lookup"><span data-stu-id="23673-319">**LastReplicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-320">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="23673-320">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="23673-321">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23673-322">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md).**Lastreplicationtime**")</span><span class="sxs-lookup"><span data-stu-id="23673-322">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationTime**")</span></span>
</dt> </dl>

<span data-ttu-id="23673-323">Der Zeitpunkt, zu dem die letzte Replikation bei der Wiederherstellung für den virtuellen Computer empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="23673-323">The time at which the last replication is received on recovery for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="23673-324">Diese Eigenschaft ist ab Windows 8.1 veraltet. Verwenden Sie stattdessen die-Eigenschaft mit demselben Namen in der [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md) -Klasse, um den Wert für die primäre oder erweiterte Beziehung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="23673-324">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

</dd> <dt>

<span data-ttu-id="23673-325">**Lastreplicationtype**</span><span class="sxs-lookup"><span data-stu-id="23673-325">**LastReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-326">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23673-326">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23673-327">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23673-328">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md).**Lastreplicationtype**")</span><span class="sxs-lookup"><span data-stu-id="23673-328">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationType**")</span></span>
</dt> </dl>

<span data-ttu-id="23673-329">Der Typ der letzten Replikation, die für den virtuellen Computer empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="23673-329">The type of the last replication that was received for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="23673-330">Diese Eigenschaft ist ab Windows 8.1 veraltet. Verwenden Sie stattdessen die-Eigenschaft mit demselben Namen in der [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md) -Klasse, um den Wert für die primäre oder erweiterte Beziehung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="23673-330">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

<span data-ttu-id="23673-331">Dabei sind folgende Werte möglich:</span><span class="sxs-lookup"><span data-stu-id="23673-331">Possible values are:</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="23673-332">**Keine** (0)</span><span class="sxs-lookup"><span data-stu-id="23673-332">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="23673-333">**Regulär** (1)</span><span class="sxs-lookup"><span data-stu-id="23673-333">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="23673-334">**Anwendungs konsistent** (2)</span><span class="sxs-lookup"><span data-stu-id="23673-334">**Application consistent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="23673-335">**Geplant** (3)</span><span class="sxs-lookup"><span data-stu-id="23673-335">**Planned** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="23673-336">**Lasterfolgreicher BackupTime**</span><span class="sxs-lookup"><span data-stu-id="23673-336">**LastSuccessfulBackupTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-337">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="23673-337">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="23673-338">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-339">Der Zeitpunkt, zu dem die letzte erfolgreiche Sicherung für den virtuellen Computer abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="23673-339">The time at which the last successful backup has completed for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="23673-340">**Name**</span><span class="sxs-lookup"><span data-stu-id="23673-340">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-341">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="23673-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23673-342">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-343">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="23673-343">The label by which the object is known.</span></span> <span data-ttu-id="23673-344">Diese Eigenschaft wird vom [**CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system)geerbt und ist immer auf "*GUID*" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="23673-344">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to "*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="23673-345">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="23673-345">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-346">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="23673-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23673-347">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-348">Eine Zeichenfolge, die angibt, wie der Systemname mithilfe der Unterklasse heuristic generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="23673-348">A string that identifies how the system name was generated, using the subclass heuristic.</span></span> <span data-ttu-id="23673-349">Diese Eigenschaft wird von [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="23673-349">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="23673-350">**NumberOfNumaNodes**</span><span class="sxs-lookup"><span data-stu-id="23673-350">**NumberOfNumaNodes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-351">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23673-351">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23673-352">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-353">Die Anzahl der NUMA-Knoten (nicht einheitlicher Speicherzugriff) des Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="23673-353">The number of nonuniform memory access (NUMA) nodes of the computer system.</span></span> <span data-ttu-id="23673-354">Wenn **MSVM \_ Computersystem** das hostingcomputersystem darstellt, enthält diese Eigenschaft die Anzahl der physischen NUMA-Knoten.</span><span class="sxs-lookup"><span data-stu-id="23673-354">When **Msvm\_ComputerSystem** represents the hosting computer system, this property contains the count of physical NUMA nodes.</span></span> <span data-ttu-id="23673-355">Wenn **MSVM \_ Computersystem** einen virtuellen Computer darstellt, enthält diese Eigenschaft die Anzahl der virtuellen NUMA-Knoten, die dem Gast Betriebssystem über die ACPI-SRAT (System Resource Affinitäts Tabelle) angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="23673-355">When **Msvm\_ComputerSystem** represents a virtual machine, this property contains the number of virtual NUMA nodes that are presented to the guest operating system through the ACPI System Resource Affinity Table (SRAT).</span></span>

</dd> <dt>

<span data-ttu-id="23673-356">**Ontimeinmilliseconds**</span><span class="sxs-lookup"><span data-stu-id="23673-356">**OnTimeInMilliseconds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-357">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="23673-357">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="23673-358">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23673-359">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Millisekunden")</span><span class="sxs-lookup"><span data-stu-id="23673-359">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds")</span></span>
</dt> </dl>

<span data-ttu-id="23673-360">Für den virtuellen Computer gibt diese Eigenschaft die Zeit in Millisekunden an, seit der Computer zuletzt eingeschaltet, zurückgesetzt oder wieder hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="23673-360">For the virtual machine, this property indicates the time, in milliseconds, since the machine was last turned on, reset, or restored.</span></span> <span data-ttu-id="23673-361">Diese Zeit schließt die Zeit aus, zu der sich der virtuelle Computer im angehaltenen Zustand befunden hat.</span><span class="sxs-lookup"><span data-stu-id="23673-361">This time excludes the time the virtual machine was in the paused state.</span></span> <span data-ttu-id="23673-362">Für das Verwaltungs Betriebssystem wird diese Eigenschaft auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="23673-362">For the management operating system, this property is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="23673-363">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="23673-363">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-364">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23673-364">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23673-365">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-366">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="23673-366">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="23673-367">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="23673-367">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="23673-368">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="23673-368">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="23673-369">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="23673-369">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-370">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="23673-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="23673-371">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-372">Ein Array, das die aktuellen Status des-Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="23673-372">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="23673-373">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="23673-373">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span> <span data-ttu-id="23673-374">Der Wert bei Index NULL (0) ist einer der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="23673-374">The value at index zero (0) is one of the following values.</span></span>



| <span data-ttu-id="23673-375">Wert</span><span class="sxs-lookup"><span data-stu-id="23673-375">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="23673-376">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="23673-376">Meaning</span></span>                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="23673-377"><dt>**OK**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="23673-377"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                      | <span data-ttu-id="23673-378">Der virtuelle Computer ist funktionsfähig und funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="23673-378">The virtual machine is functional and operating normally.</span></span><br/>                                                                                                                                                                                              |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="23673-379"><dt></dt> Heruntergestuft <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="23673-379"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                         | <span data-ttu-id="23673-380">Der virtuelle Computer ist nur teilweise funktionsfähig.</span><span class="sxs-lookup"><span data-stu-id="23673-380">The virtual machine is only partially functional.</span></span> <span data-ttu-id="23673-381">Dies gibt an, dass auf den Speicher, der die Konfiguration enthält, nicht zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="23673-381">This indicates that the storage that contains the configuration is not accessible.</span></span> <span data-ttu-id="23673-382">Ein virtueller Computer in diesem Zustand kann nur ausgeschaltet oder gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="23673-382">A virtual machine in this state can only be turned off or deleted.</span></span> <br/>                                               |
| <span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span><dl> <span data-ttu-id="23673-383"><dt>**Vorhersagefehler**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="23673-383"><dt>**Predictive Failure**</dt> <dt>5</dt></span></span> </dl> | <span data-ttu-id="23673-384">Der virtuelle Computer ist funktionsfähig, kann aber in Zukunft fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="23673-384">The virtual machine is functional but may fail in the future.</span></span> <span data-ttu-id="23673-385">Dies deutet darauf hin, dass der Speicherplatz im Speicher, der die virtuelle Festplatte des virtuellen Computers enthält, nicht mehr verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="23673-385">This indicates that the storage that contains the virtual machine's virtual hard disk is low on free space.</span></span> <span data-ttu-id="23673-386">Der virtuelle Computer wird angehalten, wenn kein Speicherplatz mehr verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="23673-386">The virtual machine will be paused if more disk space is not made available.</span></span><br/> |
| <span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span><dl> <span data-ttu-id="23673-387"><dt></dt> <dt>10</dt> beendet</span><span class="sxs-lookup"><span data-stu-id="23673-387"><dt>**Stopped**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="23673-388">Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="23673-388">This value is not supported.</span></span> <span data-ttu-id="23673-389">Wenn der virtuelle Computer beendet wird, hat die **enabledstate** -Eigenschaft den Wert 3 (deaktiviert).</span><span class="sxs-lookup"><span data-stu-id="23673-389">If the virtual machine is stopped, the **EnabledState** property will have a value of 3 (Disabled).</span></span><br/>                                                                                                                       |
| <span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span><dl> <span data-ttu-id="23673-390"><dt>**In Dienst**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="23673-390"><dt>**In Service**</dt> <dt>11</dt></span></span> </dl>                                | <span data-ttu-id="23673-391">Die virtuelle Maschine verarbeitet eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="23673-391">The virtual machine is processing a request.</span></span><br/>                                                                                                                                                                                                           |
| <span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span><dl> <span data-ttu-id="23673-392"><dt>**Ruhender**</dt> <dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="23673-392"><dt>**Dormant**</dt> <dt>15</dt></span></span> </dl>                                            | <span data-ttu-id="23673-393">Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="23673-393">This value is not supported.</span></span> <span data-ttu-id="23673-394">Wenn die virtuelle Maschine angehalten oder angehalten wird, hat die **enabledstate** -Eigenschaft den Wert 32769 (angehalten) oder 32768 (angehalten).</span><span class="sxs-lookup"><span data-stu-id="23673-394">If the virtual machine is suspended or paused, the **EnabledState** property will have a value of 32769 (Suspended) or 32768 (Paused).</span></span><br/>                                                                                    |



 

<span data-ttu-id="23673-395">Der Wert bei Index eins (1) ist optional und enthält sekundäre Statusinformationen.</span><span class="sxs-lookup"><span data-stu-id="23673-395">The value at index one (1) is optional and contains secondary status information.</span></span> <span data-ttu-id="23673-396">Ein Client sollte den primären Status von Index 0 (null) verwenden, um zu bestimmen, ob eine neue Anforderung an den virtuellen Computer ausgegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="23673-396">A client should use the primary status from index zero (0) to determine whether a new request can be issued to the virtual machine.</span></span> <span data-ttu-id="23673-397">Wenn **OperationalStatus** \[ 0 \] den Wert 2 (OK) hat, kann der von **OperationalStatus** 1 festgestellte Vorgang \[ \] unterbrochen werden.</span><span class="sxs-lookup"><span data-stu-id="23673-397">If **OperationalStatus**\[0\] is 2 (OK), then the operation indicated by **OperationalStatus**\[1\] can be interrupted.</span></span>

<span data-ttu-id="23673-398">Der Wert für **OperationalStatus** \[ 1 \] ist einer der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="23673-398">The value at **OperationalStatus**\[1\] is one of the following values.</span></span>



| <span data-ttu-id="23673-399">Wert</span><span class="sxs-lookup"><span data-stu-id="23673-399">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="23673-400">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="23673-400">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Creating_Snapshot"></span><span id="creating_snapshot"></span><span id="CREATING_SNAPSHOT"></span><dl> <span data-ttu-id="23673-401"><dt>**Erstellen der Momentaufnahme**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="23673-401"><dt>**Creating Snapshot**</dt> <dt>32768</dt></span></span> </dl>                                 | <span data-ttu-id="23673-402">Für den virtuellen Computer wird gerade eine Momentaufnahme erstellt.</span><span class="sxs-lookup"><span data-stu-id="23673-402">A snapshot is in the process of being created for the virtual machine.</span></span><br/>             |
| <span id="Applying_Snapshot"></span><span id="applying_snapshot"></span><span id="APPLYING_SNAPSHOT"></span><dl> <span data-ttu-id="23673-403"><dt>**Anwenden der Momentaufnahme**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="23673-403"><dt>**Applying Snapshot**</dt> <dt>32769</dt></span></span> </dl>                                 | <span data-ttu-id="23673-404">Eine Momentaufnahme wird gerade auf den virtuellen Computer angewendet.</span><span class="sxs-lookup"><span data-stu-id="23673-404">A snapshot is in the process of being applied to the virtual machine.</span></span><br/>              |
| <span id="Deleting_Snapshot"></span><span id="deleting_snapshot"></span><span id="DELETING_SNAPSHOT"></span><dl> <span data-ttu-id="23673-405"><dt>**Momentaufnahme**</dt> <dt>32770</dt> wird gelöscht</span><span class="sxs-lookup"><span data-stu-id="23673-405"><dt>**Deleting Snapshot**</dt> <dt>32770</dt></span></span> </dl>                                 | <span data-ttu-id="23673-406">Eine Momentaufnahme wird gerade vom virtuellen Computer gelöscht.</span><span class="sxs-lookup"><span data-stu-id="23673-406">A snapshot is in the process of being deleted from the virtual machine.</span></span><br/>            |
| <span id="Waiting_to_Start"></span><span id="waiting_to_start"></span><span id="WAITING_TO_START"></span><dl> <span data-ttu-id="23673-407"><dt>**Warten auf Start**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="23673-407"><dt>**Waiting to Start**</dt> <dt>32771</dt></span></span> </dl>                                     | <span data-ttu-id="23673-408">Der virtuelle Computer wird gestartet, nachdem die automatische Startverzögerung abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="23673-408">The virtual machine will be started after the automatic startup delay has elapsed.</span></span><br/> |
| <span id="Merging_Disks"></span><span id="merging_disks"></span><span id="MERGING_DISKS"></span><dl> <span data-ttu-id="23673-409"><dt></dt> Zusammenführen von Datenträgern <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="23673-409"><dt>**Merging Disks**</dt> <dt>32772</dt></span></span> </dl>                                                 | <span data-ttu-id="23673-410">Virtuelle Festplatten aus zuvor gelöschten Momentaufnahmen werden zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="23673-410">Virtual hard disks from previously deleted snapshots are being merged.</span></span><br/>             |
| <span id="Exporting_Virtual_Machine"></span><span id="exporting_virtual_machine"></span><span id="EXPORTING_VIRTUAL_MACHINE"></span><dl> <span data-ttu-id="23673-411"><dt>**Virtueller Computer wird exportiert**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="23673-411"><dt>**Exporting Virtual Machine**</dt> <dt>32773</dt></span></span> </dl> | <span data-ttu-id="23673-412">Der virtuelle Computer wird exportiert.</span><span class="sxs-lookup"><span data-stu-id="23673-412">The virtual machine is being exported.</span></span><br/>                                             |
| <span id="Migrating_Virtual_Machine"></span><span id="migrating_virtual_machine"></span><span id="MIGRATING_VIRTUAL_MACHINE"></span><dl> <span data-ttu-id="23673-413"><dt>**Virtuelle Maschine**</dt> <dt>32774</dt> wird migriert.</span><span class="sxs-lookup"><span data-stu-id="23673-413"><dt>**Migrating Virtual Machine**</dt> <dt>32774</dt></span></span> </dl> | <span data-ttu-id="23673-414">Der virtuelle Computer wird Live von einem physischen Computer zu einem anderen migriert.</span><span class="sxs-lookup"><span data-stu-id="23673-414">The virtual machine is being migrated live from one physical computer to another.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="23673-415">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="23673-415">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-416">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="23673-416">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="23673-417">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-417">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-418">Eine Zeichenfolge, die beschreibt, wie oder warum das System dediziert ist, wenn das **dedizierte** Array den Wert 2 (Sonstiges) enthält.</span><span class="sxs-lookup"><span data-stu-id="23673-418">A string that describes how or why the system is dedicated when the **Dedicated** array includes the value 2 (Other).</span></span> <span data-ttu-id="23673-419">Diese Eigenschaft wird von [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="23673-419">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="23673-420">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="23673-420">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-421">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="23673-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23673-422">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-423">Der aktivierte oder deaktivierte Status der virtuellen Maschine, wenn die **enabledstate** -Eigenschaft auf 1 (sonstige) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="23673-423">The enabled or disabled state of the virtual machine when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="23673-424">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="23673-424">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="23673-425">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="23673-425">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="23673-426">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="23673-426">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-427">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="23673-427">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="23673-428">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-429">Diese Eigenschaft wird von [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="23673-429">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="23673-430">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="23673-430">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-431">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="23673-431">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="23673-432">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-433">Diese Eigenschaft wird von [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="23673-433">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="23673-434">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="23673-434">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-435">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="23673-435">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23673-436">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-437">Eine Zeichenfolge, die angibt, wie der primäre Systembesitzer erreicht werden kann (z. b. eine Telefonnummer oder eine e-Mail-Adresse).</span><span class="sxs-lookup"><span data-stu-id="23673-437">A string that indicates how the primary system owner can be reached (for example, a phone number or an email address).</span></span> <span data-ttu-id="23673-438">Diese Eigenschaft wird vom [**CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="23673-438">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="23673-439">**Primaryownername**</span><span class="sxs-lookup"><span data-stu-id="23673-439">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-440">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="23673-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23673-441">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-442">Der Name des primären System Besitzers.</span><span class="sxs-lookup"><span data-stu-id="23673-442">The name of the primary system owner.</span></span> <span data-ttu-id="23673-443">Diese Eigenschaft wird vom [**CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="23673-443">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="23673-444">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="23673-444">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-445">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23673-445">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23673-446">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-447">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="23673-447">Provides high level status information.</span></span> <span data-ttu-id="23673-448">Diese Eigenschaft sollte in Verbindung mit der **detailedstatus** -Eigenschaft verwendet werden, um allgemeine und ausführliche Integritäts Statusinformationen für das-Element und seine unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="23673-448">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="23673-449">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="23673-449">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="23673-450">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="23673-450">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="23673-451">**ProcessID**</span><span class="sxs-lookup"><span data-stu-id="23673-451">**ProcessID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-452">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="23673-452">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="23673-453">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-453">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-454">Der Bezeichner des Prozesses, unter dem dieser virtuelle Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="23673-454">The identifier of the process under which this virtual machine is running.</span></span> <span data-ttu-id="23673-455">Dieser Wert kann verwendet werden, um die Instanz von Vmwp.exe auf dem System, auf dem der virtuelle Computer ausgeführt wird, eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="23673-455">This value can be used to uniquely identify the instance of Vmwp.exe on the system that is running the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="23673-456">**ReplicationHealth**</span><span class="sxs-lookup"><span data-stu-id="23673-456">**ReplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-457">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23673-457">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23673-458">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23673-459">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md).**ReplicationHealth**")</span><span class="sxs-lookup"><span data-stu-id="23673-459">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationHealth**")</span></span>
</dt> </dl>

<span data-ttu-id="23673-460">Die Replikations Integrität für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="23673-460">The replication health for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="23673-461">Diese Eigenschaft ist ab Windows 8.1 veraltet. Verwenden Sie stattdessen die-Eigenschaft mit demselben Namen in der [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md) -Klasse, um den Wert für die primäre oder erweiterte Beziehung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="23673-461">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

<span data-ttu-id="23673-462">Dabei sind folgende Werte möglich:</span><span class="sxs-lookup"><span data-stu-id="23673-462">Possible values are:</span></span>

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="23673-463">**Nicht zutreffend** (0)</span><span class="sxs-lookup"><span data-stu-id="23673-463">**Not applicable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

<span data-ttu-id="23673-464">**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="23673-464">**Ok** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="23673-465">**Warnung** (2)</span><span class="sxs-lookup"><span data-stu-id="23673-465">**Warning** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="23673-466">**Kritisch** (3)</span><span class="sxs-lookup"><span data-stu-id="23673-466">**Critical** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="23673-467">**ReplicationMode**</span><span class="sxs-lookup"><span data-stu-id="23673-467">**ReplicationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-468">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23673-468">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23673-469">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-470">Gibt den Replikations Modus für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="23673-470">Specifies the replication mode for the virtual machine.</span></span> <span data-ttu-id="23673-471">Dabei handelt es sich um einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="23673-471">This will be one of the following values.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="23673-472"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Keine** (0)</span><span class="sxs-lookup"><span data-stu-id="23673-472"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="23673-473"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primär** (1)</span><span class="sxs-lookup"><span data-stu-id="23673-473"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primary** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

<span data-ttu-id="23673-474"><span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>**Replikat** (2)</span><span class="sxs-lookup"><span data-stu-id="23673-474"><span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>**Replica** (2)</span></span>


</dt> <dd>

<span data-ttu-id="23673-475">Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="23673-475">Recovery</span></span>

</dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

<span data-ttu-id="23673-476"><span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>**Test Replikat** (3)</span><span class="sxs-lookup"><span data-stu-id="23673-476"><span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>**Test Replica** (3)</span></span>


</dt> <dd>

<span data-ttu-id="23673-477">Replikat</span><span class="sxs-lookup"><span data-stu-id="23673-477">Replica</span></span>

</dd> <dt>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>

<span data-ttu-id="23673-478"><span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>**Erweitertes Replikat** (4)</span><span class="sxs-lookup"><span data-stu-id="23673-478"><span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>**Extended Replica** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="23673-479">**ReplicationState**</span><span class="sxs-lookup"><span data-stu-id="23673-479">**ReplicationState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-480">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23673-480">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23673-481">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23673-482">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md).**Replicationstate**")</span><span class="sxs-lookup"><span data-stu-id="23673-482">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationState**")</span></span>
</dt> </dl>

<span data-ttu-id="23673-483">Der Replikations Status für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="23673-483">The replication state for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="23673-484">Diese Eigenschaft ist ab Windows 8.1 veraltet. Verwenden Sie stattdessen die-Eigenschaft mit demselben Namen in der [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md) -Klasse, um den Wert für die primäre oder erweiterte Beziehung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="23673-484">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

<span data-ttu-id="23673-485">Dabei sind folgende Werte möglich:</span><span class="sxs-lookup"><span data-stu-id="23673-485">Possible values are:</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="23673-486">**Deaktiviert** (0)</span><span class="sxs-lookup"><span data-stu-id="23673-486">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="23673-487">**Bereit für Replikation** (1)</span><span class="sxs-lookup"><span data-stu-id="23673-487">**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="23673-488">**Warten auf Abschluss der ersten Replikation** (2)</span><span class="sxs-lookup"><span data-stu-id="23673-488">**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="23673-489">**Replizieren** (3)</span><span class="sxs-lookup"><span data-stu-id="23673-489">**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="23673-490">**Synchronisierungs Replikation beendet** (4)</span><span class="sxs-lookup"><span data-stu-id="23673-490">**Synced replication complete** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="23673-491">**Wieder hergestellt** (5)</span><span class="sxs-lookup"><span data-stu-id="23673-491">**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="23673-492">Commit **ausgeführt (6** )</span><span class="sxs-lookup"><span data-stu-id="23673-492">**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="23673-493">Angeh **alten (7** )</span><span class="sxs-lookup"><span data-stu-id="23673-493">**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="23673-494">**Kritisch** (8)</span><span class="sxs-lookup"><span data-stu-id="23673-494">**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="23673-495">**Warten auf den Start der erneuten Synchronisierung** (9)</span><span class="sxs-lookup"><span data-stu-id="23673-495">**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="23673-496">**Neusynchronisierung** (10)</span><span class="sxs-lookup"><span data-stu-id="23673-496">**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span data-ttu-id="23673-497">**Neusynchronisierung** angehalten (11)</span><span class="sxs-lookup"><span data-stu-id="23673-497">**Resynchronization suspended** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span data-ttu-id="23673-498">**Failover** wird ausgeführt (12)</span><span class="sxs-lookup"><span data-stu-id="23673-498">**Failover in progress** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

<span data-ttu-id="23673-499">**Failback** wird ausgeführt (13)</span><span class="sxs-lookup"><span data-stu-id="23673-499">**Failback in progress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

<span data-ttu-id="23673-500">**Failback ist beendet** (14)</span><span class="sxs-lookup"><span data-stu-id="23673-500">**Failback complete** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="23673-501">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="23673-501">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-502">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23673-502">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23673-503">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-503">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-504">Der zuletzt angeforderte oder gewünschte Status für den virtuellen Computer, der an die [**requestStateChange**](requeststatechange-msvm-computersystem.md) -Methode weitergegeben wird, oder 12 (nicht zutreffend), wenn keine Zustandsänderung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="23673-504">The last requested or desired state for the virtual machine as passed to the [**RequestStateChange**](requeststatechange-msvm-computersystem.md) method, or 12 (Not Applicable) if no state change is in progress.</span></span> <span data-ttu-id="23673-505">Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="23673-505">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="23673-506">Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuell aktivierten oder deaktivierten Zustände zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="23673-506">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="23673-507">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="23673-507">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="23673-508">**Resetcapability**</span><span class="sxs-lookup"><span data-stu-id="23673-508">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-509">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23673-509">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23673-510">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-510">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-511">Diese Eigenschaft wird von [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)geerbt und ist immer auf 1 (sonstige) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="23673-511">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="23673-512">**Rollen**</span><span class="sxs-lookup"><span data-stu-id="23673-512">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-513">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="23673-513">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="23673-514">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-515">Ein Array von Zeichen folgen, das die Rollen beschreibt, die das System in der Informationstechnologie Umgebung spielt.</span><span class="sxs-lookup"><span data-stu-id="23673-515">An array of strings that describe the roles the system plays in the information technology environment.</span></span> <span data-ttu-id="23673-516">Diese Eigenschaft wird vom [**CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="23673-516">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="23673-517">**Status**</span><span class="sxs-lookup"><span data-stu-id="23673-517">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-518">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="23673-518">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23673-519">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-520">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="23673-520">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="23673-521">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="23673-521">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-522">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="23673-522">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="23673-523">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-523">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23673-524">Qualifizierer: **arrayType** ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="23673-524">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="23673-525">Ein Array, das Zeichen folgen enthält, die die entsprechenden **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="23673-525">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="23673-526">Wenn z. b. 11 (in Service) der Wert ist, der **OperationalStatus** \[ 0 zugewiesen ist \] , enthält **Statusbeschreibungen** \[ 0 \] möglicherweise eine Erläuterung, warum der virtuelle Computer eine Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="23673-526">For example, if 11 (In Service) is the value assigned to **OperationalStatus**\[0\], then **StatusDescriptions**\[0\] may contain an explanation as to why the virtual machine is processing a request.</span></span> <span data-ttu-id="23673-527">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="23673-527">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="23673-528">**Timeoflastconfigurationchange**</span><span class="sxs-lookup"><span data-stu-id="23673-528">**TimeOfLastConfigurationChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-529">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="23673-529">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="23673-530">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-530">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-531">Das Datum und die Uhrzeit der letzten Änderung der Konfigurationsdatei des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="23673-531">The date and time when the virtual machine configuration file was last modified.</span></span> <span data-ttu-id="23673-532">Die Konfigurationsdatei wird bei bestimmten virtuellen Maschinen Vorgängen geändert, sowie beim Hinzufügen, ändern oder Entfernen von virtuellen Computern oder Geräteeinstellungen.</span><span class="sxs-lookup"><span data-stu-id="23673-532">The configuration file is modified during certain virtual machine operations, as well as when any of the virtual machine or device settings are added, modified, or removed.</span></span>

</dd> <dt>

<span data-ttu-id="23673-533">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="23673-533">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-534">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="23673-534">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="23673-535">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-535">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-536">Das Datum und die Uhrzeit der letzten Änderung des aktivierten Zustands des Elements.</span><span class="sxs-lookup"><span data-stu-id="23673-536">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="23673-537">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="23673-537">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="23673-538">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="23673-538">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23673-539">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23673-539">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23673-540">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23673-540">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23673-541">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="23673-541">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="23673-542">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="23673-542">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23673-543">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23673-543">Remarks</span></span>

<span data-ttu-id="23673-544">Die folgende Abbildung zeigt die **enabledstate** -Werte.</span><span class="sxs-lookup"><span data-stu-id="23673-544">The following illustration shows the **EnabledState** values.</span></span>

![Zustandsdiagramm für enabledstate-Werte für Windows Server 2008 R2](images/msvm-computersystem-enabledstate-win2008r2.png)

<span data-ttu-id="23673-546">Wenn sich eine Eigenschaft der **MSVM \_ Computersystem** -Klasse ändert, gibt der WMI-Anbieter ein [**\_ \_ instancemodificationevent**](/windows/desktop/WmiSdk/--instancemodificationevent) -Ereignis an, das die Änderungen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="23673-546">When a property of the **Msvm\_ComputerSystem** class changes, the WMI provider indicates an [**\_\_InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) event that describes the changes.</span></span> <span data-ttu-id="23673-547">Der vorherige Zustand ist in der Eigenschaft **PreviousInstance** enthalten, und der neue Zustand ist in der Eigenschaft **TargetInstance** enthalten.</span><span class="sxs-lookup"><span data-stu-id="23673-547">The previous state is contained in the **PreviousInstance** property, and the new state is contained in the **TargetInstance** property.</span></span> <span data-ttu-id="23673-548">Dieses Ereignis ist asynchron. Wenn das **\_ \_ instancemodificationevent** -Ereignis verarbeitet wird, spiegelt die **TargetInstance** -Eigenschaft möglicherweise nicht den aktuellen Zustand wider.</span><span class="sxs-lookup"><span data-stu-id="23673-548">This event is asynchronous; by the time the **\_\_InstanceModificationEvent** event is processed, the **TargetInstance** property may not reflect the current state.</span></span>

<span data-ttu-id="23673-549">Der Zugriff auf die **MSVM \_ Computersystem** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="23673-549">Access to the **Msvm\_ComputerSystem** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="23673-550">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="23673-550">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="23673-551">Beispiele</span><span class="sxs-lookup"><span data-stu-id="23673-551">Examples</span></span>

<span data-ttu-id="23673-552">Weitere Informationen finden Sie unter [Abfragen von Netzwerk Objekten](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="23673-552">See [Querying Networking Objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="23673-553">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23673-553">Requirements</span></span>



| <span data-ttu-id="23673-554">Anforderung</span><span class="sxs-lookup"><span data-stu-id="23673-554">Requirement</span></span> | <span data-ttu-id="23673-555">Wert</span><span class="sxs-lookup"><span data-stu-id="23673-555">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23673-556">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="23673-556">Minimum supported client</span></span><br/> | <span data-ttu-id="23673-557">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="23673-557">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="23673-558">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="23673-558">Minimum supported server</span></span><br/> | <span data-ttu-id="23673-559">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="23673-559">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="23673-560">Namespace</span><span class="sxs-lookup"><span data-stu-id="23673-560">Namespace</span></span><br/>                | <span data-ttu-id="23673-561">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="23673-561">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="23673-562">MOF</span><span class="sxs-lookup"><span data-stu-id="23673-562">MOF</span></span><br/>                      | <dl> <span data-ttu-id="23673-563"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="23673-563"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="23673-564">DLL</span><span class="sxs-lookup"><span data-stu-id="23673-564">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23673-565"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="23673-565"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="23673-566">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23673-566">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23673-567">**CIM- \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="23673-567">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> <dt>

[<span data-ttu-id="23673-568">**\_\_Instancemodificationevent**</span><span class="sxs-lookup"><span data-stu-id="23673-568">**\_\_InstanceModificationEvent**</span></span>](/windows/desktop/WmiSdk/--instancemodificationevent)
</dt> <dt>

[<span data-ttu-id="23673-569">**CIM- \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="23673-569">**CIM\_ComputerSystem**</span></span>](/windows/desktop/CIMWin32Prov/cim-computersystem)
</dt> <dt>

[<span data-ttu-id="23673-570">**MSVM \_ Computersystem (v1)**</span><span class="sxs-lookup"><span data-stu-id="23673-570">**Msvm\_ComputerSystem (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-computersystem)
</dt> <dt>

[<span data-ttu-id="23673-571">Klassen des virtuellen Systems</span><span class="sxs-lookup"><span data-stu-id="23673-571">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

