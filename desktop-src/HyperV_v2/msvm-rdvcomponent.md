---
description: Stellt den Status der RDV-Komponente dar, die für die Bereitstellung eines Transports für das übergeordnete zum Gast zu Konfigurations Zwecken zuständig ist.
ms.assetid: 240d2659-01ec-4300-a17e-0b1ec90483df
title: Msvm_RdvComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RdvComponent
- Msvm_RdvComponent.RequestStateChange
- Msvm_RdvComponent.SetPowerState
- Msvm_RdvComponent.Reset
- Msvm_RdvComponent.EnableDevice
- Msvm_RdvComponent.OnlineDevice
- Msvm_RdvComponent.QuiesceDevice
- Msvm_RdvComponent.SaveProperties
- Msvm_RdvComponent.RestoreProperties
- Msvm_RdvComponent.InstanceID
- Msvm_RdvComponent.Caption
- Msvm_RdvComponent.Description
- Msvm_RdvComponent.ElementName
- Msvm_RdvComponent.InstallDate
- Msvm_RdvComponent.Name
- Msvm_RdvComponent.OperationalStatus
- Msvm_RdvComponent.StatusDescriptions
- Msvm_RdvComponent.Status
- Msvm_RdvComponent.HealthState
- Msvm_RdvComponent.CommunicationStatus
- Msvm_RdvComponent.DetailedStatus
- Msvm_RdvComponent.OperatingStatus
- Msvm_RdvComponent.PrimaryStatus
- Msvm_RdvComponent.EnabledState
- Msvm_RdvComponent.OtherEnabledState
- Msvm_RdvComponent.RequestedState
- Msvm_RdvComponent.EnabledDefault
- Msvm_RdvComponent.TimeOfLastStateChange
- Msvm_RdvComponent.AvailableRequestedStates
- Msvm_RdvComponent.TransitioningToState
- Msvm_RdvComponent.SystemCreationClassName
- Msvm_RdvComponent.SystemName
- Msvm_RdvComponent.CreationClassName
- Msvm_RdvComponent.DeviceID
- Msvm_RdvComponent.PowerManagementSupported
- Msvm_RdvComponent.PowerManagementCapabilities
- Msvm_RdvComponent.Availability
- Msvm_RdvComponent.StatusInfo
- Msvm_RdvComponent.LastErrorCode
- Msvm_RdvComponent.ErrorDescription
- Msvm_RdvComponent.ErrorCleared
- Msvm_RdvComponent.OtherIdentifyingInfo
- Msvm_RdvComponent.PowerOnHours
- Msvm_RdvComponent.TotalPowerOnHours
- Msvm_RdvComponent.IdentifyingDescriptions
- Msvm_RdvComponent.AdditionalAvailability
- Msvm_RdvComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e1dbffb7db18ef2441d4c8e06cff23af2648e5a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216245"
---
# <a name="msvm_rdvcomponent-class"></a><span data-ttu-id="42a6b-103">MSVM \_ rdvcomponent-Klasse</span><span class="sxs-lookup"><span data-stu-id="42a6b-103">Msvm\_RdvComponent class</span></span>

<span data-ttu-id="42a6b-104">Stellt den Status der RDV-Komponente dar, die für die Bereitstellung eines Transports für das übergeordnete zum Gast zu Konfigurations Zwecken zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="42a6b-104">Represents the state of the RDV component, which is responsible for providing a transport for the parent to the guest for configuration purposes.</span></span>

<span data-ttu-id="42a6b-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="42a6b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="42a6b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="42a6b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_RdvComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "RDV";
  string   Description = "Remote Desktop Virtualization Service";
  string   ElementName = "RDV";
  datetime InstallDate;
  string   Name = "RDV";
  uint16   OperationalStatus[] = {2};
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
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_RdvComponent";
  string   DeviceID;
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
  uint16   AdditionalAvailability[];
  uint64   MaxQuiesceTime;
};
```

## <a name="members"></a><span data-ttu-id="42a6b-107">Member</span><span class="sxs-lookup"><span data-stu-id="42a6b-107">Members</span></span>

<span data-ttu-id="42a6b-108">Die **MSVM- \_ rdvcomponent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="42a6b-108">The **Msvm\_RdvComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="42a6b-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="42a6b-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="42a6b-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="42a6b-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="42a6b-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="42a6b-111">Methods</span></span>

<span data-ttu-id="42a6b-112">Die **MSVM- \_ rdvcomponent** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="42a6b-112">The **Msvm\_RdvComponent** class has these methods.</span></span>



| <span data-ttu-id="42a6b-113">Methode</span><span class="sxs-lookup"><span data-stu-id="42a6b-113">Method</span></span>                                                       | <span data-ttu-id="42a6b-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="42a6b-114">Description</span></span>                                                                                                                                                                                                                         |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42a6b-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="42a6b-115">**EnableDevice**</span></span>                                             | <span data-ttu-id="42a6b-116">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-116">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="42a6b-117">**Enableendpoints**</span><span class="sxs-lookup"><span data-stu-id="42a6b-117">**EnableEndPoints**</span></span>](enableendpoints-msvm-rdvcomponent.md) | <span data-ttu-id="42a6b-118">Fordert das virtuelle Remotedesktopdienste virtuellen Gerät auf, eine Pipe-Verbindung mit dem virtuellen Computer zu starten.</span><span class="sxs-lookup"><span data-stu-id="42a6b-118">Requests the Remote Desktop Services virtual device to start a pipe connection with the virtual machine.</span></span> <span data-ttu-id="42a6b-119">Wenn 0 (null) zurückgegeben wird, war der Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="42a6b-119">If zero (0) is returned, then the operation was successful.</span></span> <span data-ttu-id="42a6b-120">Jeder andere Rückgabecode weist auf eine Fehlerbedingung hin.</span><span class="sxs-lookup"><span data-stu-id="42a6b-120">Any other return code indicates an error condition.</span></span><br/> |
| <span data-ttu-id="42a6b-121">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="42a6b-121">**OnlineDevice**</span></span>                                             | <span data-ttu-id="42a6b-122">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-122">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="42a6b-123">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="42a6b-123">**QuiesceDevice**</span></span>                                            | <span data-ttu-id="42a6b-124">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-124">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="42a6b-125">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="42a6b-125">**RequestStateChange**</span></span>                                       | <span data-ttu-id="42a6b-126">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-126">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="42a6b-127">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="42a6b-127">**Reset**</span></span>                                                    | <span data-ttu-id="42a6b-128">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-128">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="42a6b-129">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="42a6b-129">**RestoreProperties**</span></span>                                        | <span data-ttu-id="42a6b-130">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-130">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="42a6b-131">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="42a6b-131">**SaveProperties**</span></span>                                           | <span data-ttu-id="42a6b-132">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-132">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="42a6b-133">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="42a6b-133">**SetPowerState**</span></span>                                            | <span data-ttu-id="42a6b-134">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-134">This method is not supported.</span></span><br/>                                                                                                                                                                                            |



 

### <a name="properties"></a><span data-ttu-id="42a6b-135">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="42a6b-135">Properties</span></span>

<span data-ttu-id="42a6b-136">Die **MSVM- \_ rdvcomponent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="42a6b-136">The **Msvm\_RdvComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="42a6b-137">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="42a6b-137">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-138">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="42a6b-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-140">Alle zusätzlichen Verfügbarkeit und der Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="42a6b-140">Any additional availability and status of the device.</span></span> <span data-ttu-id="42a6b-141">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="42a6b-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="42a6b-142">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="42a6b-142">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-143">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="42a6b-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-145">Die primäre Verfügbarkeit und den Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="42a6b-145">The primary availability and status of the device.</span></span> <span data-ttu-id="42a6b-146">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="42a6b-146">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="42a6b-147">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="42a6b-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-148">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="42a6b-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-150">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="42a6b-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="42a6b-151">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="42a6b-152">**Caption**</span><span class="sxs-lookup"><span data-stu-id="42a6b-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="42a6b-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-155">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="42a6b-155">A short description of the object.</span></span> <span data-ttu-id="42a6b-156">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="42a6b-157">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="42a6b-157">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-158">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="42a6b-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-160">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="42a6b-160">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="42a6b-161">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="42a6b-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="42a6b-162">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="42a6b-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="42a6b-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="42a6b-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="42a6b-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="42a6b-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="42a6b-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="42a6b-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="42a6b-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="42a6b-170">)</span><span class="sxs-lookup"><span data-stu-id="42a6b-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="42a6b-171">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="42a6b-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-172">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="42a6b-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-174">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="42a6b-174">The scoping system's creation class name.</span></span> <span data-ttu-id="42a6b-175">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="42a6b-176">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="42a6b-176">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="42a6b-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-179">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="42a6b-179">A description of the object.</span></span> <span data-ttu-id="42a6b-180">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="42a6b-181">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="42a6b-181">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-182">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="42a6b-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-184">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="42a6b-184">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="42a6b-185">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="42a6b-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="42a6b-186">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="42a6b-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="42a6b-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="42a6b-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="42a6b-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="42a6b-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="42a6b-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="42a6b-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="42a6b-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="42a6b-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="42a6b-195">)</span><span class="sxs-lookup"><span data-stu-id="42a6b-195">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="42a6b-196">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="42a6b-196">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-197">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="42a6b-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-199">Eine Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="42a6b-199">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="42a6b-200">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="42a6b-201">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="42a6b-201">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-202">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="42a6b-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-204">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-204">A display name for the object.</span></span> <span data-ttu-id="42a6b-205">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="42a6b-206">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="42a6b-206">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-207">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="42a6b-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-208">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-209">Die Standard-oder Startkonfiguration eines Administrators für die **enabledstate** -Eigenschaft eines Elements.</span><span class="sxs-lookup"><span data-stu-id="42a6b-209">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="42a6b-210">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-210">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="42a6b-211">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="42a6b-211">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-212">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="42a6b-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-213">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-214">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="42a6b-214">The enabled and disabled states of an element.</span></span> <span data-ttu-id="42a6b-215">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, und es handelt sich um einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="42a6b-215">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="42a6b-216">Wert</span><span class="sxs-lookup"><span data-stu-id="42a6b-216">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="42a6b-217">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="42a6b-217">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="42a6b-218"><dt>**Unbekannter**</dt> Wert <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="42a6b-218"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="42a6b-219">Der Zustand des Elements konnte nicht bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="42a6b-219">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="42a6b-220"><dt>**Sonstige**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="42a6b-220"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="42a6b-221"><dt>**Aktiviert**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="42a6b-221"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="42a6b-222">Das-Element wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-222">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="42a6b-223"><dt>**Deaktiviert**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="42a6b-223"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="42a6b-224">Das Element ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="42a6b-224">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="42a6b-225"><dt>4</dt> wird <dt>**heruntergefahren**</dt></span><span class="sxs-lookup"><span data-stu-id="42a6b-225"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="42a6b-226">Das Element wird gerade in den deaktivierten Zustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-226">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="42a6b-227"><dt>**Nicht zutreffend**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="42a6b-227"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="42a6b-228">Das Element unterstützt das Aktivieren oder Deaktivieren des Elements nicht.</span><span class="sxs-lookup"><span data-stu-id="42a6b-228">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="42a6b-229"><dt>**Aktiviert, aber offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="42a6b-229"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="42a6b-230">Das Element kann Befehle abschließen und löscht alle neuen Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="42a6b-230">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="42a6b-231"><dt>**In Test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="42a6b-231"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="42a6b-232">Das-Element befindet sich in einem Testzustand.</span><span class="sxs-lookup"><span data-stu-id="42a6b-232">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="42a6b-233"><dt></dt> Verzögert <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="42a6b-233"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="42a6b-234">Das Element kann Befehle abschließen, aber alle neuen Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="42a6b-234">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="42a6b-235"><dt>**Inesce**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="42a6b-235"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="42a6b-236">Das Element ist aktiviert, jedoch in einem eingeschränkten Modus.</span><span class="sxs-lookup"><span data-stu-id="42a6b-236">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="42a6b-237">Das Verhalten des-Elements ähnelt dem aktivierten Status (2), aber es verarbeitet nur einen eingeschränkten Satz von Befehlen.</span><span class="sxs-lookup"><span data-stu-id="42a6b-237">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="42a6b-238">Alle anderen Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="42a6b-238">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="42a6b-239"><dt>**Start**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="42a6b-239"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="42a6b-240">Das Element wechselt in den Zustand "aktiviert" (2).</span><span class="sxs-lookup"><span data-stu-id="42a6b-240">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="42a6b-241">Neue Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="42a6b-241">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="42a6b-242">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="42a6b-242">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-243">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="42a6b-243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-244">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-245">Gibt an, ob der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="42a6b-245">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="42a6b-246">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="42a6b-246">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="42a6b-247">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="42a6b-247">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-248">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="42a6b-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-249">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-250">Eine Zeichenfolge, die weitere Informationen über den Fehler enthält, der in **LastErrorCode** aufgezeichnet wurde, sowie Informationen über alle Maßnahmen, die ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="42a6b-250">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="42a6b-251">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="42a6b-251">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="42a6b-252">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="42a6b-252">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-253">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="42a6b-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-254">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-255">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="42a6b-255">The current health of the element.</span></span> <span data-ttu-id="42a6b-256">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="42a6b-257">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="42a6b-257">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-258">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="42a6b-258">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-259">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-260">Ein Array von Freiform-Zeichen folgen, die Erklärungen und Details hinter den Einträgen im Eigenschafts Array " **OtherIdentifyingInfo** " bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="42a6b-260">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="42a6b-261">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="42a6b-261">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="42a6b-262">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="42a6b-262">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-263">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="42a6b-263">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-264">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-265">Das Datum und die Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="42a6b-265">The date and time when the object was installed.</span></span> <span data-ttu-id="42a6b-266">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="42a6b-266">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="42a6b-267">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="42a6b-268">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="42a6b-268">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-269">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="42a6b-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-270">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-271">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="42a6b-271">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-272">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="42a6b-272">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="42a6b-273">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-273">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="42a6b-274">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="42a6b-274">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-275">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42a6b-275">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-276">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-277">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="42a6b-277">The last error code reported by the logical device.</span></span> <span data-ttu-id="42a6b-278">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="42a6b-278">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="42a6b-279">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="42a6b-279">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-280">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="42a6b-280">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-281">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-282">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="42a6b-282">This property has been deprecated.</span></span> <span data-ttu-id="42a6b-283">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="42a6b-283">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="42a6b-284">**Name**</span><span class="sxs-lookup"><span data-stu-id="42a6b-284">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-285">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="42a6b-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-286">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-287">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="42a6b-287">The label by which the object is known.</span></span> <span data-ttu-id="42a6b-288">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-288">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="42a6b-289">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="42a6b-289">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-290">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="42a6b-290">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-291">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-292">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="42a6b-292">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="42a6b-293">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="42a6b-293">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="42a6b-294">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-294">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="42a6b-295"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="42a6b-295"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-296"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="42a6b-296"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-297"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="42a6b-297"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-298"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="42a6b-298"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-299"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="42a6b-299"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-300"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="42a6b-300"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-301"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="42a6b-301"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-302"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="42a6b-302"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-303"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="42a6b-303"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-304"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="42a6b-304"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-305"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="42a6b-305"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-306"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="42a6b-306"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-307"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="42a6b-307"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-308"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="42a6b-308"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-309"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="42a6b-309"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-310"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="42a6b-310"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-311"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="42a6b-311"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-312"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="42a6b-312"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-313"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="42a6b-313"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="42a6b-314">)</span><span class="sxs-lookup"><span data-stu-id="42a6b-314">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="42a6b-315">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="42a6b-315">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-316">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="42a6b-316">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-317">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-318">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="42a6b-318">The current statuses of the object.</span></span> <span data-ttu-id="42a6b-319">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-319">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="42a6b-320">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="42a6b-320">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-321">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="42a6b-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-322">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-323">Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="42a6b-323">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="42a6b-324">Diese Eigenschaft muss auf **null** festgelegt werden, wenn die **enabledstate** -Eigenschaft einen anderen Wert als 1 hat.</span><span class="sxs-lookup"><span data-stu-id="42a6b-324">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="42a6b-325">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-325">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="42a6b-326">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="42a6b-326">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-327">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="42a6b-327">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-328">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-329">Alle zusätzlichen Daten über Geräte-ID-Informationen, die zur Identifizierung eines logischen Geräts verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="42a6b-329">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="42a6b-330">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="42a6b-330">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="42a6b-331">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="42a6b-331">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-332">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="42a6b-332">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-333">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-334">Die Energie Verwaltungsfunktionen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="42a6b-334">The power management capabilities of the device.</span></span> <span data-ttu-id="42a6b-335">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="42a6b-335">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="42a6b-336">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="42a6b-336">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-337">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="42a6b-337">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-338">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-339">Gibt an, ob das Gerät Energie gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="42a6b-339">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="42a6b-340">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="42a6b-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="42a6b-341">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="42a6b-341">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-342">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="42a6b-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-343">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-344">Gibt an, wie viele aufeinanderfolgende Stunden dieses Gerät seit dem letzten Strom Umgebung eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="42a6b-344">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="42a6b-345">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="42a6b-345">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="42a6b-346">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="42a6b-346">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-347">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="42a6b-347">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-348">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-349">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="42a6b-349">Provides high level status information.</span></span> <span data-ttu-id="42a6b-350">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="42a6b-350">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="42a6b-351">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="42a6b-351">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="42a6b-352">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-352">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="42a6b-353"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="42a6b-353"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-354"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="42a6b-354"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-355"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="42a6b-355"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-356"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="42a6b-356"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-357"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="42a6b-357"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-358"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="42a6b-358"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="42a6b-359">)</span><span class="sxs-lookup"><span data-stu-id="42a6b-359">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="42a6b-360">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="42a6b-360">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-361">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="42a6b-361">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-362">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-363">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="42a6b-363">The last requested or desired state for the element.</span></span> <span data-ttu-id="42a6b-364">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 12 (nicht zutreffend) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-364">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="42a6b-365">**Status**</span><span class="sxs-lookup"><span data-stu-id="42a6b-365">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-366">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="42a6b-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-367">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-368">Der aktuelle Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="42a6b-368">The current status of the object.</span></span> <span data-ttu-id="42a6b-369">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="42a6b-369">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="42a6b-370">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="42a6b-370">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-371">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="42a6b-371">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-372">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-373">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="42a6b-373">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="42a6b-374">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="42a6b-375">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="42a6b-375">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-376">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="42a6b-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-377">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-378">Der aktuelle Zustand des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="42a6b-378">The current state of the logical device.</span></span> <span data-ttu-id="42a6b-379">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="42a6b-379">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="42a6b-380">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="42a6b-380">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-381">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="42a6b-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-382">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-383">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="42a6b-383">The scoping system's creation class name.</span></span> <span data-ttu-id="42a6b-384">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-384">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="42a6b-385">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="42a6b-385">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-386">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="42a6b-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-387">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-388">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="42a6b-388">The scoping system's name.</span></span> <span data-ttu-id="42a6b-389">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-389">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="42a6b-390">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="42a6b-390">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-391">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="42a6b-391">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-392">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-393">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="42a6b-393">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="42a6b-394">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-394">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="42a6b-395">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="42a6b-395">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-396">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="42a6b-396">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-397">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-398">Die Gesamtanzahl der Stunden, für die dieses Gerät eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="42a6b-398">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="42a6b-399">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="42a6b-399">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="42a6b-400">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="42a6b-400">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42a6b-401">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="42a6b-401">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="42a6b-402">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42a6b-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42a6b-403">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="42a6b-403">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="42a6b-404">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="42a6b-404">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="42a6b-405">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42a6b-405">Requirements</span></span>



| <span data-ttu-id="42a6b-406">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42a6b-406">Requirement</span></span> | <span data-ttu-id="42a6b-407">Wert</span><span class="sxs-lookup"><span data-stu-id="42a6b-407">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42a6b-408">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="42a6b-408">Minimum supported client</span></span><br/> | <span data-ttu-id="42a6b-409">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42a6b-409">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="42a6b-410">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="42a6b-410">Minimum supported server</span></span><br/> | <span data-ttu-id="42a6b-411">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42a6b-411">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="42a6b-412">Namespace</span><span class="sxs-lookup"><span data-stu-id="42a6b-412">Namespace</span></span><br/>                | <span data-ttu-id="42a6b-413">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="42a6b-413">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="42a6b-414">MOF</span><span class="sxs-lookup"><span data-stu-id="42a6b-414">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42a6b-415"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="42a6b-415"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="42a6b-416">DLL</span><span class="sxs-lookup"><span data-stu-id="42a6b-416">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42a6b-417"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="42a6b-417"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

