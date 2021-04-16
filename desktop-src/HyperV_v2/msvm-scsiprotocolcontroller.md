---
description: Stellt einen synthetischen SCSI-Controller dar.
ms.assetid: 4ABAB4C8-F922-4AA3-8FEE-5F5AA969E8B4
title: Msvm_SCSIProtocolController-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SCSIProtocolController
- Msvm_SCSIProtocolController.SetPowerState
- Msvm_SCSIProtocolController.EnableDevice
- Msvm_SCSIProtocolController.OnlineDevice
- Msvm_SCSIProtocolController.QuiesceDevice
- Msvm_SCSIProtocolController.SaveProperties
- Msvm_SCSIProtocolController.RestoreProperties
- Msvm_SCSIProtocolController.InstanceID
- Msvm_SCSIProtocolController.Caption
- Msvm_SCSIProtocolController.Description
- Msvm_SCSIProtocolController.ElementName
- Msvm_SCSIProtocolController.InstallDate
- Msvm_SCSIProtocolController.Name
- Msvm_SCSIProtocolController.OperationalStatus
- Msvm_SCSIProtocolController.StatusDescriptions
- Msvm_SCSIProtocolController.Status
- Msvm_SCSIProtocolController.HealthState
- Msvm_SCSIProtocolController.CommunicationStatus
- Msvm_SCSIProtocolController.DetailedStatus
- Msvm_SCSIProtocolController.OperatingStatus
- Msvm_SCSIProtocolController.PrimaryStatus
- Msvm_SCSIProtocolController.EnabledState
- Msvm_SCSIProtocolController.OtherEnabledState
- Msvm_SCSIProtocolController.RequestedState
- Msvm_SCSIProtocolController.EnabledDefault
- Msvm_SCSIProtocolController.TimeOfLastStateChange
- Msvm_SCSIProtocolController.AvailableRequestedStates
- Msvm_SCSIProtocolController.TransitioningToState
- Msvm_SCSIProtocolController.SystemCreationClassName
- Msvm_SCSIProtocolController.SystemName
- Msvm_SCSIProtocolController.CreationClassName
- Msvm_SCSIProtocolController.DeviceID
- Msvm_SCSIProtocolController.PowerManagementSupported
- Msvm_SCSIProtocolController.PowerManagementCapabilities
- Msvm_SCSIProtocolController.Availability
- Msvm_SCSIProtocolController.StatusInfo
- Msvm_SCSIProtocolController.LastErrorCode
- Msvm_SCSIProtocolController.ErrorDescription
- Msvm_SCSIProtocolController.ErrorCleared
- Msvm_SCSIProtocolController.OtherIdentifyingInfo
- Msvm_SCSIProtocolController.PowerOnHours
- Msvm_SCSIProtocolController.TotalPowerOnHours
- Msvm_SCSIProtocolController.IdentifyingDescriptions
- Msvm_SCSIProtocolController.AdditionalAvailability
- Msvm_SCSIProtocolController.MaxQuiesceTime
- Msvm_SCSIProtocolController.MaxUnitsControlled
- Msvm_SCSIProtocolController.NameFormat
- Msvm_SCSIProtocolController.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b65390c7cb03f195e9de39aedc3629688717e0fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530386"
---
# <a name="msvm_scsiprotocolcontroller-class"></a><span data-ttu-id="c3bed-103">MSVM \_ scsiprotocolcontroller-Klasse</span><span class="sxs-lookup"><span data-stu-id="c3bed-103">Msvm\_SCSIProtocolController class</span></span>

<span data-ttu-id="c3bed-104">Stellt einen synthetischen SCSI-Controller dar.</span><span class="sxs-lookup"><span data-stu-id="c3bed-104">Represents a synthetic SCSI controller.</span></span> <span data-ttu-id="c3bed-105">Ein synthetischer SCSI-Controller kann bis zu 256 Laufwerke unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c3bed-105">A synthetic SCSI controller can support up to 256 drives.</span></span>

<span data-ttu-id="c3bed-106">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c3bed-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3bed-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3bed-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SCSIProtocolController : CIM_SCSIProtocolController
{
  string   InstanceID;
  string   Caption = "SCSI Controller";
  string   Description = "Microsoft Virtual SCSI Controller";
  string   ElementName = "SCSI Controller";
  datetime InstallDate;
  string   Name = "SCSI Controller";
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
  string   CreationClassName = "Msvm_SCSIProtocolController";
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
  uint32   MaxUnitsControlled = 256;
  uint16   NameFormat = 0;
  string   OtherNameFormat;
};
```

## <a name="members"></a><span data-ttu-id="c3bed-108">Member</span><span class="sxs-lookup"><span data-stu-id="c3bed-108">Members</span></span>

<span data-ttu-id="c3bed-109">Die **MSVM \_ scsiprotocolcontroller** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c3bed-109">The **Msvm\_SCSIProtocolController** class has these types of members:</span></span>

-   [<span data-ttu-id="c3bed-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="c3bed-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="c3bed-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c3bed-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c3bed-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="c3bed-112">Methods</span></span>

<span data-ttu-id="c3bed-113">Die **MSVM \_ scsiprotocolcontroller** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="c3bed-113">The **Msvm\_SCSIProtocolController** class has these methods.</span></span>



| <span data-ttu-id="c3bed-114">Methode</span><span class="sxs-lookup"><span data-stu-id="c3bed-114">Method</span></span>                                                                       | <span data-ttu-id="c3bed-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c3bed-115">Description</span></span>                              |
|:-----------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="c3bed-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="c3bed-116">**EnableDevice**</span></span>                                                             | <span data-ttu-id="c3bed-117">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c3bed-118">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="c3bed-118">**OnlineDevice**</span></span>                                                             | <span data-ttu-id="c3bed-119">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c3bed-120">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="c3bed-120">**QuiesceDevice**</span></span>                                                            | <span data-ttu-id="c3bed-121">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="c3bed-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="c3bed-122">**RequestStateChange**</span></span>](msvm-scsiprotocolcontroller-requeststatechange.md) | <span data-ttu-id="c3bed-123">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="c3bed-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="c3bed-124">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="c3bed-124">**Reset**</span></span>](msvm-scsiprotocolcontroller-reset.md)                           | <span data-ttu-id="c3bed-125">Setzt das virtuelle Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="c3bed-125">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="c3bed-126">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="c3bed-126">**RestoreProperties**</span></span>                                                        | <span data-ttu-id="c3bed-127">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c3bed-128">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="c3bed-128">**SaveProperties**</span></span>                                                           | <span data-ttu-id="c3bed-129">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c3bed-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="c3bed-130">**SetPowerState**</span></span>                                                            | <span data-ttu-id="c3bed-131">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c3bed-132">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c3bed-132">Properties</span></span>

<span data-ttu-id="c3bed-133">Die **MSVM \_ scsiprotocolcontroller** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c3bed-133">The **Msvm\_SCSIProtocolController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c3bed-134">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="c3bed-134">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-135">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="c3bed-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-137">Alle zusätzlichen Verfügbarkeit und der Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="c3bed-137">Any additional availability and status of the device.</span></span> <span data-ttu-id="c3bed-138">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-138">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="c3bed-139">Wert</span><span class="sxs-lookup"><span data-stu-id="c3bed-139">Value</span></span>                                                                            | <span data-ttu-id="c3bed-140">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3bed-140">Meaning</span></span>                   |
|----------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="c3bed-141"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="c3bed-141"><dt>{ 6 }</dt></span></span> </dl> |                           |
| <dl> <span data-ttu-id="c3bed-142"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="c3bed-142"><dt>6</dt></span></span> </dl>     | <span data-ttu-id="c3bed-143">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="c3bed-143">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c3bed-144">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="c3bed-144">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-145">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3bed-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-147">Die primäre Verfügbarkeit und den Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="c3bed-147">The primary availability and status of the device.</span></span> <span data-ttu-id="c3bed-148">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-148">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="c3bed-149">Wert</span><span class="sxs-lookup"><span data-stu-id="c3bed-149">Value</span></span>                                                                        | <span data-ttu-id="c3bed-150">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3bed-150">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="c3bed-151"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="c3bed-151"><dt>6</dt></span></span> </dl> | <span data-ttu-id="c3bed-152">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="c3bed-152">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c3bed-153">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="c3bed-153">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-154">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="c3bed-154">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-156">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="c3bed-156">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="c3bed-157">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3bed-157">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3bed-158">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c3bed-158">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3bed-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-161">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c3bed-161">A short description of the object.</span></span> <span data-ttu-id="c3bed-162">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c3bed-163">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="c3bed-163">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-164">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3bed-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-166">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="c3bed-166">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="c3bed-167">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="c3bed-167">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c3bed-168">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-168">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c3bed-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="c3bed-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="c3bed-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-171"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="c3bed-171"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-172"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="c3bed-172"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-173"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="c3bed-173"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="c3bed-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="c3bed-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c3bed-176">)</span><span class="sxs-lookup"><span data-stu-id="c3bed-176">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c3bed-177">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="c3bed-177">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-178">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3bed-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-180">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c3bed-180">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c3bed-181">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-181">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c3bed-182">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c3bed-182">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-183">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3bed-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-185">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="c3bed-185">A description of the object.</span></span> <span data-ttu-id="c3bed-186">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-186">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c3bed-187">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="c3bed-187">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-188">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3bed-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-190">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="c3bed-190">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="c3bed-191">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="c3bed-191">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c3bed-192">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-192">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c3bed-193"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="c3bed-193"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-194"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="c3bed-194"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-195"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="c3bed-195"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-196"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="c3bed-196"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-197"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="c3bed-197"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-198"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="c3bed-198"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-199"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="c3bed-199"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-200"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="c3bed-200"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c3bed-201">)</span><span class="sxs-lookup"><span data-stu-id="c3bed-201">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c3bed-202">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="c3bed-202">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-203">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3bed-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-205">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und auf "Microsoft:*GUID* \\ *Device-Specific-Data*" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-205">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="c3bed-206">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c3bed-206">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-207">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3bed-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-208">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-209">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-209">A display name for the object.</span></span> <span data-ttu-id="c3bed-210">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c3bed-211">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="c3bed-211">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-212">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3bed-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-213">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-214">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="c3bed-214">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="c3bed-215">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-215">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="c3bed-216">Wert</span><span class="sxs-lookup"><span data-stu-id="c3bed-216">Value</span></span>                                                                        | <span data-ttu-id="c3bed-217">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3bed-217">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="c3bed-218"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c3bed-218"><dt>2</dt></span></span> </dl> | <span data-ttu-id="c3bed-219">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="c3bed-219">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c3bed-220">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="c3bed-220">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-221">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3bed-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-222">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-223">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="c3bed-223">The enabled and disabled states of an element.</span></span> <span data-ttu-id="c3bed-224">Sie kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben.</span><span class="sxs-lookup"><span data-stu-id="c3bed-224">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="c3bed-225">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-225">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="c3bed-226">Wert</span><span class="sxs-lookup"><span data-stu-id="c3bed-226">Value</span></span>                                                                        | <span data-ttu-id="c3bed-227">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3bed-227">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="c3bed-228"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="c3bed-228"><dt>5</dt></span></span> </dl> | <span data-ttu-id="c3bed-229">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="c3bed-229">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c3bed-230">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="c3bed-230">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-231">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c3bed-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-232">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-233">Gibt an, ob der in der **LastErrorCode** -Eigenschaft gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="c3bed-233">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="c3bed-234">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3bed-234">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3bed-235">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c3bed-235">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-236">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3bed-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-237">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-238">Eine Zeichenfolge, die weitere Informationen über den in der **LastErrorCode** -Eigenschaft aufgezeichneten Fehler sowie Informationen zu ggf. durchzuführenden Maßnahmen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-238">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="c3bed-239">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3bed-239">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3bed-240">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="c3bed-240">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-241">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3bed-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-242">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-243">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="c3bed-243">The current health of the element.</span></span> <span data-ttu-id="c3bed-244">Dadurch wird die Integrität dieses Elements, jedoch nicht notwendigerweise der seiner unter Komponenten ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-244">This expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="c3bed-245">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="c3bed-245">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="c3bed-246">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-246">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c3bed-247">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="c3bed-247">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-248">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="c3bed-248">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-249">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-250">Ein Array von Freiform-Zeichen folgen, die Erklärungen und Details hinter den Einträgen im Eigenschafts Array " **OtherIdentifyingInfo** " bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c3bed-250">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="c3bed-251">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-251">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c3bed-252">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c3bed-252">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-253">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="c3bed-253">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-254">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-255">Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="c3bed-255">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="c3bed-256">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c3bed-257">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c3bed-257">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-258">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3bed-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-259">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-260">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="c3bed-260">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-261">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="c3bed-261">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c3bed-262">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-262">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c3bed-263">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c3bed-263">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-264">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3bed-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-265">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-266">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="c3bed-266">The last error code reported by the logical device.</span></span> <span data-ttu-id="c3bed-267">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3bed-267">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3bed-268">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="c3bed-268">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-269">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c3bed-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-270">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-271">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="c3bed-271">This property has been deprecated.</span></span> <span data-ttu-id="c3bed-272">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-272">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c3bed-273">**Maxunitiongesteuert**</span><span class="sxs-lookup"><span data-stu-id="c3bed-273">**MaxUnitsControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-274">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3bed-274">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-275">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-276">Die maximale Anzahl von Einheiten, die von diesem Protokoll Controller gesteuert oder darauf zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="c3bed-276">The maximum number of units that can be controlled by or accessed through this protocol controller.</span></span> <span data-ttu-id="c3bed-277">Diese Eigenschaft wird von [**CIM \_ protocolcontroller**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-277">This property is inherited from [**CIM\_ProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="c3bed-278">**Name**</span><span class="sxs-lookup"><span data-stu-id="c3bed-278">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-279">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3bed-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-280">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-281">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="c3bed-281">The label by which the object is known.</span></span> <span data-ttu-id="c3bed-282">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-282">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c3bed-283">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="c3bed-283">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-284">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3bed-284">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-285">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-286">Gibt an, wie der Name des SCSI-Protokoll Controllers ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="c3bed-286">Identifies how the name of the SCSI protocol controller is selected.</span></span> <span data-ttu-id="c3bed-287">Diese Eigenschaft wird von [**CIM \_ scsiprotocolcontroller**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-287">This property is inherited from [**CIM\_SCSIProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span></span>



| <span data-ttu-id="c3bed-288">Wert</span><span class="sxs-lookup"><span data-stu-id="c3bed-288">Value</span></span>                                                                        | <span data-ttu-id="c3bed-289">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3bed-289">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="c3bed-290"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c3bed-290"><dt>0</dt></span></span> </dl> | <span data-ttu-id="c3bed-291">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="c3bed-291">Unknown</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c3bed-292">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="c3bed-292">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-293">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3bed-293">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-294">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-295">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c3bed-295">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="c3bed-296">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="c3bed-296">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c3bed-297">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c3bed-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="c3bed-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-299"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="c3bed-299"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-300"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="c3bed-300"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-301"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="c3bed-301"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-302"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="c3bed-302"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-303"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="c3bed-303"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-304"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="c3bed-304"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-305"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="c3bed-305"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-306"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="c3bed-306"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-307"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="c3bed-307"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-308"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="c3bed-308"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-309"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="c3bed-309"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-310"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="c3bed-310"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-311"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="c3bed-311"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-312"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="c3bed-312"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-313"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="c3bed-313"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-314"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="c3bed-314"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-315"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="c3bed-315"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-316"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="c3bed-316"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c3bed-317">)</span><span class="sxs-lookup"><span data-stu-id="c3bed-317">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c3bed-318">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="c3bed-318">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-319">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="c3bed-319">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-320">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-321">Der aktuelle Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c3bed-321">The current status of the object.</span></span> <span data-ttu-id="c3bed-322">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-322">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="c3bed-323">Wert</span><span class="sxs-lookup"><span data-stu-id="c3bed-323">Value</span></span>                                                                            | <span data-ttu-id="c3bed-324">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3bed-324">Meaning</span></span>       |
|----------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="c3bed-325"><dt>2,2</dt></span><span class="sxs-lookup"><span data-stu-id="c3bed-325"><dt>{ 2 }</dt></span></span> </dl> |               |
| <dl> <span data-ttu-id="c3bed-326"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c3bed-326"><dt>2</dt></span></span> </dl>     | <span data-ttu-id="c3bed-327">OK</span><span class="sxs-lookup"><span data-stu-id="c3bed-327">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c3bed-328">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="c3bed-328">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-329">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3bed-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-330">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-331">Der aktivierte oder deaktivierte Status des Elements, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c3bed-331">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="c3bed-332">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="c3bed-332">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="c3bed-333">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-333">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c3bed-334">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="c3bed-334">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-335">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="c3bed-335">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-336">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-337">Alle zusätzlichen Daten über Geräte-ID-Informationen, die zur Identifizierung eines logischen Geräts verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="c3bed-337">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="c3bed-338">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-338">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c3bed-339">**Othernameformat**</span><span class="sxs-lookup"><span data-stu-id="c3bed-339">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-340">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3bed-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-341">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-342">Eine Zeichenfolge, die beschreibt, wie der Protokoll Controller identifiziert wird, wenn das **NameFormat** 1 (Sonstiges) ist.</span><span class="sxs-lookup"><span data-stu-id="c3bed-342">A string that describes how the protocol controller is identified when the **NameFormat** is 1 (Other).</span></span> <span data-ttu-id="c3bed-343">Diese Eigenschaft wird von [**CIM \_ scsiprotocolcontroller**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-343">This property is inherited from [**CIM\_SCSIProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="c3bed-344">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="c3bed-344">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-345">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="c3bed-345">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-346">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-347">Die Energie Verwaltungsfunktionen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="c3bed-347">The power management capabilities of the device.</span></span> <span data-ttu-id="c3bed-348">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3bed-348">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3bed-349">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="c3bed-349">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-350">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c3bed-350">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-351">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-352">Gibt an, ob das Gerät Energie gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="c3bed-352">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="c3bed-353">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3bed-353">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3bed-354">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="c3bed-354">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-355">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c3bed-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-356">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-357">Gibt an, wie viele aufeinanderfolgende Stunden dieses Gerät seit dem letzten Strom Umgebung eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="c3bed-357">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="c3bed-358">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3bed-358">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3bed-359">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="c3bed-359">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-360">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3bed-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-361">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-362">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="c3bed-362">Provides high level status information.</span></span> <span data-ttu-id="c3bed-363">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c3bed-363">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="c3bed-364">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="c3bed-364">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c3bed-365">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-365">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c3bed-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="c3bed-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-367"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="c3bed-367"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-368"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="c3bed-368"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-369"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="c3bed-369"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-370"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="c3bed-370"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-371"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="c3bed-371"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c3bed-372">)</span><span class="sxs-lookup"><span data-stu-id="c3bed-372">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c3bed-373">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="c3bed-373">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-374">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3bed-374">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-375">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-376">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="c3bed-376">The last requested or desired state for the element.</span></span> <span data-ttu-id="c3bed-377">Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-377">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="c3bed-378">Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuell aktivierten oder deaktivierten Zustände zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="c3bed-378">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="c3bed-379">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-379">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="c3bed-380">Wert</span><span class="sxs-lookup"><span data-stu-id="c3bed-380">Value</span></span>                                                                         | <span data-ttu-id="c3bed-381">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3bed-381">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="c3bed-382"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="c3bed-382"><dt>12</dt></span></span> </dl> | <span data-ttu-id="c3bed-383">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="c3bed-383">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c3bed-384">**Status**</span><span class="sxs-lookup"><span data-stu-id="c3bed-384">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-385">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3bed-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-386">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-386">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-387">Der aktuelle Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c3bed-387">The current status of the object.</span></span> <span data-ttu-id="c3bed-388">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3bed-388">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3bed-389">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="c3bed-389">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-390">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="c3bed-390">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-391">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-392">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="c3bed-392">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="c3bed-393">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf "OK" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-393">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="c3bed-394">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="c3bed-394">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-395">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3bed-395">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-396">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-397">Der aktuelle Zustand des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="c3bed-397">The current state of the logical device.</span></span> <span data-ttu-id="c3bed-398">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3bed-398">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3bed-399">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="c3bed-399">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-400">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3bed-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-401">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-401">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-402">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="c3bed-402">The scoping system's creation class name.</span></span> <span data-ttu-id="c3bed-403">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-403">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c3bed-404">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="c3bed-404">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-405">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3bed-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-406">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-406">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-407">Der eindeutige Bezeichner für die Bereichs bezogene virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="c3bed-407">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="c3bed-408">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-408">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c3bed-409">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="c3bed-409">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-410">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="c3bed-410">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-411">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-412">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="c3bed-412">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="c3bed-413">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="c3bed-413">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c3bed-414">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="c3bed-414">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-415">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c3bed-415">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-416">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-417">Die Gesamtanzahl der Stunden, für die dieses Gerät eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="c3bed-417">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="c3bed-418">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3bed-418">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3bed-419">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="c3bed-419">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3bed-420">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3bed-420">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3bed-421">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3bed-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3bed-422">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="c3bed-422">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="c3bed-423">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3bed-423">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3bed-424">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3bed-424">Remarks</span></span>

<span data-ttu-id="c3bed-425">Der Zugriff auf die **MSVM \_ scsiprotocolcontroller** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="c3bed-425">Access to the **Msvm\_SCSIProtocolController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="c3bed-426">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="c3bed-426">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="c3bed-427">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3bed-427">Requirements</span></span>



| <span data-ttu-id="c3bed-428">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3bed-428">Requirement</span></span> | <span data-ttu-id="c3bed-429">Wert</span><span class="sxs-lookup"><span data-stu-id="c3bed-429">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3bed-430">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c3bed-430">Minimum supported client</span></span><br/> | <span data-ttu-id="c3bed-431">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3bed-431">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c3bed-432">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c3bed-432">Minimum supported server</span></span><br/> | <span data-ttu-id="c3bed-433">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3bed-433">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c3bed-434">Namespace</span><span class="sxs-lookup"><span data-stu-id="c3bed-434">Namespace</span></span><br/>                | <span data-ttu-id="c3bed-435">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="c3bed-435">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c3bed-436">MOF</span><span class="sxs-lookup"><span data-stu-id="c3bed-436">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c3bed-437"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c3bed-437"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c3bed-438">DLL</span><span class="sxs-lookup"><span data-stu-id="c3bed-438">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3bed-439"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c3bed-439"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c3bed-440">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3bed-440">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3bed-441">**CIM \_ scsiprotocolcontroller**</span><span class="sxs-lookup"><span data-stu-id="c3bed-441">**CIM\_SCSIProtocolController**</span></span>](cim-scsiprotocolcontroller.md)
</dt> <dt>

[<span data-ttu-id="c3bed-442">**CIM \_ scsiprotocolcontroller**</span><span class="sxs-lookup"><span data-stu-id="c3bed-442">**CIM\_SCSIProtocolController**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)
</dt> <dt>

[<span data-ttu-id="c3bed-443">Speicher Klassen</span><span class="sxs-lookup"><span data-stu-id="c3bed-443">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

