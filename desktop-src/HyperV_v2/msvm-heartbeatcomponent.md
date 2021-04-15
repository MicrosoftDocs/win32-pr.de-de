---
description: Stellt den Status des Takt diensdienstankts dar, der für die Überwachung des Zustands einer virtuellen Maschine zuständig ist, indem ein Takt in regelmäßigen Abständen gemeldet wird.
ms.assetid: 72DB3CD9-B083-4483-BCCD-DC8C140DDBF4
title: Msvm_HeartbeatComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HeartbeatComponent
- Msvm_HeartbeatComponent.SetPowerState
- Msvm_HeartbeatComponent.EnableDevice
- Msvm_HeartbeatComponent.OnlineDevice
- Msvm_HeartbeatComponent.QuiesceDevice
- Msvm_HeartbeatComponent.SaveProperties
- Msvm_HeartbeatComponent.RestoreProperties
- Msvm_HeartbeatComponent.InstanceID
- Msvm_HeartbeatComponent.Caption
- Msvm_HeartbeatComponent.Description
- Msvm_HeartbeatComponent.ElementName
- Msvm_HeartbeatComponent.InstallDate
- Msvm_HeartbeatComponent.Name
- Msvm_HeartbeatComponent.OperationalStatus
- Msvm_HeartbeatComponent.StatusDescriptions
- Msvm_HeartbeatComponent.Status
- Msvm_HeartbeatComponent.HealthState
- Msvm_HeartbeatComponent.CommunicationStatus
- Msvm_HeartbeatComponent.DetailedStatus
- Msvm_HeartbeatComponent.OperatingStatus
- Msvm_HeartbeatComponent.PrimaryStatus
- Msvm_HeartbeatComponent.EnabledState
- Msvm_HeartbeatComponent.OtherEnabledState
- Msvm_HeartbeatComponent.RequestedState
- Msvm_HeartbeatComponent.EnabledDefault
- Msvm_HeartbeatComponent.TimeOfLastStateChange
- Msvm_HeartbeatComponent.AvailableRequestedStates
- Msvm_HeartbeatComponent.TransitioningToState
- Msvm_HeartbeatComponent.SystemCreationClassName
- Msvm_HeartbeatComponent.SystemName
- Msvm_HeartbeatComponent.CreationClassName
- Msvm_HeartbeatComponent.DeviceID
- Msvm_HeartbeatComponent.PowerManagementSupported
- Msvm_HeartbeatComponent.PowerManagementCapabilities
- Msvm_HeartbeatComponent.Availability
- Msvm_HeartbeatComponent.StatusInfo
- Msvm_HeartbeatComponent.LastErrorCode
- Msvm_HeartbeatComponent.ErrorDescription
- Msvm_HeartbeatComponent.ErrorCleared
- Msvm_HeartbeatComponent.OtherIdentifyingInfo
- Msvm_HeartbeatComponent.PowerOnHours
- Msvm_HeartbeatComponent.TotalPowerOnHours
- Msvm_HeartbeatComponent.IdentifyingDescriptions
- Msvm_HeartbeatComponent.AdditionalAvailability
- Msvm_HeartbeatComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 61a3efaba52c2e592f405e1b95f1c62568a59229
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525229"
---
# <a name="msvm_heartbeatcomponent-class"></a><span data-ttu-id="d454b-103">MSVM- \_ Klasse "heartbeatcomponent"</span><span class="sxs-lookup"><span data-stu-id="d454b-103">Msvm\_HeartbeatComponent class</span></span>

<span data-ttu-id="d454b-104">Stellt den Status des Takt diensdienstankts dar, der für die Überwachung des Zustands einer virtuellen Maschine zuständig ist, indem ein Takt in regelmäßigen Abständen gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="d454b-104">Represents the state of the heartbeat service, which is responsible for monitoring the state of a virtual machine by reporting a heartbeat at regular intervals.</span></span>

<span data-ttu-id="d454b-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d454b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d454b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d454b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HeartbeatComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "Heartbeat";
  string   Description = "Microsoft Heartbeat Service";
  string   ElementName = "Heartbeat";
  datetime InstallDate;
  string   Name;
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
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 7;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_HeartbeatComponent";
  string   DeviceID = "Microsoft:VMGUID\GUID";
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
};
```

## <a name="members"></a><span data-ttu-id="d454b-107">Member</span><span class="sxs-lookup"><span data-stu-id="d454b-107">Members</span></span>

<span data-ttu-id="d454b-108">Die **MSVM-Klasse " \_ heartbeatcomponent** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d454b-108">The **Msvm\_HeartbeatComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="d454b-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="d454b-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="d454b-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d454b-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d454b-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="d454b-111">Methods</span></span>

<span data-ttu-id="d454b-112">Die **MSVM-Klasse " \_ heartbeatcomponent** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="d454b-112">The **Msvm\_HeartbeatComponent** class has these methods.</span></span>



| <span data-ttu-id="d454b-113">Methode</span><span class="sxs-lookup"><span data-stu-id="d454b-113">Method</span></span>                                                                   | <span data-ttu-id="d454b-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d454b-114">Description</span></span>                              |
|:-------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="d454b-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="d454b-115">**EnableDevice**</span></span>                                                         | <span data-ttu-id="d454b-116">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d454b-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d454b-117">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="d454b-117">**OnlineDevice**</span></span>                                                         | <span data-ttu-id="d454b-118">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d454b-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d454b-119">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="d454b-119">**QuiesceDevice**</span></span>                                                        | <span data-ttu-id="d454b-120">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d454b-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="d454b-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="d454b-121">**RequestStateChange**</span></span>](msvm-heartbeatcomponent-requeststatechange.md) | <span data-ttu-id="d454b-122">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="d454b-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="d454b-123">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="d454b-123">**Reset**</span></span>](msvm-heartbeatcomponent-reset.md)                           | <span data-ttu-id="d454b-124">Setzt das virtuelle Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="d454b-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="d454b-125">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="d454b-125">**RestoreProperties**</span></span>                                                    | <span data-ttu-id="d454b-126">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d454b-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d454b-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="d454b-127">**SaveProperties**</span></span>                                                       | <span data-ttu-id="d454b-128">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d454b-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d454b-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="d454b-129">**SetPowerState**</span></span>                                                        | <span data-ttu-id="d454b-130">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d454b-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d454b-131">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d454b-131">Properties</span></span>

<span data-ttu-id="d454b-132">Die **MSVM-Klasse " \_ heartbeatcomponent** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d454b-132">The **Msvm\_HeartbeatComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d454b-133">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="d454b-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-134">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="d454b-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d454b-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-136">Alle zusätzlichen Verfügbarkeit und der Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="d454b-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="d454b-137">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf 6 festgelegt (nicht zutreffend).</span><span class="sxs-lookup"><span data-stu-id="d454b-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="d454b-138">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="d454b-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-139">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d454b-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d454b-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-141">Die primäre Verfügbarkeit und den Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="d454b-141">The primary availability and status of the device.</span></span> <span data-ttu-id="d454b-142">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d454b-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d454b-143">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="d454b-143">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-144">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="d454b-144">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d454b-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-146">Gibt die möglichen Werte für den *requestedstate* -Parameter der [**requestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) -Methode an, die zum Initiieren einer Zustandsänderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d454b-146">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="d454b-147">Bei den aufgelisteten Werten handelt es sich um eine Teilmenge der Werte in der **requestedstaatsupported** -Eigenschaft der zugeordneten Instanz von **CIM \_ enabledlogicalelementfunctions**, bei der die ausgewählten Werte eine Funktion des aktuellen Zustands des [**CIM- \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))sind.</span><span class="sxs-lookup"><span data-stu-id="d454b-147">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="d454b-148">Diese Eigenschaft darf nicht **null** sein, wenn eine Implementierung den Satz möglicher Werte als Funktion des aktuellen Zustands ankündigen kann.</span><span class="sxs-lookup"><span data-stu-id="d454b-148">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="d454b-149">Diese Eigenschaft ist **null** , wenn eine Implementierung den Satz möglicher Werte nicht als Funktion des aktuellen Zustands bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="d454b-149">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="d454b-150">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="d454b-150">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="d454b-151"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="d454b-151"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d454b-152"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="d454b-152"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d454b-153"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Herunter** fahren (4)</span><span class="sxs-lookup"><span data-stu-id="d454b-153"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d454b-154"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="d454b-154"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d454b-155"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="d454b-155"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="d454b-156"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>Zurück **stellen (8** )</span><span class="sxs-lookup"><span data-stu-id="d454b-156"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d454b-157"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Still **legung (9** )</span><span class="sxs-lookup"><span data-stu-id="d454b-157"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="d454b-158"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Neustart** (10)</span><span class="sxs-lookup"><span data-stu-id="d454b-158"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="d454b-159"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Zurücksetzen** (11)</span><span class="sxs-lookup"><span data-stu-id="d454b-159"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="d454b-160"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reserviert** (..</span><span class="sxs-lookup"><span data-stu-id="d454b-160"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="d454b-161">)</span><span class="sxs-lookup"><span data-stu-id="d454b-161">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d454b-162">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d454b-162">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-163">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d454b-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d454b-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-165">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="d454b-165">A short description of the object.</span></span> <span data-ttu-id="d454b-166">Diese Eigenschaft wird von der [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) -Klasse geerbt und ist immer auf "Heartbeat" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d454b-166">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class and is always set to "Heartbeat".</span></span>

</dd> <dt>

<span data-ttu-id="d454b-167">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="d454b-167">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-168">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d454b-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d454b-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-170">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="d454b-170">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="d454b-171">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="d454b-171">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d454b-172">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d454b-172">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d454b-173">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="d454b-173">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d454b-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d454b-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-176">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="d454b-176">The scoping system's creation class name.</span></span> <span data-ttu-id="d454b-177">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf "MSVM \_ heartbeatcomponent" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d454b-177">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_HeartbeatComponent".</span></span>

</dd> <dt>

<span data-ttu-id="d454b-178">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d454b-178">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-179">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d454b-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d454b-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-181">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="d454b-181">A description of the object.</span></span> <span data-ttu-id="d454b-182">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Microsoft Heartbeat Service" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d454b-182">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Heartbeat Service".</span></span>

</dd> <dt>

<span data-ttu-id="d454b-183">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="d454b-183">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-184">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d454b-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d454b-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-186">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="d454b-186">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="d454b-187">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="d454b-187">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d454b-188">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d454b-188">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d454b-189">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="d454b-189">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-190">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d454b-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d454b-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-192">Eine Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="d454b-192">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="d454b-193">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf "Microsoft:*VMGUID* \\ *GUID*" festgelegt, wobei *VMGUID* die **Name** -Eigenschaft des [**MSVM \_ Computer Systems**](msvm-computersystem.md) ist, das diesem Gerät zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d454b-193">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*VMGUID*\\*GUID*" where *VMGUID* is the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="d454b-194">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d454b-194">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-195">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d454b-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d454b-196">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-197">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d454b-197">A display name for the object.</span></span> <span data-ttu-id="d454b-198">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Heartbeat" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d454b-198">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Heartbeat".</span></span>

</dd> <dt>

<span data-ttu-id="d454b-199">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="d454b-199">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-200">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d454b-200">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d454b-201">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-202">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 7 (kein Standardwert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d454b-202">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 7 (No Default).</span></span>

</dd> <dt>

<span data-ttu-id="d454b-203">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="d454b-203">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-204">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d454b-204">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d454b-205">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-206">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="d454b-206">The enabled and disabled states of an element.</span></span> <span data-ttu-id="d454b-207">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) geerbt und ist einer der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="d454b-207">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>



| <span data-ttu-id="d454b-208">Wert</span><span class="sxs-lookup"><span data-stu-id="d454b-208">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="d454b-209">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d454b-209">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="d454b-210"><dt>**Aktiviert**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d454b-210"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="d454b-211">Das-Element wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d454b-211">The element is running.</span></span><br/>    |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="d454b-212"><dt>**Deaktiviert**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d454b-212"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="d454b-213">Das Element ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d454b-213">The element is turned off.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d454b-214">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="d454b-214">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-215">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d454b-215">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d454b-216">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-217">Gibt an, ob der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="d454b-217">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="d454b-218">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d454b-218">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d454b-219">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="d454b-219">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-220">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d454b-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d454b-221">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-222">Eine Zeichenfolge, die weitere Informationen über den Fehler enthält, der in **LastErrorCode** aufgezeichnet wurde, sowie Informationen über alle Maßnahmen, die ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="d454b-222">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="d454b-223">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d454b-223">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d454b-224">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="d454b-224">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-225">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d454b-225">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d454b-226">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-227">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="d454b-227">The current health of the element.</span></span> <span data-ttu-id="d454b-228">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 5 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d454b-228">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="d454b-229">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d454b-229">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-230">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="d454b-230">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d454b-231">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-232">Ein Array von Freiform-Zeichen folgen, die Erklärungen und Details hinter den Einträgen im Eigenschafts Array " **OtherIdentifyingInfo** " bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d454b-232">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="d454b-233">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d454b-233">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d454b-234">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d454b-234">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-235">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="d454b-235">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d454b-236">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-237">Das Datum und die Uhrzeit, zu denen der Integrations Dienst auf dem virtuellen Computer installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d454b-237">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="d454b-238">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d454b-238">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d454b-239">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d454b-239">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-240">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d454b-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d454b-241">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d454b-242">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="d454b-242">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d454b-243">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="d454b-243">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d454b-244">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d454b-244">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d454b-245">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d454b-245">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-246">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d454b-246">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d454b-247">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-248">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="d454b-248">The last error code reported by the logical device.</span></span> <span data-ttu-id="d454b-249">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d454b-249">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d454b-250">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="d454b-250">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-251">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d454b-251">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d454b-252">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-253">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="d454b-253">This property has been deprecated.</span></span> <span data-ttu-id="d454b-254">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d454b-254">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d454b-255">**Name**</span><span class="sxs-lookup"><span data-stu-id="d454b-255">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-256">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d454b-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d454b-257">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-258">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="d454b-258">The label by which the object is known.</span></span> <span data-ttu-id="d454b-259">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d454b-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d454b-260">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="d454b-260">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-261">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d454b-261">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d454b-262">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-263">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d454b-263">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="d454b-264">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="d454b-264">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d454b-265">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d454b-265">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d454b-266">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="d454b-266">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-267">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="d454b-267">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d454b-268">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d454b-269">Qualifizierer: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="d454b-269">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="d454b-270">Der aktuelle Status des Elements.</span><span class="sxs-lookup"><span data-stu-id="d454b-270">The current status of the element.</span></span> <span data-ttu-id="d454b-271">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d454b-271">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="d454b-272">Im folgenden sind die möglichen Werte für den Wert der Eigenschaft **OperationalStatus** \[ 0 verfügbar \] .</span><span class="sxs-lookup"><span data-stu-id="d454b-272">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d454b-273"><span id="OK"></span><span id="ok"></span>**OK** (2)</span><span class="sxs-lookup"><span data-stu-id="d454b-273"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d454b-274">Der Dienst wird normal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d454b-274">The service is operating normally.</span></span> <span data-ttu-id="d454b-275">Die Eigenschaftswerte **OperationalStatus** \[ 1 \] und **Statusbeschreibungen** \[ 1 \] enthalten möglicherweise weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="d454b-275">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span>

</dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d454b-276"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (3** )</span><span class="sxs-lookup"><span data-stu-id="d454b-276"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d454b-277">Der Dienst wird normal ausgeführt, aber der Gast Dienst hat eine kompatible Kommunikationsprotokoll Version ausgehandelt.</span><span class="sxs-lookup"><span data-stu-id="d454b-277">The service is operating normally, but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="d454b-278">Die Eigenschaftswerte **OperationalStatus** \[ 1 \] und **Statusbeschreibungen** \[ 1 \] enthalten möglicherweise weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="d454b-278">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span>

</dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="d454b-279"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (7)</span><span class="sxs-lookup"><span data-stu-id="d454b-279"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (7)</span></span>


</dt> <dd>

<span data-ttu-id="d454b-280">Der Gast unterstützt keine kompatible Protokollversion.</span><span class="sxs-lookup"><span data-stu-id="d454b-280">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="d454b-281">Die Eigenschaftswerte **OperationalStatus** \[ 1 \] und **Statusbeschreibungen** \[ 1 \] enthalten möglicherweise weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="d454b-281">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span>

</dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d454b-282"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (12)</span><span class="sxs-lookup"><span data-stu-id="d454b-282"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (12)</span></span>


</dt> <dd>

<span data-ttu-id="d454b-283">Der Gast Dienst ist nicht installiert, oder er wurde noch nicht kontaktiert.</span><span class="sxs-lookup"><span data-stu-id="d454b-283">The guest service is not installed or has not yet been contacted.</span></span>

</dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="d454b-284"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (13)</span><span class="sxs-lookup"><span data-stu-id="d454b-284"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (13)</span></span>


</dt> <dd>

<span data-ttu-id="d454b-285">Der Gast Dienst antwortet nicht mehr normal.</span><span class="sxs-lookup"><span data-stu-id="d454b-285">The guest service is no longer responding normally.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="d454b-286"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (15)</span><span class="sxs-lookup"><span data-stu-id="d454b-286"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (15)</span></span>


</dt> <dd>

<span data-ttu-id="d454b-287">Der virtuelle Computer wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="d454b-287">The virtual machine is paused.</span></span>

</dd> </dl>

<span data-ttu-id="d454b-288">Der Wert der Eigenschaft **OperationalStatus** \[ 1 gibt die zusammengefügten \] Anwendungs Zustands Werte an.</span><span class="sxs-lookup"><span data-stu-id="d454b-288">The **OperationalStatus**\[1\] property value indicates the coalesced application state values.</span></span> <span data-ttu-id="d454b-289">Dabei handelt es sich um einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="d454b-289">This will be one of the following values.</span></span>

> [!Note]  
> <span data-ttu-id="d454b-290">Der Status einer Anwendung wird mit der [**setapplicationstate**](ivmapplicationhealthmonitor-setapplicationstate.md) -Methode auf dem virtuellen Computer festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d454b-290">The state for an application is set on the virtual machine by using the [**SetApplicationState**](ivmapplicationhealthmonitor-setapplicationstate.md) method.</span></span>

 

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d454b-291"><span id="OK"></span><span id="ok"></span>**OK** (2)</span><span class="sxs-lookup"><span data-stu-id="d454b-291"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d454b-292">Die Anwendungen, die auf dem virtuellen Computer ausgeführt werden, funktionieren ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="d454b-292">The applications running inside the virtual machine are operating normally.</span></span>

</dd> <dt>

<span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>

<span data-ttu-id="d454b-293"><span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>**Protokoll** Konflikt (32775)</span><span class="sxs-lookup"><span data-stu-id="d454b-293"><span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>**Protocol Mismatch** (32775)</span></span>


</dt> <dd>

<span data-ttu-id="d454b-294">Der Gast und die Host Komponenten führen verschiedene Protokoll Versionen aus.</span><span class="sxs-lookup"><span data-stu-id="d454b-294">The guest and the host components are running different protocol versions.</span></span>

</dd> <dt>

<span id="Application_Critical_State"></span><span id="application_critical_state"></span><span id="APPLICATION_CRITICAL_STATE"></span>

<span data-ttu-id="d454b-295"><span id="Application_Critical_State"></span><span id="application_critical_state"></span><span id="APPLICATION_CRITICAL_STATE"></span>**Kritischer Anwendungs Zustand** (32782)</span><span class="sxs-lookup"><span data-stu-id="d454b-295"><span id="Application_Critical_State"></span><span id="application_critical_state"></span><span id="APPLICATION_CRITICAL_STATE"></span>**Application Critical State** (32782)</span></span>


</dt> <dd>

<span data-ttu-id="d454b-296">Mindestens eine der Anwendungen auf dem virtuellen Computer befindet sich in einem kritischen Zustand.</span><span class="sxs-lookup"><span data-stu-id="d454b-296">One or more of the applications inside the virtual machine are in a critical state.</span></span>

</dd> <dt>

<span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>

<span data-ttu-id="d454b-297"><span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>**Timeout** bei der Kommunikation (32783)</span><span class="sxs-lookup"><span data-stu-id="d454b-297"><span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>**Communication Timed Out** (32783)</span></span>


</dt> <dd>

<span data-ttu-id="d454b-298">Timeout beim Warten auf eine Antwort von der Gast Komponente.</span><span class="sxs-lookup"><span data-stu-id="d454b-298">Timed out waiting for a response from the guest component.</span></span>

</dd> <dt>

<span id="Communication_Failed"></span><span id="communication_failed"></span><span id="COMMUNICATION_FAILED"></span>

<span data-ttu-id="d454b-299"><span id="Communication_Failed"></span><span id="communication_failed"></span><span id="COMMUNICATION_FAILED"></span>Fehler bei der **Kommunikation** (32784).</span><span class="sxs-lookup"><span data-stu-id="d454b-299"><span id="Communication_Failed"></span><span id="communication_failed"></span><span id="COMMUNICATION_FAILED"></span>**Communication Failed** (32784)</span></span>


</dt> <dd>

<span data-ttu-id="d454b-300">Fehler bei der Kommunikation mit der Gast Komponente.</span><span class="sxs-lookup"><span data-stu-id="d454b-300">Failed to communicate with the guest component.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d454b-301">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="d454b-301">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-302">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d454b-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d454b-303">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-304">Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d454b-304">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="d454b-305">Diese Eigenschaft muss auf **null** festgelegt werden, wenn die **enabledstate** -Eigenschaft einen anderen Wert als 1 hat.</span><span class="sxs-lookup"><span data-stu-id="d454b-305">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="d454b-306">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d454b-306">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d454b-307">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="d454b-307">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-308">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="d454b-308">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d454b-309">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-310">Alle zusätzlichen Daten über Geräte-ID-Informationen, die zur Identifizierung eines logischen Geräts verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="d454b-310">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="d454b-311">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d454b-311">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d454b-312">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="d454b-312">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-313">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="d454b-313">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d454b-314">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-315">Die Energie Verwaltungsfunktionen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="d454b-315">The power management capabilities of the device.</span></span> <span data-ttu-id="d454b-316">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d454b-316">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d454b-317">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="d454b-317">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-318">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d454b-318">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d454b-319">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-320">Gibt an, ob das Gerät Energie gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="d454b-320">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="d454b-321">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d454b-321">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d454b-322">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="d454b-322">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-323">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d454b-323">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d454b-324">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-325">Gibt an, wie viele aufeinanderfolgende Stunden dieses Gerät seit dem letzten Strom Umgebung eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="d454b-325">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="d454b-326">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d454b-326">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d454b-327">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="d454b-327">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-328">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d454b-328">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d454b-329">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-330">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="d454b-330">Provides high level status information.</span></span> <span data-ttu-id="d454b-331">Diese Eigenschaft sollte in Verbindung mit der **detailedstatus** -Eigenschaft verwendet werden, um allgemeine und ausführliche Integritäts Statusinformationen für das-Element und seine unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d454b-331">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="d454b-332">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="d454b-332">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d454b-333">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d454b-333">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d454b-334">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="d454b-334">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-335">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d454b-335">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d454b-336">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-337">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="d454b-337">The last requested or desired state for the element.</span></span> <span data-ttu-id="d454b-338">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 12 (nicht zutreffend) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d454b-338">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="d454b-339">**Status**</span><span class="sxs-lookup"><span data-stu-id="d454b-339">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-340">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d454b-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d454b-341">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-342">Der aktuelle Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="d454b-342">The current status of the object.</span></span> <span data-ttu-id="d454b-343">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d454b-343">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d454b-344">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="d454b-344">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-345">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="d454b-345">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d454b-346">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-347">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="d454b-347">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="d454b-348">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d454b-348">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d454b-349">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="d454b-349">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-350">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d454b-350">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d454b-351">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-352">Der aktuelle Zustand des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="d454b-352">The current state of the logical device.</span></span> <span data-ttu-id="d454b-353">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d454b-353">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d454b-354">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="d454b-354">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-355">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d454b-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d454b-356">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-357">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="d454b-357">The scoping system's creation class name.</span></span> <span data-ttu-id="d454b-358">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf "MSVM \_ Computersystem" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d454b-358">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="d454b-359">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="d454b-359">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-360">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d454b-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d454b-361">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-362">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="d454b-362">The scoping system's name.</span></span> <span data-ttu-id="d454b-363">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt und ist der Name des [**MSVM- \_ Computer Systems**](msvm-computersystem.md) , das diesem Takt Dienst zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d454b-363">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is the name of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) that is associated with this heartbeat service.</span></span>

</dd> <dt>

<span data-ttu-id="d454b-364">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="d454b-364">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-365">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="d454b-365">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d454b-366">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-367">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="d454b-367">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="d454b-368">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d454b-368">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d454b-369">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="d454b-369">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-370">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d454b-370">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d454b-371">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-372">Die Gesamtanzahl der Stunden, für die dieses Gerät eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="d454b-372">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="d454b-373">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d454b-373">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d454b-374">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="d454b-374">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d454b-375">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d454b-375">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d454b-376">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d454b-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d454b-377">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="d454b-377">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="d454b-378">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d454b-378">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d454b-379">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d454b-379">Remarks</span></span>

<span data-ttu-id="d454b-380">Der Zugriff auf die **MSVM-Klasse " \_ heartbeatcomponent** " kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="d454b-380">Access to the **Msvm\_HeartbeatComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d454b-381">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d454b-381">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="d454b-382">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d454b-382">Examples</span></span>

<span data-ttu-id="d454b-383">Im folgenden c#-Beispiel wird der Anwendungs Integritäts Status eines virtuellen Computers abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d454b-383">The following C# sample obtains the application health status of a virtual machine.</span></span> <span data-ttu-id="d454b-384">Die Dienstprogramme, auf die verwiesen wird, finden Sie unter [Allgemeine Hilfsprogramme für die Virtualisierungsbeispiele (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="d454b-384">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d454b-385">Der folgende Code muss mit Administrator Rechten ausgeführt werden, damit er ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="d454b-385">To function correctly, the following code must be run with Administrator privileges.</span></span>

 


```CSharp
private UInt16 OperationalStatusOk = 2;
private UInt16 OperationalStatusApplicationCriticalState = 32782;

/// <summary>
/// Gets the applications status in the VM.
/// </summary>
/// <param name="hostMachine">The hostname of the machine on which
/// the VM is running.</param>
/// <param name="vmName">The VM name.</param>
public
void
GetAppHealthStatus(
    string hostMachine,
    string vmName
    )
{
    ManagementScope scope = new ManagementScope(
        @"\\" + hostMachine + @"\root\virtualization\v2", null);

    ManagementObject heartBeatComponent = null;

    // Get the VM object and its heart beat component.
    using (ManagementObject vm = WmiUtilities.GetVirtualMachine(vmName, scope))
    using (ManagementObjectCollection heartBeatCollection =
        vm.GetRelated("Msvm_HeartbeatComponent", "Msvm_SystemDevice",
            null, null, null, null, false, null))
    {
        foreach (ManagementObject element in heartBeatCollection)
        {
            heartBeatComponent = element;
            break;
        }
    }

    if (heartBeatComponent == null)
    {
        Console.WriteLine("The VM is not running.");
        return;
    }

    using (heartBeatComponent)
    {
        UInt16[] operationalStatus = (UInt16[])heartBeatComponent["OperationalStatus"];
        UInt16 vmStatus = operationalStatus[0];

        if (vmStatus != OperationalStatusOk)
        {
            Console.WriteLine("The VM heartbeat status is not OK");
            return;
        }

        if (operationalStatus.Length != 2)
        {
            Console.WriteLine("The required Integration Components are not running " +
                "or not installed.");
            return;
        }

        UInt16 appStatus = operationalStatus[1];
        if (appStatus == OperationalStatusOk)
        {
            Console.WriteLine("The VM applications health status: OK");
        }
        else if (appStatus == OperationalStatusApplicationCriticalState)
        {
            Console.WriteLine("The VM applications health status: Critical");
        }
        else
        {
            throw new ManagementException("Unknown application health status");
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="d454b-386">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d454b-386">Requirements</span></span>



| <span data-ttu-id="d454b-387">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d454b-387">Requirement</span></span> | <span data-ttu-id="d454b-388">Wert</span><span class="sxs-lookup"><span data-stu-id="d454b-388">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d454b-389">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d454b-389">Minimum supported client</span></span><br/> | <span data-ttu-id="d454b-390">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d454b-390">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d454b-391">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d454b-391">Minimum supported server</span></span><br/> | <span data-ttu-id="d454b-392">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d454b-392">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d454b-393">Namespace</span><span class="sxs-lookup"><span data-stu-id="d454b-393">Namespace</span></span><br/>                | <span data-ttu-id="d454b-394">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="d454b-394">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d454b-395">MOF</span><span class="sxs-lookup"><span data-stu-id="d454b-395">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d454b-396"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d454b-396"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d454b-397">DLL</span><span class="sxs-lookup"><span data-stu-id="d454b-397">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d454b-398"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d454b-398"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d454b-399">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d454b-399">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d454b-400">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="d454b-400">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="d454b-401">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="d454b-401">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> <dt>

[<span data-ttu-id="d454b-402">**MSVM \_ heartbeatcomponent**</span><span class="sxs-lookup"><span data-stu-id="d454b-402">**Msvm\_HeartbeatComponent**</span></span>](/previous-versions/windows/desktop/virtual/msvm-heartbeatcomponent)
</dt> </dl>

 

