---
description: Stellt den Status des Diensts für das Herunterfahren dar, der einen Mechanismus zum Herunterfahren des Betriebssystems des virtuellen Computers von den Verwaltungs Schnittstellen auf dem Host System bereitstellt.
ms.assetid: E9BBB08C-A3FE-4226-A2CF-458706E759D6
title: Msvm_ShutdownComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent
- Msvm_ShutdownComponent.EnableDevice
- Msvm_ShutdownComponent.OnlineDevice
- Msvm_ShutdownComponent.QuiesceDevice
- Msvm_ShutdownComponent.RestoreProperties
- Msvm_ShutdownComponent.SaveProperties
- Msvm_ShutdownComponent.SetPowerState
- Msvm_ShutdownComponent.InstanceID
- Msvm_ShutdownComponent.Caption
- Msvm_ShutdownComponent.Description
- Msvm_ShutdownComponent.ElementName
- Msvm_ShutdownComponent.InstallDate
- Msvm_ShutdownComponent.Name
- Msvm_ShutdownComponent.OperationalStatus
- Msvm_ShutdownComponent.StatusDescriptions
- Msvm_ShutdownComponent.Status
- Msvm_ShutdownComponent.HealthState
- Msvm_ShutdownComponent.CommunicationStatus
- Msvm_ShutdownComponent.DetailedStatus
- Msvm_ShutdownComponent.OperatingStatus
- Msvm_ShutdownComponent.PrimaryStatus
- Msvm_ShutdownComponent.EnabledState
- Msvm_ShutdownComponent.OtherEnabledState
- Msvm_ShutdownComponent.RequestedState
- Msvm_ShutdownComponent.EnabledDefault
- Msvm_ShutdownComponent.TimeOfLastStateChange
- Msvm_ShutdownComponent.AvailableRequestedStates
- Msvm_ShutdownComponent.TransitioningToState
- Msvm_ShutdownComponent.SystemCreationClassName
- Msvm_ShutdownComponent.SystemName
- Msvm_ShutdownComponent.CreationClassName
- Msvm_ShutdownComponent.DeviceID
- Msvm_ShutdownComponent.PowerManagementSupported
- Msvm_ShutdownComponent.PowerManagementCapabilities
- Msvm_ShutdownComponent.Availability
- Msvm_ShutdownComponent.StatusInfo
- Msvm_ShutdownComponent.LastErrorCode
- Msvm_ShutdownComponent.ErrorDescription
- Msvm_ShutdownComponent.ErrorCleared
- Msvm_ShutdownComponent.OtherIdentifyingInfo
- Msvm_ShutdownComponent.PowerOnHours
- Msvm_ShutdownComponent.TotalPowerOnHours
- Msvm_ShutdownComponent.IdentifyingDescriptions
- Msvm_ShutdownComponent.AdditionalAvailability
- Msvm_ShutdownComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 49729568a1625b3df723b1b5b88cc1044b41e715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041950"
---
# <a name="msvm_shutdowncomponent-class"></a><span data-ttu-id="f8b97-103">MSVM \_ shutdowncomponent-Klasse</span><span class="sxs-lookup"><span data-stu-id="f8b97-103">Msvm\_ShutdownComponent class</span></span>

<span data-ttu-id="f8b97-104">Stellt den Status des Diensts für das Herunterfahren dar, der einen Mechanismus zum Herunterfahren des Betriebssystems des virtuellen Computers von den Verwaltungs Schnittstellen auf dem Host System bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-104">Represents the state of the shutdown service, which provides a mechanism to shut down the operating system of the virtual machine from the management interfaces on the host system.</span></span>

<span data-ttu-id="f8b97-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f8b97-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8b97-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8b97-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ShutdownComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "Shutdown";
  string   Description = "Microsoft Shutdown Service";
  string   ElementName = "Shutdown";
  datetime InstallDate;
  string   Name = "Shutdown";
  uint16   OperationalStatus[];
  string   StatusDescriptions[] = { "OK" };
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
  string   CreationClassName = "Msvm_ShutdownComponent";
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
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
};
```

## <a name="members"></a><span data-ttu-id="f8b97-107">Member</span><span class="sxs-lookup"><span data-stu-id="f8b97-107">Members</span></span>

<span data-ttu-id="f8b97-108">Die **MSVM \_ shutdowncomponent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f8b97-108">The **Msvm\_ShutdownComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="f8b97-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="f8b97-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="f8b97-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f8b97-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f8b97-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="f8b97-111">Methods</span></span>

<span data-ttu-id="f8b97-112">Die **MSVM \_ shutdowncomponent** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f8b97-112">The **Msvm\_ShutdownComponent** class has these methods.</span></span>



| <span data-ttu-id="f8b97-113">Methode</span><span class="sxs-lookup"><span data-stu-id="f8b97-113">Method</span></span>                                                                  | <span data-ttu-id="f8b97-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f8b97-114">Description</span></span>                                                                                        |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8b97-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="f8b97-115">**EnableDevice**</span></span>                                                        | <span data-ttu-id="f8b97-116">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-116">This method is not supported.</span></span><br/>                                                           |
| [<span data-ttu-id="f8b97-117">**Initiatereboot**</span><span class="sxs-lookup"><span data-stu-id="f8b97-117">**InitiateReboot**</span></span>](msvm-shutdowncomponent-initiatereboot.md)         | <span data-ttu-id="f8b97-118">Initiiert einen Neustart Vorgang des Betriebssystems auf der zugeordneten untergeordneten virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="f8b97-118">Initiates an operating system reboot operation on the associated child virtual machine.</span></span><br/> |
| [<span data-ttu-id="f8b97-119">**InitiateShutdown**</span><span class="sxs-lookup"><span data-stu-id="f8b97-119">**InitiateShutdown**</span></span>](msvm-shutdowncomponent-initiateshutdown.md)     | <span data-ttu-id="f8b97-120">Initiiert den Vorgang zum Herunterfahren des Betriebssystems auf der zugeordneten untergeordneten virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="f8b97-120">Initiates an operating system shutdown operation on associated child virtual machine.</span></span><br/>   |
| <span data-ttu-id="f8b97-121">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="f8b97-121">**OnlineDevice**</span></span>                                                        | <span data-ttu-id="f8b97-122">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-122">This method is not supported.</span></span><br/>                                                           |
| <span data-ttu-id="f8b97-123">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="f8b97-123">**QuiesceDevice**</span></span>                                                       | <span data-ttu-id="f8b97-124">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-124">This method is not supported.</span></span><br/>                                                           |
| [<span data-ttu-id="f8b97-125">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="f8b97-125">**RequestStateChange**</span></span>](msvm-shutdowncomponent-requeststatechange.md) | <span data-ttu-id="f8b97-126">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="f8b97-126">Requests a state change.</span></span><br/>                                                                |
| [<span data-ttu-id="f8b97-127">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="f8b97-127">**Reset**</span></span>](msvm-shutdowncomponent-reset.md)                           | <span data-ttu-id="f8b97-128">Setzt die Komponente zurück.</span><span class="sxs-lookup"><span data-stu-id="f8b97-128">Resets the component.</span></span><br/>                                                                   |
| <span data-ttu-id="f8b97-129">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="f8b97-129">**RestoreProperties**</span></span>                                                   | <span data-ttu-id="f8b97-130">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-130">This method is not supported.</span></span><br/>                                                           |
| <span data-ttu-id="f8b97-131">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="f8b97-131">**SaveProperties**</span></span>                                                      | <span data-ttu-id="f8b97-132">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-132">This method is not supported.</span></span><br/>                                                           |
| <span data-ttu-id="f8b97-133">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="f8b97-133">**SetPowerState**</span></span>                                                       | <span data-ttu-id="f8b97-134">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-134">This method is not supported.</span></span><br/>                                                           |



 

### <a name="properties"></a><span data-ttu-id="f8b97-135">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f8b97-135">Properties</span></span>

<span data-ttu-id="f8b97-136">Die **MSVM \_ shutdowncomponent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f8b97-136">The **Msvm\_ShutdownComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f8b97-137">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="f8b97-137">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-138">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="f8b97-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-140">Zusätzliche Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="f8b97-140">Additional availability and status of the device.</span></span> <span data-ttu-id="f8b97-141">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="f8b97-142">Wert</span><span class="sxs-lookup"><span data-stu-id="f8b97-142">Value</span></span>                                                                        | <span data-ttu-id="f8b97-143">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f8b97-143">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="f8b97-144"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="f8b97-144"><dt>6</dt></span></span> </dl> | <span data-ttu-id="f8b97-145">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="f8b97-145">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f8b97-146">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="f8b97-146">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-147">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8b97-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-149">Die primäre Verfügbarkeit und den Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="f8b97-149">The primary availability and status of the device.</span></span> <span data-ttu-id="f8b97-150">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8b97-150">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>



| <span data-ttu-id="f8b97-151">Wert</span><span class="sxs-lookup"><span data-stu-id="f8b97-151">Value</span></span>                                                                        | <span data-ttu-id="f8b97-152">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f8b97-152">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="f8b97-153"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="f8b97-153"><dt>6</dt></span></span> </dl> | <span data-ttu-id="f8b97-154">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="f8b97-154">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f8b97-155">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="f8b97-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-156">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="f8b97-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-158">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="f8b97-158">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="f8b97-159">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8b97-159">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f8b97-160">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f8b97-160">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-161">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f8b97-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-163">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="f8b97-163">A short description of the object.</span></span> <span data-ttu-id="f8b97-164">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-164">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f8b97-165">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="f8b97-165">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-166">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8b97-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-168">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="f8b97-168">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="f8b97-169">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="f8b97-169">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f8b97-170">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-170">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f8b97-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="f8b97-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="f8b97-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-173"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="f8b97-173"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-174"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="f8b97-174"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-175"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="f8b97-175"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="f8b97-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="f8b97-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f8b97-178">)</span><span class="sxs-lookup"><span data-stu-id="f8b97-178">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f8b97-179">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="f8b97-179">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-180">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f8b97-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-182">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="f8b97-182">The scoping system's creation class name.</span></span> <span data-ttu-id="f8b97-183">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-183">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f8b97-184">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f8b97-184">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-185">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f8b97-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-187">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="f8b97-187">A description of the object.</span></span> <span data-ttu-id="f8b97-188">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f8b97-189">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="f8b97-189">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-190">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8b97-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-192">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="f8b97-192">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="f8b97-193">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="f8b97-193">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f8b97-194">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f8b97-195"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="f8b97-195"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-196"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="f8b97-196"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-197"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="f8b97-197"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-198"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="f8b97-198"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-199"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="f8b97-199"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-200"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="f8b97-200"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="f8b97-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-202"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="f8b97-202"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f8b97-203">)</span><span class="sxs-lookup"><span data-stu-id="f8b97-203">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f8b97-204">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="f8b97-204">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-205">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f8b97-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-206">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-207">Eine Adresse oder andere identifizierende Informationen, um LogicalDevice eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="f8b97-207">An address or other identifying information to uniquely name the LogicalDevice.</span></span> <span data-ttu-id="f8b97-208">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf "Microsoft:*VMGUID* \\ *GUID*" festgelegt, wobei *VMGUID* die **Name** -Eigenschaft der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Instanz ist, die diesem Gerät zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f8b97-208">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*VMGUID*\\*GUID*" where *VMGUID* is the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) instance associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="f8b97-209">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f8b97-209">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-210">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f8b97-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-212">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-212">A display name for the object.</span></span> <span data-ttu-id="f8b97-213">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-213">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f8b97-214">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="f8b97-214">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-215">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8b97-215">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-216">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-217">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-217">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="f8b97-218">Wert</span><span class="sxs-lookup"><span data-stu-id="f8b97-218">Value</span></span>                                                                        | <span data-ttu-id="f8b97-219">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f8b97-219">Meaning</span></span>               |
|------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="f8b97-220"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="f8b97-220"><dt>7</dt></span></span> </dl> | <span data-ttu-id="f8b97-221">Kein Standardwert</span><span class="sxs-lookup"><span data-stu-id="f8b97-221">No Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f8b97-222">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="f8b97-222">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-223">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8b97-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-225">Der aktivierte Status des Elements.</span><span class="sxs-lookup"><span data-stu-id="f8b97-225">The enabled state of the element.</span></span> <span data-ttu-id="f8b97-226">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) geerbt und ist entweder auf 2 (aktiviert) oder 3 (deaktiviert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-226">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is either set to 2 (Enabled) or 3 (Disabled).</span></span>



| <span data-ttu-id="f8b97-227">Wert</span><span class="sxs-lookup"><span data-stu-id="f8b97-227">Value</span></span>                                                                        | <span data-ttu-id="f8b97-228">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f8b97-228">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="f8b97-229"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f8b97-229"><dt>2</dt></span></span> </dl> | <span data-ttu-id="f8b97-230">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="f8b97-230">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="f8b97-231"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f8b97-231"><dt>3</dt></span></span> </dl> | <span data-ttu-id="f8b97-232">Disabled</span><span class="sxs-lookup"><span data-stu-id="f8b97-232">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f8b97-233">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="f8b97-233">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-234">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f8b97-234">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-235">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-236">Gibt an, ob der in der **LastErrorCode** -Eigenschaft gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="f8b97-236">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="f8b97-237">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8b97-237">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f8b97-238">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="f8b97-238">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-239">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f8b97-239">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-240">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-241">Eine Zeichenfolge, die weitere Informationen über den in der **LastErrorCode** -Eigenschaft aufgezeichneten Fehler sowie Informationen zu ggf. durchzuführenden Maßnahmen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-241">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="f8b97-242">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8b97-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f8b97-243">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="f8b97-243">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-244">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8b97-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-245">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-246">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="f8b97-246">The current health of the element.</span></span> <span data-ttu-id="f8b97-247">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="f8b97-247">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="f8b97-248">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-248">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f8b97-249">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="f8b97-249">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-250">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="f8b97-250">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-251">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-252">Ein Array von Freiform-Zeichen folgen, die Erklärungen und Details hinter den Einträgen im " **OtherIdentifyingInfo** "-Array bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f8b97-252">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="f8b97-253">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8b97-253">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f8b97-254">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f8b97-254">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-255">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="f8b97-255">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-256">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-257">Das Datum und die Uhrzeit, zu denen der Integrations Dienst auf dem virtuellen Computer installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f8b97-257">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="f8b97-258">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-258">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f8b97-259">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f8b97-259">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-260">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f8b97-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-261">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-262">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="f8b97-262">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-263">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="f8b97-263">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="f8b97-264">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-264">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f8b97-265">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f8b97-265">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-266">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f8b97-266">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-267">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-268">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="f8b97-268">The last error code reported by the logical device.</span></span> <span data-ttu-id="f8b97-269">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8b97-269">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f8b97-270">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="f8b97-270">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-271">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f8b97-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-272">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-273">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="f8b97-273">This property has been deprecated.</span></span> <span data-ttu-id="f8b97-274">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-274">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f8b97-275">**Name**</span><span class="sxs-lookup"><span data-stu-id="f8b97-275">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-276">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f8b97-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-277">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-278">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="f8b97-278">The label by which the object is known.</span></span> <span data-ttu-id="f8b97-279">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-279">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f8b97-280">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="f8b97-280">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-281">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8b97-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-282">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-283">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f8b97-283">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="f8b97-284">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="f8b97-284">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f8b97-285">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-285">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f8b97-286"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="f8b97-286"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-287"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="f8b97-287"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-288"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="f8b97-288"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-289"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="f8b97-289"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-290"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="f8b97-290"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-291"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="f8b97-291"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-292"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="f8b97-292"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-293"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="f8b97-293"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-294"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="f8b97-294"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-295"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="f8b97-295"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-296"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="f8b97-296"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-297"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="f8b97-297"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-298"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="f8b97-298"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-299"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="f8b97-299"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-300"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="f8b97-300"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-301"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="f8b97-301"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-302"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="f8b97-302"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-303"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="f8b97-303"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-304"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="f8b97-304"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f8b97-305">)</span><span class="sxs-lookup"><span data-stu-id="f8b97-305">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f8b97-306">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="f8b97-306">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-307">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="f8b97-307">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-308">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-309">Der aktuelle Status des Elements.</span><span class="sxs-lookup"><span data-stu-id="f8b97-309">The current status of the element.</span></span> <span data-ttu-id="f8b97-310">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-310">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="f8b97-311">Im folgenden sind die möglichen Werte für den Wert der Eigenschaft **OperationalStatus** \[ 0 verfügbar \] .</span><span class="sxs-lookup"><span data-stu-id="f8b97-311">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>



| <span data-ttu-id="f8b97-312">Wert</span><span class="sxs-lookup"><span data-stu-id="f8b97-312">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="f8b97-313">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f8b97-313">Meaning</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="f8b97-314"><dt>**OK**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f8b97-314"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                                  | <span data-ttu-id="f8b97-315">Der Dienst wird normal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-315">The service is operating normally.</span></span> <span data-ttu-id="f8b97-316">Die Eigenschaftswerte **OperationalStatus** \[ 1 \] und **Statusbeschreibungen** \[ 1 \] enthalten möglicherweise weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="f8b97-316">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                                               |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="f8b97-317"><dt></dt> Heruntergestuft <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f8b97-317"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                                     | <span data-ttu-id="f8b97-318">Der Dienst wird normal ausgeführt, aber der Gast Dienst hat eine kompatible Kommunikationsprotokoll Version ausgehandelt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-318">The service is operating normally but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="f8b97-319">Die Eigenschaftswerte **OperationalStatus** \[ 1 \] und **Statusbeschreibungen** \[ 1 \] enthalten möglicherweise weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="f8b97-319">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/> |
| <span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span><dl> <span data-ttu-id="f8b97-320"><dt>**Nicht BEHEB barer Fehler**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="f8b97-320"><dt>**Non-Recoverable Error**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="f8b97-321">Der Gast unterstützt keine kompatible Protokollversion.</span><span class="sxs-lookup"><span data-stu-id="f8b97-321">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="f8b97-322">Die Eigenschaftswerte **OperationalStatus** \[ 1 \] und **Statusbeschreibungen** \[ 1 \] enthalten möglicherweise weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="f8b97-322">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                        |
| <span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dl> <span data-ttu-id="f8b97-323"><dt>**Kein Kontakt**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="f8b97-323"><dt>**No Contact**</dt> <dt>12</dt></span></span> </dl>                                            | <span data-ttu-id="f8b97-324">Der Gast Dienst ist nicht installiert, oder er wurde noch nicht kontaktiert.</span><span class="sxs-lookup"><span data-stu-id="f8b97-324">The guest service is not installed or has not yet been contacted.</span></span><br/>                                                                                                                                                             |
| <span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span><dl> <span data-ttu-id="f8b97-325"><dt>**Verlorene Kommunikation**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="f8b97-325"><dt>**Lost Communication**</dt> <dt>13</dt></span></span> </dl>            | <span data-ttu-id="f8b97-326">Der Gast Dienst antwortet nicht mehr normal.</span><span class="sxs-lookup"><span data-stu-id="f8b97-326">The guest service is no longer responding normally.</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="f8b97-327">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="f8b97-327">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-328">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f8b97-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-329">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-330">Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f8b97-330">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="f8b97-331">Diese Eigenschaft muss auf **null** festgelegt werden, wenn die **enabledstate** -Eigenschaft einen anderen Wert als 1 hat.</span><span class="sxs-lookup"><span data-stu-id="f8b97-331">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="f8b97-332">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-332">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f8b97-333">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="f8b97-333">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-334">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="f8b97-334">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-335">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-336">Alle zusätzlichen Daten über Geräte-ID-Informationen, die zur Identifizierung eines logischen Geräts verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="f8b97-336">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="f8b97-337">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-337">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f8b97-338">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="f8b97-338">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-339">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="f8b97-339">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-340">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-341">Die Energie Verwaltungsfunktionen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="f8b97-341">The power management capabilities of the device.</span></span> <span data-ttu-id="f8b97-342">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8b97-342">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f8b97-343">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="f8b97-343">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-344">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f8b97-344">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-345">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-346">Gibt an, ob das Gerät Energie gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f8b97-346">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="f8b97-347">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8b97-347">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f8b97-348">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="f8b97-348">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-349">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f8b97-349">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-350">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-351">Gibt an, wie viele aufeinanderfolgende Stunden dieses Gerät seit dem letzten Strom Umgebung eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="f8b97-351">The number of consecutive hours that this Device has been powered on since its last power cycle.</span></span> <span data-ttu-id="f8b97-352">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8b97-352">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f8b97-353">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="f8b97-353">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-354">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8b97-354">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-355">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-356">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="f8b97-356">Provides high level status information.</span></span> <span data-ttu-id="f8b97-357">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f8b97-357">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="f8b97-358">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="f8b97-358">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f8b97-359">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-359">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f8b97-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="f8b97-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-361"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="f8b97-361"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-362"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="f8b97-362"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-363"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="f8b97-363"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-364"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="f8b97-364"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-365"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="f8b97-365"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f8b97-366">)</span><span class="sxs-lookup"><span data-stu-id="f8b97-366">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f8b97-367">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="f8b97-367">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-368">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8b97-368">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-369">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-370">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="f8b97-370">The last requested or desired state for the element.</span></span> <span data-ttu-id="f8b97-371">Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-371">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="f8b97-372">Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuell aktivierten oder deaktivierten Zustände zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="f8b97-372">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="f8b97-373">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 12 (nicht zutreffend) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-373">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="f8b97-374">Wert</span><span class="sxs-lookup"><span data-stu-id="f8b97-374">Value</span></span>                                                                         | <span data-ttu-id="f8b97-375">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f8b97-375">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="f8b97-376"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="f8b97-376"><dt>12</dt></span></span> </dl> | <span data-ttu-id="f8b97-377">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="f8b97-377">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f8b97-378">**Status**</span><span class="sxs-lookup"><span data-stu-id="f8b97-378">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-379">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f8b97-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-380">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-381">Der aktuelle Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="f8b97-381">The current status of the object.</span></span> <span data-ttu-id="f8b97-382">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8b97-382">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f8b97-383">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="f8b97-383">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-384">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="f8b97-384">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-385">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-386">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="f8b97-386">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="f8b97-387">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-387">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f8b97-388">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="f8b97-388">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-389">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8b97-389">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-390">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-391">Der aktuelle Zustand des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="f8b97-391">The current state of the logical device.</span></span> <span data-ttu-id="f8b97-392">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8b97-392">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f8b97-393">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="f8b97-393">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-394">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f8b97-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-395">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-396">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="f8b97-396">The scoping system's creation class name.</span></span> <span data-ttu-id="f8b97-397">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-397">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f8b97-398">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="f8b97-398">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-399">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f8b97-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-400">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-401">Der eindeutige Bezeichner für die Bereichs bezogene virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="f8b97-401">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="f8b97-402">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-402">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f8b97-403">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="f8b97-403">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-404">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="f8b97-404">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-405">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-406">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="f8b97-406">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="f8b97-407">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="f8b97-407">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f8b97-408">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="f8b97-408">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-409">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f8b97-409">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-410">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-411">Die Gesamtanzahl der Stunden, für die dieses Gerät eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="f8b97-411">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="f8b97-412">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8b97-412">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f8b97-413">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="f8b97-413">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8b97-414">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8b97-414">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8b97-415">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f8b97-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8b97-416">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="f8b97-416">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="f8b97-417">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8b97-417">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f8b97-418">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8b97-418">Remarks</span></span>

<span data-ttu-id="f8b97-419">Der Zugriff auf die **MSVM \_ shutdowncomponent** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="f8b97-419">Access to the **Msvm\_ShutdownComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f8b97-420">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="f8b97-420">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8b97-421">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8b97-421">Requirements</span></span>



| <span data-ttu-id="f8b97-422">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f8b97-422">Requirement</span></span> | <span data-ttu-id="f8b97-423">Wert</span><span class="sxs-lookup"><span data-stu-id="f8b97-423">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8b97-424">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f8b97-424">Minimum supported client</span></span><br/> | <span data-ttu-id="f8b97-425">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8b97-425">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f8b97-426">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f8b97-426">Minimum supported server</span></span><br/> | <span data-ttu-id="f8b97-427">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8b97-427">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f8b97-428">Namespace</span><span class="sxs-lookup"><span data-stu-id="f8b97-428">Namespace</span></span><br/>                | <span data-ttu-id="f8b97-429">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="f8b97-429">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f8b97-430">MOF</span><span class="sxs-lookup"><span data-stu-id="f8b97-430">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8b97-431"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f8b97-431"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f8b97-432">DLL</span><span class="sxs-lookup"><span data-stu-id="f8b97-432">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8b97-433"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f8b97-433"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f8b97-434">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8b97-434">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8b97-435">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="f8b97-435">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="f8b97-436">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="f8b97-436">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

