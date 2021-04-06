---
description: Beschreibt die physische 3D-Grafikverarbeitungseinheit (GPU).
ms.assetid: 24e3d141-cbfe-4d40-907c-9a467c586c46
title: Msvm_Physical3dGraphicsProcessor-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Physical3dGraphicsProcessor
- Msvm_Physical3dGraphicsProcessor.RequestStateChange
- Msvm_Physical3dGraphicsProcessor.SetPowerState
- Msvm_Physical3dGraphicsProcessor.Reset
- Msvm_Physical3dGraphicsProcessor.EnableDevice
- Msvm_Physical3dGraphicsProcessor.OnlineDevice
- Msvm_Physical3dGraphicsProcessor.QuiesceDevice
- Msvm_Physical3dGraphicsProcessor.SaveProperties
- Msvm_Physical3dGraphicsProcessor.RestoreProperties
- Msvm_Physical3dGraphicsProcessor.InstanceID
- Msvm_Physical3dGraphicsProcessor.Caption
- Msvm_Physical3dGraphicsProcessor.Description
- Msvm_Physical3dGraphicsProcessor.ElementName
- Msvm_Physical3dGraphicsProcessor.InstallDate
- Msvm_Physical3dGraphicsProcessor.Name
- Msvm_Physical3dGraphicsProcessor.OperationalStatus
- Msvm_Physical3dGraphicsProcessor.StatusDescriptions
- Msvm_Physical3dGraphicsProcessor.Status
- Msvm_Physical3dGraphicsProcessor.HealthState
- Msvm_Physical3dGraphicsProcessor.CommunicationStatus
- Msvm_Physical3dGraphicsProcessor.DetailedStatus
- Msvm_Physical3dGraphicsProcessor.OperatingStatus
- Msvm_Physical3dGraphicsProcessor.PrimaryStatus
- Msvm_Physical3dGraphicsProcessor.EnabledState
- Msvm_Physical3dGraphicsProcessor.OtherEnabledState
- Msvm_Physical3dGraphicsProcessor.RequestedState
- Msvm_Physical3dGraphicsProcessor.EnabledDefault
- Msvm_Physical3dGraphicsProcessor.TimeOfLastStateChange
- Msvm_Physical3dGraphicsProcessor.AvailableRequestedStates
- Msvm_Physical3dGraphicsProcessor.TransitioningToState
- Msvm_Physical3dGraphicsProcessor.SystemCreationClassName
- Msvm_Physical3dGraphicsProcessor.SystemName
- Msvm_Physical3dGraphicsProcessor.CreationClassName
- Msvm_Physical3dGraphicsProcessor.DeviceID
- Msvm_Physical3dGraphicsProcessor.PowerManagementSupported
- Msvm_Physical3dGraphicsProcessor.PowerManagementCapabilities
- Msvm_Physical3dGraphicsProcessor.Availability
- Msvm_Physical3dGraphicsProcessor.StatusInfo
- Msvm_Physical3dGraphicsProcessor.LastErrorCode
- Msvm_Physical3dGraphicsProcessor.ErrorDescription
- Msvm_Physical3dGraphicsProcessor.ErrorCleared
- Msvm_Physical3dGraphicsProcessor.OtherIdentifyingInfo
- Msvm_Physical3dGraphicsProcessor.PowerOnHours
- Msvm_Physical3dGraphicsProcessor.TotalPowerOnHours
- Msvm_Physical3dGraphicsProcessor.IdentifyingDescriptions
- Msvm_Physical3dGraphicsProcessor.AdditionalAvailability
- Msvm_Physical3dGraphicsProcessor.MaxQuiesceTime
- Msvm_Physical3dGraphicsProcessor.EnabledForVirtualization
- Msvm_Physical3dGraphicsProcessor.CompatibleForVirtualization
- Msvm_Physical3dGraphicsProcessor.GPUID
- Msvm_Physical3dGraphicsProcessor.DirectXVersion
- Msvm_Physical3dGraphicsProcessor.PixelShaderVersion
- Msvm_Physical3dGraphicsProcessor.DedicatedVideoMemory
- Msvm_Physical3dGraphicsProcessor.DedicatedSystemMemory
- Msvm_Physical3dGraphicsProcessor.SharedSystemMemory
- Msvm_Physical3dGraphicsProcessor.TotalVideoMemory
- Msvm_Physical3dGraphicsProcessor.AvailableVideoMemory
- Msvm_Physical3dGraphicsProcessor.DriverProvider
- Msvm_Physical3dGraphicsProcessor.DriverDate
- Msvm_Physical3dGraphicsProcessor.DriverInstalled
- Msvm_Physical3dGraphicsProcessor.DriverVersion
- Msvm_Physical3dGraphicsProcessor.DriverModelVersion
- Msvm_Physical3dGraphicsProcessor.Rating
- Msvm_Physical3dGraphicsProcessor.AdapterIndexID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e257fa319b1d1b55562f47c7a3049a694fc27f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759643"
---
# <a name="msvm_physical3dgraphicsprocessor-class"></a><span data-ttu-id="4ac7d-103">MSVM \_ Physical3dGraphicsProcessor-Klasse</span><span class="sxs-lookup"><span data-stu-id="4ac7d-103">Msvm\_Physical3dGraphicsProcessor class</span></span>

<span data-ttu-id="4ac7d-104">Beschreibt die physische 3D-Grafikverarbeitungseinheit (GPU).</span><span class="sxs-lookup"><span data-stu-id="4ac7d-104">Describes the physical 3-D graphics processing unit (GPU).</span></span>

<span data-ttu-id="4ac7d-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ac7d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ac7d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_Physical3dGraphicsProcessor : CIM_LogicalDevice
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
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
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
  Boolean  EnabledForVirtualization;
  Boolean  CompatibleForVirtualization;
  string   GPUID;
  string   DirectXVersion;
  string   PixelShaderVersion;
  uint64   DedicatedVideoMemory;
  uint64   DedicatedSystemMemory;
  uint64   SharedSystemMemory;
  uint64   TotalVideoMemory;
  uint64   AvailableVideoMemory;
  string   DriverProvider;
  datetime DriverDate;
  datetime DriverInstalled;
  string   DriverVersion;
  string   DriverModelVersion;
  uint64   Rating;
  uint64   AdapterIndexID;
};
```

## <a name="members"></a><span data-ttu-id="4ac7d-107">Member</span><span class="sxs-lookup"><span data-stu-id="4ac7d-107">Members</span></span>

<span data-ttu-id="4ac7d-108">Die **MSVM \_ Physical3dGraphicsProcessor** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4ac7d-108">The **Msvm\_Physical3dGraphicsProcessor** class has these types of members:</span></span>

-   [<span data-ttu-id="4ac7d-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="4ac7d-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="4ac7d-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4ac7d-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4ac7d-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="4ac7d-111">Methods</span></span>

<span data-ttu-id="4ac7d-112">Die **MSVM- \_ Physical3dGraphicsProcessor** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-112">The **Msvm\_Physical3dGraphicsProcessor** class has these methods.</span></span>



| <span data-ttu-id="4ac7d-113">Methode</span><span class="sxs-lookup"><span data-stu-id="4ac7d-113">Method</span></span>                 | <span data-ttu-id="4ac7d-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ac7d-114">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="4ac7d-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-115">**EnableDevice**</span></span>       | <span data-ttu-id="4ac7d-116">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="4ac7d-117">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-117">**OnlineDevice**</span></span>       | <span data-ttu-id="4ac7d-118">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="4ac7d-119">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-119">**QuiesceDevice**</span></span>      | <span data-ttu-id="4ac7d-120">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="4ac7d-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-121">**RequestStateChange**</span></span> | <span data-ttu-id="4ac7d-122">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-122">This method is not supported.</span></span><br/> |
| <span data-ttu-id="4ac7d-123">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-123">**Reset**</span></span>              | <span data-ttu-id="4ac7d-124">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-124">This method is not supported.</span></span><br/> |
| <span data-ttu-id="4ac7d-125">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-125">**RestoreProperties**</span></span>  | <span data-ttu-id="4ac7d-126">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="4ac7d-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-127">**SaveProperties**</span></span>     | <span data-ttu-id="4ac7d-128">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="4ac7d-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-129">**SetPowerState**</span></span>      | <span data-ttu-id="4ac7d-130">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4ac7d-131">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4ac7d-131">Properties</span></span>

<span data-ttu-id="4ac7d-132">Die **MSVM- \_ Physical3dGraphicsProcessor** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-132">The **Msvm\_Physical3dGraphicsProcessor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4ac7d-133">**Adapterindexid**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-133">**AdapterIndexID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-134">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-136">Gibt den Adapter Index Bezeichner an, der diesem Gerät zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-136">Specifies the adapter index identifier allocated to this device.</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-137">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-137">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-138">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="4ac7d-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-140">Alle zusätzlichen Verfügbarkeit und der Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-140">Any additional availability and status of the device.</span></span> <span data-ttu-id="4ac7d-141">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-142">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-142">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-143">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-145">Die primäre Verfügbarkeit und den Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-145">The primary availability and status of the device.</span></span> <span data-ttu-id="4ac7d-146">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-146">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-147">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-148">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="4ac7d-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-150">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="4ac7d-151">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-152">**Availablevideomemory**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-152">**AvailableVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-153">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-155">Gibt die Größe des Video Speichers in Bytes an, der für die GPU verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-155">Specifies the amount of video memory, in bytes, that is available to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-156">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-156">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-157">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-159">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-159">A short description of the object.</span></span> <span data-ttu-id="4ac7d-160">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-160">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-161">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-161">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-162">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-162">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-164">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-164">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="4ac7d-165">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-165">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4ac7d-166">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-166">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4ac7d-167"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-167"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-168"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-168"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-169"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-169"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-170"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-170"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-171"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-171"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-172"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-172"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-173"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="4ac7d-173"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4ac7d-174">)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-174">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4ac7d-175">**Compatibleforvirtualization**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-175">**CompatibleForVirtualization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-176">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4ac7d-176">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-178">**true** , wenn für die Virtualisierung kompatibel andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-178">**true** if compatible for virtualization; otherwise, **false**.</span></span>

> [!Note]  
> <span data-ttu-id="4ac7d-179">Diese Eigenschaft wurde in Windows 10, Version 1703, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-179">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="4ac7d-180">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-180">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-181">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-182">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-183">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-183">The scoping system's creation class name.</span></span> <span data-ttu-id="4ac7d-184">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-184">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-185">**Dedialisiedsystemmemory**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-185">**DedicatedSystemMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-186">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-186">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-188">Gibt die Größe des System Speichers in Bytes an, der für die GPU reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-188">Specifies the amount of system memory, in bytes, that is dedicated to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-189">**Dedialisiedvideomemory**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-189">**DedicatedVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-190">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-190">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-192">Gibt die Größe des Video Speichers in Bytes an, der für die GPU reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-192">Specifies the amount of video memory, in bytes, that is dedicated to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-193">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-193">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-194">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-196">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-196">A description of the object.</span></span> <span data-ttu-id="4ac7d-197">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-197">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-198">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-198">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-199">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-200">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-201">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-201">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="4ac7d-202">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-202">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4ac7d-203">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-203">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4ac7d-204"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-204"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-205"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-205"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-206"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-206"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-207"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-207"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-208"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-208"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-209"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-209"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-210"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-210"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-211"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="4ac7d-211"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4ac7d-212">)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-212">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4ac7d-213">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-213">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-214">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-215">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-216">Eine Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-216">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="4ac7d-217">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-217">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-218">**Directxversion**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-218">**DirectXVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-219">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-220">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-221">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-221">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-222">Gibt die Debugversion von DirectX an, die von der GPU unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-222">Specifies the verison of DirectX that is supported by the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-223">**Driverdate**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-223">**DriverDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-224">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-224">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-225">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-226">Gibt das Builddatum des Treibers an.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-226">Specifies the driver build date.</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-227">**Driverinstalliert**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-227">**DriverInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-228">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-228">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-229">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-230">Gibt das Datum und die Uhrzeit der Installation des Treibers an.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-230">Specifies the date and time that the driver was installed.</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-231">**Drivermodelversion**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-231">**DriverModelVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-232">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-233">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-234">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-234">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-235">Gibt die Treibermodell Version an.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-235">Specifies the driver model version.</span></span>

> [!Note]  
> <span data-ttu-id="4ac7d-236">Diese Eigenschaft wurde in Windows 10, Version 1703, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-236">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="4ac7d-237">**Driverprovider**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-237">**DriverProvider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-238">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-239">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-240">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-240">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-241">Gibt den Namen des Treiber Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-241">Specifies the name of the driver provider.</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-242">**DriverVersion**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-242">**DriverVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-243">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-244">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-245">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-245">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-246">Gibt die Treiber Version an.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-246">Specifies the driver version.</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-247">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-247">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-248">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-249">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-250">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-250">A display name for the object.</span></span> <span data-ttu-id="4ac7d-251">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-251">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-252">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-252">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-253">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-254">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-255">Die Standard-oder Startkonfiguration eines Administrators für die **enabledstate** -Eigenschaft eines Elements.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-255">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="4ac7d-256">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 2 (aktiviert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-256">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-257">**Enabledforvirtualization**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-257">**EnabledForVirtualization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-258">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4ac7d-258">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-259">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-260">Gibt an, ob der Adapter für die Verwendung mit remotefx aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-260">Specifies whether the adapter has been enabled for use with RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-261">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-261">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-262">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-263">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-264">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-264">The enabled and disabled states of an element.</span></span> <span data-ttu-id="4ac7d-265">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt, und es handelt sich um einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-265">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="4ac7d-266">Wert</span><span class="sxs-lookup"><span data-stu-id="4ac7d-266">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="4ac7d-267">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4ac7d-267">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="4ac7d-268"><dt>**Unbekannter**</dt> Wert <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4ac7d-268"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="4ac7d-269">Der Zustand des Elements konnte nicht bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-269">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="4ac7d-270"><dt>**Sonstige**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4ac7d-270"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="4ac7d-271"><dt>**Aktiviert**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4ac7d-271"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="4ac7d-272">Das-Element wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-272">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="4ac7d-273"><dt>**Deaktiviert**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="4ac7d-273"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="4ac7d-274">Das Element ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-274">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="4ac7d-275"><dt>4</dt> wird <dt>**heruntergefahren**</dt></span><span class="sxs-lookup"><span data-stu-id="4ac7d-275"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="4ac7d-276">Das Element wird gerade in den deaktivierten Zustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-276">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="4ac7d-277"><dt>**Nicht zutreffend**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="4ac7d-277"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="4ac7d-278">Das Element unterstützt das Aktivieren oder Deaktivieren des Elements nicht.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-278">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="4ac7d-279"><dt>**Aktiviert, aber offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="4ac7d-279"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="4ac7d-280">Das Element kann Befehle abschließen und löscht alle neuen Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-280">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="4ac7d-281"><dt>**In Test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="4ac7d-281"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="4ac7d-282">Das-Element befindet sich in einem Testzustand.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-282">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="4ac7d-283"><dt></dt> Verzögert <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="4ac7d-283"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="4ac7d-284">Das Element kann Befehle abschließen, aber alle neuen Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-284">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="4ac7d-285"><dt>**Inesce**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="4ac7d-285"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="4ac7d-286">Das Element ist aktiviert, jedoch in einem eingeschränkten Modus.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-286">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="4ac7d-287">Das Verhalten des-Elements ähnelt dem aktivierten Status (2), aber es verarbeitet nur einen eingeschränkten Satz von Befehlen.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-287">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="4ac7d-288">Alle anderen Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-288">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="4ac7d-289"><dt>**Start**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="4ac7d-289"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="4ac7d-290">Das Element wechselt in den Zustand "aktiviert" (2).</span><span class="sxs-lookup"><span data-stu-id="4ac7d-290">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="4ac7d-291">Neue Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-291">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="4ac7d-292">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-292">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-293">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4ac7d-293">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-294">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-295">Gibt an, ob der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-295">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="4ac7d-296">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-296">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-297">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-297">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-298">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-299">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-300">Eine Zeichenfolge, die weitere Informationen über den Fehler enthält, der in **LastErrorCode** aufgezeichnet wurde, sowie Informationen über alle Maßnahmen, die ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-300">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="4ac7d-301">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-301">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-302">**GPUID**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-302">**GPUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-303">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-304">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-305">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-305">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-306">Enthält den GPU-Bezeichner für den Adapter.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-306">Contains the GPU identifier for the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-307">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-307">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-308">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-308">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-309">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-310">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-310">The current health of the element.</span></span> <span data-ttu-id="4ac7d-311">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-311">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-312">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-312">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-313">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="4ac7d-313">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-314">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-315">Ein Array von Freiform-Zeichen folgen, die Erklärungen und Details hinter den Einträgen im Eigenschafts Array " **OtherIdentifyingInfo** " bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-315">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="4ac7d-316">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-316">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-317">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-317">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-318">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-318">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-319">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-320">Das Datum und die Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-320">The date and time when the object was installed.</span></span> <span data-ttu-id="4ac7d-321">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-321">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="4ac7d-322">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-322">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-323">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-323">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-324">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-325">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-326">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-326">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-327">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-327">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="4ac7d-328">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-328">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-329">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-329">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-330">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-330">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-331">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-332">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-332">The last error code reported by the logical device.</span></span> <span data-ttu-id="4ac7d-333">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-333">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-334">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-334">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-335">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-335">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-336">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-337">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-337">This property has been deprecated.</span></span> <span data-ttu-id="4ac7d-338">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-338">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-339">**Name**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-339">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-340">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-341">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-342">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-342">The label by which the object is known.</span></span> <span data-ttu-id="4ac7d-343">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-343">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-344">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-344">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-345">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-345">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-346">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-347">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-347">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="4ac7d-348">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-348">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4ac7d-349">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-349">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4ac7d-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-351"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-351"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-352"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-352"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-353"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-353"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-354"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="4ac7d-354"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-355"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-355"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-356"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-356"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-357"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-357"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-358"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-358"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-359"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-359"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-360"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-360"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-361"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-361"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-362"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-362"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-363"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-363"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-364"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-364"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-365"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-365"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-366"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-366"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-367"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-367"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-368"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="4ac7d-368"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4ac7d-369">)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-369">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4ac7d-370">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-370">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-371">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="4ac7d-371">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-372">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-373">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-373">The current statuses of the object.</span></span> <span data-ttu-id="4ac7d-374">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-375">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-375">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-376">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-377">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-378">Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-378">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="4ac7d-379">Diese Eigenschaft muss auf **null** festgelegt werden, wenn die **enabledstate** -Eigenschaft einen anderen Wert als 1 hat.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-379">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="4ac7d-380">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-380">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-381">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-381">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-382">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="4ac7d-382">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-383">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-384">Alle zusätzlichen Daten über Geräte-ID-Informationen, die zur Identifizierung eines logischen Geräts verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-384">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="4ac7d-385">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-385">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-386">**PixelShaderVersion**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-386">**PixelShaderVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-387">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-388">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-389">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-389">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-390">Gibt die Pixel-Shader-Debugversion an, die von der GPU unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-390">Specifies the pixel shader verison that is supported by the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-391">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-391">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-392">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="4ac7d-392">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-393">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-394">Die Energie Verwaltungsfunktionen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-394">The power management capabilities of the device.</span></span> <span data-ttu-id="4ac7d-395">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-395">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-396">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-396">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-397">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4ac7d-397">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-398">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-399">Gibt an, ob das Gerät Energie gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-399">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="4ac7d-400">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-400">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-401">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-401">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-402">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-402">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-403">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-403">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-404">Gibt an, wie viele aufeinanderfolgende Stunden dieses Gerät seit dem letzten Strom Umgebung eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-404">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="4ac7d-405">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-405">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-406">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-406">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-407">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-407">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-408">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-409">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-409">Provides high level status information.</span></span> <span data-ttu-id="4ac7d-410">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-410">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="4ac7d-411">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-411">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4ac7d-412">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-412">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4ac7d-413"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-413"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-414"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-414"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-415"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="4ac7d-415"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-416"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-416"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-417"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-417"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-418"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="4ac7d-418"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4ac7d-419">)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-419">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4ac7d-420">**Rating**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-420">**Rating**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-421">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-421">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-422">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-423">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("kein Wert")</span><span class="sxs-lookup"><span data-stu-id="4ac7d-423">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-424">Gibt die GPU-remotefx-Bewertung für dieses Gerät an.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-424">Specifies the GPU RemoteFX rating for this device.</span></span> <span data-ttu-id="4ac7d-425">Diese Eigenschaft wird derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-425">This property is not currently used.</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-426">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-426">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-427">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-427">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-428">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-429">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-429">The last requested or desired state for the element.</span></span> <span data-ttu-id="4ac7d-430">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 12 (nicht zutreffend) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-430">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-431">**Sharedsystemmemory**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-431">**SharedSystemMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-432">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-432">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-433">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-434">Gibt die Menge des freigegebenen System Speichers in Bytes an, der für die GPU verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-434">Specifies the amount of shared system memory, in bytes, that is available to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-435">**Status**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-435">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-436">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-437">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-438">Der aktuelle Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-438">The current status of the object.</span></span> <span data-ttu-id="4ac7d-439">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-439">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-440">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-440">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-441">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="4ac7d-441">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-442">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-443">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-443">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="4ac7d-444">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-444">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-445">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-445">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-446">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-446">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-447">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-448">Der aktuelle Zustand des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-448">The current state of the logical device.</span></span> <span data-ttu-id="4ac7d-449">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-449">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-450">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-450">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-451">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-452">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-452">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-453">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-453">The scoping system's creation class name.</span></span> <span data-ttu-id="4ac7d-454">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-454">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-455">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-455">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-456">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-456">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-457">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-457">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-458">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-458">The scoping system's name.</span></span> <span data-ttu-id="4ac7d-459">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-459">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-460">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-460">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-461">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-461">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-462">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-462">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-463">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-463">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="4ac7d-464">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-464">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-465">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-465">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-466">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-466">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-467">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-467">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-468">Die Gesamtanzahl der Stunden, für die dieses Gerät eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-468">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="4ac7d-469">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-469">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-470">**Totalvideomemory**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-470">**TotalVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-471">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-471">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-472">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-473">Gibt die Gesamtmenge an Videospeicher in Bytes an, die auf der GPU vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-473">Specifies the total amount of video memory, in bytes, present on the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="4ac7d-474">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-474">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ac7d-475">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4ac7d-475">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4ac7d-476">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ac7d-476">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ac7d-477">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-477">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="4ac7d-478">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4ac7d-478">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4ac7d-479">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ac7d-479">Requirements</span></span>



| <span data-ttu-id="4ac7d-480">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ac7d-480">Requirement</span></span> | <span data-ttu-id="4ac7d-481">Wert</span><span class="sxs-lookup"><span data-stu-id="4ac7d-481">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ac7d-482">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-482">Minimum supported client</span></span><br/> | <span data-ttu-id="4ac7d-483">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="4ac7d-483">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="4ac7d-484">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4ac7d-484">Minimum supported server</span></span><br/> | <span data-ttu-id="4ac7d-485">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4ac7d-485">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4ac7d-486">Namespace</span><span class="sxs-lookup"><span data-stu-id="4ac7d-486">Namespace</span></span><br/>                | <span data-ttu-id="4ac7d-487">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="4ac7d-487">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4ac7d-488">MOF</span><span class="sxs-lookup"><span data-stu-id="4ac7d-488">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4ac7d-489"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4ac7d-489"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4ac7d-490">DLL</span><span class="sxs-lookup"><span data-stu-id="4ac7d-490">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ac7d-491"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4ac7d-491"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

