---
description: Stellt den synthetischen 3D-Anzeige Controller dar, der einem virtuellen Computer zugewiesen ist.
ms.assetid: 5679668B-7D0B-421C-92B6-8A320090DFF7
title: Msvm_Synthetic3DDisplayController-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DDisplayController
- Msvm_Synthetic3DDisplayController.RequestStateChange
- Msvm_Synthetic3DDisplayController.SetPowerState
- Msvm_Synthetic3DDisplayController.Reset
- Msvm_Synthetic3DDisplayController.EnableDevice
- Msvm_Synthetic3DDisplayController.OnlineDevice
- Msvm_Synthetic3DDisplayController.QuiesceDevice
- Msvm_Synthetic3DDisplayController.SaveProperties
- Msvm_Synthetic3DDisplayController.RestoreProperties
- Msvm_Synthetic3DDisplayController.InstanceID
- Msvm_Synthetic3DDisplayController.Caption
- Msvm_Synthetic3DDisplayController.Description
- Msvm_Synthetic3DDisplayController.ElementName
- Msvm_Synthetic3DDisplayController.InstallDate
- Msvm_Synthetic3DDisplayController.Name
- Msvm_Synthetic3DDisplayController.OperationalStatus
- Msvm_Synthetic3DDisplayController.StatusDescriptions
- Msvm_Synthetic3DDisplayController.Status
- Msvm_Synthetic3DDisplayController.HealthState
- Msvm_Synthetic3DDisplayController.CommunicationStatus
- Msvm_Synthetic3DDisplayController.DetailedStatus
- Msvm_Synthetic3DDisplayController.OperatingStatus
- Msvm_Synthetic3DDisplayController.PrimaryStatus
- Msvm_Synthetic3DDisplayController.EnabledState
- Msvm_Synthetic3DDisplayController.OtherEnabledState
- Msvm_Synthetic3DDisplayController.RequestedState
- Msvm_Synthetic3DDisplayController.EnabledDefault
- Msvm_Synthetic3DDisplayController.TimeOfLastStateChange
- Msvm_Synthetic3DDisplayController.AvailableRequestedStates
- Msvm_Synthetic3DDisplayController.TransitioningToState
- Msvm_Synthetic3DDisplayController.SystemCreationClassName
- Msvm_Synthetic3DDisplayController.SystemName
- Msvm_Synthetic3DDisplayController.CreationClassName
- Msvm_Synthetic3DDisplayController.DeviceID
- Msvm_Synthetic3DDisplayController.PowerManagementSupported
- Msvm_Synthetic3DDisplayController.PowerManagementCapabilities
- Msvm_Synthetic3DDisplayController.Availability
- Msvm_Synthetic3DDisplayController.StatusInfo
- Msvm_Synthetic3DDisplayController.LastErrorCode
- Msvm_Synthetic3DDisplayController.ErrorDescription
- Msvm_Synthetic3DDisplayController.ErrorCleared
- Msvm_Synthetic3DDisplayController.PowerOnHours
- Msvm_Synthetic3DDisplayController.TotalPowerOnHours
- Msvm_Synthetic3DDisplayController.OtherIdentifyingInfo
- Msvm_Synthetic3DDisplayController.IdentifyingDescriptions
- Msvm_Synthetic3DDisplayController.AdditionalAvailability
- Msvm_Synthetic3DDisplayController.MaxQuiesceTime
- Msvm_Synthetic3DDisplayController.TimeOfLastReset
- Msvm_Synthetic3DDisplayController.ProtocolSupported
- Msvm_Synthetic3DDisplayController.MaxNumberControlled
- Msvm_Synthetic3DDisplayController.ProtocolDescription
- Msvm_Synthetic3DDisplayController.VideoProcessor
- Msvm_Synthetic3DDisplayController.VideoMemoryType
- Msvm_Synthetic3DDisplayController.OtherVideoMemoryType
- Msvm_Synthetic3DDisplayController.NumberOfVideoPages
- Msvm_Synthetic3DDisplayController.MaxMemorySupported
- Msvm_Synthetic3DDisplayController.AcceleratorCapabilities
- Msvm_Synthetic3DDisplayController.CapabilityDescriptions
- Msvm_Synthetic3DDisplayController.OtherVideoArchitecture
- Msvm_Synthetic3DDisplayController.VideoArchitecture
- Msvm_Synthetic3DDisplayController.AllocatedGPU
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0cd102fe29cf34aa0930ca264c8820868da7daf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350575"
---
# <a name="msvm_synthetic3ddisplaycontroller-class"></a><span data-ttu-id="343f9-103">MSVM \_ Synthetic3DDisplayController-Klasse</span><span class="sxs-lookup"><span data-stu-id="343f9-103">Msvm\_Synthetic3DDisplayController class</span></span>

<span data-ttu-id="343f9-104">Stellt den synthetischen 3D-Anzeige Controller dar, der einem virtuellen Computer zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="343f9-104">Represents the synthetic 3-D display controller that is assigned to a virtual machine.</span></span> <span data-ttu-id="343f9-105">Diese Klasse wird nur bei virtuellen Computern verwendet, die remotefx verwenden.</span><span class="sxs-lookup"><span data-stu-id="343f9-105">This class is only used with virtual machines that use RemoteFX.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="343f9-106">Wenn Sie einem virtuellen Computer einen synthetischen 3D-Anzeige Controller hinzufügen, müssen Sie alle synthetischen Anzeige Controller ([**MSVM \_ syntheticdisplaycontroller**](msvm-syntheticdisplaycontroller.md)) deaktivieren, die mit diesem virtuellen Computer verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="343f9-106">When you add a synthetic 3-D display controller to a virtual machine, you must disable any synthetic display controller ([**Msvm\_SyntheticDisplayController**](msvm-syntheticdisplaycontroller.md)) that is attached to that virtual machine.</span></span>

 

<span data-ttu-id="343f9-107">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="343f9-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="343f9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="343f9-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_Synthetic3DDisplayController : CIM_DisplayController
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
  string   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   CreationClassName;
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[];
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 1;
  uint32   MaxNumberControlled = 1;
  string   ProtocolDescription = "Video";
  string   VideoProcessor = "Synthetic Video Processor";
  uint16   VideoMemoryType = 2;
  string   OtherVideoMemoryType;
  uint32   NumberOfVideoPages = 2048;
  uint32   MaxMemorySupported = 8388608;
  uint16   AcceleratorCapabilities[] = { 2 };
  string   CapabilityDescriptions[] = { "Graphics Accelerator" };
  string   OtherVideoArchitecture;
  uint16   VideoArchitecture;
  string   AllocatedGPU;
};
```

## <a name="members"></a><span data-ttu-id="343f9-109">Member</span><span class="sxs-lookup"><span data-stu-id="343f9-109">Members</span></span>

<span data-ttu-id="343f9-110">Die **MSVM \_ Synthetic3DDisplayController** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="343f9-110">The **Msvm\_Synthetic3DDisplayController** class has these types of members:</span></span>

-   [<span data-ttu-id="343f9-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="343f9-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="343f9-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="343f9-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="343f9-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="343f9-113">Methods</span></span>

<span data-ttu-id="343f9-114">Die **MSVM- \_ Synthetic3DDisplayController** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="343f9-114">The **Msvm\_Synthetic3DDisplayController** class has these methods.</span></span>



| <span data-ttu-id="343f9-115">Methode</span><span class="sxs-lookup"><span data-stu-id="343f9-115">Method</span></span>                 | <span data-ttu-id="343f9-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="343f9-116">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="343f9-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="343f9-117">**EnableDevice**</span></span>       | <span data-ttu-id="343f9-118">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="343f9-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="343f9-119">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="343f9-119">**OnlineDevice**</span></span>       | <span data-ttu-id="343f9-120">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="343f9-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="343f9-121">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="343f9-121">**QuiesceDevice**</span></span>      | <span data-ttu-id="343f9-122">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="343f9-122">This method is not supported.</span></span><br/> |
| <span data-ttu-id="343f9-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="343f9-123">**RequestStateChange**</span></span> | <span data-ttu-id="343f9-124">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="343f9-124">This method is not supported.</span></span><br/> |
| <span data-ttu-id="343f9-125">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="343f9-125">**Reset**</span></span>              | <span data-ttu-id="343f9-126">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="343f9-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="343f9-127">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="343f9-127">**RestoreProperties**</span></span>  | <span data-ttu-id="343f9-128">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="343f9-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="343f9-129">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="343f9-129">**SaveProperties**</span></span>     | <span data-ttu-id="343f9-130">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="343f9-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="343f9-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="343f9-131">**SetPowerState**</span></span>      | <span data-ttu-id="343f9-132">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="343f9-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="343f9-133">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="343f9-133">Properties</span></span>

<span data-ttu-id="343f9-134">Die **MSVM- \_ Synthetic3DDisplayController** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="343f9-134">The **Msvm\_Synthetic3DDisplayController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="343f9-135">**Beschleuniger Funktionen**</span><span class="sxs-lookup"><span data-stu-id="343f9-135">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-136">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="343f9-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="343f9-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-138">Die Grafiken und 3D-Funktionen des Anzeige Controllers.</span><span class="sxs-lookup"><span data-stu-id="343f9-138">The graphics and 3-D capabilities of the display controller.</span></span> <span data-ttu-id="343f9-139">Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="343f9-139">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="343f9-140">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="343f9-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-141">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="343f9-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="343f9-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-143">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf 6 festgelegt (nicht zutreffend).</span><span class="sxs-lookup"><span data-stu-id="343f9-143">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="343f9-144">**Zugedgpu**</span><span class="sxs-lookup"><span data-stu-id="343f9-144">**AllocatedGPU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="343f9-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="343f9-147">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="343f9-147">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="343f9-148">Der Bezeichner der physischen Grafikverarbeitungseinheit (GPU), die dieser virtuellen Maschine zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="343f9-148">The identifier of the physical graphics processing unit (GPU) allocated to this virtual machine.</span></span> <span data-ttu-id="343f9-149">Diese Eigenschaft gilt nur für virtuelle Maschinen, die remotefx verwenden.</span><span class="sxs-lookup"><span data-stu-id="343f9-149">This property only applies to virtual machines that use RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="343f9-150">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="343f9-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-151">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="343f9-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-153">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf 6 festgelegt (nicht zutreffend).</span><span class="sxs-lookup"><span data-stu-id="343f9-153">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="343f9-154">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="343f9-154">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-155">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="343f9-155">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="343f9-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-157">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="343f9-157">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="343f9-158">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="343f9-158">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="343f9-159">**Capabilitybeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="343f9-159">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-160">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="343f9-160">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="343f9-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-162">Ein Array von Freiform-Zeichen folgen, die Ausführlichere Erläuterungen zu allen Video-Accelerator-Funktionen bereitstellen, die im **acceleratorfunktionalitäten** -Eigenschafts Array angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="343f9-162">An array of free-form strings that provide more detailed explanations for any of the video accelerator features indicated in the **AcceleratorCapabilities** property array.</span></span> <span data-ttu-id="343f9-163">Jeder Eintrag dieses Arrays bezieht sich auf den Eintrag im **acceleratorfunktionalitäten** -Eigenschafts Array, das sich im gleichen Index befindet.</span><span class="sxs-lookup"><span data-stu-id="343f9-163">Each entry of this array is related to the entry in the **AcceleratorCapabilities** property array that is located at the same index.</span></span> <span data-ttu-id="343f9-164">Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="343f9-164">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="343f9-165">**Caption**</span><span class="sxs-lookup"><span data-stu-id="343f9-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-166">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="343f9-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-168">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="343f9-168">A short description of the object.</span></span> <span data-ttu-id="343f9-169">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="343f9-169">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="343f9-170">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="343f9-170">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-171">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="343f9-171">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-173">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="343f9-173">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="343f9-174">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="343f9-174">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="343f9-175">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="343f9-175">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="343f9-176"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="343f9-176"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="343f9-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-178"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="343f9-178"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-179"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="343f9-179"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-180"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="343f9-180"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="343f9-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-182"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="343f9-182"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="343f9-183">)</span><span class="sxs-lookup"><span data-stu-id="343f9-183">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="343f9-184">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="343f9-184">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-185">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="343f9-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-187">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="343f9-187">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="343f9-188">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="343f9-188">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="343f9-189">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="343f9-189">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-190">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="343f9-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-192">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="343f9-192">A description of the object.</span></span> <span data-ttu-id="343f9-193">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="343f9-193">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="343f9-194">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="343f9-194">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-195">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="343f9-195">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-196">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-197">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="343f9-197">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="343f9-198">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="343f9-198">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="343f9-199">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="343f9-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="343f9-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="343f9-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-201"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="343f9-201"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-202"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="343f9-202"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-203"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="343f9-203"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-204"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="343f9-204"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-205"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="343f9-205"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-206"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="343f9-206"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-207"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="343f9-207"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="343f9-208">)</span><span class="sxs-lookup"><span data-stu-id="343f9-208">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="343f9-209">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="343f9-209">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-210">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="343f9-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-212">Der Geräte Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="343f9-212">The device identifier.</span></span> <span data-ttu-id="343f9-213">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf "Microsoft:*GUID*" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="343f9-213">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="343f9-214">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="343f9-214">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-215">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="343f9-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-216">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-217">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="343f9-217">A display name for the object.</span></span> <span data-ttu-id="343f9-218">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="343f9-218">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="343f9-219">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="343f9-219">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-220">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="343f9-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-221">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-222">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="343f9-222">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="343f9-223">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 2 (aktiviert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="343f9-223">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="343f9-224">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="343f9-224">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-225">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="343f9-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-226">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-227">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="343f9-227">The enabled and disabled states of an element.</span></span> <span data-ttu-id="343f9-228">Sie kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben.</span><span class="sxs-lookup"><span data-stu-id="343f9-228">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="343f9-229">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 2 (aktiviert) oder 3 (deaktiviert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="343f9-229">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to either 2 (Enabled) or 3 (Disabled).</span></span>

</dd> <dt>

<span data-ttu-id="343f9-230">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="343f9-230">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-231">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="343f9-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-232">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-233">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="343f9-233">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="343f9-234">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="343f9-234">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-235">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="343f9-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-236">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-237">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="343f9-237">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="343f9-238">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="343f9-238">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-239">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="343f9-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-240">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-241">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="343f9-241">The current health of the element.</span></span> <span data-ttu-id="343f9-242">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Elemente.</span><span class="sxs-lookup"><span data-stu-id="343f9-242">This attribute expresses the health of this element but not necessarily that of its subelements.</span></span> <span data-ttu-id="343f9-243">Die möglichen Werte liegen zwischen 0 und 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="343f9-243">The possible values are from 0 through 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="343f9-244">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="343f9-244">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="343f9-245">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="343f9-245">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-246">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="343f9-246">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="343f9-247">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-248">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="343f9-248">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="343f9-249">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="343f9-249">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-250">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="343f9-250">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-251">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-252">Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="343f9-252">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="343f9-253">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="343f9-253">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="343f9-254">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="343f9-254">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-255">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="343f9-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-256">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="343f9-257">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="343f9-257">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="343f9-258">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="343f9-258">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="343f9-259">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="343f9-259">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="343f9-260">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="343f9-260">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-261">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="343f9-261">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-262">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-263">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="343f9-263">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="343f9-264">**Maxmemorysupported**</span><span class="sxs-lookup"><span data-stu-id="343f9-264">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-265">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="343f9-265">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-266">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-267">Die maximal unterstützte Arbeitsspeicher Größe in Bytes.</span><span class="sxs-lookup"><span data-stu-id="343f9-267">The maximum amount of memory supported, in bytes.</span></span> <span data-ttu-id="343f9-268">Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="343f9-268">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="343f9-269">**Maxnuma**</span><span class="sxs-lookup"><span data-stu-id="343f9-269">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-270">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="343f9-270">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-271">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-272">Die maximale Anzahl direkt Adressier barer Entitäten, die von diesem Controller unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="343f9-272">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="343f9-273">Wenn die Zahl unbekannt oder unbegrenzt ist, sollte der Wert 0 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="343f9-273">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="343f9-274">Das Protokoll, das vom Controller für den Zugriff auf gesteuerte Geräte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="343f9-274">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="343f9-275">Diese Eigenschaft wird vom [**CIM- \_ Controller**](/windows/desktop/CIMWin32Prov/cim-controller)geerbt.</span><span class="sxs-lookup"><span data-stu-id="343f9-275">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="343f9-276">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="343f9-276">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-277">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="343f9-277">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-278">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-279">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="343f9-279">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="343f9-280">**Name**</span><span class="sxs-lookup"><span data-stu-id="343f9-280">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-281">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="343f9-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-282">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-283">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="343f9-283">The label by which the object is known.</span></span> <span data-ttu-id="343f9-284">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="343f9-284">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="343f9-285">**Anzahl der videopages**</span><span class="sxs-lookup"><span data-stu-id="343f9-285">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-286">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="343f9-286">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-287">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-288">Die Anzahl der unterstützten Videoseiten anhand der aktuellen Auflösungen und des verfügbaren Arbeitsspeichers.</span><span class="sxs-lookup"><span data-stu-id="343f9-288">The number of video pages supported given the current resolutions and available memory.</span></span> <span data-ttu-id="343f9-289">Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="343f9-289">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="343f9-290">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="343f9-290">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-291">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="343f9-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-292">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-293">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="343f9-293">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="343f9-294">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="343f9-294">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="343f9-295">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="343f9-295">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="343f9-296"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="343f9-296"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-297"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="343f9-297"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-298"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="343f9-298"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-299"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="343f9-299"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-300"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="343f9-300"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-301"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="343f9-301"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-302"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="343f9-302"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-303"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="343f9-303"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-304"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="343f9-304"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-305"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="343f9-305"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-306"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="343f9-306"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-307"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="343f9-307"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-308"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="343f9-308"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-309"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="343f9-309"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-310"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="343f9-310"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-311"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="343f9-311"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-312"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="343f9-312"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-313"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="343f9-313"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-314"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="343f9-314"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="343f9-315">)</span><span class="sxs-lookup"><span data-stu-id="343f9-315">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="343f9-316">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="343f9-316">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-317">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="343f9-317">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="343f9-318">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-319">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="343f9-319">The current statuses of the object.</span></span> <span data-ttu-id="343f9-320">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="343f9-320">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="343f9-321">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="343f9-321">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-322">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="343f9-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-323">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-324">Der aktivierte oder deaktivierte Status des Elements, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="343f9-324">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="343f9-325">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="343f9-325">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="343f9-326">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="343f9-326">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="343f9-327">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="343f9-327">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-328">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="343f9-328">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="343f9-329">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-330">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="343f9-330">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="343f9-331">**Othervideoarchitecture**</span><span class="sxs-lookup"><span data-stu-id="343f9-331">**OtherVideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-332">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="343f9-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-333">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-334">Eine Zeichenfolge, die den Typ der Video Architektur beschreibt, wenn die **Video Architecture** -Eigenschaft 1 ("Other") ist.</span><span class="sxs-lookup"><span data-stu-id="343f9-334">A string that describes the video architecture type when the **VideoArchitecture** property is 1 ("Other").</span></span> <span data-ttu-id="343f9-335">Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="343f9-335">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="343f9-336">**Othervideomemorytype**</span><span class="sxs-lookup"><span data-stu-id="343f9-336">**OtherVideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-337">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="343f9-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-338">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-339">Der Typ des Video Speichers, wenn die **videomemorytype** -Eigenschaft der Instanz 1 (Other) ist.</span><span class="sxs-lookup"><span data-stu-id="343f9-339">The video memory type when the instance's **VideoMemoryType** property is 1 (Other).</span></span> <span data-ttu-id="343f9-340">Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="343f9-340">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="343f9-341">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="343f9-341">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-342">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="343f9-342">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="343f9-343">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-344">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="343f9-344">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="343f9-345">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="343f9-345">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-346">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="343f9-346">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-347">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-348">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="343f9-348">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="343f9-349">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="343f9-349">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-350">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="343f9-350">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-351">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-352">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="343f9-352">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="343f9-353">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="343f9-353">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-354">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="343f9-354">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-355">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-356">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="343f9-356">Provides high level status information.</span></span> <span data-ttu-id="343f9-357">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="343f9-357">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="343f9-358">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="343f9-358">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="343f9-359">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="343f9-359">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="343f9-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="343f9-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-361"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="343f9-361"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-362"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="343f9-362"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-363"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="343f9-363"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-364"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="343f9-364"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-365"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="343f9-365"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="343f9-366">)</span><span class="sxs-lookup"><span data-stu-id="343f9-366">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="343f9-367">**Protocoldescription**</span><span class="sxs-lookup"><span data-stu-id="343f9-367">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-368">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="343f9-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-369">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-370">Eine Zeichenfolge, die weitere Informationen bereitstellt, die mit dem vom Controller unterstützten Protokoll verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="343f9-370">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="343f9-371">Diese Eigenschaft wird vom [**CIM- \_ Controller**](/windows/desktop/CIMWin32Prov/cim-controller)geerbt.</span><span class="sxs-lookup"><span data-stu-id="343f9-371">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="343f9-372">**Protocolsupported**</span><span class="sxs-lookup"><span data-stu-id="343f9-372">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-373">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="343f9-373">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-374">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-375">Das Protokoll, das vom Controller für den Zugriff auf gesteuerte Geräte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="343f9-375">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="343f9-376">Diese Eigenschaft wird vom [**CIM- \_ Controller**](/windows/desktop/CIMWin32Prov/cim-controller)geerbt.</span><span class="sxs-lookup"><span data-stu-id="343f9-376">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="343f9-377">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="343f9-377">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-378">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="343f9-378">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-379">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-380">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="343f9-380">The last requested or desired state for the element.</span></span> <span data-ttu-id="343f9-381">Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="343f9-381">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="343f9-382">Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuell aktivierten oder deaktivierten Zustände zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="343f9-382">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="343f9-383">**RequestStateChange** kann von einer bestimmten Instanz von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="343f9-383">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support **RequestStateChange**.</span></span> <span data-ttu-id="343f9-384">Wenn dies auftritt, wird der Wert 12 (nicht zutreffend) verwendet.</span><span class="sxs-lookup"><span data-stu-id="343f9-384">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="343f9-385">Diese Eigenschaft wird von **CIM \_ enabledlogicalelement** geerbt und ist immer auf 2 (aktiviert), 3 (deaktiviert) oder 12 (nicht zutreffend) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="343f9-385">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 2 (Enabled), 3 (Disabled), or 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="343f9-386">**Status**</span><span class="sxs-lookup"><span data-stu-id="343f9-386">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-387">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="343f9-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-388">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-389">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="343f9-389">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="343f9-390">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="343f9-390">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-391">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="343f9-391">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="343f9-392">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-393">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="343f9-393">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="343f9-394">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="343f9-394">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="343f9-395">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="343f9-395">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-396">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="343f9-396">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-397">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-398">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="343f9-398">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="343f9-399">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="343f9-399">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-400">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="343f9-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-401">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-401">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-402">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="343f9-402">The scoping system's creation class name.</span></span> <span data-ttu-id="343f9-403">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="343f9-403">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="343f9-404">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="343f9-404">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-405">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="343f9-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-406">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-406">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-407">Der eindeutige Bezeichner für die Bereichs bezogene virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="343f9-407">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="343f9-408">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="343f9-408">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="343f9-409">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="343f9-409">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-410">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="343f9-410">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-411">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-412">Der Zeitpunkt, zu dem die virtuelle Maschine zuletzt eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="343f9-412">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="343f9-413">Diese Eigenschaft wird vom [**CIM- \_ Controller**](/windows/desktop/CIMWin32Prov/cim-controller)geerbt.</span><span class="sxs-lookup"><span data-stu-id="343f9-413">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="343f9-414">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="343f9-414">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-415">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="343f9-415">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-416">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-417">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="343f9-417">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="343f9-418">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="343f9-418">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="343f9-419">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="343f9-419">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-420">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="343f9-420">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-421">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-422">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="343f9-422">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="343f9-423">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="343f9-423">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-424">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="343f9-424">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-425">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-426">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="343f9-426">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="343f9-427">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="343f9-427">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="343f9-428">**Videoarchitecture**</span><span class="sxs-lookup"><span data-stu-id="343f9-428">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-429">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="343f9-429">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-430">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-431">Gibt die Video Architektur des Anzeige Controllers an, mit der das Videosignal generiert wird.</span><span class="sxs-lookup"><span data-stu-id="343f9-431">Specifies the display controller's video architecture used to generate the video signal.</span></span> <span data-ttu-id="343f9-432">In der Regel generiert ein dedizierter Videoprozessor das Videosignal entsprechend der angegebenen Architektur.</span><span class="sxs-lookup"><span data-stu-id="343f9-432">Usually, a dedicated video processor generates the video signal in accordance with the specified architecture.</span></span> <span data-ttu-id="343f9-433">Es ist ein Indikator für die maximale Auflösungs Funktion des Anzeige Controllers.</span><span class="sxs-lookup"><span data-stu-id="343f9-433">It is an indicator of the maximum resolution capability of the display controller.</span></span> <span data-ttu-id="343f9-434">Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="343f9-434">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="343f9-435"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="343f9-435"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-436"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="343f9-436"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-437"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span><span class="sxs-lookup"><span data-stu-id="343f9-437"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-438"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span><span class="sxs-lookup"><span data-stu-id="343f9-438"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-439"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span><span class="sxs-lookup"><span data-stu-id="343f9-439"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-440"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span><span class="sxs-lookup"><span data-stu-id="343f9-440"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-441"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span><span class="sxs-lookup"><span data-stu-id="343f9-441"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-442"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span><span class="sxs-lookup"><span data-stu-id="343f9-442"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-443"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span><span class="sxs-lookup"><span data-stu-id="343f9-443"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-444"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span><span class="sxs-lookup"><span data-stu-id="343f9-444"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-445"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span><span class="sxs-lookup"><span data-stu-id="343f9-445"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-446"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Linearer Rahmen Puffer** (11)</span><span class="sxs-lookup"><span data-stu-id="343f9-446"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Linear Frame Buffer** (11)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-447"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="343f9-447"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-448"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="343f9-448"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="343f9-449"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="343f9-449"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="343f9-450">)</span><span class="sxs-lookup"><span data-stu-id="343f9-450">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="343f9-451">**Videomemorytype**</span><span class="sxs-lookup"><span data-stu-id="343f9-451">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-452">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="343f9-452">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-453">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-453">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-454">Der Typ des Video Speichers.</span><span class="sxs-lookup"><span data-stu-id="343f9-454">The type of video memory.</span></span> <span data-ttu-id="343f9-455">Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="343f9-455">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="343f9-456">**Videoprocessor**</span><span class="sxs-lookup"><span data-stu-id="343f9-456">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="343f9-457">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="343f9-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="343f9-458">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="343f9-458">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="343f9-459">Eine Zeichenfolge, die den Videoprozessor/-Controller beschreibt.</span><span class="sxs-lookup"><span data-stu-id="343f9-459">A string that describes the video processor/controller.</span></span> <span data-ttu-id="343f9-460">Diese Eigenschaft wird von [**CIM \_ Displaycontroller**](/previous-versions//cc136810(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="343f9-460">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="343f9-461">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="343f9-461">Requirements</span></span>



| <span data-ttu-id="343f9-462">Anforderung</span><span class="sxs-lookup"><span data-stu-id="343f9-462">Requirement</span></span> | <span data-ttu-id="343f9-463">Wert</span><span class="sxs-lookup"><span data-stu-id="343f9-463">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="343f9-464">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="343f9-464">Minimum supported client</span></span><br/> | <span data-ttu-id="343f9-465">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="343f9-465">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="343f9-466">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="343f9-466">Minimum supported server</span></span><br/> | <span data-ttu-id="343f9-467">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="343f9-467">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="343f9-468">Namespace</span><span class="sxs-lookup"><span data-stu-id="343f9-468">Namespace</span></span><br/>                | <span data-ttu-id="343f9-469">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="343f9-469">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="343f9-470">MOF</span><span class="sxs-lookup"><span data-stu-id="343f9-470">MOF</span></span><br/>                      | <dl> <span data-ttu-id="343f9-471"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="343f9-471"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="343f9-472">DLL</span><span class="sxs-lookup"><span data-stu-id="343f9-472">DLL</span></span><br/>                      | <dl> <span data-ttu-id="343f9-473"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="343f9-473"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="343f9-474">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="343f9-474">See also</span></span>

<dl> <dt>

[<span data-ttu-id="343f9-475">**CIM- \_ Display Controller**</span><span class="sxs-lookup"><span data-stu-id="343f9-475">**CIM\_DisplayController**</span></span>](cim-displaycontroller.md)
</dt> </dl>

 

