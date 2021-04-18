---
description: Stellt die Funktionen und die Verwaltung des seriellen Controllers dar.
ms.assetid: 0F4DCF98-8EE4-4005-ADD5-BA23CB4CBE82
title: Msvm_SerialController-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialController
- Msvm_SerialController.SetPowerState
- Msvm_SerialController.EnableDevice
- Msvm_SerialController.OnlineDevice
- Msvm_SerialController.QuiesceDevice
- Msvm_SerialController.SaveProperties
- Msvm_SerialController.RestoreProperties
- Msvm_SerialController.InstanceID
- Msvm_SerialController.Caption
- Msvm_SerialController.Description
- Msvm_SerialController.ElementName
- Msvm_SerialController.InstallDate
- Msvm_SerialController.Name
- Msvm_SerialController.OperationalStatus
- Msvm_SerialController.StatusDescriptions
- Msvm_SerialController.Status
- Msvm_SerialController.HealthState
- Msvm_SerialController.CommunicationStatus
- Msvm_SerialController.DetailedStatus
- Msvm_SerialController.OperatingStatus
- Msvm_SerialController.PrimaryStatus
- Msvm_SerialController.EnabledState
- Msvm_SerialController.OtherEnabledState
- Msvm_SerialController.RequestedState
- Msvm_SerialController.EnabledDefault
- Msvm_SerialController.TimeOfLastStateChange
- Msvm_SerialController.AvailableRequestedStates
- Msvm_SerialController.TransitioningToState
- Msvm_SerialController.SystemCreationClassName
- Msvm_SerialController.SystemName
- Msvm_SerialController.CreationClassName
- Msvm_SerialController.DeviceID
- Msvm_SerialController.PowerManagementSupported
- Msvm_SerialController.PowerManagementCapabilities
- Msvm_SerialController.Availability
- Msvm_SerialController.StatusInfo
- Msvm_SerialController.LastErrorCode
- Msvm_SerialController.ErrorDescription
- Msvm_SerialController.ErrorCleared
- Msvm_SerialController.OtherIdentifyingInfo
- Msvm_SerialController.PowerOnHours
- Msvm_SerialController.TotalPowerOnHours
- Msvm_SerialController.IdentifyingDescriptions
- Msvm_SerialController.AdditionalAvailability
- Msvm_SerialController.MaxQuiesceTime
- Msvm_SerialController.TimeOfLastReset
- Msvm_SerialController.ProtocolSupported
- Msvm_SerialController.MaxNumberControlled
- Msvm_SerialController.ProtocolDescription
- Msvm_SerialController.Capabilities
- Msvm_SerialController.CapabilityDescriptions
- Msvm_SerialController.MaxBaudRate
- Msvm_SerialController.Security
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d3f1bbc9dabe078751d58875745a789895cb4c9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347232"
---
# <a name="msvm_serialcontroller-class"></a><span data-ttu-id="ab94d-103">MSVM \_ SerialController-Klasse</span><span class="sxs-lookup"><span data-stu-id="ab94d-103">Msvm\_SerialController class</span></span>

<span data-ttu-id="ab94d-104">Stellt die Funktionen und die Verwaltung des seriellen Controllers dar.</span><span class="sxs-lookup"><span data-stu-id="ab94d-104">Represents the capabilities and management of the serial controller.</span></span> <span data-ttu-id="ab94d-105">Serielle Controller sind logische Geräte, die immer auf einem virtuellen Computer vorhanden sind und daher nicht über einen Ressourcenpool zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="ab94d-105">Serial controllers are logical devices that are always present in a virtual machine, and thus are not allocated through a resource pool.</span></span> <span data-ttu-id="ab94d-106">Eine Instanz eines seriellen Controllers ist immer auf einem virtuellen Computer vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ab94d-106">One serial controller instance is always present in a virtual machine.</span></span> <span data-ttu-id="ab94d-107">Serielle Controller verfügen über eine Fixed-Anzahl von Port Instanzen.</span><span class="sxs-lookup"><span data-stu-id="ab94d-107">Serial controllers have a fixed number of port instances.</span></span> <span data-ttu-id="ab94d-108">Diese Implementierung unterstützt zwei Ports pro Controller.</span><span class="sxs-lookup"><span data-stu-id="ab94d-108">This implementation supports two ports per controller.</span></span>

> [!Note]  
> <span data-ttu-id="ab94d-109">Serielle Controller sind bei [virtuellen Maschinen der Generation 2](virtualization-glossary.md)optional.</span><span class="sxs-lookup"><span data-stu-id="ab94d-109">Serial controllers are optional in [generation 2 virtual machines](virtualization-glossary.md).</span></span>

 

<span data-ttu-id="ab94d-110">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ab94d-110">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab94d-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab94d-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialController : CIM_SerialController
{
  string   InstanceID;
  string   Caption = "Serial Controller";
  string   Description = "Microsoft Virtual Serial Controller";
  string   ElementName = "Serial Controller";
  datetime InstallDate;
  string   Name = "Serial Controller";
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
  string   CreationClassName = "Msvm_SerialController";
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
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 26;
  uint32   MaxNumberControlled = 2;
  string   ProtocolDescription;
  uint16   Capabilities[] = { 5 };
  string   CapabilityDescriptions[] = { "16550 compatible" };
  uint32   MaxBaudRate = 115200;
  uint16   Security = 3;
};
```

## <a name="members"></a><span data-ttu-id="ab94d-112">Member</span><span class="sxs-lookup"><span data-stu-id="ab94d-112">Members</span></span>

<span data-ttu-id="ab94d-113">Die **MSVM \_ SerialController** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ab94d-113">The **Msvm\_SerialController** class has these types of members:</span></span>

-   [<span data-ttu-id="ab94d-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="ab94d-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="ab94d-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ab94d-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ab94d-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="ab94d-116">Methods</span></span>

<span data-ttu-id="ab94d-117">Die **MSVM \_ SerialController** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="ab94d-117">The **Msvm\_SerialController** class has these methods.</span></span>



| <span data-ttu-id="ab94d-118">Methode</span><span class="sxs-lookup"><span data-stu-id="ab94d-118">Method</span></span>                                                                 | <span data-ttu-id="ab94d-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ab94d-119">Description</span></span>                              |
|:-----------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="ab94d-120">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="ab94d-120">**EnableDevice**</span></span>                                                       | <span data-ttu-id="ab94d-121">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-121">This method is not supported.</span></span><br/> |
| <span data-ttu-id="ab94d-122">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="ab94d-122">**OnlineDevice**</span></span>                                                       | <span data-ttu-id="ab94d-123">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-123">This method is not supported.</span></span><br/> |
| <span data-ttu-id="ab94d-124">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="ab94d-124">**QuiesceDevice**</span></span>                                                      | <span data-ttu-id="ab94d-125">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-125">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="ab94d-126">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="ab94d-126">**RequestStateChange**</span></span>](msvm-serialcontroller-requeststatechange.md) | <span data-ttu-id="ab94d-127">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="ab94d-127">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="ab94d-128">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="ab94d-128">**Reset**</span></span>](msvm-serialcontroller-reset.md)                           | <span data-ttu-id="ab94d-129">Setzt das Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="ab94d-129">Resets the device.</span></span><br/>            |
| <span data-ttu-id="ab94d-130">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="ab94d-130">**RestoreProperties**</span></span>                                                  | <span data-ttu-id="ab94d-131">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-131">This method is not supported.</span></span><br/> |
| <span data-ttu-id="ab94d-132">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="ab94d-132">**SaveProperties**</span></span>                                                     | <span data-ttu-id="ab94d-133">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-133">This method is not supported.</span></span><br/> |
| <span data-ttu-id="ab94d-134">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="ab94d-134">**SetPowerState**</span></span>                                                      | <span data-ttu-id="ab94d-135">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-135">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ab94d-136">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ab94d-136">Properties</span></span>

<span data-ttu-id="ab94d-137">Die **MSVM \_ SerialController** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ab94d-137">The **Msvm\_SerialController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ab94d-138">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="ab94d-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-139">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="ab94d-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-141">Alle zusätzlichen Verfügbarkeit und der Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="ab94d-141">Any additional availability and status of the device.</span></span> <span data-ttu-id="ab94d-142">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="ab94d-143">Wert</span><span class="sxs-lookup"><span data-stu-id="ab94d-143">Value</span></span>                                                                            | <span data-ttu-id="ab94d-144">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ab94d-144">Meaning</span></span>                   |
|----------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="ab94d-145"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="ab94d-145"><dt>{ 6 }</dt></span></span> </dl> |                           |
| <dl> <span data-ttu-id="ab94d-146"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="ab94d-146"><dt>6</dt></span></span> </dl>     | <span data-ttu-id="ab94d-147">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="ab94d-147">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ab94d-148">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="ab94d-148">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-149">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ab94d-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-151">Die primäre Verfügbarkeit und den Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="ab94d-151">The primary availability and status of the device.</span></span> <span data-ttu-id="ab94d-152">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-152">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="ab94d-153">Wert</span><span class="sxs-lookup"><span data-stu-id="ab94d-153">Value</span></span>                                                                        | <span data-ttu-id="ab94d-154">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ab94d-154">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="ab94d-155"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="ab94d-155"><dt>6</dt></span></span> </dl> | <span data-ttu-id="ab94d-156">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="ab94d-156">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ab94d-157">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="ab94d-157">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-158">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="ab94d-158">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-160">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="ab94d-160">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="ab94d-161">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ab94d-161">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-162">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="ab94d-162">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-163">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="ab94d-163">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-165">Die Pufferung und andere Funktionen des seriellen Controllers, die möglicherweise in der Chip Hardware enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="ab94d-165">The buffering and other capabilities of the serial controller that might be inherent in the chip hardware.</span></span> <span data-ttu-id="ab94d-166">Diese Eigenschaft wird von [**CIM \_ SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-166">This property is inherited from [**CIM\_SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-167">**Capabilitybeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="ab94d-167">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-168">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="ab94d-168">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-170">Ein Array von Freiform-Zeichen folgen, das Ausführlichere Erläuterungen zu allen seriellen Controller Features bereitstellt **, die im Funktions Array angegeben** sind.</span><span class="sxs-lookup"><span data-stu-id="ab94d-170">An array of free-form strings that provides more detailed explanations for any of the serial controller features that are indicated in the **Capabilities** array.</span></span> <span data-ttu-id="ab94d-171">Diese Eigenschaft wird von [**CIM \_ SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-171">This property is inherited from [**CIM\_SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-172">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ab94d-172">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-173">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ab94d-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-175">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="ab94d-175">A short description of the object.</span></span> <span data-ttu-id="ab94d-176">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-176">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-177">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="ab94d-177">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-178">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ab94d-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-180">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="ab94d-180">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="ab94d-181">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="ab94d-181">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ab94d-182">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-182">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ab94d-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="ab94d-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="ab94d-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-185"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="ab94d-185"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-186"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="ab94d-186"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-187"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="ab94d-187"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="ab94d-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="ab94d-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ab94d-190">)</span><span class="sxs-lookup"><span data-stu-id="ab94d-190">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ab94d-191">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="ab94d-191">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-192">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ab94d-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-194">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ab94d-194">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="ab94d-195">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-195">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-196">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ab94d-196">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-197">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ab94d-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-199">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="ab94d-199">A description of the object.</span></span> <span data-ttu-id="ab94d-200">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-201">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="ab94d-201">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-202">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ab94d-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-204">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="ab94d-204">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="ab94d-205">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="ab94d-205">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ab94d-206">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-206">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ab94d-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="ab94d-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="ab94d-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="ab94d-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="ab94d-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="ab94d-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="ab94d-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="ab94d-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="ab94d-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ab94d-215">)</span><span class="sxs-lookup"><span data-stu-id="ab94d-215">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ab94d-216">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="ab94d-216">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-217">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ab94d-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-218">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-219">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf "Microsoft:" festgelegt *<GUID>* .</span><span class="sxs-lookup"><span data-stu-id="ab94d-219">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*<GUID>*".</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-220">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ab94d-220">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-221">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ab94d-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-222">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-223">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-223">A display name for the object.</span></span> <span data-ttu-id="ab94d-224">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-224">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-225">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="ab94d-225">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-226">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ab94d-226">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-227">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-228">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="ab94d-228">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="ab94d-229">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-229">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="ab94d-230">Wert</span><span class="sxs-lookup"><span data-stu-id="ab94d-230">Value</span></span>                                                                        | <span data-ttu-id="ab94d-231">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ab94d-231">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="ab94d-232"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ab94d-232"><dt>2</dt></span></span> </dl> | <span data-ttu-id="ab94d-233">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="ab94d-233">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ab94d-234">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="ab94d-234">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-235">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ab94d-235">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-236">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-237">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="ab94d-237">The enabled and disabled states of an element.</span></span> <span data-ttu-id="ab94d-238">Sie kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben.</span><span class="sxs-lookup"><span data-stu-id="ab94d-238">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="ab94d-239">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-239">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="ab94d-240">Wert</span><span class="sxs-lookup"><span data-stu-id="ab94d-240">Value</span></span>                                                                        | <span data-ttu-id="ab94d-241">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ab94d-241">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="ab94d-242"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="ab94d-242"><dt>5</dt></span></span> </dl> | <span data-ttu-id="ab94d-243">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="ab94d-243">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ab94d-244">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="ab94d-244">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-245">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ab94d-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-246">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-247">Gibt an, ob der in der **LastErrorCode** -Eigenschaft gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="ab94d-247">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="ab94d-248">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ab94d-248">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-249">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="ab94d-249">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-250">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ab94d-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-251">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-252">Eine Zeichenfolge, die weitere Informationen über den in der **LastErrorCode** -Eigenschaft aufgezeichneten Fehler sowie Informationen zu ggf. durchzuführenden Maßnahmen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-252">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="ab94d-253">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ab94d-253">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-254">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="ab94d-254">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-255">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ab94d-255">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-256">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-257">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="ab94d-257">The current health of the element.</span></span> <span data-ttu-id="ab94d-258">Dadurch wird die Integrität dieses Elements, jedoch nicht notwendigerweise der seiner unter Komponenten ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-258">This expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="ab94d-259">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="ab94d-259">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="ab94d-260">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-260">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-261">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ab94d-261">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-262">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="ab94d-262">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-263">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-264">Ein Array von Freiform-Zeichen folgen, die Erklärungen und Details hinter den Einträgen im Eigenschafts Array " **OtherIdentifyingInfo** " bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ab94d-264">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="ab94d-265">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-265">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-266">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ab94d-266">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-267">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="ab94d-267">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-268">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-269">Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="ab94d-269">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="ab94d-270">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-270">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-271">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ab94d-271">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-272">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ab94d-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-273">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-274">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="ab94d-274">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-275">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="ab94d-275">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ab94d-276">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-276">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-277">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="ab94d-277">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-278">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab94d-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-279">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-280">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="ab94d-280">The last error code reported by the logical device.</span></span> <span data-ttu-id="ab94d-281">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ab94d-281">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-282">**Maxbaudrate**</span><span class="sxs-lookup"><span data-stu-id="ab94d-282">**MaxBaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-283">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab94d-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-284">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-285">Die maximale Baudrate (in Bits pro Sekunde), die vom seriellen Controller unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="ab94d-285">The maximum baud rate, in bits per second, that is supported by the serial controller.</span></span> <span data-ttu-id="ab94d-286">Diese Eigenschaft wird von [**CIM \_ SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-286">This property is inherited from [**CIM\_SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-287">**Maxnuma**</span><span class="sxs-lookup"><span data-stu-id="ab94d-287">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-288">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab94d-288">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-289">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-290">Die maximale Anzahl direkt Adressier barer Entitäten, die von diesem Controller unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="ab94d-290">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="ab94d-291">Wenn die Zahl unbekannt oder unbegrenzt ist, sollte der Wert 0 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab94d-291">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="ab94d-292">Das Protokoll, das vom Controller für den Zugriff auf gesteuerte Geräte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ab94d-292">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="ab94d-293">Diese Eigenschaft wird vom [**CIM- \_ Controller**](/windows/desktop/CIMWin32Prov/cim-controller)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-293">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-294">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="ab94d-294">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-295">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ab94d-295">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-296">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-297">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="ab94d-297">This property has been deprecated.</span></span> <span data-ttu-id="ab94d-298">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ab94d-298">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-299">**Name**</span><span class="sxs-lookup"><span data-stu-id="ab94d-299">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-300">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ab94d-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-301">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-302">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="ab94d-302">The label by which the object is known.</span></span> <span data-ttu-id="ab94d-303">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und entspricht der Element **Name** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ab94d-303">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-304">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="ab94d-304">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-305">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ab94d-305">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-306">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-307">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ab94d-307">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="ab94d-308">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="ab94d-308">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ab94d-309">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-309">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ab94d-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="ab94d-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-311"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="ab94d-311"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-312"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="ab94d-312"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-313"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="ab94d-313"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-314"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="ab94d-314"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-315"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="ab94d-315"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-316"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="ab94d-316"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-317"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="ab94d-317"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-318"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="ab94d-318"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-319"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="ab94d-319"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-320"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="ab94d-320"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-321"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="ab94d-321"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-322"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="ab94d-322"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-323"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="ab94d-323"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-324"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="ab94d-324"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-325"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="ab94d-325"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-326"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="ab94d-326"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-327"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="ab94d-327"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-328"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="ab94d-328"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ab94d-329">)</span><span class="sxs-lookup"><span data-stu-id="ab94d-329">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ab94d-330">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="ab94d-330">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-331">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="ab94d-331">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-332">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-333">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="ab94d-333">The current statuses of the object.</span></span> <span data-ttu-id="ab94d-334">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-334">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-335">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="ab94d-335">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-336">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ab94d-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-337">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-338">Der aktivierte oder deaktivierte Status des Elements, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ab94d-338">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="ab94d-339">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="ab94d-339">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="ab94d-340">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-340">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-341">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="ab94d-341">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-342">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="ab94d-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-343">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-344">Alle zusätzlichen Daten über Geräte-ID-Informationen, die zur Identifizierung eines logischen Geräts verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="ab94d-344">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="ab94d-345">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-345">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-346">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="ab94d-346">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-347">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="ab94d-347">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-348">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-349">Die Energie Verwaltungsfunktionen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="ab94d-349">The power management capabilities of the device.</span></span> <span data-ttu-id="ab94d-350">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ab94d-350">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-351">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="ab94d-351">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-352">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ab94d-352">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-353">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-354">Gibt an, ob das Gerät Energie gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="ab94d-354">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="ab94d-355">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ab94d-355">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-356">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="ab94d-356">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-357">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ab94d-357">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-358">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-359">Gibt an, wie viele aufeinanderfolgende Stunden dieses Gerät seit dem letzten Strom Umgebung eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="ab94d-359">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="ab94d-360">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ab94d-360">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-361">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="ab94d-361">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-362">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ab94d-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-363">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-364">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="ab94d-364">Provides high level status information.</span></span> <span data-ttu-id="ab94d-365">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ab94d-365">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="ab94d-366">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="ab94d-366">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ab94d-367">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-367">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ab94d-368"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="ab94d-368"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-369"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="ab94d-369"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-370"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="ab94d-370"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-371"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="ab94d-371"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-372"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="ab94d-372"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-373"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="ab94d-373"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ab94d-374">)</span><span class="sxs-lookup"><span data-stu-id="ab94d-374">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ab94d-375">**Protocoldescription**</span><span class="sxs-lookup"><span data-stu-id="ab94d-375">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-376">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ab94d-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-377">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-378">Eine Zeichenfolge, die weitere Informationen bereitstellt, die mit dem vom Controller unterstützten Protokoll verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="ab94d-378">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="ab94d-379">Diese Eigenschaft wird vom [**CIM- \_ Controller**](/windows/desktop/CIMWin32Prov/cim-controller)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-379">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-380">**Protocolsupported**</span><span class="sxs-lookup"><span data-stu-id="ab94d-380">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-381">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ab94d-381">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-382">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-383">Das Protokoll, das vom Controller für den Zugriff auf gesteuerte Geräte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ab94d-383">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="ab94d-384">Diese Eigenschaft wird vom [**CIM- \_ Controller**](/windows/desktop/CIMWin32Prov/cim-controller)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-384">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>



| <span data-ttu-id="ab94d-385">Wert</span><span class="sxs-lookup"><span data-stu-id="ab94d-385">Value</span></span>                                                                         | <span data-ttu-id="ab94d-386">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ab94d-386">Meaning</span></span>             |
|-------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="ab94d-387"><dt>26</dt></span><span class="sxs-lookup"><span data-stu-id="ab94d-387"><dt>26</dt></span></span> </dl> | <span data-ttu-id="ab94d-388">IEEE-488</span><span class="sxs-lookup"><span data-stu-id="ab94d-388">IEEE-488</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ab94d-389">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="ab94d-389">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-390">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ab94d-390">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-391">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-392">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="ab94d-392">The last requested or desired state for the element.</span></span> <span data-ttu-id="ab94d-393">Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-393">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="ab94d-394">Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuell aktivierten oder deaktivierten Zustände zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="ab94d-394">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="ab94d-395">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-395">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="ab94d-396">Wert</span><span class="sxs-lookup"><span data-stu-id="ab94d-396">Value</span></span>                                                                         | <span data-ttu-id="ab94d-397">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ab94d-397">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="ab94d-398"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="ab94d-398"><dt>12</dt></span></span> </dl> | <span data-ttu-id="ab94d-399">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="ab94d-399">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ab94d-400">**Security**</span><span class="sxs-lookup"><span data-stu-id="ab94d-400">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-401">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ab94d-401">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-402">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-403">Die Betriebssicherheit für den Controller.</span><span class="sxs-lookup"><span data-stu-id="ab94d-403">The operational security for the controller.</span></span> <span data-ttu-id="ab94d-404">Diese Eigenschaft wird von [**CIM \_ SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-404">This property is inherited from [**CIM\_SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span></span>



| <span data-ttu-id="ab94d-405">Wert</span><span class="sxs-lookup"><span data-stu-id="ab94d-405">Value</span></span>                                                                        | <span data-ttu-id="ab94d-406">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ab94d-406">Meaning</span></span>         |
|------------------------------------------------------------------------------|-----------------|
| <dl> <span data-ttu-id="ab94d-407"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ab94d-407"><dt>3</dt></span></span> </dl> | <span data-ttu-id="ab94d-408">Keine</span><span class="sxs-lookup"><span data-stu-id="ab94d-408">None</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ab94d-409">**Status**</span><span class="sxs-lookup"><span data-stu-id="ab94d-409">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-410">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ab94d-410">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-411">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-412">Der aktuelle Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="ab94d-412">The current status of the object.</span></span> <span data-ttu-id="ab94d-413">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ab94d-413">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-414">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="ab94d-414">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-415">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="ab94d-415">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-416">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-417">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="ab94d-417">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="ab94d-418">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-418">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-419">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="ab94d-419">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-420">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ab94d-420">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-421">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-422">Der aktuelle Zustand des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="ab94d-422">The current state of the logical device.</span></span> <span data-ttu-id="ab94d-423">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ab94d-423">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-424">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="ab94d-424">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-425">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ab94d-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-426">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-427">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="ab94d-427">The scoping system's creation class name.</span></span> <span data-ttu-id="ab94d-428">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-428">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-429">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="ab94d-429">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-430">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ab94d-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-431">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-432">Der eindeutige Bezeichner für die Bereichs bezogene virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="ab94d-432">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="ab94d-433">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-433">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-434">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="ab94d-434">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-435">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="ab94d-435">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-436">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-437">Der letzte Zeitpunkt, an dem der Controller eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="ab94d-437">The last time the controller was powered on.</span></span> <span data-ttu-id="ab94d-438">Diese Eigenschaft wird vom [**CIM- \_ Controller**](/windows/desktop/CIMWin32Prov/cim-controller)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-438">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-439">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="ab94d-439">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-440">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="ab94d-440">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-441">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-442">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="ab94d-442">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="ab94d-443">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ab94d-443">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-444">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="ab94d-444">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-445">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ab94d-445">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-446">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-447">Die Gesamtanzahl der Stunden, für die dieses Gerät eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="ab94d-447">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="ab94d-448">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ab94d-448">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ab94d-449">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="ab94d-449">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab94d-450">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ab94d-450">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ab94d-451">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab94d-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab94d-452">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="ab94d-452">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="ab94d-453">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ab94d-453">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab94d-454">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab94d-454">Remarks</span></span>

<span data-ttu-id="ab94d-455">Der Zugriff auf die **MSVM \_ SerialController** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="ab94d-455">Access to the **Msvm\_SerialController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ab94d-456">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="ab94d-456">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab94d-457">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab94d-457">Requirements</span></span>



| <span data-ttu-id="ab94d-458">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab94d-458">Requirement</span></span> | <span data-ttu-id="ab94d-459">Wert</span><span class="sxs-lookup"><span data-stu-id="ab94d-459">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab94d-460">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ab94d-460">Minimum supported client</span></span><br/> | <span data-ttu-id="ab94d-461">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ab94d-461">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ab94d-462">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ab94d-462">Minimum supported server</span></span><br/> | <span data-ttu-id="ab94d-463">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ab94d-463">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ab94d-464">Namespace</span><span class="sxs-lookup"><span data-stu-id="ab94d-464">Namespace</span></span><br/>                | <span data-ttu-id="ab94d-465">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="ab94d-465">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ab94d-466">MOF</span><span class="sxs-lookup"><span data-stu-id="ab94d-466">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab94d-467"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ab94d-467"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab94d-468">DLL</span><span class="sxs-lookup"><span data-stu-id="ab94d-468">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab94d-469"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ab94d-469"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ab94d-470">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab94d-470">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab94d-471">**CIM- \_ SerialController**</span><span class="sxs-lookup"><span data-stu-id="ab94d-471">**CIM\_SerialController**</span></span>](cim-serialcontroller.md)
</dt> <dt>

[<span data-ttu-id="ab94d-472">**CIM- \_ SerialController**</span><span class="sxs-lookup"><span data-stu-id="ab94d-472">**CIM\_SerialController**</span></span>](/windows/desktop/CIMWin32Prov/cim-serialcontroller)
</dt> <dt>

[<span data-ttu-id="ab94d-473">Serielle Geräteklassen</span><span class="sxs-lookup"><span data-stu-id="ab94d-473">Serial Devices Classes</span></span>](serial-devices-classes.md)
</dt> </dl>

 

