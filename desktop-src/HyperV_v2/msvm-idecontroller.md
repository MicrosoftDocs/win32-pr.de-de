---
description: Stellt einen IDE-Controller dar.
ms.assetid: DFD4D90E-CA91-42B3-AC88-9E9D26089C36
title: Msvm_IDEController-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_IDEController
- Msvm_IDEController.SetPowerState
- Msvm_IDEController.EnableDevice
- Msvm_IDEController.OnlineDevice
- Msvm_IDEController.QuiesceDevice
- Msvm_IDEController.SaveProperties
- Msvm_IDEController.RestoreProperties
- Msvm_IDEController.InstanceID
- Msvm_IDEController.Caption
- Msvm_IDEController.Description
- Msvm_IDEController.ElementName
- Msvm_IDEController.InstallDate
- Msvm_IDEController.Name
- Msvm_IDEController.OperationalStatus
- Msvm_IDEController.StatusDescriptions
- Msvm_IDEController.Status
- Msvm_IDEController.HealthState
- Msvm_IDEController.CommunicationStatus
- Msvm_IDEController.DetailedStatus
- Msvm_IDEController.OperatingStatus
- Msvm_IDEController.PrimaryStatus
- Msvm_IDEController.EnabledState
- Msvm_IDEController.OtherEnabledState
- Msvm_IDEController.RequestedState
- Msvm_IDEController.EnabledDefault
- Msvm_IDEController.TimeOfLastStateChange
- Msvm_IDEController.AvailableRequestedStates
- Msvm_IDEController.TransitioningToState
- Msvm_IDEController.SystemCreationClassName
- Msvm_IDEController.SystemName
- Msvm_IDEController.CreationClassName
- Msvm_IDEController.DeviceID
- Msvm_IDEController.PowerManagementSupported
- Msvm_IDEController.PowerManagementCapabilities
- Msvm_IDEController.Availability
- Msvm_IDEController.StatusInfo
- Msvm_IDEController.LastErrorCode
- Msvm_IDEController.ErrorDescription
- Msvm_IDEController.ErrorCleared
- Msvm_IDEController.OtherIdentifyingInfo
- Msvm_IDEController.PowerOnHours
- Msvm_IDEController.TotalPowerOnHours
- Msvm_IDEController.IdentifyingDescriptions
- Msvm_IDEController.AdditionalAvailability
- Msvm_IDEController.MaxQuiesceTime
- Msvm_IDEController.TimeOfLastReset
- Msvm_IDEController.ProtocolSupported
- Msvm_IDEController.MaxNumberControlled
- Msvm_IDEController.ProtocolDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 25da1bddfa029ca5a6892006283e322d91a328a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372865"
---
# <a name="msvm_idecontroller-class"></a><span data-ttu-id="62fa5-103">MSVM- \_ idecontroller-Klasse</span><span class="sxs-lookup"><span data-stu-id="62fa5-103">Msvm\_IDEController class</span></span>

<span data-ttu-id="62fa5-104">Stellt einen IDE-Controller dar.</span><span class="sxs-lookup"><span data-stu-id="62fa5-104">Represents an IDE controller.</span></span> <span data-ttu-id="62fa5-105">Diese Klasse kann bis zu vier Laufwerke unterstützen, die an den Controller angeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="62fa5-105">This class can support up to four drives attached to the controller.</span></span> <span data-ttu-id="62fa5-106">Der IDE-Controller ist auf dem virtuellen Computer korrigiert und verfügt daher nicht über einen zugeordneten Ressourcenpool.</span><span class="sxs-lookup"><span data-stu-id="62fa5-106">The IDE controller is fixed in the virtual machine and therefore does not have a resource pool associated with it.</span></span>

> [!Note]  
> <span data-ttu-id="62fa5-107">Diese Klasse ist für virtuelle Maschinen der Generation 2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="62fa5-107">This class is not available to generation 2 virtual machines.</span></span>

 

<span data-ttu-id="62fa5-108">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="62fa5-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="62fa5-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="62fa5-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_IDEController : CIM_IDEController
{
  string   InstanceID;
  string   Caption;
  string   Description = "Microsoft Virtual IDE Controller";
  string   ElementName;
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
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_IDEController";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = {6};
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 37;
  uint32   MaxNumberControlled = 2;
  string   ProtocolDescription = "IDE";
};
```

## <a name="members"></a><span data-ttu-id="62fa5-110">Member</span><span class="sxs-lookup"><span data-stu-id="62fa5-110">Members</span></span>

<span data-ttu-id="62fa5-111">Die **MSVM- \_ idecontroller** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="62fa5-111">The **Msvm\_IDEController** class has these types of members:</span></span>

-   [<span data-ttu-id="62fa5-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="62fa5-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="62fa5-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="62fa5-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="62fa5-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="62fa5-114">Methods</span></span>

<span data-ttu-id="62fa5-115">Die **MSVM- \_ idecontroller** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="62fa5-115">The **Msvm\_IDEController** class has these methods.</span></span>



| <span data-ttu-id="62fa5-116">Methode</span><span class="sxs-lookup"><span data-stu-id="62fa5-116">Method</span></span>                                                              | <span data-ttu-id="62fa5-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="62fa5-117">Description</span></span>                              |
|:--------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="62fa5-118">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="62fa5-118">**EnableDevice**</span></span>                                                    | <span data-ttu-id="62fa5-119">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="62fa5-120">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="62fa5-120">**OnlineDevice**</span></span>                                                    | <span data-ttu-id="62fa5-121">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-121">This method is not supported.</span></span><br/> |
| <span data-ttu-id="62fa5-122">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="62fa5-122">**QuiesceDevice**</span></span>                                                   | <span data-ttu-id="62fa5-123">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-123">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="62fa5-124">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="62fa5-124">**RequestStateChange**</span></span>](msvm-idecontroller-requeststatechange.md) | <span data-ttu-id="62fa5-125">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="62fa5-125">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="62fa5-126">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="62fa5-126">**Reset**</span></span>](msvm-idecontroller-reset.md)                           | <span data-ttu-id="62fa5-127">Setzt das virtuelle Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="62fa5-127">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="62fa5-128">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="62fa5-128">**RestoreProperties**</span></span>                                               | <span data-ttu-id="62fa5-129">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="62fa5-130">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="62fa5-130">**SaveProperties**</span></span>                                                  | <span data-ttu-id="62fa5-131">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-131">This method is not supported.</span></span><br/> |
| <span data-ttu-id="62fa5-132">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="62fa5-132">**SetPowerState**</span></span>                                                   | <span data-ttu-id="62fa5-133">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-133">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="62fa5-134">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="62fa5-134">Properties</span></span>

<span data-ttu-id="62fa5-135">Die **MSVM- \_ idecontroller** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="62fa5-135">The **Msvm\_IDEController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="62fa5-136">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="62fa5-136">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-137">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="62fa5-137">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-139">Alle zusätzlichen Verfügbarkeit und der Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="62fa5-139">Any additional availability and status of the device.</span></span> <span data-ttu-id="62fa5-140">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-140">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-141">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="62fa5-141">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-142">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62fa5-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-144">Die primäre Verfügbarkeit und den Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="62fa5-144">The primary availability and status of the device.</span></span> <span data-ttu-id="62fa5-145">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-145">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-146">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="62fa5-146">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-147">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="62fa5-147">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-149">Gibt die möglichen Werte für den *requestedstate* -Parameter der [**requestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) -Methode an, die zum Initiieren einer Zustandsänderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="62fa5-149">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="62fa5-150">Bei den aufgelisteten Werten handelt es sich um eine Teilmenge der Werte, die in der **requestedstaatsupported** -Eigenschaft der zugeordneten Instanz von **CIM \_ enabledlogicalelementfunctions** enthalten sind, wobei die ausgewählten Werte eine Funktion des aktuellen Zustands des [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) -Objekts sind.</span><span class="sxs-lookup"><span data-stu-id="62fa5-150">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="62fa5-151">Diese Eigenschaft darf nicht **null** sein, wenn eine Implementierung den Satz möglicher Werte als Funktion des aktuellen Zustands ankündigen kann.</span><span class="sxs-lookup"><span data-stu-id="62fa5-151">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="62fa5-152">Diese Eigenschaft ist **null** , wenn eine Implementierung den Satz möglicher Werte nicht als Funktion des aktuellen Zustands bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="62fa5-152">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="62fa5-153">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-153">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-154">**Caption**</span><span class="sxs-lookup"><span data-stu-id="62fa5-154">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-155">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62fa5-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-157">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="62fa5-157">A short description of the object.</span></span> <span data-ttu-id="62fa5-158">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-158">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>



| <span data-ttu-id="62fa5-159">Wert</span><span class="sxs-lookup"><span data-stu-id="62fa5-159">Value</span></span>                                                                                         | <span data-ttu-id="62fa5-160">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="62fa5-160">Meaning</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="62fa5-161"><dt>"IDE-Controller 0"</dt></span><span class="sxs-lookup"><span data-stu-id="62fa5-161"><dt>"IDE Controller 0"</dt></span></span> </dl> | <span data-ttu-id="62fa5-162">Die-Instanz stellt den primären Controller dar.</span><span class="sxs-lookup"><span data-stu-id="62fa5-162">The instance represents the primary controller.</span></span><br/>   |
| <dl> <span data-ttu-id="62fa5-163"><dt>"IDE-Controller 1"</dt></span><span class="sxs-lookup"><span data-stu-id="62fa5-163"><dt>"IDE Controller 1"</dt></span></span> </dl> | <span data-ttu-id="62fa5-164">Die-Instanz stellt den sekundären Controller dar.</span><span class="sxs-lookup"><span data-stu-id="62fa5-164">The instance represents the secondary controller.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="62fa5-165">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="62fa5-165">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-166">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62fa5-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-168">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="62fa5-168">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="62fa5-169">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="62fa5-169">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="62fa5-170">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-170">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-171">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="62fa5-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-172">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62fa5-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-174">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="62fa5-174">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="62fa5-175">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-176">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="62fa5-176">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62fa5-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-179">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="62fa5-179">A description of the object.</span></span> <span data-ttu-id="62fa5-180">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-181">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="62fa5-181">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-182">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62fa5-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-184">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="62fa5-184">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="62fa5-185">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="62fa5-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="62fa5-186">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-187">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="62fa5-187">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-188">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62fa5-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-190">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und auf "Microsoft:*GUID* \\ *Device-Specific-Data*" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-190">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-191">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="62fa5-191">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-192">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62fa5-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-194">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-194">A display name for the object.</span></span> <span data-ttu-id="62fa5-195">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-195">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>



| <span data-ttu-id="62fa5-196">Wert</span><span class="sxs-lookup"><span data-stu-id="62fa5-196">Value</span></span>                                                                                         | <span data-ttu-id="62fa5-197">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="62fa5-197">Meaning</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="62fa5-198"><dt>"IDE-Controller 0"</dt></span><span class="sxs-lookup"><span data-stu-id="62fa5-198"><dt>"IDE Controller 0"</dt></span></span> </dl> | <span data-ttu-id="62fa5-199">Die-Instanz stellt den primären Controller dar.</span><span class="sxs-lookup"><span data-stu-id="62fa5-199">The instance represents the primary controller.</span></span><br/>   |
| <dl> <span data-ttu-id="62fa5-200"><dt>"IDE-Controller 1"</dt></span><span class="sxs-lookup"><span data-stu-id="62fa5-200"><dt>"IDE Controller 1"</dt></span></span> </dl> | <span data-ttu-id="62fa5-201">Die-Instanz stellt den sekundären Controller dar.</span><span class="sxs-lookup"><span data-stu-id="62fa5-201">The instance represents the secondary controller.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="62fa5-202">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="62fa5-202">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-203">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62fa5-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-205">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="62fa5-205">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="62fa5-206">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-206">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-207">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="62fa5-207">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-208">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62fa5-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-210">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="62fa5-210">The enabled and disabled states of an element.</span></span> <span data-ttu-id="62fa5-211">Sie kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben.</span><span class="sxs-lookup"><span data-stu-id="62fa5-211">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="62fa5-212">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-212">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-213">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="62fa5-213">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-214">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="62fa5-214">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-215">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-216">Gibt an, ob der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="62fa5-216">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="62fa5-217">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="62fa5-217">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-218">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="62fa5-218">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-219">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62fa5-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-220">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-221">Eine Zeichenfolge, die weitere Informationen über den Fehler enthält, der in **LastErrorCode** aufgezeichnet wurde, sowie Informationen über alle Maßnahmen, die ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="62fa5-221">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="62fa5-222">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="62fa5-222">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-223">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="62fa5-223">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-224">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62fa5-224">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-225">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-226">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="62fa5-226">The current health of the element.</span></span> <span data-ttu-id="62fa5-227">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="62fa5-227">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="62fa5-228">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="62fa5-228">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="62fa5-229">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-229">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-230">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="62fa5-230">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-231">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="62fa5-231">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-232">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-233">Ein Array von Freiform-Zeichen folgen, die Erklärungen und Details hinter den Einträgen im Eigenschafts Array " **OtherIdentifyingInfo** " bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="62fa5-233">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="62fa5-234">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="62fa5-234">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-235">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="62fa5-235">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-236">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="62fa5-236">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-237">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-238">Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="62fa5-238">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="62fa5-239">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-239">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-240">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="62fa5-240">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-241">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62fa5-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-242">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-243">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="62fa5-243">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-244">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="62fa5-244">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="62fa5-245">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-245">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-246">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="62fa5-246">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-247">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="62fa5-247">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-248">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-249">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="62fa5-249">The last error code reported by the logical device.</span></span> <span data-ttu-id="62fa5-250">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="62fa5-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-251">**Maxnuma**</span><span class="sxs-lookup"><span data-stu-id="62fa5-251">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-252">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="62fa5-252">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-253">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-254">Die maximale Anzahl direkt Adressier barer Entitäten, die von diesem Controller unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="62fa5-254">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="62fa5-255">Wenn die Zahl unbekannt oder unbegrenzt ist, sollte der Wert 0 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="62fa5-255">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="62fa5-256">Das Protokoll, das vom Controller für den Zugriff auf gesteuerte Geräte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="62fa5-256">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="62fa5-257">Diese Eigenschaft wird vom [**CIM- \_ Controller**](/windows/desktop/CIMWin32Prov/cim-controller)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-257">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-258">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="62fa5-258">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-259">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="62fa5-259">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-260">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-261">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="62fa5-261">This property has been deprecated.</span></span> <span data-ttu-id="62fa5-262">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="62fa5-262">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-263">**Name**</span><span class="sxs-lookup"><span data-stu-id="62fa5-263">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-264">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62fa5-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-265">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-266">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="62fa5-266">The label by which the object is known.</span></span> <span data-ttu-id="62fa5-267">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und entspricht der Element **Name** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="62fa5-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-268">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="62fa5-268">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-269">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62fa5-269">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-270">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-271">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="62fa5-271">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="62fa5-272">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="62fa5-272">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="62fa5-273">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-273">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-274">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="62fa5-274">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-275">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="62fa5-275">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-276">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-277">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="62fa5-277">The current statuses of the object.</span></span> <span data-ttu-id="62fa5-278">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-278">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-279">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="62fa5-279">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-280">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62fa5-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-281">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-282">Der aktivierte oder deaktivierte Status des Elements, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="62fa5-282">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="62fa5-283">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="62fa5-283">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="62fa5-284">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-284">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-285">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="62fa5-285">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-286">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="62fa5-286">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-287">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-288">Alle zusätzlichen Daten über Geräte-ID-Informationen, die zur Identifizierung eines logischen Geräts verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="62fa5-288">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="62fa5-289">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-289">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-290">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="62fa5-290">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-291">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="62fa5-291">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-292">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-293">Die Energie Verwaltungsfunktionen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="62fa5-293">The power management capabilities of the device.</span></span> <span data-ttu-id="62fa5-294">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="62fa5-294">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-295">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="62fa5-295">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-296">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="62fa5-296">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-297">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-298">Gibt an, ob das Gerät Energie gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="62fa5-298">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="62fa5-299">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="62fa5-299">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-300">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="62fa5-300">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-301">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="62fa5-301">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-302">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-303">Gibt an, wie viele aufeinanderfolgende Stunden dieses Gerät seit dem letzten Strom Umgebung eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="62fa5-303">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="62fa5-304">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="62fa5-304">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-305">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="62fa5-305">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-306">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62fa5-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-307">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-308">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="62fa5-308">Provides high level status information.</span></span> <span data-ttu-id="62fa5-309">Diese Eigenschaft sollte in Verbindung mit der **detailedstatus** -Eigenschaft verwendet werden, um allgemeine und ausführliche Integritäts Statusinformationen für das-Element und seine unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="62fa5-309">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="62fa5-310">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="62fa5-310">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="62fa5-311">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-311">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-312">**Protocoldescription**</span><span class="sxs-lookup"><span data-stu-id="62fa5-312">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-313">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62fa5-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-314">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-315">Eine Zeichenfolge, die weitere Informationen bereitstellt, die mit dem vom Controller unterstützten Protokoll verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="62fa5-315">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="62fa5-316">Diese Eigenschaft wird vom [**CIM- \_ Controller**](/windows/desktop/CIMWin32Prov/cim-controller)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-316">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-317">**Protocolsupported**</span><span class="sxs-lookup"><span data-stu-id="62fa5-317">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-318">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62fa5-318">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-319">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-320">Das Protokoll, das vom Controller für den Zugriff auf gesteuerte Geräte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="62fa5-320">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="62fa5-321">Diese Eigenschaft wird vom [**CIM- \_ Controller**](/windows/desktop/CIMWin32Prov/cim-controller)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-321">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>



| <span data-ttu-id="62fa5-322">Wert</span><span class="sxs-lookup"><span data-stu-id="62fa5-322">Value</span></span>                                                                         | <span data-ttu-id="62fa5-323">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="62fa5-323">Meaning</span></span>        |
|-------------------------------------------------------------------------------|----------------|
| <dl> <span data-ttu-id="62fa5-324"><dt>37</dt></span><span class="sxs-lookup"><span data-stu-id="62fa5-324"><dt>37</dt></span></span> </dl> | <span data-ttu-id="62fa5-325">IDE</span><span class="sxs-lookup"><span data-stu-id="62fa5-325">IDE</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="62fa5-326">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="62fa5-326">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-327">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62fa5-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-328">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-329">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="62fa5-329">The last requested or desired state for the element.</span></span> <span data-ttu-id="62fa5-330">Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-330">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="62fa5-331">Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuell aktivierten oder deaktivierten Zustände zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="62fa5-331">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="62fa5-332">Eine bestimmte Instanz eines aktivierten logischen Elements unterstützt **requestedstatechange** möglicherweise nicht.</span><span class="sxs-lookup"><span data-stu-id="62fa5-332">A particular instance of an enabled logical element might not support **RequestedStateChange**.</span></span> <span data-ttu-id="62fa5-333">Wenn dies auftritt, wird der Wert 12 (nicht zutreffend) verwendet.</span><span class="sxs-lookup"><span data-stu-id="62fa5-333">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="62fa5-334">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-335">**Status**</span><span class="sxs-lookup"><span data-stu-id="62fa5-335">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-336">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62fa5-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-337">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-338">Der aktuelle Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="62fa5-338">The current status of the object.</span></span> <span data-ttu-id="62fa5-339">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="62fa5-339">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-340">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="62fa5-340">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-341">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="62fa5-341">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-342">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-343">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="62fa5-343">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="62fa5-344">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-344">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-345">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="62fa5-345">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-346">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62fa5-346">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-347">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-348">Der aktuelle Zustand des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="62fa5-348">The current state of the logical device.</span></span> <span data-ttu-id="62fa5-349">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="62fa5-349">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-350">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="62fa5-350">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-351">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62fa5-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-352">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-353">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="62fa5-353">The scoping system's creation class name.</span></span> <span data-ttu-id="62fa5-354">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-354">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-355">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="62fa5-355">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-356">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62fa5-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-357">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-358">Der eindeutige Bezeichner für die Bereichs bezogene virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="62fa5-358">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="62fa5-359">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-359">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-360">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="62fa5-360">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-361">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="62fa5-361">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-362">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-363">Der Zeitpunkt, zu dem die virtuelle Maschine zuletzt eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="62fa5-363">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="62fa5-364">Diese Eigenschaft wird vom [**CIM- \_ Controller**](/windows/desktop/CIMWin32Prov/cim-controller)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-364">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-365">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="62fa5-365">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-366">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="62fa5-366">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-367">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-368">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="62fa5-368">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="62fa5-369">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="62fa5-369">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-370">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="62fa5-370">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-371">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="62fa5-371">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-372">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-373">Die Gesamtanzahl der Stunden, für die dieses Gerät eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="62fa5-373">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="62fa5-374">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="62fa5-374">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="62fa5-375">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="62fa5-375">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62fa5-376">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62fa5-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62fa5-377">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62fa5-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62fa5-378">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="62fa5-378">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="62fa5-379">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="62fa5-379">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="62fa5-380">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62fa5-380">Remarks</span></span>

<span data-ttu-id="62fa5-381">Der Zugriff auf die **MSVM- \_ idecontroller** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="62fa5-381">Access to the **Msvm\_IDEController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="62fa5-382">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="62fa5-382">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="62fa5-383">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62fa5-383">Requirements</span></span>



| <span data-ttu-id="62fa5-384">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62fa5-384">Requirement</span></span> | <span data-ttu-id="62fa5-385">Wert</span><span class="sxs-lookup"><span data-stu-id="62fa5-385">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62fa5-386">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="62fa5-386">Minimum supported client</span></span><br/> | <span data-ttu-id="62fa5-387">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="62fa5-387">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="62fa5-388">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="62fa5-388">Minimum supported server</span></span><br/> | <span data-ttu-id="62fa5-389">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="62fa5-389">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="62fa5-390">Namespace</span><span class="sxs-lookup"><span data-stu-id="62fa5-390">Namespace</span></span><br/>                | <span data-ttu-id="62fa5-391">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="62fa5-391">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="62fa5-392">MOF</span><span class="sxs-lookup"><span data-stu-id="62fa5-392">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62fa5-393"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="62fa5-393"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="62fa5-394">DLL</span><span class="sxs-lookup"><span data-stu-id="62fa5-394">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62fa5-395"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="62fa5-395"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="62fa5-396">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62fa5-396">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62fa5-397">**CIM- \_ idecontroller**</span><span class="sxs-lookup"><span data-stu-id="62fa5-397">**CIM\_IDEController**</span></span>](cim-idecontroller.md)
</dt> <dt>

<span data-ttu-id="62fa5-398">[**CIM- \_ idecontroller**](/previous-versions//cc136863(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="62fa5-398">[**CIM\_IDEController**](/previous-versions//cc136863(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="62fa5-399">Speicher Klassen</span><span class="sxs-lookup"><span data-stu-id="62fa5-399">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

