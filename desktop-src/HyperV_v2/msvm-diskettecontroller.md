---
description: Stellt den Disketten Controller auf dem virtuellen Computer dar.
ms.assetid: 38A19BF3-0E8F-4DCE-B2DB-B2E3F8100E00
title: Msvm_DisketteController-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DisketteController
- Msvm_DisketteController.SetPowerState
- Msvm_DisketteController.EnableDevice
- Msvm_DisketteController.OnlineDevice
- Msvm_DisketteController.QuiesceDevice
- Msvm_DisketteController.SaveProperties
- Msvm_DisketteController.RestoreProperties
- Msvm_DisketteController.InstanceID
- Msvm_DisketteController.Caption
- Msvm_DisketteController.Description
- Msvm_DisketteController.ElementName
- Msvm_DisketteController.InstallDate
- Msvm_DisketteController.Name
- Msvm_DisketteController.OperationalStatus
- Msvm_DisketteController.StatusDescriptions
- Msvm_DisketteController.Status
- Msvm_DisketteController.HealthState
- Msvm_DisketteController.CommunicationStatus
- Msvm_DisketteController.DetailedStatus
- Msvm_DisketteController.OperatingStatus
- Msvm_DisketteController.PrimaryStatus
- Msvm_DisketteController.EnabledState
- Msvm_DisketteController.OtherEnabledState
- Msvm_DisketteController.RequestedState
- Msvm_DisketteController.EnabledDefault
- Msvm_DisketteController.TimeOfLastStateChange
- Msvm_DisketteController.AvailableRequestedStates
- Msvm_DisketteController.TransitioningToState
- Msvm_DisketteController.SystemCreationClassName
- Msvm_DisketteController.SystemName
- Msvm_DisketteController.CreationClassName
- Msvm_DisketteController.DeviceID
- Msvm_DisketteController.PowerManagementSupported
- Msvm_DisketteController.PowerManagementCapabilities
- Msvm_DisketteController.Availability
- Msvm_DisketteController.StatusInfo
- Msvm_DisketteController.LastErrorCode
- Msvm_DisketteController.ErrorDescription
- Msvm_DisketteController.ErrorCleared
- Msvm_DisketteController.OtherIdentifyingInfo
- Msvm_DisketteController.PowerOnHours
- Msvm_DisketteController.TotalPowerOnHours
- Msvm_DisketteController.IdentifyingDescriptions
- Msvm_DisketteController.AdditionalAvailability
- Msvm_DisketteController.MaxQuiesceTime
- Msvm_DisketteController.TimeOfLastReset
- Msvm_DisketteController.ProtocolSupported
- Msvm_DisketteController.MaxNumberControlled
- Msvm_DisketteController.ProtocolDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f1e4e731464e25dc8e871ebd17cdcddd4e262673
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751176"
---
# <a name="msvm_diskettecontroller-class"></a><span data-ttu-id="1ffaa-103">MSVM \_ diskettecontroller-Klasse</span><span class="sxs-lookup"><span data-stu-id="1ffaa-103">Msvm\_DisketteController class</span></span>

<span data-ttu-id="1ffaa-104">Stellt den Disketten Controller auf dem virtuellen Computer dar.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-104">Represents the floppy controller in the virtual machine.</span></span> <span data-ttu-id="1ffaa-105">Der Disketten Controller ist korrigiert, daher ist kein Ressourcenpool zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-105">The floppy controller is fixed, therefore there is no resource pool associated with it.</span></span>

<span data-ttu-id="1ffaa-106">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ffaa-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ffaa-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DisketteController : CIM_Controller
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName = "Msvm_DisketteController";
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
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 7;
  uint32   MaxNumberControlled = 1;
  string   ProtocolDescription = "Diskette Protocol";
};
```

## <a name="members"></a><span data-ttu-id="1ffaa-108">Member</span><span class="sxs-lookup"><span data-stu-id="1ffaa-108">Members</span></span>

<span data-ttu-id="1ffaa-109">Die **MSVM \_ diskettecontroller** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1ffaa-109">The **Msvm\_DisketteController** class has these types of members:</span></span>

-   [<span data-ttu-id="1ffaa-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="1ffaa-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="1ffaa-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1ffaa-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1ffaa-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="1ffaa-112">Methods</span></span>

<span data-ttu-id="1ffaa-113">Die **MSVM \_ diskettecontroller** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-113">The **Msvm\_DisketteController** class has these methods.</span></span>



| <span data-ttu-id="1ffaa-114">Methode</span><span class="sxs-lookup"><span data-stu-id="1ffaa-114">Method</span></span>                                                                   | <span data-ttu-id="1ffaa-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1ffaa-115">Description</span></span>                              |
|:-------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="1ffaa-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-116">**EnableDevice**</span></span>                                                         | <span data-ttu-id="1ffaa-117">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="1ffaa-118">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-118">**OnlineDevice**</span></span>                                                         | <span data-ttu-id="1ffaa-119">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="1ffaa-120">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-120">**QuiesceDevice**</span></span>                                                        | <span data-ttu-id="1ffaa-121">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="1ffaa-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-122">**RequestStateChange**</span></span>](msvm-diskettecontroller-requeststatechange.md) | <span data-ttu-id="1ffaa-123">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="1ffaa-124">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-124">**Reset**</span></span>](msvm-diskettecontroller-reset.md)                           | <span data-ttu-id="1ffaa-125">Setzt das virtuelle Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-125">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="1ffaa-126">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-126">**RestoreProperties**</span></span>                                                    | <span data-ttu-id="1ffaa-127">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="1ffaa-128">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-128">**SaveProperties**</span></span>                                                       | <span data-ttu-id="1ffaa-129">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="1ffaa-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-130">**SetPowerState**</span></span>                                                        | <span data-ttu-id="1ffaa-131">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1ffaa-132">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1ffaa-132">Properties</span></span>

<span data-ttu-id="1ffaa-133">Die **MSVM \_ diskettecontroller** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-133">The **Msvm\_DisketteController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1ffaa-134">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-134">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-135">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="1ffaa-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-137">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist auf 6 festgelegt (nicht zutreffend).</span><span class="sxs-lookup"><span data-stu-id="1ffaa-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-138">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-139">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-141">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist auf 6 festgelegt (nicht zutreffend).</span><span class="sxs-lookup"><span data-stu-id="1ffaa-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-142">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-142">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-143">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="1ffaa-143">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-145">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-145">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="1ffaa-146">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-146">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-147">**Caption**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-147">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-148">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-150">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-150">A short description of the object.</span></span> <span data-ttu-id="1ffaa-151">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-151">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-152">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-152">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-153">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-155">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-155">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="1ffaa-156">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-156">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1ffaa-157">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-157">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1ffaa-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-159"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-159"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-160"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-160"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-161"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-161"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-162"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-162"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-163"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-163"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-164"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="1ffaa-164"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1ffaa-165">)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-165">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1ffaa-166">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-166">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-167">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-169">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-169">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="1ffaa-170">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und auf "MSVM \_ diskettecontroller" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-170">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Msvm\_DisketteController".</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-171">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-171">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-172">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-174">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-174">A description of the object.</span></span> <span data-ttu-id="1ffaa-175">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-175">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-176">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-176">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-177">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-179">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-179">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="1ffaa-180">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-180">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1ffaa-181">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-181">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1ffaa-182"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-182"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-183"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-183"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-184"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-184"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-185"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-185"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-186"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-186"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-187"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-187"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="1ffaa-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1ffaa-190">)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-190">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1ffaa-191">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-191">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-192">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-194">Eine Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-194">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="1ffaa-195">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-195">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-196">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-196">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-197">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-199">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-199">A display name for the object.</span></span> <span data-ttu-id="1ffaa-200">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-201">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-201">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-202">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-204">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-204">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="1ffaa-205">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-205">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-206">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-206">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-207">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-208">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-209">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-209">The enabled and disabled states of an element.</span></span> <span data-ttu-id="1ffaa-210">Sie kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-210">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="1ffaa-211">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-211">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="1ffaa-212">Wert</span><span class="sxs-lookup"><span data-stu-id="1ffaa-212">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="1ffaa-213">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1ffaa-213">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="1ffaa-214"><dt>**Unbekannter**</dt> Wert <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1ffaa-214"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="1ffaa-215">Der Zustand des Elements konnte nicht bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-215">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="1ffaa-216"><dt>**Sonstige**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="1ffaa-216"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="1ffaa-217"><dt>**Aktiviert**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1ffaa-217"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="1ffaa-218">Das-Element wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-218">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="1ffaa-219"><dt>**Deaktiviert**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1ffaa-219"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="1ffaa-220">Das Element ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-220">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="1ffaa-221"><dt>4</dt> wird <dt>**heruntergefahren**</dt></span><span class="sxs-lookup"><span data-stu-id="1ffaa-221"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="1ffaa-222">Das Element wird gerade in den deaktivierten Zustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-222">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="1ffaa-223"><dt>**Nicht zutreffend**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="1ffaa-223"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="1ffaa-224">Das Element unterstützt das Aktivieren oder Deaktivieren des Elements nicht.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-224">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="1ffaa-225"><dt>**Aktiviert, aber offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="1ffaa-225"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="1ffaa-226">Das Element kann Befehle abschließen und löscht alle neuen Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-226">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="1ffaa-227"><dt>**In Test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="1ffaa-227"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="1ffaa-228">Das-Element befindet sich in einem Testzustand.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-228">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="1ffaa-229"><dt></dt> Verzögert <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="1ffaa-229"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="1ffaa-230">Das Element kann Befehle abschließen, aber alle neuen Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-230">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="1ffaa-231"><dt>**Inesce**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="1ffaa-231"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="1ffaa-232">Das-Element ist aktiviert, befindet sich jedoch in einem eingeschränkten Modus.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-232">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="1ffaa-233">Das Verhalten des-Elements ähnelt dem aktivierten Status (2), aber es verarbeitet nur einen eingeschränkten Satz von Befehlen.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-233">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="1ffaa-234">Alle anderen Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-234">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="1ffaa-235"><dt>**Start**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="1ffaa-235"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="1ffaa-236">Das Element wechselt in den Zustand "aktiviert" (2).</span><span class="sxs-lookup"><span data-stu-id="1ffaa-236">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="1ffaa-237">Neue Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-237">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="1ffaa-238">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-238">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-239">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1ffaa-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-240">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-241">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-241">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-242">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-242">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-243">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-244">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-245">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-245">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-246">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-246">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-247">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-248">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-249">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-249">The current health of the element.</span></span> <span data-ttu-id="1ffaa-250">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-250">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="1ffaa-251">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-251">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="1ffaa-252">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-252">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-253">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-253">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-254">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="1ffaa-254">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-255">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-256">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-256">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-257">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-257">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-258">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-258">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-259">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-260">Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-260">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="1ffaa-261">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-261">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-262">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-262">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-263">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-264">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-265">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-265">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-266">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-266">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="1ffaa-267">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-267">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-268">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-268">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-269">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-269">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-270">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-271">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-271">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-272">**Maxnuma**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-272">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-273">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-274">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-275">Die maximale Anzahl direkt Adressier barer Entitäten, die von diesem Controller unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-275">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="1ffaa-276">Wenn die Zahl unbekannt oder unbegrenzt ist, sollte der Wert 0 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-276">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="1ffaa-277">Das Protokoll, das vom Controller für den Zugriff auf gesteuerte Geräte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-277">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="1ffaa-278">Diese Eigenschaft wird vom [**CIM- \_ Controller**](/windows/desktop/CIMWin32Prov/cim-controller)geerbt und auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-278">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-279">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-279">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-280">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-280">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-281">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-282">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-282">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-283">**Name**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-283">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-284">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-285">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-286">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-286">The label by which the object is known.</span></span> <span data-ttu-id="1ffaa-287">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-287">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-288">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-288">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-289">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-289">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-290">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-291">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-291">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="1ffaa-292">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-292">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1ffaa-293">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-293">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1ffaa-294"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-294"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-295"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-295"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-296"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-296"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-297"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-297"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-298"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="1ffaa-298"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-299"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-299"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-300"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-300"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-301"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-301"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-302"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-302"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-303"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-303"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-304"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-304"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-305"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-305"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-306"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-306"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-307"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-307"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-308"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-308"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-309"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-309"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-310"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-310"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-311"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-311"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-312"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="1ffaa-312"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1ffaa-313">)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-313">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1ffaa-314">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-314">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-315">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="1ffaa-315">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-316">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-317">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-317">The current statuses of the object.</span></span> <span data-ttu-id="1ffaa-318">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-318">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-319">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-319">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-320">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-321">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-322">Der aktivierte oder deaktivierte Status des Elements, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-322">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="1ffaa-323">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-323">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="1ffaa-324">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-324">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-325">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-325">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-326">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="1ffaa-326">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-327">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-328">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-328">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-329">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-329">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-330">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="1ffaa-330">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-331">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-332">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-332">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-333">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-333">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-334">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1ffaa-334">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-335">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-336">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-336">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-337">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-337">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-338">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-338">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-339">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-340">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-341">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-341">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-342">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-342">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-343">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-344">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-344">Provides high level status information.</span></span> <span data-ttu-id="1ffaa-345">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-345">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="1ffaa-346">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-346">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1ffaa-347">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-347">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1ffaa-348"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-348"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-349"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-349"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-350"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="1ffaa-350"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-351"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-351"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-352"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-352"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-353"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="1ffaa-353"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1ffaa-354">)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-354">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1ffaa-355">**Protocoldescription**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-355">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-356">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-357">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-358">Eine Zeichenfolge, die weitere Informationen bereitstellt, die mit dem vom Controller unterstützten Protokoll verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-358">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="1ffaa-359">Diese Eigenschaft wird vom [**CIM- \_ Controller**](/windows/desktop/CIMWin32Prov/cim-controller)geerbt und auf "Disketten Protokoll" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-359">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is set to "Diskette Protocol".</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-360">**Protocolsupported**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-360">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-361">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-361">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-362">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-363">Das Protokoll, das vom Controller für den Zugriff auf gesteuerte Geräte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-363">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="1ffaa-364">Diese Eigenschaft wird vom [**CIM- \_ Controller**](/windows/desktop/CIMWin32Prov/cim-controller)geerbt und auf 7 (flexible Diskette) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-364">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is set to 7 (Flexible Diskette).</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-365">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-365">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-366">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-366">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-367">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-368">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-368">The last requested or desired state for the element.</span></span> <span data-ttu-id="1ffaa-369">Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-369">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="1ffaa-370">Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuell aktivierten oder deaktivierten Zustände zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-370">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="1ffaa-371">Eine bestimmte Instanz eines aktivierten logischen Elements unterstützt **requestedstatechange** möglicherweise nicht.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-371">A particular instance of an enabled logical element might not support **RequestedStateChange**.</span></span> <span data-ttu-id="1ffaa-372">Wenn dies auftritt, wird der Wert 12 (nicht zutreffend) verwendet.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-372">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="1ffaa-373">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-373">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-374">**Status**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-374">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-375">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-376">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-377">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-377">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-378">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-378">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-379">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="1ffaa-379">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-380">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-381">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-381">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="1ffaa-382">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-382">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-383">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-383">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-384">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-384">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-385">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-386">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-386">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-387">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-387">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-388">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-389">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-390">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-390">The scoping system's creation class name.</span></span> <span data-ttu-id="1ffaa-391">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-391">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-392">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-392">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-393">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-394">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-395">Der eindeutige Bezeichner für die Bereichs bezogene virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-395">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="1ffaa-396">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-396">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-397">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-397">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-398">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-398">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-399">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-400">Der Zeitpunkt, zu dem die virtuelle Maschine zuletzt eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-400">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="1ffaa-401">Diese Eigenschaft wird vom [**CIM- \_ Controller**](/windows/desktop/CIMWin32Prov/cim-controller)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-401">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-402">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-402">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-403">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-403">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-404">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-405">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-405">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="1ffaa-406">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-406">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-407">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-407">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-408">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-408">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-409">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-410">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-410">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1ffaa-411">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-411">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ffaa-412">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ffaa-413">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ffaa-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ffaa-414">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-414">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="1ffaa-415">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-415">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1ffaa-416">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ffaa-416">Remarks</span></span>

<span data-ttu-id="1ffaa-417">Der Zugriff auf die **MSVM \_ diskettecontroller** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="1ffaa-417">Access to the **Msvm\_DisketteController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="1ffaa-418">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="1ffaa-418">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="1ffaa-419">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ffaa-419">Requirements</span></span>



| <span data-ttu-id="1ffaa-420">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ffaa-420">Requirement</span></span> | <span data-ttu-id="1ffaa-421">Wert</span><span class="sxs-lookup"><span data-stu-id="1ffaa-421">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ffaa-422">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-422">Minimum supported client</span></span><br/> | <span data-ttu-id="1ffaa-423">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1ffaa-423">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1ffaa-424">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1ffaa-424">Minimum supported server</span></span><br/> | <span data-ttu-id="1ffaa-425">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1ffaa-425">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1ffaa-426">Namespace</span><span class="sxs-lookup"><span data-stu-id="1ffaa-426">Namespace</span></span><br/>                | <span data-ttu-id="1ffaa-427">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="1ffaa-427">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1ffaa-428">MOF</span><span class="sxs-lookup"><span data-stu-id="1ffaa-428">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ffaa-429"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1ffaa-429"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ffaa-430">DLL</span><span class="sxs-lookup"><span data-stu-id="1ffaa-430">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ffaa-431"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1ffaa-431"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1ffaa-432">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ffaa-432">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ffaa-433">**CIM- \_ Controller**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-433">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> <dt>

[<span data-ttu-id="1ffaa-434">**CIM- \_ Controller**</span><span class="sxs-lookup"><span data-stu-id="1ffaa-434">**CIM\_Controller**</span></span>](/windows/desktop/CIMWin32Prov/cim-controller)
</dt> <dt>

[<span data-ttu-id="1ffaa-435">Speicher Klassen</span><span class="sxs-lookup"><span data-stu-id="1ffaa-435">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

