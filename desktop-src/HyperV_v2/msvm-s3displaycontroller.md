---
description: Stellt den Zustand des emulierten S3-Controllers dar, der in jeder Konfiguration der virtuellen Maschine vorhanden ist.
ms.assetid: 194E0195-1AFF-4298-8000-2249495818C2
title: Msvm_S3DisplayController-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_S3DisplayController
- Msvm_S3DisplayController.SetPowerState
- Msvm_S3DisplayController.EnableDevice
- Msvm_S3DisplayController.OnlineDevice
- Msvm_S3DisplayController.QuiesceDevice
- Msvm_S3DisplayController.SaveProperties
- Msvm_S3DisplayController.RestoreProperties
- Msvm_S3DisplayController.InstanceID
- Msvm_S3DisplayController.Caption
- Msvm_S3DisplayController.Description
- Msvm_S3DisplayController.ElementName
- Msvm_S3DisplayController.InstallDate
- Msvm_S3DisplayController.Name
- Msvm_S3DisplayController.OperationalStatus
- Msvm_S3DisplayController.StatusDescriptions
- Msvm_S3DisplayController.Status
- Msvm_S3DisplayController.HealthState
- Msvm_S3DisplayController.CommunicationStatus
- Msvm_S3DisplayController.DetailedStatus
- Msvm_S3DisplayController.OperatingStatus
- Msvm_S3DisplayController.PrimaryStatus
- Msvm_S3DisplayController.EnabledState
- Msvm_S3DisplayController.OtherEnabledState
- Msvm_S3DisplayController.RequestedState
- Msvm_S3DisplayController.EnabledDefault
- Msvm_S3DisplayController.TimeOfLastStateChange
- Msvm_S3DisplayController.AvailableRequestedStates
- Msvm_S3DisplayController.TransitioningToState
- Msvm_S3DisplayController.SystemCreationClassName
- Msvm_S3DisplayController.SystemName
- Msvm_S3DisplayController.CreationClassName
- Msvm_S3DisplayController.DeviceID
- Msvm_S3DisplayController.PowerManagementSupported
- Msvm_S3DisplayController.PowerManagementCapabilities
- Msvm_S3DisplayController.Availability
- Msvm_S3DisplayController.StatusInfo
- Msvm_S3DisplayController.LastErrorCode
- Msvm_S3DisplayController.ErrorDescription
- Msvm_S3DisplayController.ErrorCleared
- Msvm_S3DisplayController.OtherIdentifyingInfo
- Msvm_S3DisplayController.PowerOnHours
- Msvm_S3DisplayController.TotalPowerOnHours
- Msvm_S3DisplayController.IdentifyingDescriptions
- Msvm_S3DisplayController.AdditionalAvailability
- Msvm_S3DisplayController.MaxQuiesceTime
- Msvm_S3DisplayController.TimeOfLastReset
- Msvm_S3DisplayController.ProtocolSupported
- Msvm_S3DisplayController.MaxNumberControlled
- Msvm_S3DisplayController.ProtocolDescription
- Msvm_S3DisplayController.VideoProcessor
- Msvm_S3DisplayController.VideoMemoryType
- Msvm_S3DisplayController.OtherVideoMemoryType
- Msvm_S3DisplayController.NumberOfVideoPages
- Msvm_S3DisplayController.MaxMemorySupported
- Msvm_S3DisplayController.AcceleratorCapabilities
- Msvm_S3DisplayController.CapabilityDescriptions
- Msvm_S3DisplayController.OtherVideoArchitecture
- Msvm_S3DisplayController.VideoArchitecture
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a4195ff8947bf92d8e4af3a95df320ed950ab21e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104132097"
---
# <a name="msvm_s3displaycontroller-class"></a><span data-ttu-id="82d84-103">MSVM \_ S3DisplayController-Klasse</span><span class="sxs-lookup"><span data-stu-id="82d84-103">Msvm\_S3DisplayController class</span></span>

<span data-ttu-id="82d84-104">Stellt den Zustand des emulierten S3-Controllers dar, der in jeder Konfiguration der virtuellen Maschine vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="82d84-104">Represents the state of the emulated S3 controller that is present in each virtual machine configuration.</span></span> <span data-ttu-id="82d84-105">Auf einem virtuellen Computer kann zu einem beliebigen Zeitpunkt nur ein Anzeige Controller aktiv sein.</span><span class="sxs-lookup"><span data-stu-id="82d84-105">Only one display controller can be active in a virtual machine at any time.</span></span>

> [!Note]  
> <span data-ttu-id="82d84-106">Diese Klasse gilt nur für virtuelle Maschinen der Generation 1.</span><span class="sxs-lookup"><span data-stu-id="82d84-106">This class only applies to generation 1 virtual machines.</span></span>

 

<span data-ttu-id="82d84-107">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="82d84-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="82d84-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="82d84-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_S3DisplayController : CIM_DisplayController
{
  string   InstanceID;
  string   Caption = "Display Controller";
  string   Description = "Microsoft Emulated Display Controller";
  string   ElementName = "Display Controller";
  datetime InstallDate;
  string   Name = "Display Controller";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 3;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_S3DisplayController";
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
  uint16   ProtocolSupported = 1;
  uint32   MaxNumberControlled = 1;
  string   ProtocolDescription = "Video";
  string   VideoProcessor = "Virtual S3 Video Processor";
  uint16   VideoMemoryType = 2;
  string   OtherVideoMemoryType;
  uint32   NumberOfVideoPages = 32768;
  uint32   MaxMemorySupported = 134217728;
  uint16   AcceleratorCapabilities[] = { 2 };
  string   CapabilityDescriptions[] = { "Graphics Accelerator" };
  string   OtherVideoArchitecture;
  uint16   VideoArchitecture;
};
```

## <a name="members"></a><span data-ttu-id="82d84-109">Member</span><span class="sxs-lookup"><span data-stu-id="82d84-109">Members</span></span>

<span data-ttu-id="82d84-110">Die **MSVM \_ S3DisplayController** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="82d84-110">The **Msvm\_S3DisplayController** class has these types of members:</span></span>

-   [<span data-ttu-id="82d84-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="82d84-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="82d84-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="82d84-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="82d84-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="82d84-113">Methods</span></span>

<span data-ttu-id="82d84-114">Die **MSVM- \_ S3DisplayController** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="82d84-114">The **Msvm\_S3DisplayController** class has these methods.</span></span>



| <span data-ttu-id="82d84-115">Methode</span><span class="sxs-lookup"><span data-stu-id="82d84-115">Method</span></span>                                                                    | <span data-ttu-id="82d84-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="82d84-116">Description</span></span>                              |
|:--------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="82d84-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="82d84-117">**EnableDevice**</span></span>                                                          | <span data-ttu-id="82d84-118">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="82d84-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="82d84-119">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="82d84-119">**OnlineDevice**</span></span>                                                          | <span data-ttu-id="82d84-120">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="82d84-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="82d84-121">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="82d84-121">**QuiesceDevice**</span></span>                                                         | <span data-ttu-id="82d84-122">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="82d84-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="82d84-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="82d84-123">**RequestStateChange**</span></span>](msvm-s3displaycontroller-requeststatechange.md) | <span data-ttu-id="82d84-124">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="82d84-124">Requests a state change.</span></span> <br/>     |
| [<span data-ttu-id="82d84-125">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="82d84-125">**Reset**</span></span>](msvm-s3displaycontroller-reset.md)                           | <span data-ttu-id="82d84-126">Setzt das virtuelle Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="82d84-126">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="82d84-127">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="82d84-127">**RestoreProperties**</span></span>                                                     | <span data-ttu-id="82d84-128">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="82d84-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="82d84-129">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="82d84-129">**SaveProperties**</span></span>                                                        | <span data-ttu-id="82d84-130">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="82d84-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="82d84-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="82d84-131">**SetPowerState**</span></span>                                                         | <span data-ttu-id="82d84-132">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="82d84-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="82d84-133">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="82d84-133">Properties</span></span>

<span data-ttu-id="82d84-134">Die **MSVM- \_ S3DisplayController** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="82d84-134">The **Msvm\_S3DisplayController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="82d84-135">**Beschleuniger Funktionen**</span><span class="sxs-lookup"><span data-stu-id="82d84-135">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-136">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="82d84-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="82d84-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-138">Die Grafik-und 3D-Funktionen des Anzeige Controllers.</span><span class="sxs-lookup"><span data-stu-id="82d84-138">The graphics and 3D capabilities of the display controller.</span></span> <span data-ttu-id="82d84-139">Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="82d84-139">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="82d84-140">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="82d84-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-141">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="82d84-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="82d84-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-143">Alle zusätzlichen Verfügbarkeit und der Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="82d84-143">Any additional availability and status of the device.</span></span> <span data-ttu-id="82d84-144">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="82d84-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="82d84-145">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="82d84-145">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-146">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="82d84-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-148">Die primäre Verfügbarkeit und den Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="82d84-148">The primary availability and status of the device.</span></span> <span data-ttu-id="82d84-149">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="82d84-149">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="82d84-150">Wert</span><span class="sxs-lookup"><span data-stu-id="82d84-150">Value</span></span>                                                                        | <span data-ttu-id="82d84-151">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="82d84-151">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="82d84-152"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="82d84-152"><dt>6</dt></span></span> </dl> | <span data-ttu-id="82d84-153">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="82d84-153">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="82d84-154">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="82d84-154">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-155">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="82d84-155">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="82d84-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-157">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="82d84-157">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="82d84-158">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="82d84-158">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="82d84-159">**Capabilitybeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="82d84-159">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-160">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="82d84-160">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="82d84-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-162">Ein Array von Freiform-Zeichen folgen, die Ausführlichere Erläuterungen zu den im **acceleratorforms** -Array angegebenen Video Zugriffs Funktionen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="82d84-162">An array of free-form strings that provide more detailed explanations for any of the video accelerator features indicated in the **AcceleratorCapabilities** array.</span></span> <span data-ttu-id="82d84-163">Jeder Eintrag dieses Arrays bezieht sich auf den Eintrag im **acceleratorfunktionalitäten** -Array, das sich am gleichen Index befindet.</span><span class="sxs-lookup"><span data-stu-id="82d84-163">Each entry of this array is related to the entry in the **AcceleratorCapabilities** array that is located at the same index.</span></span> <span data-ttu-id="82d84-164">Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="82d84-164">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="82d84-165">**Caption**</span><span class="sxs-lookup"><span data-stu-id="82d84-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-166">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="82d84-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-168">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="82d84-168">A short description of the object.</span></span> <span data-ttu-id="82d84-169">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="82d84-169">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="82d84-170">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="82d84-170">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-171">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="82d84-171">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-173">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="82d84-173">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="82d84-174">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="82d84-174">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="82d84-175">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="82d84-175">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="82d84-176"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="82d84-176"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="82d84-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-178"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="82d84-178"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-179"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="82d84-179"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-180"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="82d84-180"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="82d84-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-182"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="82d84-182"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="82d84-183">)</span><span class="sxs-lookup"><span data-stu-id="82d84-183">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="82d84-184">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="82d84-184">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-185">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="82d84-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-187">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="82d84-187">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="82d84-188">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf "MSVM \_ S3DisplayController" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="82d84-188">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_S3DisplayController".</span></span>

</dd> <dt>

<span data-ttu-id="82d84-189">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="82d84-189">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-190">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="82d84-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-192">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="82d84-192">A description of the object.</span></span> <span data-ttu-id="82d84-193">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="82d84-193">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="82d84-194">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="82d84-194">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-195">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="82d84-195">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-196">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-197">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="82d84-197">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="82d84-198">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="82d84-198">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="82d84-199">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="82d84-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="82d84-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="82d84-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-201"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="82d84-201"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-202"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="82d84-202"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-203"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="82d84-203"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-204"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="82d84-204"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-205"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="82d84-205"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-206"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="82d84-206"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-207"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="82d84-207"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="82d84-208">)</span><span class="sxs-lookup"><span data-stu-id="82d84-208">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="82d84-209">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="82d84-209">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-210">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="82d84-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-212">Eine Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="82d84-212">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="82d84-213">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="82d84-213">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="82d84-214">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="82d84-214">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-215">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="82d84-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-216">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-217">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="82d84-217">A display name for the object.</span></span> <span data-ttu-id="82d84-218">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="82d84-218">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="82d84-219">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="82d84-219">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-220">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="82d84-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-221">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-222">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="82d84-222">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="82d84-223">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="82d84-223">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="82d84-224">Wert</span><span class="sxs-lookup"><span data-stu-id="82d84-224">Value</span></span>                                                                        | <span data-ttu-id="82d84-225">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="82d84-225">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="82d84-226"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="82d84-226"><dt>2</dt></span></span> </dl> | <span data-ttu-id="82d84-227">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="82d84-227">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="82d84-228"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="82d84-228"><dt>3</dt></span></span> </dl> | <span data-ttu-id="82d84-229">Disabled</span><span class="sxs-lookup"><span data-stu-id="82d84-229">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="82d84-230">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="82d84-230">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-231">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="82d84-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-232">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-233">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="82d84-233">The enabled and disabled states of an element.</span></span> <span data-ttu-id="82d84-234">Sie kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben.</span><span class="sxs-lookup"><span data-stu-id="82d84-234">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="82d84-235">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 2 (aktiviert) oder 3 (deaktiviert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="82d84-235">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled) or 3 (Disabled).</span></span>



| <span data-ttu-id="82d84-236">Wert</span><span class="sxs-lookup"><span data-stu-id="82d84-236">Value</span></span>                                                                        | <span data-ttu-id="82d84-237">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="82d84-237">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="82d84-238"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="82d84-238"><dt>2</dt></span></span> </dl> | <span data-ttu-id="82d84-239">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="82d84-239">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="82d84-240"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="82d84-240"><dt>3</dt></span></span> </dl> | <span data-ttu-id="82d84-241">Disabled</span><span class="sxs-lookup"><span data-stu-id="82d84-241">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="82d84-242">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="82d84-242">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-243">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="82d84-243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-244">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-245">Gibt an, ob der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="82d84-245">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="82d84-246">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="82d84-246">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="82d84-247">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="82d84-247">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-248">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="82d84-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-249">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-250">Eine Zeichenfolge, die weitere Informationen über den Fehler enthält, der in **LastErrorCode** aufgezeichnet wurde, sowie Informationen über alle Maßnahmen, die ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="82d84-250">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="82d84-251">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="82d84-251">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="82d84-252">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="82d84-252">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-253">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="82d84-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-254">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-255">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="82d84-255">The current health of the element.</span></span> <span data-ttu-id="82d84-256">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="82d84-256">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="82d84-257">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="82d84-257">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="82d84-258">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="82d84-258">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="82d84-259">Wert</span><span class="sxs-lookup"><span data-stu-id="82d84-259">Value</span></span>                                                                        | <span data-ttu-id="82d84-260">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="82d84-260">Meaning</span></span>       |
|------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="82d84-261"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="82d84-261"><dt>5</dt></span></span> </dl> | <span data-ttu-id="82d84-262">OK</span><span class="sxs-lookup"><span data-stu-id="82d84-262">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="82d84-263">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="82d84-263">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-264">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="82d84-264">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="82d84-265">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-266">Ein Array von Freiform-Zeichen folgen, die Erklärungen und Details hinter den Einträgen im Eigenschafts Array " **OtherIdentifyingInfo** " bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="82d84-266">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="82d84-267">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="82d84-267">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="82d84-268">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="82d84-268">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-269">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="82d84-269">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-270">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-271">Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="82d84-271">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="82d84-272">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="82d84-272">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="82d84-273">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="82d84-273">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-274">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="82d84-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-275">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82d84-276">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="82d84-276">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="82d84-277">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="82d84-277">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="82d84-278">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="82d84-278">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="82d84-279">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="82d84-279">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-280">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="82d84-280">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-281">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-282">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="82d84-282">The last error code reported by the logical device.</span></span> <span data-ttu-id="82d84-283">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="82d84-283">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="82d84-284">**Maxmemorysupported**</span><span class="sxs-lookup"><span data-stu-id="82d84-284">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-285">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="82d84-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-286">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-287">Die maximal unterstützte Arbeitsspeicher Größe in Bytes.</span><span class="sxs-lookup"><span data-stu-id="82d84-287">The maximum amount of memory supported, in bytes.</span></span> <span data-ttu-id="82d84-288">Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="82d84-288">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="82d84-289">**Maxnuma**</span><span class="sxs-lookup"><span data-stu-id="82d84-289">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-290">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="82d84-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-291">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-292">Die maximale Anzahl direkt Adressier barer Entitäten, die von diesem Controller unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="82d84-292">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="82d84-293">Wenn die Zahl unbekannt oder unbegrenzt ist, sollte der Wert 0 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="82d84-293">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="82d84-294">Das Protokoll, das vom Controller für den Zugriff auf gesteuerte Geräte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="82d84-294">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="82d84-295">Diese Eigenschaft wird vom [**CIM- \_ Controller**](/windows/desktop/CIMWin32Prov/cim-controller)geerbt.</span><span class="sxs-lookup"><span data-stu-id="82d84-295">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="82d84-296">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="82d84-296">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-297">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="82d84-297">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-298">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-299">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="82d84-299">This property has been deprecated.</span></span> <span data-ttu-id="82d84-300">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="82d84-300">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="82d84-301">**Name**</span><span class="sxs-lookup"><span data-stu-id="82d84-301">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-302">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="82d84-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-303">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-304">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="82d84-304">The label by which the object is known.</span></span> <span data-ttu-id="82d84-305">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="82d84-305">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="82d84-306">**Anzahl der videopages**</span><span class="sxs-lookup"><span data-stu-id="82d84-306">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-307">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="82d84-307">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-308">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-309">Die Anzahl der unterstützten Videoseiten anhand der aktuellen Auflösungen und des verfügbaren Arbeitsspeichers.</span><span class="sxs-lookup"><span data-stu-id="82d84-309">The number of video pages supported given the current resolutions and available memory.</span></span> <span data-ttu-id="82d84-310">Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="82d84-310">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="82d84-311">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="82d84-311">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-312">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="82d84-312">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-313">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-314">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="82d84-314">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="82d84-315">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="82d84-315">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="82d84-316">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="82d84-316">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="82d84-317"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="82d84-317"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-318"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="82d84-318"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-319"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="82d84-319"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-320"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="82d84-320"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-321"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="82d84-321"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-322"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="82d84-322"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-323"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="82d84-323"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-324"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="82d84-324"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-325"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="82d84-325"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-326"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="82d84-326"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-327"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="82d84-327"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-328"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="82d84-328"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-329"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="82d84-329"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-330"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="82d84-330"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-331"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="82d84-331"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-332"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="82d84-332"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-333"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="82d84-333"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-334"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="82d84-334"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-335"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="82d84-335"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="82d84-336">)</span><span class="sxs-lookup"><span data-stu-id="82d84-336">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="82d84-337">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="82d84-337">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-338">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="82d84-338">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="82d84-339">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-340">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="82d84-340">The current statuses of the object.</span></span> <span data-ttu-id="82d84-341">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf 2 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="82d84-341">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="82d84-342">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="82d84-342">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-343">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="82d84-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-344">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-345">Der aktivierte oder deaktivierte Status des Elements, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="82d84-345">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="82d84-346">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="82d84-346">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="82d84-347">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="82d84-347">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="82d84-348">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="82d84-348">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-349">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="82d84-349">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="82d84-350">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-351">Alle zusätzlichen Daten über Geräte-ID-Informationen, die zur Identifizierung eines logischen Geräts verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="82d84-351">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="82d84-352">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="82d84-352">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="82d84-353">**Othervideoarchitecture**</span><span class="sxs-lookup"><span data-stu-id="82d84-353">**OtherVideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-354">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="82d84-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-355">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-356">Eine Zeichenfolge, die den Typ der Video Architektur beschreibt, wenn die **Video Architecture** -Eigenschaft 1 ("Other") ist.</span><span class="sxs-lookup"><span data-stu-id="82d84-356">A string that describes the video architecture type when the **VideoArchitecture** property is 1 ("Other").</span></span> <span data-ttu-id="82d84-357">Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="82d84-357">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="82d84-358">**Othervideomemorytype**</span><span class="sxs-lookup"><span data-stu-id="82d84-358">**OtherVideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-359">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="82d84-359">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-360">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-361">Der Typ des Video Speichers, wenn die **videomemorytype** -Eigenschaft der Instanz 1 (Other) ist.</span><span class="sxs-lookup"><span data-stu-id="82d84-361">The video memory type when the instance's **VideoMemoryType** property is 1 (Other).</span></span> <span data-ttu-id="82d84-362">Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="82d84-362">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="82d84-363">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="82d84-363">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-364">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="82d84-364">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="82d84-365">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-366">Die Energie Verwaltungsfunktionen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="82d84-366">The power management capabilities of the device.</span></span> <span data-ttu-id="82d84-367">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="82d84-367">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="82d84-368">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="82d84-368">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-369">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="82d84-369">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-370">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-371">Gibt an, ob das Gerät Energie gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="82d84-371">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="82d84-372">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="82d84-372">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="82d84-373">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="82d84-373">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-374">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="82d84-374">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-375">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-376">Gibt an, wie viele aufeinanderfolgende Stunden dieses Gerät seit dem letzten Strom Umgebung eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="82d84-376">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="82d84-377">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="82d84-377">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="82d84-378">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="82d84-378">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-379">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="82d84-379">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-380">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-381">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="82d84-381">Provides high level status information.</span></span> <span data-ttu-id="82d84-382">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="82d84-382">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="82d84-383">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="82d84-383">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="82d84-384">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="82d84-384">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="82d84-385"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="82d84-385"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-386"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="82d84-386"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-387"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="82d84-387"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-388"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="82d84-388"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-389"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="82d84-389"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-390"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="82d84-390"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="82d84-391">)</span><span class="sxs-lookup"><span data-stu-id="82d84-391">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="82d84-392">**Protocoldescription**</span><span class="sxs-lookup"><span data-stu-id="82d84-392">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-393">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="82d84-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-394">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-395">Eine Zeichenfolge, die weitere Informationen bereitstellt, die mit dem vom Controller unterstützten Protokoll verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="82d84-395">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="82d84-396">Diese Eigenschaft wird vom [**CIM- \_ Controller**](/windows/desktop/CIMWin32Prov/cim-controller)geerbt.</span><span class="sxs-lookup"><span data-stu-id="82d84-396">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="82d84-397">**Protocolsupported**</span><span class="sxs-lookup"><span data-stu-id="82d84-397">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-398">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="82d84-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-399">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-400">Das Protokoll, das vom Controller für den Zugriff auf gesteuerte Geräte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="82d84-400">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="82d84-401">Diese Eigenschaft wird vom [**CIM- \_ Controller**](/windows/desktop/CIMWin32Prov/cim-controller)geerbt.</span><span class="sxs-lookup"><span data-stu-id="82d84-401">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="82d84-402">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="82d84-402">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-403">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="82d84-403">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-404">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-405">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="82d84-405">The last requested or desired state for the element.</span></span> <span data-ttu-id="82d84-406">Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="82d84-406">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="82d84-407">Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuell aktivierten oder deaktivierten Zustände zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="82d84-407">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="82d84-408">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="82d84-408">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="82d84-409">Wert</span><span class="sxs-lookup"><span data-stu-id="82d84-409">Value</span></span>                                                                         | <span data-ttu-id="82d84-410">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="82d84-410">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="82d84-411"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="82d84-411"><dt>12</dt></span></span> </dl> | <span data-ttu-id="82d84-412">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="82d84-412">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="82d84-413">**Status**</span><span class="sxs-lookup"><span data-stu-id="82d84-413">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-414">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="82d84-414">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-415">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-416">Der aktuelle Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="82d84-416">The current status of the object.</span></span> <span data-ttu-id="82d84-417">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="82d84-417">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="82d84-418">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="82d84-418">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-419">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="82d84-419">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="82d84-420">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-421">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="82d84-421">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="82d84-422">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf "OK" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="82d84-422">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="82d84-423">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="82d84-423">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-424">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="82d84-424">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-425">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-426">Der aktuelle Zustand des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="82d84-426">The current state of the logical device.</span></span> <span data-ttu-id="82d84-427">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="82d84-427">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="82d84-428">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="82d84-428">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-429">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="82d84-429">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-430">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-431">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="82d84-431">The scoping system's creation class name.</span></span> <span data-ttu-id="82d84-432">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="82d84-432">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="82d84-433">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="82d84-433">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-434">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="82d84-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-435">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-436">Der eindeutige Bezeichner für die Bereichs bezogene virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="82d84-436">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="82d84-437">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="82d84-437">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="82d84-438">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="82d84-438">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-439">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="82d84-439">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-440">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-441">Der Zeitpunkt, zu dem die virtuelle Maschine zuletzt eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="82d84-441">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="82d84-442">Diese Eigenschaft wird vom [**CIM- \_ Controller**](/windows/desktop/CIMWin32Prov/cim-controller)geerbt.</span><span class="sxs-lookup"><span data-stu-id="82d84-442">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="82d84-443">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="82d84-443">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-444">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="82d84-444">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-445">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-446">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="82d84-446">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="82d84-447">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="82d84-447">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="82d84-448">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="82d84-448">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-449">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="82d84-449">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-450">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-451">Die Gesamtanzahl der Stunden, für die dieses Gerät eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="82d84-451">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="82d84-452">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="82d84-452">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="82d84-453">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="82d84-453">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-454">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="82d84-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-455">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-456">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="82d84-456">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="82d84-457">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="82d84-457">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="82d84-458">**Videoarchitecture**</span><span class="sxs-lookup"><span data-stu-id="82d84-458">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-459">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="82d84-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-460">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-461">Gibt die Video Architektur des Anzeige Controllers an, mit der das Videosignal generiert wird.</span><span class="sxs-lookup"><span data-stu-id="82d84-461">Specifies the display controller's video architecture used to generate the video signal.</span></span> <span data-ttu-id="82d84-462">In der Regel generiert ein dedizierter Videoprozessor das Videosignal entsprechend der angegebenen Architektur.</span><span class="sxs-lookup"><span data-stu-id="82d84-462">Usually, a dedicated video processor generates the video signal in accordance with the specified architecture.</span></span> <span data-ttu-id="82d84-463">Es ist ein Indikator für die maximale Auflösungs Funktion des Anzeige Controllers.</span><span class="sxs-lookup"><span data-stu-id="82d84-463">It is an indicator of the maximum resolution capability of the display controller.</span></span> <span data-ttu-id="82d84-464">Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="82d84-464">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="82d84-465"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="82d84-465"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-466"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="82d84-466"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-467"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span><span class="sxs-lookup"><span data-stu-id="82d84-467"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-468"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span><span class="sxs-lookup"><span data-stu-id="82d84-468"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-469"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span><span class="sxs-lookup"><span data-stu-id="82d84-469"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-470"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span><span class="sxs-lookup"><span data-stu-id="82d84-470"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-471"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span><span class="sxs-lookup"><span data-stu-id="82d84-471"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-472"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span><span class="sxs-lookup"><span data-stu-id="82d84-472"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-473"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span><span class="sxs-lookup"><span data-stu-id="82d84-473"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-474"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span><span class="sxs-lookup"><span data-stu-id="82d84-474"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-475"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span><span class="sxs-lookup"><span data-stu-id="82d84-475"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-476"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Linearer Rahmen Puffer** (11)</span><span class="sxs-lookup"><span data-stu-id="82d84-476"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Linear Frame Buffer** (11)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-477"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="82d84-477"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-478"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="82d84-478"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="82d84-479"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="82d84-479"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="82d84-480">)</span><span class="sxs-lookup"><span data-stu-id="82d84-480">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="82d84-481">**Videomemorytype**</span><span class="sxs-lookup"><span data-stu-id="82d84-481">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-482">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="82d84-482">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-483">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-483">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-484">Der Typ des Video Speichers.</span><span class="sxs-lookup"><span data-stu-id="82d84-484">The type of video memory.</span></span> <span data-ttu-id="82d84-485">Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="82d84-485">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="82d84-486">**Videoprocessor**</span><span class="sxs-lookup"><span data-stu-id="82d84-486">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d84-487">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="82d84-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82d84-488">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82d84-488">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82d84-489">Eine Zeichenfolge, die den Videoprozessor/-Controller beschreibt.</span><span class="sxs-lookup"><span data-stu-id="82d84-489">A string that describes the video processor/controller.</span></span> <span data-ttu-id="82d84-490">Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="82d84-490">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="82d84-491">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82d84-491">Remarks</span></span>

<span data-ttu-id="82d84-492">Der Zugriff auf die **MSVM- \_ S3DisplayController** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="82d84-492">Access to the **Msvm\_S3DisplayController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="82d84-493">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="82d84-493">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="82d84-494">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="82d84-494">Requirements</span></span>



| <span data-ttu-id="82d84-495">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82d84-495">Requirement</span></span> | <span data-ttu-id="82d84-496">Wert</span><span class="sxs-lookup"><span data-stu-id="82d84-496">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82d84-497">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="82d84-497">Minimum supported client</span></span><br/> | <span data-ttu-id="82d84-498">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="82d84-498">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="82d84-499">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="82d84-499">Minimum supported server</span></span><br/> | <span data-ttu-id="82d84-500">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="82d84-500">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="82d84-501">Namespace</span><span class="sxs-lookup"><span data-stu-id="82d84-501">Namespace</span></span><br/>                | <span data-ttu-id="82d84-502">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="82d84-502">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="82d84-503">MOF</span><span class="sxs-lookup"><span data-stu-id="82d84-503">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82d84-504"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="82d84-504"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="82d84-505">DLL</span><span class="sxs-lookup"><span data-stu-id="82d84-505">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82d84-506"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="82d84-506"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="82d84-507">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82d84-507">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82d84-508">**CIM- \_ Display Controller**</span><span class="sxs-lookup"><span data-stu-id="82d84-508">**CIM\_DisplayController**</span></span>](cim-displaycontroller.md)
</dt> <dt>

<span data-ttu-id="82d84-509">[**CIM- \_ Display Controller**](/previous-versions//cc136810(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="82d84-509">[**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="82d84-510">Video Klassen</span><span class="sxs-lookup"><span data-stu-id="82d84-510">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

