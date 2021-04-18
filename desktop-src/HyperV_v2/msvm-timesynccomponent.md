---
description: Stellt den Status des Zeit Synchronisierungs dienstanens dar, der für die Synchronisierung der Systemzeit eines virtuellen Computers mit der Systemzeit des Betriebssystems im Verwaltungs Betriebssystem zuständig ist.
ms.assetid: 551A81E9-E924-4A9C-965D-02FF25EE4A49
title: Msvm_TimeSyncComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TimeSyncComponent
- Msvm_TimeSyncComponent.SetPowerState
- Msvm_TimeSyncComponent.EnableDevice
- Msvm_TimeSyncComponent.OnlineDevice
- Msvm_TimeSyncComponent.QuiesceDevice
- Msvm_TimeSyncComponent.SaveProperties
- Msvm_TimeSyncComponent.RestoreProperties
- Msvm_TimeSyncComponent.InstanceID
- Msvm_TimeSyncComponent.Caption
- Msvm_TimeSyncComponent.Description
- Msvm_TimeSyncComponent.ElementName
- Msvm_TimeSyncComponent.InstallDate
- Msvm_TimeSyncComponent.Name
- Msvm_TimeSyncComponent.OperationalStatus
- Msvm_TimeSyncComponent.StatusDescriptions
- Msvm_TimeSyncComponent.Status
- Msvm_TimeSyncComponent.HealthState
- Msvm_TimeSyncComponent.CommunicationStatus
- Msvm_TimeSyncComponent.DetailedStatus
- Msvm_TimeSyncComponent.OperatingStatus
- Msvm_TimeSyncComponent.PrimaryStatus
- Msvm_TimeSyncComponent.EnabledState
- Msvm_TimeSyncComponent.OtherEnabledState
- Msvm_TimeSyncComponent.RequestedState
- Msvm_TimeSyncComponent.EnabledDefault
- Msvm_TimeSyncComponent.TimeOfLastStateChange
- Msvm_TimeSyncComponent.AvailableRequestedStates
- Msvm_TimeSyncComponent.TransitioningToState
- Msvm_TimeSyncComponent.SystemCreationClassName
- Msvm_TimeSyncComponent.SystemName
- Msvm_TimeSyncComponent.CreationClassName
- Msvm_TimeSyncComponent.DeviceID
- Msvm_TimeSyncComponent.PowerManagementSupported
- Msvm_TimeSyncComponent.PowerManagementCapabilities
- Msvm_TimeSyncComponent.Availability
- Msvm_TimeSyncComponent.StatusInfo
- Msvm_TimeSyncComponent.LastErrorCode
- Msvm_TimeSyncComponent.ErrorDescription
- Msvm_TimeSyncComponent.ErrorCleared
- Msvm_TimeSyncComponent.OtherIdentifyingInfo
- Msvm_TimeSyncComponent.PowerOnHours
- Msvm_TimeSyncComponent.TotalPowerOnHours
- Msvm_TimeSyncComponent.IdentifyingDescriptions
- Msvm_TimeSyncComponent.AdditionalAvailability
- Msvm_TimeSyncComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ea9a33d665a315861d9e6c51fd529f10f07b4aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347842"
---
# <a name="msvm_timesynccomponent-class"></a><span data-ttu-id="60909-103">MSVM \_ timesynccomponent-Klasse</span><span class="sxs-lookup"><span data-stu-id="60909-103">Msvm\_TimeSyncComponent class</span></span>

<span data-ttu-id="60909-104">Stellt den Status des Zeit Synchronisierungs dienstanens dar, der für die Synchronisierung der Systemzeit eines virtuellen Computers mit der Systemzeit des Betriebssystems im Verwaltungs Betriebssystem zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="60909-104">Represents the state of the time synchronization service, which is responsible for synchronizing the system time of a virtual machine with the system time of the operating system running in the management operating system.</span></span>

<span data-ttu-id="60909-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="60909-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="60909-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="60909-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TimeSyncComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "Time Synchronization";
  string   Description = "Microsoft Time Synchronization Service";
  string   ElementName = "Time Synchronization";
  datetime InstallDate;
  string   Name = "Time Synchronization";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = {"OK"};
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
  uint16   TransitioningToState = 12;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_TimeSyncComponent";
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
};
```

## <a name="members"></a><span data-ttu-id="60909-107">Member</span><span class="sxs-lookup"><span data-stu-id="60909-107">Members</span></span>

<span data-ttu-id="60909-108">Die **MSVM \_ timesynccomponent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="60909-108">The **Msvm\_TimeSyncComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="60909-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="60909-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="60909-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="60909-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="60909-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="60909-111">Methods</span></span>

<span data-ttu-id="60909-112">Die **MSVM \_ timesynccomponent** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="60909-112">The **Msvm\_TimeSyncComponent** class has these methods.</span></span>



| <span data-ttu-id="60909-113">Methode</span><span class="sxs-lookup"><span data-stu-id="60909-113">Method</span></span>                                                                  | <span data-ttu-id="60909-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60909-114">Description</span></span>                              |
|:------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="60909-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="60909-115">**EnableDevice**</span></span>                                                        | <span data-ttu-id="60909-116">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="60909-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="60909-117">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="60909-117">**OnlineDevice**</span></span>                                                        | <span data-ttu-id="60909-118">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="60909-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="60909-119">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="60909-119">**QuiesceDevice**</span></span>                                                       | <span data-ttu-id="60909-120">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="60909-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="60909-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="60909-121">**RequestStateChange**</span></span>](msvm-timesynccomponent-requeststatechange.md) | <span data-ttu-id="60909-122">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="60909-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="60909-123">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="60909-123">**Reset**</span></span>](msvm-timesynccomponent-reset.md)                           | <span data-ttu-id="60909-124">Setzt die Komponente zurück.</span><span class="sxs-lookup"><span data-stu-id="60909-124">Resets the component.</span></span><br/>         |
| <span data-ttu-id="60909-125">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="60909-125">**RestoreProperties**</span></span>                                                   | <span data-ttu-id="60909-126">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="60909-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="60909-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="60909-127">**SaveProperties**</span></span>                                                      | <span data-ttu-id="60909-128">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="60909-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="60909-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="60909-129">**SetPowerState**</span></span>                                                       | <span data-ttu-id="60909-130">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="60909-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="60909-131">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="60909-131">Properties</span></span>

<span data-ttu-id="60909-132">Die **MSVM \_ timesynccomponent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="60909-132">The **Msvm\_TimeSyncComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="60909-133">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="60909-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-134">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="60909-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="60909-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-136">Alle zusätzlichen Verfügbarkeit und der Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="60909-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="60909-137">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf 6 festgelegt (nicht zutreffend).</span><span class="sxs-lookup"><span data-stu-id="60909-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="60909-138">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="60909-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-139">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="60909-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="60909-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-141">Die primäre Verfügbarkeit und den Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="60909-141">The primary availability and status of the device.</span></span> <span data-ttu-id="60909-142">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60909-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="60909-143">Wert</span><span class="sxs-lookup"><span data-stu-id="60909-143">Value</span></span>                                                                        | <span data-ttu-id="60909-144">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="60909-144">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="60909-145"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="60909-145"><dt>6</dt></span></span> </dl> | <span data-ttu-id="60909-146">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="60909-146">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="60909-147">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="60909-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-148">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="60909-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="60909-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-150">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="60909-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="60909-151">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="60909-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="60909-152">**Caption**</span><span class="sxs-lookup"><span data-stu-id="60909-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60909-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60909-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-155">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="60909-155">A short description of the object.</span></span> <span data-ttu-id="60909-156">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60909-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="60909-157">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="60909-157">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-158">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="60909-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="60909-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-160">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="60909-160">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="60909-161">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="60909-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="60909-162">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60909-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="60909-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="60909-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="60909-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="60909-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="60909-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="60909-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="60909-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="60909-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="60909-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="60909-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="60909-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="60909-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="60909-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="60909-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="60909-170">)</span><span class="sxs-lookup"><span data-stu-id="60909-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="60909-171">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="60909-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-172">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60909-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60909-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-174">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="60909-174">The scoping system's creation class name.</span></span> <span data-ttu-id="60909-175">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60909-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="60909-176">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="60909-176">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60909-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60909-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-179">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="60909-179">A description of the object.</span></span> <span data-ttu-id="60909-180">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60909-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="60909-181">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="60909-181">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-182">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="60909-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="60909-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-184">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="60909-184">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="60909-185">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="60909-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="60909-186">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60909-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="60909-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="60909-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="60909-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="60909-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="60909-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="60909-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="60909-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="60909-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="60909-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="60909-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="60909-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="60909-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="60909-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="60909-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="60909-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="60909-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="60909-195">)</span><span class="sxs-lookup"><span data-stu-id="60909-195">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="60909-196">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="60909-196">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-197">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60909-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60909-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-199">Eine Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="60909-199">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="60909-200">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf "Microsoft:*VMGUID* \\ *GUID*" festgelegt, wobei *VMGUID* die **Name** -Eigenschaft der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Instanz ist, die diesem Gerät zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="60909-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*VMGUID*\\*GUID*" where *VMGUID* is the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) instance associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="60909-201">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="60909-201">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-202">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60909-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60909-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-204">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="60909-204">A display name for the object.</span></span> <span data-ttu-id="60909-205">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60909-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="60909-206">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="60909-206">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-207">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="60909-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="60909-208">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-209">Die Standard-oder Startkonfiguration eines Administrators für den **enabledstate** eines Elements.</span><span class="sxs-lookup"><span data-stu-id="60909-209">An administrator's default or startup configuration for the **EnabledState** of an element.</span></span> <span data-ttu-id="60909-210">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="60909-210">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="60909-211">Wert</span><span class="sxs-lookup"><span data-stu-id="60909-211">Value</span></span>                                                                        | <span data-ttu-id="60909-212">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="60909-212">Meaning</span></span>               |
|------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="60909-213"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="60909-213"><dt>7</dt></span></span> </dl> | <span data-ttu-id="60909-214">Kein Standardwert</span><span class="sxs-lookup"><span data-stu-id="60909-214">No Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="60909-215">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="60909-215">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-216">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="60909-216">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="60909-217">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-218">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="60909-218">The enabled and disabled states of an element.</span></span> <span data-ttu-id="60909-219">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) geerbt und ist entweder auf 2 (aktiviert) oder 3 (deaktiviert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="60909-219">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is either set to 2 (Enabled) or 3 (Disabled).</span></span>



| <span data-ttu-id="60909-220">Wert</span><span class="sxs-lookup"><span data-stu-id="60909-220">Value</span></span>                                                                        | <span data-ttu-id="60909-221">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="60909-221">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="60909-222"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="60909-222"><dt>2</dt></span></span> </dl> | <span data-ttu-id="60909-223">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="60909-223">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="60909-224"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="60909-224"><dt>3</dt></span></span> </dl> | <span data-ttu-id="60909-225">Disabled</span><span class="sxs-lookup"><span data-stu-id="60909-225">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="60909-226">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="60909-226">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-227">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="60909-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="60909-228">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-229">Gibt an, ob der in der **LastErrorCode** -Eigenschaft gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="60909-229">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="60909-230">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="60909-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="60909-231">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="60909-231">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-232">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60909-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60909-233">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-234">Eine Zeichenfolge, die weitere Informationen über den in der **LastErrorCode** -Eigenschaft aufgezeichneten Fehler sowie Informationen zu ggf. durchzuführenden Maßnahmen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="60909-234">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="60909-235">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="60909-235">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="60909-236">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="60909-236">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-237">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="60909-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="60909-238">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-239">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="60909-239">The current health of the element.</span></span> <span data-ttu-id="60909-240">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60909-240">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="60909-241">Wert</span><span class="sxs-lookup"><span data-stu-id="60909-241">Value</span></span>                                                                        | <span data-ttu-id="60909-242">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="60909-242">Meaning</span></span>       |
|------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="60909-243"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="60909-243"><dt>5</dt></span></span> </dl> | <span data-ttu-id="60909-244">OK</span><span class="sxs-lookup"><span data-stu-id="60909-244">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="60909-245">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="60909-245">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-246">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="60909-246">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="60909-247">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-248">Ein Array von Freiform-Zeichen folgen, die Erklärungen und Details hinter den Einträgen im Eigenschafts Array " **OtherIdentifyingInfo** " bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="60909-248">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="60909-249">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="60909-249">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="60909-250">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="60909-250">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-251">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="60909-251">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="60909-252">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-253">Das Datum und die Uhrzeit, zu denen der Integrations Dienst auf dem virtuellen Computer installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="60909-253">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="60909-254">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60909-254">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="60909-255">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="60909-255">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-256">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60909-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60909-257">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60909-258">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="60909-258">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="60909-259">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="60909-259">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="60909-260">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60909-260">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="60909-261">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="60909-261">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-262">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60909-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60909-263">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-264">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="60909-264">The last error code reported by the logical device.</span></span> <span data-ttu-id="60909-265">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="60909-265">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="60909-266">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="60909-266">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-267">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="60909-267">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="60909-268">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-269">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="60909-269">This property has been deprecated.</span></span> <span data-ttu-id="60909-270">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60909-270">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="60909-271">**Name**</span><span class="sxs-lookup"><span data-stu-id="60909-271">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-272">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60909-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60909-273">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-274">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="60909-274">The label by which the object is known.</span></span> <span data-ttu-id="60909-275">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60909-275">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="60909-276">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="60909-276">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-277">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="60909-277">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="60909-278">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-279">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="60909-279">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="60909-280">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="60909-280">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="60909-281">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60909-281">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="60909-282"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="60909-282"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="60909-283"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="60909-283"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="60909-284"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="60909-284"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="60909-285"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="60909-285"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="60909-286"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="60909-286"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="60909-287"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="60909-287"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="60909-288"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="60909-288"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="60909-289"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="60909-289"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="60909-290"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="60909-290"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="60909-291"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="60909-291"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="60909-292"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="60909-292"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="60909-293"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="60909-293"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="60909-294"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="60909-294"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="60909-295"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="60909-295"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="60909-296"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="60909-296"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="60909-297"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="60909-297"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="60909-298"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="60909-298"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="60909-299"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="60909-299"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="60909-300"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="60909-300"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="60909-301">)</span><span class="sxs-lookup"><span data-stu-id="60909-301">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="60909-302">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="60909-302">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-303">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="60909-303">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="60909-304">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-305">Der aktuelle Status des Elements.</span><span class="sxs-lookup"><span data-stu-id="60909-305">The current status of the element.</span></span> <span data-ttu-id="60909-306">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60909-306">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="60909-307">Im folgenden sind die möglichen Werte für den Wert der Eigenschaft **OperationalStatus** \[ 0 verfügbar \] .</span><span class="sxs-lookup"><span data-stu-id="60909-307">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>



| <span data-ttu-id="60909-308">Wert</span><span class="sxs-lookup"><span data-stu-id="60909-308">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="60909-309">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="60909-309">Meaning</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="60909-310"><dt>2,2</dt></span><span class="sxs-lookup"><span data-stu-id="60909-310"><dt>{ 2 }</dt></span></span> </dl>                                                                                                                                                                                                    |                                                                                                                                                                                                                                          |
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="60909-311"><dt>**OK**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="60909-311"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                                  | <span data-ttu-id="60909-312">Der Dienst wird normal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="60909-312">The service is operating normally.</span></span> <span data-ttu-id="60909-313">Die Eigenschaftswerte **OperationalStatus** \[ 1 \] und **Statusbeschreibungen** \[ 1 \] enthalten möglicherweise weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="60909-313">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                                               |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="60909-314"><dt></dt> Heruntergestuft <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="60909-314"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                                     | <span data-ttu-id="60909-315">Der Dienst wird normal ausgeführt, aber der Gast Dienst hat eine kompatible Kommunikationsprotokoll Version ausgehandelt.</span><span class="sxs-lookup"><span data-stu-id="60909-315">The service is operating normally but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="60909-316">Die Eigenschaftswerte **OperationalStatus** \[ 1 \] und **Statusbeschreibungen** \[ 1 \] enthalten möglicherweise weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="60909-316">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/> |
| <span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span><dl> <span data-ttu-id="60909-317"><dt>**Nicht BEHEB barer Fehler**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="60909-317"><dt>**Non-Recoverable Error**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="60909-318">Der Gast unterstützt keine kompatible Protokollversion.</span><span class="sxs-lookup"><span data-stu-id="60909-318">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="60909-319">Die Eigenschaftswerte **OperationalStatus** \[ 1 \] und **Statusbeschreibungen** \[ 1 \] enthalten möglicherweise weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="60909-319">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                        |
| <span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dl> <span data-ttu-id="60909-320"><dt>**Kein Kontakt**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="60909-320"><dt>**No Contact**</dt> <dt>12</dt></span></span> </dl>                                            | <span data-ttu-id="60909-321">Der Gast Dienst ist nicht installiert, oder er wurde noch nicht kontaktiert.</span><span class="sxs-lookup"><span data-stu-id="60909-321">The guest service is not installed or has not yet been contacted.</span></span><br/>                                                                                                                                                             |
| <span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span><dl> <span data-ttu-id="60909-322"><dt>**Verlorene Kommunikation**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="60909-322"><dt>**Lost Communication**</dt> <dt>13</dt></span></span> </dl>            | <span data-ttu-id="60909-323">Der Gast Dienst antwortet nicht mehr normal.</span><span class="sxs-lookup"><span data-stu-id="60909-323">The guest service is no longer responding normally.</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="60909-324">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="60909-324">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-325">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60909-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60909-326">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-327">Der aktivierte oder deaktivierte Status des Elements, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="60909-327">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="60909-328">Diese Eigenschaft muss auf **null** festgelegt werden, wenn die **enabledstate** -Eigenschaft einen anderen Wert als 1 hat.</span><span class="sxs-lookup"><span data-stu-id="60909-328">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="60909-329">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="60909-329">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="60909-330">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="60909-330">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-331">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="60909-331">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="60909-332">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-333">Alle zusätzlichen Daten über Geräte-ID-Informationen, die zur Identifizierung eines logischen Geräts verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="60909-333">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="60909-334">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="60909-334">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="60909-335">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="60909-335">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-336">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="60909-336">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="60909-337">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-338">Die Energie Verwaltungsfunktionen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="60909-338">The power management capabilities of the device.</span></span> <span data-ttu-id="60909-339">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="60909-339">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="60909-340">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="60909-340">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-341">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="60909-341">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="60909-342">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-343">Gibt an, ob das Gerät Energie gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="60909-343">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="60909-344">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="60909-344">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="60909-345">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="60909-345">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-346">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="60909-346">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="60909-347">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-348">Gibt an, wie viele aufeinanderfolgende Stunden dieses Gerät seit dem letzten Strom Umgebung eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="60909-348">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="60909-349">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="60909-349">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="60909-350">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="60909-350">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-351">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="60909-351">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="60909-352">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-353">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="60909-353">Provides high level status information.</span></span> <span data-ttu-id="60909-354">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="60909-354">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="60909-355">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="60909-355">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="60909-356">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60909-356">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="60909-357"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="60909-357"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="60909-358"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="60909-358"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="60909-359"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="60909-359"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="60909-360"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="60909-360"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="60909-361"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="60909-361"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="60909-362"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="60909-362"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="60909-363">)</span><span class="sxs-lookup"><span data-stu-id="60909-363">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="60909-364">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="60909-364">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-365">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="60909-365">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="60909-366">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-367">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="60909-367">The last requested or desired state for the element.</span></span> <span data-ttu-id="60909-368">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="60909-368">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="60909-369">Wert</span><span class="sxs-lookup"><span data-stu-id="60909-369">Value</span></span>                                                                         | <span data-ttu-id="60909-370">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="60909-370">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="60909-371"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="60909-371"><dt>12</dt></span></span> </dl> | <span data-ttu-id="60909-372">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="60909-372">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="60909-373">**Status**</span><span class="sxs-lookup"><span data-stu-id="60909-373">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-374">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60909-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60909-375">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-376">Eine Zeichenfolge, die den aktuellen Status des-Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="60909-376">A string that specifies the current status of the object.</span></span> <span data-ttu-id="60909-377">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="60909-377">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="60909-378">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="60909-378">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-379">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="60909-379">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="60909-380">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-381">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="60909-381">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="60909-382">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60909-382">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="60909-383">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="60909-383">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-384">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="60909-384">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="60909-385">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-386">Der aktuelle Zustand des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="60909-386">The current state of the logical device.</span></span> <span data-ttu-id="60909-387">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="60909-387">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="60909-388">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="60909-388">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-389">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60909-389">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60909-390">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-391">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="60909-391">The creation class name of the scoping system.</span></span> <span data-ttu-id="60909-392">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60909-392">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="60909-393">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="60909-393">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-394">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60909-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60909-395">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-396">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="60909-396">The name of the scoping system.</span></span> <span data-ttu-id="60909-397">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60909-397">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="60909-398">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="60909-398">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-399">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="60909-399">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="60909-400">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-401">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="60909-401">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="60909-402">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="60909-402">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="60909-403">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="60909-403">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-404">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="60909-404">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="60909-405">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-406">Die Gesamtanzahl der Stunden, für die dieses Gerät eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="60909-406">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="60909-407">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="60909-407">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="60909-408">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="60909-408">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60909-409">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="60909-409">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="60909-410">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60909-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60909-411">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="60909-411">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="60909-412">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="60909-412">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="60909-413">Wert</span><span class="sxs-lookup"><span data-stu-id="60909-413">Value</span></span>                                                                         | <span data-ttu-id="60909-414">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="60909-414">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="60909-415"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="60909-415"><dt>12</dt></span></span> </dl> | <span data-ttu-id="60909-416">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="60909-416">Not Applicable</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="60909-417">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60909-417">Remarks</span></span>

<span data-ttu-id="60909-418">Der Zugriff auf die **MSVM \_ timesynccomponent** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="60909-418">Access to the **Msvm\_TimeSyncComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="60909-419">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="60909-419">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="60909-420">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60909-420">Requirements</span></span>



| <span data-ttu-id="60909-421">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60909-421">Requirement</span></span> | <span data-ttu-id="60909-422">Wert</span><span class="sxs-lookup"><span data-stu-id="60909-422">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60909-423">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="60909-423">Minimum supported client</span></span><br/> | <span data-ttu-id="60909-424">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60909-424">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="60909-425">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="60909-425">Minimum supported server</span></span><br/> | <span data-ttu-id="60909-426">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60909-426">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="60909-427">Namespace</span><span class="sxs-lookup"><span data-stu-id="60909-427">Namespace</span></span><br/>                | <span data-ttu-id="60909-428">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="60909-428">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="60909-429">MOF</span><span class="sxs-lookup"><span data-stu-id="60909-429">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60909-430"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="60909-430"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="60909-431">DLL</span><span class="sxs-lookup"><span data-stu-id="60909-431">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60909-432"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="60909-432"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="60909-433">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60909-433">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60909-434">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="60909-434">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="60909-435">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="60909-435">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

