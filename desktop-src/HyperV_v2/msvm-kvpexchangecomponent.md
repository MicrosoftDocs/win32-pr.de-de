---
description: Stellt den Status des Schlüssel-Wert-Paar-Exchange-Dienstanbieter dar, der einen Mechanismus zum Austauschen von Daten zwischen dem virtuellen Computer und dem Betriebssystem bereitstellt, das unter dem Verwaltungs Betriebssystem ausgeführt wird.
ms.assetid: AA68BC74-A919-4029-B703-E08F00449F20
title: Msvm_KvpExchangeComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_KvpExchangeComponent
- Msvm_KvpExchangeComponent.SetPowerState
- Msvm_KvpExchangeComponent.EnableDevice
- Msvm_KvpExchangeComponent.OnlineDevice
- Msvm_KvpExchangeComponent.QuiesceDevice
- Msvm_KvpExchangeComponent.SaveProperties
- Msvm_KvpExchangeComponent.RestoreProperties
- Msvm_KvpExchangeComponent.InstanceID
- Msvm_KvpExchangeComponent.Caption
- Msvm_KvpExchangeComponent.Description
- Msvm_KvpExchangeComponent.ElementName
- Msvm_KvpExchangeComponent.InstallDate
- Msvm_KvpExchangeComponent.Name
- Msvm_KvpExchangeComponent.OperationalStatus
- Msvm_KvpExchangeComponent.StatusDescriptions
- Msvm_KvpExchangeComponent.Status
- Msvm_KvpExchangeComponent.HealthState
- Msvm_KvpExchangeComponent.CommunicationStatus
- Msvm_KvpExchangeComponent.DetailedStatus
- Msvm_KvpExchangeComponent.OperatingStatus
- Msvm_KvpExchangeComponent.PrimaryStatus
- Msvm_KvpExchangeComponent.EnabledState
- Msvm_KvpExchangeComponent.OtherEnabledState
- Msvm_KvpExchangeComponent.RequestedState
- Msvm_KvpExchangeComponent.EnabledDefault
- Msvm_KvpExchangeComponent.TimeOfLastStateChange
- Msvm_KvpExchangeComponent.AvailableRequestedStates
- Msvm_KvpExchangeComponent.TransitioningToState
- Msvm_KvpExchangeComponent.SystemCreationClassName
- Msvm_KvpExchangeComponent.SystemName
- Msvm_KvpExchangeComponent.CreationClassName
- Msvm_KvpExchangeComponent.DeviceID
- Msvm_KvpExchangeComponent.PowerManagementSupported
- Msvm_KvpExchangeComponent.PowerManagementCapabilities
- Msvm_KvpExchangeComponent.Availability
- Msvm_KvpExchangeComponent.StatusInfo
- Msvm_KvpExchangeComponent.LastErrorCode
- Msvm_KvpExchangeComponent.ErrorDescription
- Msvm_KvpExchangeComponent.ErrorCleared
- Msvm_KvpExchangeComponent.OtherIdentifyingInfo
- Msvm_KvpExchangeComponent.PowerOnHours
- Msvm_KvpExchangeComponent.TotalPowerOnHours
- Msvm_KvpExchangeComponent.IdentifyingDescriptions
- Msvm_KvpExchangeComponent.AdditionalAvailability
- Msvm_KvpExchangeComponent.MaxQuiesceTime
- Msvm_KvpExchangeComponent.GuestExchangeItems
- Msvm_KvpExchangeComponent.GuestIntrinsicExchangeItems
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e3aa7f269d24c284eef3ad2c519f5fdbf48513a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868512"
---
# <a name="msvm_kvpexchangecomponent-class"></a><span data-ttu-id="af766-103">MSVM- \_ kvpexchangecomponent-Klasse</span><span class="sxs-lookup"><span data-stu-id="af766-103">Msvm\_KvpExchangeComponent class</span></span>

<span data-ttu-id="af766-104">Stellt den Status des Schlüssel-Wert-Paar-Exchange-Dienstanbieter dar, der einen Mechanismus zum Austauschen von Daten zwischen dem virtuellen Computer und dem Betriebssystem bereitstellt, das unter dem Verwaltungs Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="af766-104">Represents the state of the key/value pair exchange service, which provides a mechanism to exchange data between the virtual machine and the operating system running on the management operating system.</span></span>

<span data-ttu-id="af766-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="af766-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="af766-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="af766-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_KvpExchangeComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "Key-Value Pair Exchange";
  string   Description = "Microsoft Key-Value Pair Exchange Service";
  string   ElementName = "Key-Value pair Exchange";
  datetime InstallDate;
  string   Name = "Key-Value Pair Exchange";
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 7;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_KvpExchangeComponent";
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
  string   GuestExchangeItems[];
  string   GuestIntrinsicExchangeItems[];
};
```

## <a name="members"></a><span data-ttu-id="af766-107">Member</span><span class="sxs-lookup"><span data-stu-id="af766-107">Members</span></span>

<span data-ttu-id="af766-108">Die **MSVM- \_ kvpexchangecomponent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="af766-108">The **Msvm\_KvpExchangeComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="af766-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="af766-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="af766-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="af766-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="af766-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="af766-111">Methods</span></span>

<span data-ttu-id="af766-112">Die **MSVM- \_ kvpexchangecomponent** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="af766-112">The **Msvm\_KvpExchangeComponent** class has these methods.</span></span>



| <span data-ttu-id="af766-113">Methode</span><span class="sxs-lookup"><span data-stu-id="af766-113">Method</span></span>                                                                     | <span data-ttu-id="af766-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="af766-114">Description</span></span>                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="af766-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="af766-115">**EnableDevice**</span></span>                                                           | <span data-ttu-id="af766-116">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="af766-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="af766-117">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="af766-117">**OnlineDevice**</span></span>                                                           | <span data-ttu-id="af766-118">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="af766-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="af766-119">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="af766-119">**QuiesceDevice**</span></span>                                                          | <span data-ttu-id="af766-120">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="af766-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="af766-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="af766-121">**RequestStateChange**</span></span>](msvm-kvpexchangecomponent-requeststatechange.md) | <span data-ttu-id="af766-122">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="af766-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="af766-123">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="af766-123">**Reset**</span></span>](msvm-kvpexchangecomponent-reset.md)                           | <span data-ttu-id="af766-124">Setzt die Komponente zurück.</span><span class="sxs-lookup"><span data-stu-id="af766-124">Resets the component.</span></span><br/>         |
| <span data-ttu-id="af766-125">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="af766-125">**RestoreProperties**</span></span>                                                      | <span data-ttu-id="af766-126">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="af766-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="af766-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="af766-127">**SaveProperties**</span></span>                                                         | <span data-ttu-id="af766-128">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="af766-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="af766-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="af766-129">**SetPowerState**</span></span>                                                          | <span data-ttu-id="af766-130">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="af766-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="af766-131">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="af766-131">Properties</span></span>

<span data-ttu-id="af766-132">Die **MSVM- \_ kvpexchangecomponent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="af766-132">The **Msvm\_KvpExchangeComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="af766-133">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="af766-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-134">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="af766-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="af766-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-136">Alle zusätzlichen Verfügbarkeit und der Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="af766-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="af766-137">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="af766-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="af766-138">Wert</span><span class="sxs-lookup"><span data-stu-id="af766-138">Value</span></span>                                                                            | <span data-ttu-id="af766-139">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="af766-139">Meaning</span></span>                   |
|----------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="af766-140"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="af766-140"><dt>{ 6 }</dt></span></span> </dl> |                           |
| <dl> <span data-ttu-id="af766-141"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="af766-141"><dt>6</dt></span></span> </dl>     | <span data-ttu-id="af766-142">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="af766-142">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="af766-143">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="af766-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-144">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af766-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af766-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-146">Die primäre Verfügbarkeit und den Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="af766-146">The primary availability and status of the device.</span></span> <span data-ttu-id="af766-147">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="af766-147">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="af766-148">Wert</span><span class="sxs-lookup"><span data-stu-id="af766-148">Value</span></span>                                                                        | <span data-ttu-id="af766-149">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="af766-149">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="af766-150"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="af766-150"><dt>6</dt></span></span> </dl> | <span data-ttu-id="af766-151">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="af766-151">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="af766-152">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="af766-152">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-153">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="af766-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="af766-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-155">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="af766-155">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="af766-156">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="af766-156">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="af766-157">**Caption**</span><span class="sxs-lookup"><span data-stu-id="af766-157">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-158">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="af766-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af766-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-160">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="af766-160">A short description of the object.</span></span> <span data-ttu-id="af766-161">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="af766-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="af766-162">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="af766-162">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-163">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af766-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af766-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-165">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="af766-165">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="af766-166">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="af766-166">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="af766-167">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="af766-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="af766-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="af766-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="af766-169"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="af766-169"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="af766-170"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="af766-170"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="af766-171"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="af766-171"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="af766-172"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="af766-172"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="af766-173"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="af766-173"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="af766-174"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="af766-174"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="af766-175">)</span><span class="sxs-lookup"><span data-stu-id="af766-175">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="af766-176">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="af766-176">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="af766-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af766-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-179">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="af766-179">The scoping system's creation class name.</span></span> <span data-ttu-id="af766-180">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="af766-180">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="af766-181">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="af766-181">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-182">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="af766-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af766-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-184">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="af766-184">A description of the object.</span></span> <span data-ttu-id="af766-185">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="af766-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="af766-186">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="af766-186">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-187">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af766-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af766-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-189">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="af766-189">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="af766-190">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="af766-190">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="af766-191">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="af766-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="af766-192"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="af766-192"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="af766-193"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="af766-193"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="af766-194"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="af766-194"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="af766-195"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="af766-195"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="af766-196"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="af766-196"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="af766-197"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="af766-197"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="af766-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="af766-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="af766-199"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="af766-199"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="af766-200">)</span><span class="sxs-lookup"><span data-stu-id="af766-200">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="af766-201">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="af766-201">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-202">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="af766-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af766-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-204">Eine Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="af766-204">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="af766-205">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="af766-205">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="af766-206">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="af766-206">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-207">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="af766-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af766-208">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-209">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="af766-209">A display name for the object.</span></span> <span data-ttu-id="af766-210">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="af766-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="af766-211">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="af766-211">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-212">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af766-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af766-213">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-214">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="af766-214">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="af766-215">Wert</span><span class="sxs-lookup"><span data-stu-id="af766-215">Value</span></span>                                                                        | <span data-ttu-id="af766-216">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="af766-216">Meaning</span></span>               |
|------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="af766-217"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="af766-217"><dt>7</dt></span></span> </dl> | <span data-ttu-id="af766-218">Kein Standardwert</span><span class="sxs-lookup"><span data-stu-id="af766-218">No Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="af766-219">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="af766-219">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-220">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af766-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af766-221">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-222">Der aktivierte Status des Elements.</span><span class="sxs-lookup"><span data-stu-id="af766-222">The enabled state of the element.</span></span> <span data-ttu-id="af766-223">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="af766-223">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="af766-224"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="af766-224"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="af766-225"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="af766-225"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="af766-226">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="af766-226">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-227">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="af766-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="af766-228">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-229">Gibt an, ob der in der **LastErrorCode** -Eigenschaft gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="af766-229">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="af766-230">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="af766-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="af766-231">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="af766-231">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-232">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="af766-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af766-233">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-234">Eine Zeichenfolge, die weitere Informationen über den in der **LastErrorCode** -Eigenschaft aufgezeichneten Fehler sowie Informationen zu ggf. durchzuführenden Maßnahmen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="af766-234">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="af766-235">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="af766-235">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="af766-236">**Guestexchangeitems**</span><span class="sxs-lookup"><span data-stu-id="af766-236">**GuestExchangeItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-237">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="af766-237">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="af766-238">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af766-239">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), **hypervembeddedinstance** ("MSVM \_ kvpexchangedataitem")</span><span class="sxs-lookup"><span data-stu-id="af766-239">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_KvpExchangeDataItem")</span></span>
</dt> </dl>

<span data-ttu-id="af766-240">Ein Array von eingebetteten [**MSVM- \_ kvpexchangedataitem**](msvm-kvpexchangedataitem.md) -Instanzen, die den Satz von Schlüssel-Wert-Paaren enthalten, die von Diensten, die im Gast Betriebssystem ausgeführt werden, für den Zugriff durch externe Clients bereitgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="af766-240">An array of embedded [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) instances which contain the set of key-value pairs that services running within the guest operating system have pushed up to be available for access by external clients.</span></span> <span data-ttu-id="af766-241">Dieses Array enthält keine systeminternen Elemente, die durch den Integrations Dienst direkt per Pushvorgang übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="af766-241">This array will not contain any intrinsic items that are pushed by the integration service directly.</span></span>

</dd> <dt>

<span data-ttu-id="af766-242">**GuestIntrinsicExchangeItems**</span><span class="sxs-lookup"><span data-stu-id="af766-242">**GuestIntrinsicExchangeItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-243">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="af766-243">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="af766-244">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af766-245">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), **hypervembeddedinstance** ("MSVM \_ kvpexchangedataitem")</span><span class="sxs-lookup"><span data-stu-id="af766-245">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_KvpExchangeDataItem")</span></span>
</dt> </dl>

<span data-ttu-id="af766-246">Ein Array von eingebetteten [**MSVM- \_ kvpexchangedataitem**](msvm-kvpexchangedataitem.md) -Instanzen, die den Satz von Schlüssel-Wert-Paaren enthalten, die das Gast Betriebssystem für den Zugriff durch externe Clients bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="af766-246">An array of embedded [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) instances which contain the set of key-value pairs that the guest operating system has pushed up to be available for access by external clients.</span></span> <span data-ttu-id="af766-247">Dieses Array enthält keine Datenelemente, die von anderen Diensten übermittelt werden, die innerhalb des Gast Betriebssystems ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="af766-247">This array will not contain any data items pushed by other services running within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="af766-248">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="af766-248">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-249">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af766-249">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af766-250">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-251">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="af766-251">The current health of the element.</span></span> <span data-ttu-id="af766-252">Dadurch wird die Integrität dieses Elements, jedoch nicht notwendigerweise der seiner unter Komponenten ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="af766-252">This expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="af766-253">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="af766-253">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="af766-254">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="af766-254">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="af766-255">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="af766-255">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-256">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="af766-256">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="af766-257">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-258">Ein Array von Freiform-Zeichen folgen, die Erklärungen und Details hinter den Einträgen im Eigenschafts Array " **OtherIdentifyingInfo** " bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="af766-258">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="af766-259">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="af766-259">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="af766-260">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="af766-260">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-261">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="af766-261">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="af766-262">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-263">Das Datum und die Uhrzeit, zu denen der Integrations Dienst auf dem virtuellen Computer installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="af766-263">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="af766-264">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="af766-264">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="af766-265">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="af766-265">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-266">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="af766-266">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af766-267">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af766-268">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="af766-268">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="af766-269">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="af766-269">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="af766-270">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="af766-270">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="af766-271">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="af766-271">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-272">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af766-272">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af766-273">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-274">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="af766-274">The last error code reported by the logical device.</span></span> <span data-ttu-id="af766-275">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="af766-275">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="af766-276">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="af766-276">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-277">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="af766-277">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="af766-278">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-279">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="af766-279">This property has been deprecated.</span></span> <span data-ttu-id="af766-280">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="af766-280">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="af766-281">**Name**</span><span class="sxs-lookup"><span data-stu-id="af766-281">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-282">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="af766-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af766-283">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-284">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="af766-284">The label by which the object is known.</span></span> <span data-ttu-id="af766-285">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="af766-285">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="af766-286">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="af766-286">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-287">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af766-287">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af766-288">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-289">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="af766-289">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="af766-290">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="af766-290">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="af766-291">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="af766-291">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="af766-292"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="af766-292"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="af766-293"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="af766-293"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="af766-294"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="af766-294"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="af766-295"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="af766-295"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="af766-296"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="af766-296"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="af766-297"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="af766-297"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="af766-298"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="af766-298"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="af766-299"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="af766-299"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="af766-300"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="af766-300"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="af766-301"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="af766-301"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="af766-302"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="af766-302"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="af766-303"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="af766-303"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="af766-304"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="af766-304"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="af766-305"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="af766-305"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="af766-306"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="af766-306"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="af766-307"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="af766-307"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="af766-308"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="af766-308"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="af766-309"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="af766-309"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="af766-310"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="af766-310"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="af766-311">)</span><span class="sxs-lookup"><span data-stu-id="af766-311">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="af766-312">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="af766-312">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-313">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="af766-313">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="af766-314">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-315">Der aktuelle Status des Elements.</span><span class="sxs-lookup"><span data-stu-id="af766-315">The current status of the element.</span></span> <span data-ttu-id="af766-316">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="af766-316">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="af766-317">Im folgenden sind die möglichen Werte für den Wert der Eigenschaft **OperationalStatus** \[ 0 verfügbar \] .</span><span class="sxs-lookup"><span data-stu-id="af766-317">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>



| <span data-ttu-id="af766-318">Wert</span><span class="sxs-lookup"><span data-stu-id="af766-318">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="af766-319">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="af766-319">Meaning</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="af766-320"><dt>**OK**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="af766-320"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                                  | <span data-ttu-id="af766-321">Der Dienst wird normal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="af766-321">The service is operating normally.</span></span> <span data-ttu-id="af766-322">Die Eigenschaftswerte **OperationalStatus** \[ 1 \] und **Statusbeschreibungen** \[ 1 \] enthalten möglicherweise weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="af766-322">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                                               |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="af766-323"><dt></dt> Heruntergestuft <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="af766-323"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                                     | <span data-ttu-id="af766-324">Der Dienst wird normal ausgeführt, aber der Gast Dienst hat eine kompatible Kommunikationsprotokoll Version ausgehandelt.</span><span class="sxs-lookup"><span data-stu-id="af766-324">The service is operating normally but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="af766-325">Die Eigenschaftswerte **OperationalStatus** \[ 1 \] und **Statusbeschreibungen** \[ 1 \] enthalten möglicherweise weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="af766-325">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/> |
| <span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span><dl> <span data-ttu-id="af766-326"><dt>**Nicht BEHEB barer Fehler**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="af766-326"><dt>**Non-Recoverable Error**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="af766-327">Der Gast unterstützt keine kompatible Protokollversion.</span><span class="sxs-lookup"><span data-stu-id="af766-327">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="af766-328">Die Eigenschaftswerte **OperationalStatus** \[ 1 \] und **Statusbeschreibungen** \[ 1 \] enthalten möglicherweise weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="af766-328">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                        |
| <span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dl> <span data-ttu-id="af766-329"><dt>**Kein Kontakt**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="af766-329"><dt>**No Contact**</dt> <dt>12</dt></span></span> </dl>                                            | <span data-ttu-id="af766-330">Der Gast Dienst ist nicht installiert, oder er wurde noch nicht kontaktiert.</span><span class="sxs-lookup"><span data-stu-id="af766-330">The guest service is not installed or has not yet been contacted.</span></span><br/>                                                                                                                                                             |
| <span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span><dl> <span data-ttu-id="af766-331"><dt>**Verlorene Kommunikation**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="af766-331"><dt>**Lost Communication**</dt> <dt>13</dt></span></span> </dl>            | <span data-ttu-id="af766-332">Der Gast Dienst antwortet nicht mehr normal.</span><span class="sxs-lookup"><span data-stu-id="af766-332">The guest service is no longer responding normally.</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="af766-333">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="af766-333">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-334">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="af766-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af766-335">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-336">Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="af766-336">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="af766-337">Diese Eigenschaft muss auf **null** festgelegt werden, wenn die **enabledstate** -Eigenschaft einen anderen Wert als 1 hat.</span><span class="sxs-lookup"><span data-stu-id="af766-337">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="af766-338">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="af766-338">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="af766-339">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="af766-339">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-340">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="af766-340">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="af766-341">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-342">Alle zusätzlichen Daten über Geräte-ID-Informationen, die zur Identifizierung eines logischen Geräts verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="af766-342">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="af766-343">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="af766-343">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="af766-344">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="af766-344">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-345">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="af766-345">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="af766-346">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-347">Die Energie Verwaltungsfunktionen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="af766-347">The power management capabilities of the device.</span></span> <span data-ttu-id="af766-348">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="af766-348">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="af766-349">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="af766-349">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-350">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="af766-350">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="af766-351">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-352">Gibt an, ob das Gerät Energie gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="af766-352">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="af766-353">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="af766-353">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="af766-354">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="af766-354">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-355">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="af766-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="af766-356">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-357">Gibt an, wie viele aufeinanderfolgende Stunden dieses Gerät seit dem letzten Strom Umgebung eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="af766-357">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="af766-358">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="af766-358">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="af766-359">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="af766-359">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-360">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af766-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af766-361">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-362">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="af766-362">Provides high level status information.</span></span> <span data-ttu-id="af766-363">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="af766-363">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="af766-364">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="af766-364">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="af766-365">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="af766-365">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="af766-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="af766-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="af766-367"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="af766-367"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="af766-368"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="af766-368"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="af766-369"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="af766-369"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="af766-370"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="af766-370"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="af766-371"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="af766-371"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="af766-372">)</span><span class="sxs-lookup"><span data-stu-id="af766-372">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="af766-373">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="af766-373">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-374">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af766-374">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af766-375">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-376">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="af766-376">The last requested or desired state for the element.</span></span> <span data-ttu-id="af766-377">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="af766-377">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="af766-378">Wert</span><span class="sxs-lookup"><span data-stu-id="af766-378">Value</span></span>                                                                         | <span data-ttu-id="af766-379">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="af766-379">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="af766-380"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="af766-380"><dt>12</dt></span></span> </dl> | <span data-ttu-id="af766-381">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="af766-381">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="af766-382">**Status**</span><span class="sxs-lookup"><span data-stu-id="af766-382">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-383">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="af766-383">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af766-384">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-385">Der aktuelle Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="af766-385">The current status of the object.</span></span> <span data-ttu-id="af766-386">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="af766-386">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="af766-387">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="af766-387">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-388">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="af766-388">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="af766-389">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-390">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="af766-390">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="af766-391">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="af766-391">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="af766-392">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="af766-392">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-393">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af766-393">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af766-394">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-395">Der aktuelle Zustand des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="af766-395">The current state of the logical device.</span></span> <span data-ttu-id="af766-396">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="af766-396">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="af766-397">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="af766-397">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-398">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="af766-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af766-399">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-400">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="af766-400">The scoping system's creation class name.</span></span> <span data-ttu-id="af766-401">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="af766-401">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="af766-402">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="af766-402">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-403">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="af766-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af766-404">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-405">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="af766-405">The scoping system's name.</span></span> <span data-ttu-id="af766-406">Dieser Wert entspricht dem Wert der [**Name**](msvm-computersystem.md) -Eigenschaft der **MSVM \_ Computersystem** -Klasse für die Bereichs bezogene virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="af766-406">This value corresponds to the value of the [**Name**](msvm-computersystem.md) property of the **Msvm\_ComputerSystem** class for the scoping virtual machine.</span></span> <span data-ttu-id="af766-407">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="af766-407">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="af766-408">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="af766-408">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-409">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="af766-409">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="af766-410">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-411">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="af766-411">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="af766-412">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="af766-412">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="af766-413">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="af766-413">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-414">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="af766-414">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="af766-415">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-416">Die Gesamtanzahl der Stunden, für die dieses Gerät eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="af766-416">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="af766-417">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="af766-417">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="af766-418">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="af766-418">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af766-419">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af766-419">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af766-420">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="af766-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af766-421">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="af766-421">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="af766-422">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="af766-422">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="af766-423">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="af766-423">Remarks</span></span>

<span data-ttu-id="af766-424">Der Zugriff auf die **MSVM \_ kvpexchangecomponent** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="af766-424">Access to the **Msvm\_KvpExchangeComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="af766-425">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="af766-425">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="af766-426">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af766-426">Requirements</span></span>



| <span data-ttu-id="af766-427">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af766-427">Requirement</span></span> | <span data-ttu-id="af766-428">Wert</span><span class="sxs-lookup"><span data-stu-id="af766-428">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af766-429">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="af766-429">Minimum supported client</span></span><br/> | <span data-ttu-id="af766-430">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="af766-430">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="af766-431">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="af766-431">Minimum supported server</span></span><br/> | <span data-ttu-id="af766-432">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="af766-432">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="af766-433">Namespace</span><span class="sxs-lookup"><span data-stu-id="af766-433">Namespace</span></span><br/>                | <span data-ttu-id="af766-434">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="af766-434">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="af766-435">MOF</span><span class="sxs-lookup"><span data-stu-id="af766-435">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af766-436"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="af766-436"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="af766-437">DLL</span><span class="sxs-lookup"><span data-stu-id="af766-437">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af766-438"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="af766-438"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="af766-439">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af766-439">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af766-440">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="af766-440">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="af766-441">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="af766-441">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

