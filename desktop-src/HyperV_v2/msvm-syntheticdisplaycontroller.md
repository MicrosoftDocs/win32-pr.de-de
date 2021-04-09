---
description: Stellt den Status des synthetischen Anzeige Controllers dar, der in jeder Konfiguration der virtuellen Maschine vorhanden ist.
ms.assetid: E496B887-9032-43D8-A7D2-67BB77342AFD
title: Msvm_SyntheticDisplayController-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticDisplayController
- Msvm_SyntheticDisplayController.SetPowerState
- Msvm_SyntheticDisplayController.EnableDevice
- Msvm_SyntheticDisplayController.OnlineDevice
- Msvm_SyntheticDisplayController.QuiesceDevice
- Msvm_SyntheticDisplayController.SaveProperties
- Msvm_SyntheticDisplayController.RestoreProperties
- Msvm_SyntheticDisplayController.InstanceID
- Msvm_SyntheticDisplayController.Caption
- Msvm_SyntheticDisplayController.Description
- Msvm_SyntheticDisplayController.ElementName
- Msvm_SyntheticDisplayController.InstallDate
- Msvm_SyntheticDisplayController.Name
- Msvm_SyntheticDisplayController.OperationalStatus
- Msvm_SyntheticDisplayController.StatusDescriptions
- Msvm_SyntheticDisplayController.Status
- Msvm_SyntheticDisplayController.HealthState
- Msvm_SyntheticDisplayController.CommunicationStatus
- Msvm_SyntheticDisplayController.DetailedStatus
- Msvm_SyntheticDisplayController.OperatingStatus
- Msvm_SyntheticDisplayController.PrimaryStatus
- Msvm_SyntheticDisplayController.EnabledState
- Msvm_SyntheticDisplayController.OtherEnabledState
- Msvm_SyntheticDisplayController.RequestedState
- Msvm_SyntheticDisplayController.EnabledDefault
- Msvm_SyntheticDisplayController.TimeOfLastStateChange
- Msvm_SyntheticDisplayController.AvailableRequestedStates
- Msvm_SyntheticDisplayController.TransitioningToState
- Msvm_SyntheticDisplayController.SystemCreationClassName
- Msvm_SyntheticDisplayController.SystemName
- Msvm_SyntheticDisplayController.CreationClassName
- Msvm_SyntheticDisplayController.DeviceID
- Msvm_SyntheticDisplayController.PowerManagementSupported
- Msvm_SyntheticDisplayController.PowerManagementCapabilities
- Msvm_SyntheticDisplayController.Availability
- Msvm_SyntheticDisplayController.StatusInfo
- Msvm_SyntheticDisplayController.LastErrorCode
- Msvm_SyntheticDisplayController.ErrorDescription
- Msvm_SyntheticDisplayController.ErrorCleared
- Msvm_SyntheticDisplayController.PowerOnHours
- Msvm_SyntheticDisplayController.TotalPowerOnHours
- Msvm_SyntheticDisplayController.OtherIdentifyingInfo
- Msvm_SyntheticDisplayController.IdentifyingDescriptions
- Msvm_SyntheticDisplayController.AdditionalAvailability
- Msvm_SyntheticDisplayController.MaxQuiesceTime
- Msvm_SyntheticDisplayController.TimeOfLastReset
- Msvm_SyntheticDisplayController.ProtocolSupported
- Msvm_SyntheticDisplayController.MaxNumberControlled
- Msvm_SyntheticDisplayController.ProtocolDescription
- Msvm_SyntheticDisplayController.VideoProcessor
- Msvm_SyntheticDisplayController.VideoMemoryType
- Msvm_SyntheticDisplayController.OtherVideoMemoryType
- Msvm_SyntheticDisplayController.NumberOfVideoPages
- Msvm_SyntheticDisplayController.MaxMemorySupported
- Msvm_SyntheticDisplayController.AcceleratorCapabilities
- Msvm_SyntheticDisplayController.CapabilityDescriptions
- Msvm_SyntheticDisplayController.OtherVideoArchitecture
- Msvm_SyntheticDisplayController.VideoArchitecture
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d7f566bf2a75b3ed4f503da245d7b6ce428dce5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863559"
---
# <a name="msvm_syntheticdisplaycontroller-class"></a><span data-ttu-id="16c7d-103">MSVM \_ syntheticdisplaycontroller-Klasse</span><span class="sxs-lookup"><span data-stu-id="16c7d-103">Msvm\_SyntheticDisplayController class</span></span>

<span data-ttu-id="16c7d-104">Stellt den Status des synthetischen Anzeige Controllers dar, der in jeder Konfiguration der virtuellen Maschine vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="16c7d-104">Represents the state of the synthetic display controller that is present in each virtual machine configuration.</span></span> <span data-ttu-id="16c7d-105">Es kann immer nur ein Anzeige Controller auf einem virtuellen Computer aktiv sein, und der synthetische Controller kann nur aktiviert werden, wenn das Gast Betriebssystem die erforderlichen Video Beschleunigungs Dienste geladen hat.</span><span class="sxs-lookup"><span data-stu-id="16c7d-105">Only one display controller can be active in a virtual machine at any time and the synthetic controller can be activated only when the guest operating system has loaded the required video acceleration services.</span></span>

<span data-ttu-id="16c7d-106">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="16c7d-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="16c7d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="16c7d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticDisplayController : CIM_DisplayController
{
  string   InstanceID;
  string   Caption = "Display Controller";
  string   Description = "Microsoft Synthetic Display Controller";
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
  string   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_SyntheticDisplayController";
  string   DeviceID = "Microsoft:GUID";
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 1;
  uint32   MaxNumberControlled = 1;
  string   ProtocolDescription = "Video";
  string   VideoProcessor = "Synthetic Video Processor";
  uint16   VideoMemoryType = 2;
  string   OtherVideoMemoryType;
  uint32   NumberOfVideoPages = 1024;
  uint32   MaxMemorySupported = 4194304;
  uint16   AcceleratorCapabilities[] = { 2 };
  string   CapabilityDescriptions[] = { "Graphics Accelerator" };
  string   OtherVideoArchitecture;
  uint16   VideoArchitecture;
};
```

## <a name="members"></a><span data-ttu-id="16c7d-108">Member</span><span class="sxs-lookup"><span data-stu-id="16c7d-108">Members</span></span>

<span data-ttu-id="16c7d-109">Die **MSVM \_ syntheticdisplaycontroller** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="16c7d-109">The **Msvm\_SyntheticDisplayController** class has these types of members:</span></span>

-   [<span data-ttu-id="16c7d-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="16c7d-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="16c7d-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="16c7d-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="16c7d-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="16c7d-112">Methods</span></span>

<span data-ttu-id="16c7d-113">Die **MSVM \_ syntheticdisplaycontroller** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="16c7d-113">The **Msvm\_SyntheticDisplayController** class has these methods.</span></span>



| <span data-ttu-id="16c7d-114">Methode</span><span class="sxs-lookup"><span data-stu-id="16c7d-114">Method</span></span>                                                                           | <span data-ttu-id="16c7d-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="16c7d-115">Description</span></span>                              |
|:---------------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="16c7d-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="16c7d-116">**EnableDevice**</span></span>                                                                 | <span data-ttu-id="16c7d-117">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="16c7d-118">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="16c7d-118">**OnlineDevice**</span></span>                                                                 | <span data-ttu-id="16c7d-119">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="16c7d-120">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="16c7d-120">**QuiesceDevice**</span></span>                                                                | <span data-ttu-id="16c7d-121">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="16c7d-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="16c7d-122">**RequestStateChange**</span></span>](msvm-syntheticdisplaycontroller-requeststatechange.md) | <span data-ttu-id="16c7d-123">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="16c7d-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="16c7d-124">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="16c7d-124">**Reset**</span></span>](msvm-syntheticdisplaycontroller-reset.md)                           | <span data-ttu-id="16c7d-125">Setzt das virtuelle Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="16c7d-125">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="16c7d-126">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="16c7d-126">**RestoreProperties**</span></span>                                                            | <span data-ttu-id="16c7d-127">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="16c7d-128">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="16c7d-128">**SaveProperties**</span></span>                                                               | <span data-ttu-id="16c7d-129">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="16c7d-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="16c7d-130">**SetPowerState**</span></span>                                                                | <span data-ttu-id="16c7d-131">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="16c7d-132">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="16c7d-132">Properties</span></span>

<span data-ttu-id="16c7d-133">Die **MSVM \_ syntheticdisplaycontroller** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="16c7d-133">The **Msvm\_SyntheticDisplayController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="16c7d-134">**Beschleuniger Funktionen**</span><span class="sxs-lookup"><span data-stu-id="16c7d-134">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-135">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="16c7d-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-137">Die Grafiken und 3D-Funktionen des Anzeige Controllers.</span><span class="sxs-lookup"><span data-stu-id="16c7d-137">The graphics and 3-D capabilities of the display controller.</span></span> <span data-ttu-id="16c7d-138">Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt und ist immer auf 2 (Grafikbeschleuniger) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-138">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to 2 (Graphics Accelerator).</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-139">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="16c7d-139">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-140">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="16c7d-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-142">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf 6 festgelegt (nicht zutreffend).</span><span class="sxs-lookup"><span data-stu-id="16c7d-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-143">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="16c7d-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-144">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="16c7d-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-146">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf 6 festgelegt (nicht zutreffend).</span><span class="sxs-lookup"><span data-stu-id="16c7d-146">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-147">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="16c7d-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-148">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="16c7d-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-150">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="16c7d-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="16c7d-151">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-152">**Capabilitybeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="16c7d-152">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-153">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="16c7d-153">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-155">Ein Array von Freiform-Zeichen folgen, die Ausführlichere Erläuterungen zu allen Video-Accelerator-Funktionen bereitstellen, die im **acceleratorfunktionalitäten** -Eigenschafts Array angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="16c7d-155">An array of free-form strings that provide more detailed explanations for any of the video accelerator features indicated in the **AcceleratorCapabilities** property array.</span></span> <span data-ttu-id="16c7d-156">Jeder Eintrag dieses Arrays bezieht sich auf den Eintrag im **acceleratorfunktionalitäten** -Eigenschafts Array, das sich im gleichen Index befindet.</span><span class="sxs-lookup"><span data-stu-id="16c7d-156">Each entry of this array is related to the entry in the **AcceleratorCapabilities** property array that is located at the same index.</span></span> <span data-ttu-id="16c7d-157">Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt und ist immer auf "Graphics Accelerator" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-157">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to "Graphics Accelerator".</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-158">**Caption**</span><span class="sxs-lookup"><span data-stu-id="16c7d-158">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="16c7d-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-161">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="16c7d-161">A short description of the object.</span></span> <span data-ttu-id="16c7d-162">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Anzeige Controller" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Display Controller".</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-163">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="16c7d-163">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-164">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="16c7d-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-166">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="16c7d-166">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="16c7d-167">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="16c7d-167">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="16c7d-168">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-168">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="16c7d-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="16c7d-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="16c7d-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-171"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="16c7d-171"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-172"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="16c7d-172"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-173"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="16c7d-173"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="16c7d-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="16c7d-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="16c7d-176">)</span><span class="sxs-lookup"><span data-stu-id="16c7d-176">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="16c7d-177">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="16c7d-177">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-178">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="16c7d-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-180">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="16c7d-180">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="16c7d-181">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf "MSVM \_ syntheticdisplaycontroller" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-181">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_SyntheticDisplayController".</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-182">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="16c7d-182">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-183">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="16c7d-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-185">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="16c7d-185">A description of the object.</span></span> <span data-ttu-id="16c7d-186">Diese Eigenschaft wird vom [**CIM \_ managedelta-Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Microsoft Synthetic Display Controller" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-186">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Synthetic Display Controller".</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-187">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="16c7d-187">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-188">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="16c7d-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-190">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="16c7d-190">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="16c7d-191">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="16c7d-191">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="16c7d-192">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-192">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="16c7d-193"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="16c7d-193"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-194"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="16c7d-194"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-195"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="16c7d-195"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-196"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="16c7d-196"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-197"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="16c7d-197"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-198"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="16c7d-198"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-199"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="16c7d-199"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-200"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="16c7d-200"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="16c7d-201">)</span><span class="sxs-lookup"><span data-stu-id="16c7d-201">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="16c7d-202">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="16c7d-202">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-203">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="16c7d-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-205">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf "Microsoft:*GUID*" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-205">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-206">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="16c7d-206">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-207">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="16c7d-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-208">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-209">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-209">A display name for the object.</span></span> <span data-ttu-id="16c7d-210">Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist standardmäßig immer auf "Anzeige Controller" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Display Controller" by default.</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-211">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="16c7d-211">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-212">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="16c7d-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-213">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-214">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="16c7d-214">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="16c7d-215">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 2 (aktiviert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-215">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-216">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="16c7d-216">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-217">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="16c7d-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-218">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-219">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="16c7d-219">The enabled and disabled states of an element.</span></span> <span data-ttu-id="16c7d-220">Sie kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben.</span><span class="sxs-lookup"><span data-stu-id="16c7d-220">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="16c7d-221">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 2 (aktiviert) oder 3 (deaktiviert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-221">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled) or 3 (Disabled).</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-222">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="16c7d-222">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-223">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="16c7d-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-225">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="16c7d-225">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-226">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="16c7d-226">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-227">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="16c7d-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-228">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-229">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="16c7d-229">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-230">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="16c7d-230">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-231">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="16c7d-231">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-232">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-233">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="16c7d-233">The current health of the element.</span></span> <span data-ttu-id="16c7d-234">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Elemente.</span><span class="sxs-lookup"><span data-stu-id="16c7d-234">This attribute expresses the health of this element but not necessarily that of its subelements.</span></span> <span data-ttu-id="16c7d-235">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="16c7d-235">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="16c7d-236">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 5 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-236">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-237">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="16c7d-237">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-238">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="16c7d-238">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-239">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-240">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-240">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-241">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="16c7d-241">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-242">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="16c7d-242">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-243">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-244">Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="16c7d-244">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="16c7d-245">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-246">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="16c7d-246">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-247">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="16c7d-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-248">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-249">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="16c7d-249">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-250">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="16c7d-250">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="16c7d-251">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-251">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-252">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="16c7d-252">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-253">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="16c7d-253">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-254">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-255">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="16c7d-255">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-256">**Maxmemorysupported**</span><span class="sxs-lookup"><span data-stu-id="16c7d-256">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-257">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="16c7d-257">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-258">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-259">Die maximal unterstützte Arbeitsspeicher Größe in Bytes.</span><span class="sxs-lookup"><span data-stu-id="16c7d-259">The maximum amount of memory supported, in bytes.</span></span> <span data-ttu-id="16c7d-260">Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt und ist immer auf 4.194.304 (0x400000) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-260">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to 4,194,304 (0x400000).</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-261">**Maxnuma**</span><span class="sxs-lookup"><span data-stu-id="16c7d-261">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-262">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="16c7d-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-263">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-264">Die maximale Anzahl direkt Adressier barer Entitäten, die von diesem Controller unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="16c7d-264">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="16c7d-265">Wenn die Zahl unbekannt oder unbegrenzt ist, sollte der Wert 0 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="16c7d-265">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="16c7d-266">Das Protokoll, das vom Controller für den Zugriff auf gesteuerte Geräte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="16c7d-266">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="16c7d-267">Diese Eigenschaft wird vom [**CIM- \_ Controller**](/windows/desktop/CIMWin32Prov/cim-controller)geerbt und ist immer auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-267">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-268">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="16c7d-268">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-269">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="16c7d-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-270">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-271">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="16c7d-271">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-272">**Name**</span><span class="sxs-lookup"><span data-stu-id="16c7d-272">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-273">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="16c7d-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-274">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-275">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="16c7d-275">The label by which the object is known.</span></span> <span data-ttu-id="16c7d-276">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und entspricht der Element **Name** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="16c7d-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-277">**Anzahl der videopages**</span><span class="sxs-lookup"><span data-stu-id="16c7d-277">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-278">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="16c7d-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-279">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-280">Die Anzahl der unterstützten Videoseiten anhand der aktuellen Auflösungen und des verfügbaren Arbeitsspeichers.</span><span class="sxs-lookup"><span data-stu-id="16c7d-280">The number of video pages supported given the current resolutions and available memory.</span></span> <span data-ttu-id="16c7d-281">Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt und ist immer auf 1024 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-281">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to 1024.</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-282">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="16c7d-282">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-283">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="16c7d-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-284">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-285">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="16c7d-285">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="16c7d-286">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="16c7d-286">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="16c7d-287">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-287">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="16c7d-288"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="16c7d-288"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-289"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="16c7d-289"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-290"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="16c7d-290"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-291"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="16c7d-291"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-292"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="16c7d-292"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-293"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="16c7d-293"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-294"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="16c7d-294"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-295"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="16c7d-295"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-296"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="16c7d-296"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-297"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="16c7d-297"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-298"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="16c7d-298"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-299"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="16c7d-299"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-300"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="16c7d-300"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-301"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="16c7d-301"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-302"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="16c7d-302"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-303"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="16c7d-303"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-304"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="16c7d-304"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-305"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="16c7d-305"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-306"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="16c7d-306"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="16c7d-307">)</span><span class="sxs-lookup"><span data-stu-id="16c7d-307">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="16c7d-308">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="16c7d-308">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-309">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="16c7d-309">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-310">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-311">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="16c7d-311">The current statuses of the object.</span></span> <span data-ttu-id="16c7d-312">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf 2 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-313">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="16c7d-313">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-314">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="16c7d-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-315">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-316">Der aktivierte oder deaktivierte Status des Elements, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="16c7d-316">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="16c7d-317">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="16c7d-317">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="16c7d-318">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-318">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-319">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="16c7d-319">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-320">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="16c7d-320">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-321">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-322">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-322">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-323">**Othervideoarchitecture**</span><span class="sxs-lookup"><span data-stu-id="16c7d-323">**OtherVideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-324">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="16c7d-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-325">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-326">Eine Zeichenfolge, die den Typ der Video Architektur beschreibt, wenn die **Video Architecture** -Eigenschaft 1 ("Other") ist.</span><span class="sxs-lookup"><span data-stu-id="16c7d-326">A string that describes the video architecture type when the **VideoArchitecture** property is 1 ("Other").</span></span> <span data-ttu-id="16c7d-327">Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-327">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-328">**Othervideomemorytype**</span><span class="sxs-lookup"><span data-stu-id="16c7d-328">**OtherVideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-329">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="16c7d-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-330">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-331">Der Typ des Video Speichers, wenn die **videomemorytype** -Eigenschaft der Instanz 1 (Other) ist.</span><span class="sxs-lookup"><span data-stu-id="16c7d-331">The video memory type when the instance's **VideoMemoryType** property is 1 (Other).</span></span> <span data-ttu-id="16c7d-332">Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-332">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-333">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="16c7d-333">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-334">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="16c7d-334">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-335">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-336">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="16c7d-336">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-337">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="16c7d-337">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-338">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="16c7d-338">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-339">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-340">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="16c7d-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-341">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="16c7d-341">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-342">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="16c7d-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-343">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-344">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="16c7d-344">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-345">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="16c7d-345">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-346">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="16c7d-346">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-347">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-348">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="16c7d-348">Provides high level status information.</span></span> <span data-ttu-id="16c7d-349">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="16c7d-349">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="16c7d-350">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="16c7d-350">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="16c7d-351">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-351">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="16c7d-352"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="16c7d-352"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-353"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="16c7d-353"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-354"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="16c7d-354"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-355"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="16c7d-355"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-356"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="16c7d-356"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-357"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="16c7d-357"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="16c7d-358">)</span><span class="sxs-lookup"><span data-stu-id="16c7d-358">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="16c7d-359">**Protocoldescription**</span><span class="sxs-lookup"><span data-stu-id="16c7d-359">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-360">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="16c7d-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-361">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-362">Eine Zeichenfolge, die weitere Informationen bereitstellt, die mit dem vom Controller unterstützten Protokoll verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="16c7d-362">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="16c7d-363">Diese Eigenschaft wird vom [**CIM- \_ Controller**](/windows/desktop/CIMWin32Prov/cim-controller)geerbt und ist immer auf "Video" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-363">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is always set to "Video".</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-364">**Protocolsupported**</span><span class="sxs-lookup"><span data-stu-id="16c7d-364">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-365">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="16c7d-365">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-366">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-367">Das Protokoll, das vom Controller für den Zugriff auf gesteuerte Geräte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="16c7d-367">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="16c7d-368">Diese Eigenschaft wird vom [**CIM- \_ Controller**](/windows/desktop/CIMWin32Prov/cim-controller)geerbt und immer auf 1 (sonstige) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-368">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is always set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-369">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="16c7d-369">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-370">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="16c7d-370">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-371">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-372">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="16c7d-372">The last requested or desired state for the element.</span></span> <span data-ttu-id="16c7d-373">Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-373">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="16c7d-374">Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuell aktivierten oder deaktivierten Zustände zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="16c7d-374">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="16c7d-375">**RequestStateChange** kann von einer bestimmten Instanz von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="16c7d-375">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support **RequestStateChange**.</span></span> <span data-ttu-id="16c7d-376">Wenn dies auftritt, wird der Wert 12 (nicht zutreffend) verwendet.</span><span class="sxs-lookup"><span data-stu-id="16c7d-376">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="16c7d-377">Diese Eigenschaft wird von **CIM \_ enabledlogicalelement** geerbt und auf 2 (aktiviert), 3 (deaktiviert) oder 12 (nicht zutreffend) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-377">This property is inherited from **CIM\_EnabledLogicalElement**, and it is set to 2 (Enabled), 3 (Disabled), or 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-378">**Status**</span><span class="sxs-lookup"><span data-stu-id="16c7d-378">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-379">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="16c7d-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-380">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-381">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="16c7d-381">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-382">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="16c7d-382">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-383">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="16c7d-383">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-384">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-385">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="16c7d-385">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="16c7d-386">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf "OK" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-386">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-387">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="16c7d-387">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-388">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="16c7d-388">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-389">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-390">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="16c7d-390">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-391">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="16c7d-391">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-392">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="16c7d-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-393">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-394">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="16c7d-394">The scoping system's creation class name.</span></span> <span data-ttu-id="16c7d-395">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf "MSVM \_ Computersystem" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-395">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-396">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="16c7d-396">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-397">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="16c7d-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-398">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-399">Der eindeutige Bezeichner für die Bereichs bezogene virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="16c7d-399">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="16c7d-400">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-400">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-401">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="16c7d-401">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-402">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="16c7d-402">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-403">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-403">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-404">Der Zeitpunkt, zu dem die virtuelle Maschine zuletzt eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="16c7d-404">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="16c7d-405">Diese Eigenschaft wird vom [**CIM- \_ Controller**](/windows/desktop/CIMWin32Prov/cim-controller)geerbt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-405">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-406">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="16c7d-406">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-407">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="16c7d-407">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-408">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-409">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="16c7d-409">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="16c7d-410">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-410">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-411">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="16c7d-411">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-412">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="16c7d-412">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-413">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-414">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="16c7d-414">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-415">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="16c7d-415">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-416">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="16c7d-416">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-417">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-417">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-418">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="16c7d-418">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="16c7d-419">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-419">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-420">**Videoarchitecture**</span><span class="sxs-lookup"><span data-stu-id="16c7d-420">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-421">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="16c7d-421">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-422">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-423">Gibt die Video Architektur des Anzeige Controllers an, mit der das Videosignal generiert wird.</span><span class="sxs-lookup"><span data-stu-id="16c7d-423">Specifies the display controller's video architecture used to generate the video signal.</span></span> <span data-ttu-id="16c7d-424">In der Regel generiert ein dedizierter Videoprozessor das Videosignal entsprechend der angegebenen Architektur.</span><span class="sxs-lookup"><span data-stu-id="16c7d-424">Usually, a dedicated video processor generates the video signal in accordance with the specified architecture.</span></span> <span data-ttu-id="16c7d-425">Es ist ein Indikator für die maximale Auflösungs Funktion des Anzeige Controllers.</span><span class="sxs-lookup"><span data-stu-id="16c7d-425">It is an indicator of the maximum resolution capability of the display controller.</span></span> <span data-ttu-id="16c7d-426">Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-426">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="16c7d-427"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="16c7d-427"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-428"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="16c7d-428"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-429"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span><span class="sxs-lookup"><span data-stu-id="16c7d-429"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-430"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span><span class="sxs-lookup"><span data-stu-id="16c7d-430"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-431"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span><span class="sxs-lookup"><span data-stu-id="16c7d-431"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-432"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span><span class="sxs-lookup"><span data-stu-id="16c7d-432"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-433"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span><span class="sxs-lookup"><span data-stu-id="16c7d-433"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-434"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span><span class="sxs-lookup"><span data-stu-id="16c7d-434"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-435"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span><span class="sxs-lookup"><span data-stu-id="16c7d-435"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-436"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span><span class="sxs-lookup"><span data-stu-id="16c7d-436"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-437"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span><span class="sxs-lookup"><span data-stu-id="16c7d-437"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-438"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Linearer Rahmen Puffer** (11)</span><span class="sxs-lookup"><span data-stu-id="16c7d-438"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Linear Frame Buffer** (11)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-439"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="16c7d-439"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-440"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="16c7d-440"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-441"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="16c7d-441"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="16c7d-442">)</span><span class="sxs-lookup"><span data-stu-id="16c7d-442">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="16c7d-443">**Videomemorytype**</span><span class="sxs-lookup"><span data-stu-id="16c7d-443">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-444">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="16c7d-444">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-445">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-446">Der Typ des Video Speichers.</span><span class="sxs-lookup"><span data-stu-id="16c7d-446">The type of video memory.</span></span> <span data-ttu-id="16c7d-447">Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt und ist immer auf 2 (VRAM) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-447">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to 2 (VRAM).</span></span>

</dd> <dt>

<span data-ttu-id="16c7d-448">**Videoprocessor**</span><span class="sxs-lookup"><span data-stu-id="16c7d-448">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c7d-449">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="16c7d-449">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16c7d-450">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="16c7d-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c7d-451">Eine Zeichenfolge, die den Videoprozessor/-Controller beschreibt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-451">A string that describes the video processor/controller.</span></span> <span data-ttu-id="16c7d-452">Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt und ist immer auf "synthetischer Video Prozessor" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16c7d-452">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to "Synthetic Video Processor".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="16c7d-453">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="16c7d-453">Remarks</span></span>

<span data-ttu-id="16c7d-454">Der Zugriff auf die **MSVM \_ syntheticdisplaycontroller** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="16c7d-454">Access to the **Msvm\_SyntheticDisplayController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="16c7d-455">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="16c7d-455">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="16c7d-456">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16c7d-456">Requirements</span></span>



| <span data-ttu-id="16c7d-457">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16c7d-457">Requirement</span></span> | <span data-ttu-id="16c7d-458">Wert</span><span class="sxs-lookup"><span data-stu-id="16c7d-458">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16c7d-459">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="16c7d-459">Minimum supported client</span></span><br/> | <span data-ttu-id="16c7d-460">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16c7d-460">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="16c7d-461">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="16c7d-461">Minimum supported server</span></span><br/> | <span data-ttu-id="16c7d-462">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16c7d-462">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="16c7d-463">Namespace</span><span class="sxs-lookup"><span data-stu-id="16c7d-463">Namespace</span></span><br/>                | <span data-ttu-id="16c7d-464">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="16c7d-464">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="16c7d-465">MOF</span><span class="sxs-lookup"><span data-stu-id="16c7d-465">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16c7d-466"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="16c7d-466"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="16c7d-467">DLL</span><span class="sxs-lookup"><span data-stu-id="16c7d-467">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16c7d-468"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="16c7d-468"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="16c7d-469">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16c7d-469">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16c7d-470">**CIM- \_ Display Controller**</span><span class="sxs-lookup"><span data-stu-id="16c7d-470">**CIM\_DisplayController**</span></span>](cim-displaycontroller.md)
</dt> <dt>

<span data-ttu-id="16c7d-471">[**CIM- \_ Display Controller**](/previous-versions//cc136810(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="16c7d-471">[**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="16c7d-472">Video Klassen</span><span class="sxs-lookup"><span data-stu-id="16c7d-472">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

