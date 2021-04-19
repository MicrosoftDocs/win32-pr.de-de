---
description: Stellt den Status des Volumeschattenkopie-Dienst-Diensts (VSS) dar, der die VSS-Anforderer im Gast Betriebssystem implementiert.
ms.assetid: 4DD38929-1E3F-4105-BC1A-B367516F7B6E
title: Msvm_VssComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssComponent
- Msvm_VssComponent.SetPowerState
- Msvm_VssComponent.EnableDevice
- Msvm_VssComponent.OnlineDevice
- Msvm_VssComponent.QuiesceDevice
- Msvm_VssComponent.SaveProperties
- Msvm_VssComponent.RestoreProperties
- Msvm_VssComponent.InstanceID
- Msvm_VssComponent.Caption
- Msvm_VssComponent.Description
- Msvm_VssComponent.ElementName
- Msvm_VssComponent.InstallDate
- Msvm_VssComponent.Name
- Msvm_VssComponent.OperationalStatus
- Msvm_VssComponent.StatusDescriptions
- Msvm_VssComponent.Status
- Msvm_VssComponent.HealthState
- Msvm_VssComponent.CommunicationStatus
- Msvm_VssComponent.DetailedStatus
- Msvm_VssComponent.OperatingStatus
- Msvm_VssComponent.PrimaryStatus
- Msvm_VssComponent.EnabledState
- Msvm_VssComponent.OtherEnabledState
- Msvm_VssComponent.RequestedState
- Msvm_VssComponent.EnabledDefault
- Msvm_VssComponent.TimeOfLastStateChange
- Msvm_VssComponent.AvailableRequestedStates
- Msvm_VssComponent.TransitioningToState
- Msvm_VssComponent.SystemCreationClassName
- Msvm_VssComponent.SystemName
- Msvm_VssComponent.CreationClassName
- Msvm_VssComponent.DeviceID
- Msvm_VssComponent.PowerManagementSupported
- Msvm_VssComponent.PowerManagementCapabilities
- Msvm_VssComponent.Availability
- Msvm_VssComponent.StatusInfo
- Msvm_VssComponent.LastErrorCode
- Msvm_VssComponent.ErrorDescription
- Msvm_VssComponent.ErrorCleared
- Msvm_VssComponent.OtherIdentifyingInfo
- Msvm_VssComponent.PowerOnHours
- Msvm_VssComponent.TotalPowerOnHours
- Msvm_VssComponent.IdentifyingDescriptions
- Msvm_VssComponent.AdditionalAvailability
- Msvm_VssComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ab4039ce110af9fa023a662c31d1f9962b080e5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341180"
---
# <a name="msvm_vsscomponent-class"></a><span data-ttu-id="980b5-103">MSVM- \_ vsscomponent-Klasse</span><span class="sxs-lookup"><span data-stu-id="980b5-103">Msvm\_VssComponent class</span></span>

<span data-ttu-id="980b5-104">Stellt den Status des Volumeschattenkopie-Dienst-Diensts (VSS) dar, der die VSS-Anforderer im Gast Betriebssystem implementiert.</span><span class="sxs-lookup"><span data-stu-id="980b5-104">Represents the state of the Volume Shadow Copy Service (VSS) service, which implements the VSS Requester in the guest operating system.</span></span>

<span data-ttu-id="980b5-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="980b5-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="980b5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="980b5-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VssComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "VSS";
  string   Description = "Microsoft VSS Service";
  string   ElementName = "VSS";
  datetime InstallDate;
  string   Name = "VSS";
  uint16   OperationalStatus[] = { 2 };
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
  uint16   TransitioningToState = 12;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_VssComponent";
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

## <a name="members"></a><span data-ttu-id="980b5-107">Member</span><span class="sxs-lookup"><span data-stu-id="980b5-107">Members</span></span>

<span data-ttu-id="980b5-108">Die **MSVM- \_ vsscomponent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="980b5-108">The **Msvm\_VssComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="980b5-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="980b5-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="980b5-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="980b5-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="980b5-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="980b5-111">Methods</span></span>

<span data-ttu-id="980b5-112">Die **MSVM- \_ vsscomponent** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="980b5-112">The **Msvm\_VssComponent** class has these methods.</span></span>



| <span data-ttu-id="980b5-113">Methode</span><span class="sxs-lookup"><span data-stu-id="980b5-113">Method</span></span>                                                             | <span data-ttu-id="980b5-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="980b5-114">Description</span></span>                              |
|:-------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="980b5-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="980b5-115">**EnableDevice**</span></span>                                                   | <span data-ttu-id="980b5-116">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="980b5-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="980b5-117">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="980b5-117">**OnlineDevice**</span></span>                                                   | <span data-ttu-id="980b5-118">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="980b5-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="980b5-119">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="980b5-119">**QuiesceDevice**</span></span>                                                  | <span data-ttu-id="980b5-120">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="980b5-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="980b5-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="980b5-121">**RequestStateChange**</span></span>](msvm-vsscomponent-requeststatechange.md) | <span data-ttu-id="980b5-122">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="980b5-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="980b5-123">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="980b5-123">**Reset**</span></span>](msvm-vsscomponent-reset.md)                           | <span data-ttu-id="980b5-124">Setzt das virtuelle Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="980b5-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="980b5-125">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="980b5-125">**RestoreProperties**</span></span>                                              | <span data-ttu-id="980b5-126">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="980b5-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="980b5-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="980b5-127">**SaveProperties**</span></span>                                                 | <span data-ttu-id="980b5-128">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="980b5-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="980b5-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="980b5-129">**SetPowerState**</span></span>                                                  | <span data-ttu-id="980b5-130">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="980b5-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="980b5-131">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="980b5-131">Properties</span></span>

<span data-ttu-id="980b5-132">Die **MSVM- \_ vsscomponent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="980b5-132">The **Msvm\_VssComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="980b5-133">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="980b5-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-134">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="980b5-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="980b5-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-136">Alle zusätzlichen Verfügbarkeit und der Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="980b5-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="980b5-137">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="980b5-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="980b5-138">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="980b5-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-139">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="980b5-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="980b5-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-141">Die primäre Verfügbarkeit und den Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="980b5-141">The primary availability and status of the device.</span></span> <span data-ttu-id="980b5-142">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="980b5-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="980b5-143">Wert</span><span class="sxs-lookup"><span data-stu-id="980b5-143">Value</span></span>                                                                        | <span data-ttu-id="980b5-144">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="980b5-144">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="980b5-145"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="980b5-145"><dt>6</dt></span></span> </dl> | <span data-ttu-id="980b5-146">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="980b5-146">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="980b5-147">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="980b5-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-148">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="980b5-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="980b5-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-150">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="980b5-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="980b5-151">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="980b5-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="980b5-152">**Caption**</span><span class="sxs-lookup"><span data-stu-id="980b5-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="980b5-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980b5-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-155">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="980b5-155">A short description of the object.</span></span> <span data-ttu-id="980b5-156">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="980b5-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="980b5-157">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="980b5-157">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-158">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="980b5-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="980b5-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-160">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="980b5-160">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="980b5-161">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="980b5-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="980b5-162">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="980b5-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="980b5-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="980b5-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="980b5-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="980b5-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="980b5-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="980b5-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="980b5-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="980b5-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="980b5-170">)</span><span class="sxs-lookup"><span data-stu-id="980b5-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="980b5-171">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="980b5-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-172">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="980b5-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980b5-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-174">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="980b5-174">The scoping system's creation class name.</span></span> <span data-ttu-id="980b5-175">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="980b5-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="980b5-176">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="980b5-176">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="980b5-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980b5-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-179">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="980b5-179">A description of the object.</span></span> <span data-ttu-id="980b5-180">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="980b5-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="980b5-181">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="980b5-181">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-182">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="980b5-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="980b5-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-184">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="980b5-184">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="980b5-185">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="980b5-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="980b5-186">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="980b5-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="980b5-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="980b5-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="980b5-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="980b5-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="980b5-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="980b5-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="980b5-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="980b5-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="980b5-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="980b5-195">)</span><span class="sxs-lookup"><span data-stu-id="980b5-195">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="980b5-196">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="980b5-196">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-197">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="980b5-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980b5-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-199">Eine Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="980b5-199">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="980b5-200">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf "Microsoft:*VMGUID* \\ *GUID*" festgelegt, wobei *VMGUID* die **Name** -Eigenschaft des [**MSVM \_ Computer Systems**](msvm-computersystem.md) ist, das diesem Gerät zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="980b5-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*VMGUID*\\*GUID*" where *VMGUID* is the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="980b5-201">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="980b5-201">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-202">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="980b5-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980b5-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-204">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="980b5-204">A display name for the object.</span></span> <span data-ttu-id="980b5-205">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="980b5-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="980b5-206">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="980b5-206">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-207">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="980b5-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="980b5-208">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-209">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 7 (kein Standardwert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="980b5-209">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 7 (No Default).</span></span>



| <span data-ttu-id="980b5-210">Wert</span><span class="sxs-lookup"><span data-stu-id="980b5-210">Value</span></span>                                                                        | <span data-ttu-id="980b5-211">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="980b5-211">Meaning</span></span>               |
|------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="980b5-212"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="980b5-212"><dt>2</dt></span></span> </dl> | <span data-ttu-id="980b5-213">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="980b5-213">Enabled</span></span><br/>    |
| <dl> <span data-ttu-id="980b5-214"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="980b5-214"><dt>3</dt></span></span> </dl> | <span data-ttu-id="980b5-215">Disabled</span><span class="sxs-lookup"><span data-stu-id="980b5-215">Disabled</span></span><br/>   |
| <dl> <span data-ttu-id="980b5-216"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="980b5-216"><dt>7</dt></span></span> </dl> | <span data-ttu-id="980b5-217">Kein Standardwert</span><span class="sxs-lookup"><span data-stu-id="980b5-217">No Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="980b5-218">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="980b5-218">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-219">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="980b5-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="980b5-220">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-221">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="980b5-221">The enabled and disabled states of an element.</span></span> <span data-ttu-id="980b5-222">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="980b5-222">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="980b5-223">Wert</span><span class="sxs-lookup"><span data-stu-id="980b5-223">Value</span></span>                                                                        | <span data-ttu-id="980b5-224">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="980b5-224">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="980b5-225"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="980b5-225"><dt>2</dt></span></span> </dl> | <span data-ttu-id="980b5-226">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="980b5-226">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="980b5-227"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="980b5-227"><dt>3</dt></span></span> </dl> | <span data-ttu-id="980b5-228">Disabled</span><span class="sxs-lookup"><span data-stu-id="980b5-228">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="980b5-229">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="980b5-229">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-230">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="980b5-230">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="980b5-231">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-232">Gibt an, ob der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="980b5-232">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="980b5-233">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="980b5-233">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="980b5-234">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="980b5-234">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-235">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="980b5-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980b5-236">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-237">Eine Zeichenfolge, die weitere Informationen über den Fehler enthält, der in **LastErrorCode** aufgezeichnet wurde, sowie Informationen zu den Maßnahmen, die ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="980b5-237">A string that provides more information about the error recorded in **LastErrorCode**, and information on any corrective actions that can be taken.</span></span> <span data-ttu-id="980b5-238">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="980b5-238">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="980b5-239">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="980b5-239">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-240">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="980b5-240">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="980b5-241">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-242">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="980b5-242">The current health of the element.</span></span> <span data-ttu-id="980b5-243">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="980b5-243">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="980b5-244">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="980b5-244">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="980b5-245">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="980b5-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="980b5-246">Wert</span><span class="sxs-lookup"><span data-stu-id="980b5-246">Value</span></span>                                                                        | <span data-ttu-id="980b5-247">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="980b5-247">Meaning</span></span>       |
|------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="980b5-248"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="980b5-248"><dt>5</dt></span></span> </dl> | <span data-ttu-id="980b5-249">OK</span><span class="sxs-lookup"><span data-stu-id="980b5-249">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="980b5-250">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="980b5-250">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-251">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="980b5-251">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="980b5-252">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-253">Ein Array von Freiform-Zeichen folgen, die Erklärungen und Details hinter den Einträgen im " **OtherIdentifyingInfo** "-Array bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="980b5-253">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="980b5-254">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="980b5-254">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="980b5-255">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="980b5-255">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-256">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="980b5-256">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="980b5-257">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-258">Das Datum und die Uhrzeit, zu denen der Integrations Dienst auf dem virtuellen Computer installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="980b5-258">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="980b5-259">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="980b5-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="980b5-260">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="980b5-260">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-261">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="980b5-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980b5-262">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="980b5-263">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="980b5-263">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="980b5-264">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="980b5-264">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="980b5-265">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="980b5-265">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="980b5-266">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="980b5-266">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-267">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="980b5-267">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="980b5-268">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-269">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="980b5-269">The last error code reported by the logical device.</span></span> <span data-ttu-id="980b5-270">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="980b5-270">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="980b5-271">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="980b5-271">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-272">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="980b5-272">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="980b5-273">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-274">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="980b5-274">This property has been deprecated.</span></span> <span data-ttu-id="980b5-275">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="980b5-275">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="980b5-276">**Name**</span><span class="sxs-lookup"><span data-stu-id="980b5-276">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-277">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="980b5-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980b5-278">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-279">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="980b5-279">The label by which the object is known.</span></span> <span data-ttu-id="980b5-280">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="980b5-280">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="980b5-281">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="980b5-281">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-282">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="980b5-282">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="980b5-283">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-284">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="980b5-284">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="980b5-285">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="980b5-285">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="980b5-286">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="980b5-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="980b5-287"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="980b5-287"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-288"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="980b5-288"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-289"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="980b5-289"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-290"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="980b5-290"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-291"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="980b5-291"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-292"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="980b5-292"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-293"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="980b5-293"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-294"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="980b5-294"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-295"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="980b5-295"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-296"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="980b5-296"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-297"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="980b5-297"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-298"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="980b5-298"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-299"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="980b5-299"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-300"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="980b5-300"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-301"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="980b5-301"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-302"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="980b5-302"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-303"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="980b5-303"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-304"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="980b5-304"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-305"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="980b5-305"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="980b5-306">)</span><span class="sxs-lookup"><span data-stu-id="980b5-306">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="980b5-307">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="980b5-307">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-308">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="980b5-308">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="980b5-309">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-310">Der aktuelle Status des Elements.</span><span class="sxs-lookup"><span data-stu-id="980b5-310">The current status of the element.</span></span> <span data-ttu-id="980b5-311">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="980b5-311">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="980b5-312">Im folgenden sind die möglichen Werte für den Wert der Eigenschaft **OperationalStatus** \[ 0 verfügbar \] .</span><span class="sxs-lookup"><span data-stu-id="980b5-312">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>



| <span data-ttu-id="980b5-313">Wert</span><span class="sxs-lookup"><span data-stu-id="980b5-313">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="980b5-314">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="980b5-314">Meaning</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="980b5-315"><dt>2,2</dt></span><span class="sxs-lookup"><span data-stu-id="980b5-315"><dt>{ 2 }</dt></span></span> </dl>                                                                                                                                                                                                    |                                                                                                                                                                                                                                          |
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="980b5-316"><dt>**OK**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="980b5-316"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                                  | <span data-ttu-id="980b5-317">Der Dienst wird normal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="980b5-317">The service is operating normally.</span></span> <span data-ttu-id="980b5-318">Die Eigenschaftswerte **OperationalStatus** \[ 1 \] und **Statusbeschreibungen** \[ 1 \] enthalten möglicherweise weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="980b5-318">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                                               |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="980b5-319"><dt></dt> Heruntergestuft <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="980b5-319"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                                     | <span data-ttu-id="980b5-320">Der Dienst wird normal ausgeführt, aber der Gast Dienst hat eine kompatible Kommunikationsprotokoll Version ausgehandelt.</span><span class="sxs-lookup"><span data-stu-id="980b5-320">The service is operating normally but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="980b5-321">Die Eigenschaftswerte **OperationalStatus** \[ 1 \] und **Statusbeschreibungen** \[ 1 \] enthalten möglicherweise weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="980b5-321">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/> |
| <span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span><dl> <span data-ttu-id="980b5-322"><dt>**Nicht BEHEB barer Fehler**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="980b5-322"><dt>**Non-Recoverable Error**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="980b5-323">Der Gast unterstützt keine kompatible Protokollversion.</span><span class="sxs-lookup"><span data-stu-id="980b5-323">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="980b5-324">Die Eigenschaftswerte **OperationalStatus** \[ 1 \] und **Statusbeschreibungen** \[ 1 \] enthalten möglicherweise weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="980b5-324">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                        |
| <span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dl> <span data-ttu-id="980b5-325"><dt>**Kein Kontakt**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="980b5-325"><dt>**No Contact**</dt> <dt>12</dt></span></span> </dl>                                            | <span data-ttu-id="980b5-326">Der Gast Dienst ist nicht installiert, oder er wurde noch nicht kontaktiert.</span><span class="sxs-lookup"><span data-stu-id="980b5-326">The guest service is not installed or has not yet been contacted.</span></span><br/>                                                                                                                                                             |
| <span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span><dl> <span data-ttu-id="980b5-327"><dt>**Verlorene Kommunikation**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="980b5-327"><dt>**Lost Communication**</dt> <dt>13</dt></span></span> </dl>            | <span data-ttu-id="980b5-328">Der Gast Dienst antwortet nicht mehr normal.</span><span class="sxs-lookup"><span data-stu-id="980b5-328">The guest service is no longer responding normally.</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="980b5-329">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="980b5-329">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-330">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="980b5-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980b5-331">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-332">Der aktivierte oder deaktivierte Status des Elements, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="980b5-332">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="980b5-333">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="980b5-333">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="980b5-334">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="980b5-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="980b5-335">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="980b5-335">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-336">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="980b5-336">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="980b5-337">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-338">Zusätzliche Daten über Geräte-ID-Informationen, die zur Identifizierung eines logischen Geräts verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="980b5-338">Additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="980b5-339">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="980b5-339">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="980b5-340">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="980b5-340">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-341">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="980b5-341">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="980b5-342">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-343">Die Energie Verwaltungsfunktionen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="980b5-343">The power management capabilities of the device.</span></span> <span data-ttu-id="980b5-344">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="980b5-344">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="980b5-345">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="980b5-345">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-346">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="980b5-346">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="980b5-347">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-348">Gibt an, ob das Gerät Energie gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="980b5-348">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="980b5-349">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="980b5-349">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="980b5-350">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="980b5-350">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-351">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="980b5-351">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="980b5-352">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-353">Gibt an, wie viele aufeinanderfolgende Stunden dieses Gerät seit dem letzten Strom Umgebung eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="980b5-353">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="980b5-354">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="980b5-354">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="980b5-355">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="980b5-355">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-356">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="980b5-356">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="980b5-357">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-358">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="980b5-358">Provides high level status information.</span></span> <span data-ttu-id="980b5-359">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="980b5-359">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="980b5-360">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="980b5-360">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="980b5-361">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="980b5-361">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="980b5-362"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="980b5-362"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-363"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="980b5-363"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-364"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="980b5-364"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-365"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="980b5-365"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-366"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="980b5-366"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="980b5-367"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="980b5-367"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="980b5-368">)</span><span class="sxs-lookup"><span data-stu-id="980b5-368">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="980b5-369">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="980b5-369">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-370">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="980b5-370">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="980b5-371">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-372">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="980b5-372">The last requested or desired state for the element.</span></span> <span data-ttu-id="980b5-373">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="980b5-373">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="980b5-374">Wert</span><span class="sxs-lookup"><span data-stu-id="980b5-374">Value</span></span>                                                                         | <span data-ttu-id="980b5-375">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="980b5-375">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="980b5-376"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="980b5-376"><dt>12</dt></span></span> </dl> | <span data-ttu-id="980b5-377">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="980b5-377">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="980b5-378">**Status**</span><span class="sxs-lookup"><span data-stu-id="980b5-378">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-379">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="980b5-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980b5-380">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-381">Eine Zeichenfolge, die den aktuellen Status des-Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="980b5-381">A string that specifies the current status of the object.</span></span> <span data-ttu-id="980b5-382">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="980b5-382">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="980b5-383">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="980b5-383">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-384">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="980b5-384">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="980b5-385">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-386">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="980b5-386">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="980b5-387">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="980b5-387">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="980b5-388">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="980b5-388">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-389">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="980b5-389">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="980b5-390">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-391">Der aktuelle Zustand des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="980b5-391">The current state of the logical device.</span></span> <span data-ttu-id="980b5-392">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="980b5-392">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="980b5-393">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="980b5-393">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-394">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="980b5-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980b5-395">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-396">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="980b5-396">The scoping system's creation class name.</span></span> <span data-ttu-id="980b5-397">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="980b5-397">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="980b5-398">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="980b5-398">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-399">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="980b5-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980b5-400">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-401">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="980b5-401">The scoping system's name.</span></span> <span data-ttu-id="980b5-402">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="980b5-402">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="980b5-403">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="980b5-403">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-404">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="980b5-404">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="980b5-405">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-406">Das Datum oder die Uhrzeit der letzten Änderung des **enabledstate** des Elements.</span><span class="sxs-lookup"><span data-stu-id="980b5-406">The date or time when the **EnabledState** of the element last changed.</span></span> <span data-ttu-id="980b5-407">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="980b5-407">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="980b5-408">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="980b5-408">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-409">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="980b5-409">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="980b5-410">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-411">Die Gesamtanzahl der Stunden, für die dieses Gerät eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="980b5-411">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="980b5-412">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="980b5-412">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="980b5-413">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="980b5-413">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980b5-414">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="980b5-414">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="980b5-415">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980b5-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980b5-416">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="980b5-416">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="980b5-417">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="980b5-417">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="980b5-418">Wert</span><span class="sxs-lookup"><span data-stu-id="980b5-418">Value</span></span>                                                                         | <span data-ttu-id="980b5-419">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="980b5-419">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="980b5-420"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="980b5-420"><dt>12</dt></span></span> </dl> | <span data-ttu-id="980b5-421">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="980b5-421">Not Applicable</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="980b5-422">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="980b5-422">Remarks</span></span>

<span data-ttu-id="980b5-423">Der Zugriff auf die **MSVM \_ vsscomponent** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="980b5-423">Access to the **Msvm\_VssComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="980b5-424">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="980b5-424">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="980b5-425">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="980b5-425">Requirements</span></span>



| <span data-ttu-id="980b5-426">Anforderung</span><span class="sxs-lookup"><span data-stu-id="980b5-426">Requirement</span></span> | <span data-ttu-id="980b5-427">Wert</span><span class="sxs-lookup"><span data-stu-id="980b5-427">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="980b5-428">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="980b5-428">Minimum supported client</span></span><br/> | <span data-ttu-id="980b5-429">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="980b5-429">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="980b5-430">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="980b5-430">Minimum supported server</span></span><br/> | <span data-ttu-id="980b5-431">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="980b5-431">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="980b5-432">Namespace</span><span class="sxs-lookup"><span data-stu-id="980b5-432">Namespace</span></span><br/>                | <span data-ttu-id="980b5-433">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="980b5-433">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="980b5-434">MOF</span><span class="sxs-lookup"><span data-stu-id="980b5-434">MOF</span></span><br/>                      | <dl> <span data-ttu-id="980b5-435"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="980b5-435"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="980b5-436">DLL</span><span class="sxs-lookup"><span data-stu-id="980b5-436">DLL</span></span><br/>                      | <dl> <span data-ttu-id="980b5-437"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="980b5-437"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="980b5-438">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="980b5-438">See also</span></span>

<dl> <dt>

[<span data-ttu-id="980b5-439">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="980b5-439">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="980b5-440">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="980b5-440">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

