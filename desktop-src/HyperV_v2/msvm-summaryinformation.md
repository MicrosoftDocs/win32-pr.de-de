---
description: Wird in der getsummaryinformation-Methode und der GetDefinitionFileSummaryInformation-Methode in der MSVM \_ virtualsystemmanagementservice-Klasse verwendet, um schnell allgemeine Informationen zu einem virtuellen Computer oder einer Momentaufnahme abzurufen.
ms.assetid: 8D188BB2-4A56-4738-94DD-64D9F9B90B73
title: Msvm_SummaryInformation-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SummaryInformation
- Msvm_SummaryInformation.InstanceID
- Msvm_SummaryInformation.AllocatedGPU
- Msvm_SummaryInformation.Shielded
- Msvm_SummaryInformation.AsynchronousTasks
- Msvm_SummaryInformation.CreationTime
- Msvm_SummaryInformation.ElementName
- Msvm_SummaryInformation.EnabledState
- Msvm_SummaryInformation.OtherEnabledState
- Msvm_SummaryInformation.GuestOperatingSystem
- Msvm_SummaryInformation.HealthState
- Msvm_SummaryInformation.Heartbeat
- Msvm_SummaryInformation.MemoryUsage
- Msvm_SummaryInformation.MemoryAvailable
- Msvm_SummaryInformation.AvailableMemoryBuffer
- Msvm_SummaryInformation.SwapFilesInUse
- Msvm_SummaryInformation.Name
- Msvm_SummaryInformation.Notes
- Msvm_SummaryInformation.Version
- Msvm_SummaryInformation.NumberOfProcessors
- Msvm_SummaryInformation.OperationalStatus
- Msvm_SummaryInformation.ProcessorLoad
- Msvm_SummaryInformation.ProcessorLoadHistory
- Msvm_SummaryInformation.Snapshots
- Msvm_SummaryInformation.StatusDescriptions
- Msvm_SummaryInformation.ThumbnailImage
- Msvm_SummaryInformation.ThumbnailImageHeight
- Msvm_SummaryInformation.ThumbnailImageWidth
- Msvm_SummaryInformation.UpTime
- Msvm_SummaryInformation.ReplicationState
- Msvm_SummaryInformation.ReplicationStateEx
- Msvm_SummaryInformation.ReplicationHealth
- Msvm_SummaryInformation.ReplicationHealthEx
- Msvm_SummaryInformation.ReplicationMode
- Msvm_SummaryInformation.TestReplicaSystem
- Msvm_SummaryInformation.ApplicationHealth
- Msvm_SummaryInformation.IntegrationServicesVersionState
- Msvm_SummaryInformation.MemorySpansPhysicalNumaNodes
- Msvm_SummaryInformation.ReplicationProviderId
- Msvm_SummaryInformation.EnhancedSessionModeState
- Msvm_SummaryInformation.VirtualSwitchNames
- Msvm_SummaryInformation.VirtualSystemSubType
- Msvm_SummaryInformation.HostComputerSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 817d025551ae10002b008a181edd8a7dfd2ec68c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348436"
---
# <a name="msvm_summaryinformation-class"></a><span data-ttu-id="4285d-103">MSVM \_ SummaryInformation-Klasse</span><span class="sxs-lookup"><span data-stu-id="4285d-103">Msvm\_SummaryInformation class</span></span>

<span data-ttu-id="4285d-104">Wird in der [**getsummaryinformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) -Methode und der [**GetDefinitionFileSummaryInformation**](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md) -Methode in der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse verwendet, um schnell allgemeine Informationen zu einem virtuellen Computer oder einer Momentaufnahme abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4285d-104">Used in the [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) and [**GetDefinitionFileSummaryInformation**](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md) methods in the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to quickly retrieve common information related to a virtual machine or snapshot.</span></span>

<span data-ttu-id="4285d-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="4285d-105">The following syntax is simplified Managed Object Format (MOF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4285d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4285d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SummaryInformation : Msvm_SummaryInformationBase
{
  string                       InstanceID;
  string                       AllocatedGPU;
  boolean                      Shielded;
  CIM_ConcreteJob              AsynchronousTasks[];
  DateTime                     CreationTime;
  string                       ElementName;
  uint16                       EnabledState;
  string                       OtherEnabledState;
  string                       GuestOperatingSystem;
  uint16                       HealthState;
  uint16                       Heartbeat;
  uint64                       MemoryUsage;
  sint32                       MemoryAvailable;
  sint32                       AvailableMemoryBuffer;
  boolean                      SwapFilesInUse;
  string                       Name;
  string                       Notes;
  string                       Version;
  uint16                       NumberOfProcessors;
  uint16                       OperationalStatus[];
  uint16                       ProcessorLoad;
  uint16                       ProcessorLoadHistory[];
  CIM_VirtualSystemSettingData Snapshots[];
  string                       StatusDescriptions[];
  uint8                        ThumbnailImage[];
  uint16                       ThumbnailImageHeight;
  uint16                       ThumbnailImageWidth;
  uint64                       UpTime;
  uint16                       ReplicationState;
  uint16                       ReplicationStateEx[];
  uint16                       ReplicationHealth;
  uint16                       ReplicationHealthEx[];
  uint16                       ReplicationMode;
  CIM_ComputerSystem       REF TestReplicaSystem;
  uint16                       ApplicationHealth;
  uint16                       IntegrationServicesVersionState;
  boolean                      MemorySpansPhysicalNumaNodes;
  string                       ReplicationProviderId[];
  uint16                       EnhancedSessionModeState;
  string                       VirtualSwitchNames[];
  string                       VirtualSystemSubType;
  string                       HostComputerSystemName;
};
```

## <a name="members"></a><span data-ttu-id="4285d-107">Member</span><span class="sxs-lookup"><span data-stu-id="4285d-107">Members</span></span>

<span data-ttu-id="4285d-108">Die **MSVM \_ SummaryInformation** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4285d-108">The **Msvm\_SummaryInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="4285d-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4285d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4285d-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4285d-110">Properties</span></span>

<span data-ttu-id="4285d-111">Die **MSVM \_ SummaryInformation** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4285d-111">The **Msvm\_SummaryInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4285d-112">**Zugedgpu**</span><span class="sxs-lookup"><span data-stu-id="4285d-112">**AllocatedGPU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4285d-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4285d-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4285d-115">Der Bezeichner der physischen Grafikverarbeitungseinheit (GPU), die dieser virtuellen Maschine zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4285d-115">The identifier of the physical graphics processing unit (GPU) allocated to this virtual machine.</span></span> <span data-ttu-id="4285d-116">Diese Eigenschaft gilt nur für virtuelle Maschinen, die remotefx verwenden.</span><span class="sxs-lookup"><span data-stu-id="4285d-116">This property only applies to virtual machines that use RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="4285d-117">**Applicationhealth**</span><span class="sxs-lookup"><span data-stu-id="4285d-117">**ApplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-118">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4285d-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4285d-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4285d-120">Der aktuelle Integritäts Status der Anwendung für die virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="4285d-120">The current application health status for the virtual machine.</span></span> <span data-ttu-id="4285d-121">Diese Eigenschaft ist für Instanzen von **MSVM \_ SummaryInformation** , die eine Momentaufnahme eines virtuellen Computers darstellen, ungültig.</span><span class="sxs-lookup"><span data-stu-id="4285d-121">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="4285d-122">**OK** (2)</span><span class="sxs-lookup"><span data-stu-id="4285d-122">**OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Critical"></span><span id="application_critical"></span><span id="APPLICATION_CRITICAL"></span>

<span data-ttu-id="4285d-123">**Anwendungs kritisch** (32782)</span><span class="sxs-lookup"><span data-stu-id="4285d-123">**Application Critical** (32782)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4285d-124">**Deaktiviert** (32896)</span><span class="sxs-lookup"><span data-stu-id="4285d-124">**Disabled** (32896)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4285d-125">**Asynchronoustasks**</span><span class="sxs-lookup"><span data-stu-id="4285d-125">**AsynchronousTasks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-126">Datentyp: **CIM \_ concretejob** -Array</span><span class="sxs-lookup"><span data-stu-id="4285d-126">Data type: **CIM\_ConcreteJob** array</span></span>
</dt> <dt>

<span data-ttu-id="4285d-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4285d-128">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="4285d-128">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="4285d-129">Ein Array von [**MSVM-" \_ concretejob**](msvm-concretejob.md) "-Instanzen, die alle asynchronen Vorgänge im Zusammenhang mit dem derzeit ausgeführten virtuellen Computer darstellen.</span><span class="sxs-lookup"><span data-stu-id="4285d-129">An array of [**Msvm\_ConcreteJob**](msvm-concretejob.md) instances that represent any asynchronous operations related to the virtual machine that are currently executing.</span></span> <span data-ttu-id="4285d-130">Diese Eigenschaft ist für Instanzen von **MSVM \_ SummaryInformation** , die eine Momentaufnahme eines virtuellen Computers darstellen, ungültig.</span><span class="sxs-lookup"><span data-stu-id="4285d-130">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="4285d-131">**Availablememorybuffer**</span><span class="sxs-lookup"><span data-stu-id="4285d-131">**AvailableMemoryBuffer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-132">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4285d-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4285d-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4285d-134">Der Prozentsatz des verfügbaren Arbeitsspeicher Puffers für die virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="4285d-134">The percentage of available memory buffer for the virtual machine.</span></span> <span data-ttu-id="4285d-135">Wenn dynamischer Arbeitsspeicher für eine virtuelle Maschine aktiviert ist, stellt diese Eigenschaft das Verhältnis des verfügbaren Arbeitsspeicher Puffers zum idealen Speicherpuffer für den virtuellen Computer dar.</span><span class="sxs-lookup"><span data-stu-id="4285d-135">When dynamic memory is enabled for a virtual machine, this property represents the ratio of available memory buffer to the ideal memory buffer for the virtual machine.</span></span> <span data-ttu-id="4285d-136">Die ideale Größe des Arbeitsspeicher Puffers wird mit der **targetmemorybuffer** -Eigenschaft der [**MSVM \_ memorysettingdata**](msvm-memorysettingdata.md) -Klasse konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="4285d-136">The ideal memory buffer size is configured by using the **TargetMemoryBuffer** property of the [**Msvm\_MemorySettingData**](msvm-memorysettingdata.md) class.</span></span>

<span data-ttu-id="4285d-137">Diese Eigenschaft ist für Instanzen der **MSVM-Klasse " \_ SummaryInformation** " ungültig, die virtuelle Computer darstellt, für die der dynamische Arbeitsspeicher nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4285d-137">This property is not valid for instances of the **Msvm\_SummaryInformation** class that represent virtual machines for which dynamic memory is not enabled.</span></span>

<span data-ttu-id="4285d-138">Diese Eigenschaft ist für Instanzen der **MSVM \_ SummaryInformation** -Klasse, die eine Momentaufnahme eines virtuellen Computers darstellen, ungültig.</span><span class="sxs-lookup"><span data-stu-id="4285d-138">This property is not valid for instances of the **Msvm\_SummaryInformation** class that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="4285d-139">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="4285d-139">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-140">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="4285d-140">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="4285d-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4285d-142">Der Zeitpunkt, zu dem der virtuelle Computer oder die Momentaufnahme erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="4285d-142">The time at which the virtual machine or snapshot was created.</span></span>

</dd> <dt>

<span data-ttu-id="4285d-143">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="4285d-143">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4285d-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4285d-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4285d-146">Der Anzeige Name für den virtuellen Computer oder die Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="4285d-146">The display name for the virtual machine or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="4285d-147">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="4285d-147">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-148">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4285d-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4285d-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4285d-150">Der aktuelle Zustand des virtuellen Computers oder der Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="4285d-150">The current state of the virtual machine or snapshot.</span></span> <span data-ttu-id="4285d-151">Mögliche Werte finden Sie unter der **enabledstate** -Eigenschaft der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="4285d-151">See the **EnabledState** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

</dd> <dt>

<span data-ttu-id="4285d-152">**Enhancedsessionmodestate**</span><span class="sxs-lookup"><span data-stu-id="4285d-152">**EnhancedSessionModeState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-153">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4285d-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4285d-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4285d-155">Gibt an, ob Verbindungen im erweiterten Modus vom Host zugelassen werden und ob Sie für den virtuellen Computer verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="4285d-155">Indicates whether enhanced mode connections are allowed by the host, and if allowed, whether they are available to the virtual machine.</span></span>

<span data-ttu-id="4285d-156">**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4285d-156">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

<span data-ttu-id="4285d-157">**Zulässig und verfügbar** (2)</span><span class="sxs-lookup"><span data-stu-id="4285d-157">**Allowed and available** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span data-ttu-id="4285d-158">**Nicht zulässig** (3)</span><span class="sxs-lookup"><span data-stu-id="4285d-158">**Not allowed** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

<span data-ttu-id="4285d-159">**Zulässig, aber nicht verfügbar** (6)</span><span class="sxs-lookup"><span data-stu-id="4285d-159">**Allowed but not available** (6 )</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4285d-160">**Guestoperatingsystem**</span><span class="sxs-lookup"><span data-stu-id="4285d-160">**GuestOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-161">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4285d-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4285d-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4285d-163">Der Name des Gast Betriebssystems, falls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4285d-163">The name of the guest operating system, if available.</span></span> <span data-ttu-id="4285d-164">Wenn diese Informationen nicht verfügbar sind, ist der Wert dieser Eigenschaft **null**.</span><span class="sxs-lookup"><span data-stu-id="4285d-164">If this information is not available, the value of this property is **Null**.</span></span> <span data-ttu-id="4285d-165">Diese Eigenschaft ist für Instanzen von **MSVM \_ SummaryInformation** , die eine Momentaufnahme eines virtuellen Computers darstellen, ungültig.</span><span class="sxs-lookup"><span data-stu-id="4285d-165">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="4285d-166">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="4285d-166">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-167">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4285d-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4285d-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4285d-169">Der aktuelle Integritäts Status für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="4285d-169">The current health state for the virtual machine.</span></span> <span data-ttu-id="4285d-170">Diese Eigenschaft ist für Instanzen von **MSVM \_ SummaryInformation** , die eine Momentaufnahme eines virtuellen Computers darstellen, ungültig.</span><span class="sxs-lookup"><span data-stu-id="4285d-170">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="4285d-171">**Heartbeat**</span><span class="sxs-lookup"><span data-stu-id="4285d-171">**Heartbeat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-172">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4285d-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4285d-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4285d-174">Der aktuelle Takt Status für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="4285d-174">The current heartbeat status for the virtual machine.</span></span> <span data-ttu-id="4285d-175">Weitere Informationen finden Sie in der Dokumentation für die [**Statusbeschreibungen**](msvm-heartbeatcomponent.md) -Eigenschaft der **MSVM \_ heartbeatcomponent** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="4285d-175">For more information, see the documentation for the [**StatusDescriptions**](msvm-heartbeatcomponent.md) property of the **Msvm\_HeartbeatComponent** class.</span></span> <span data-ttu-id="4285d-176">Diese Eigenschaft ist für Instanzen von **MSVM \_ SummaryInformation** , die eine Momentaufnahme eines virtuellen Computers darstellen, ungültig.</span><span class="sxs-lookup"><span data-stu-id="4285d-176">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

<dl> <dt>

<span data-ttu-id="4285d-177"><span id="OK"></span><span id="ok"></span>**OK** (2)</span><span class="sxs-lookup"><span data-stu-id="4285d-177"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4285d-178"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (6)</span><span class="sxs-lookup"><span data-stu-id="4285d-178"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (6)</span></span>
</dt> <dt>

<span data-ttu-id="4285d-179"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (12)</span><span class="sxs-lookup"><span data-stu-id="4285d-179"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (12)</span></span>
</dt> <dt>

<span data-ttu-id="4285d-180"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (13)</span><span class="sxs-lookup"><span data-stu-id="4285d-180"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (13)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4285d-181">**Hostcomputersystemname**</span><span class="sxs-lookup"><span data-stu-id="4285d-181">**HostComputerSystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-182">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4285d-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4285d-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4285d-184">Der Name des Computers, auf dem dieser virtuelle Computer gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="4285d-184">The name of the computer hosting this virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="4285d-185">In Windows 10 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4285d-185">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="4285d-186">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4285d-186">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-187">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4285d-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4285d-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4285d-189">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("CIM \_ managedelta Element. InstanceId"), [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4285d-189">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ManagedElement.InstanceID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4285d-190">"InstanceId" ist eine optionale Eigenschaft, die verwendet werden kann, um eine Instanz dieser Klasse innerhalb des Gültigkeits Bereichs des instanziierten Namespace eindeutig und eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="4285d-190">InstanceID is an optional property that may be used to opaquely and uniquely identify an instance of this class within the scope of the instantiating Namespace.</span></span> <span data-ttu-id="4285d-191">Verschiedene Unterklassen dieser Klasse können diese Eigenschaft überschreiben, um Sie erforderlich zu machen, oder einen Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="4285d-191">Various subclasses of this class may override this property to make it required, or a key.</span></span> <span data-ttu-id="4285d-192">Diese Unterklassen können auch die bevorzugten Algorithmen zum Sicherstellen der Eindeutigkeit ändern, die unten definiert sind.</span><span class="sxs-lookup"><span data-stu-id="4285d-192">Such subclasses may also modify the preferred algorithms for ensuring uniqueness that are defined below.</span></span>

<span data-ttu-id="4285d-193">Um die Eindeutigkeit innerhalb des Namespaces sicherzustellen, sollte der Wert von InstanceId mit dem folgenden "bevorzugten" Algorithmus erstellt werden:</span><span class="sxs-lookup"><span data-stu-id="4285d-193">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm:</span></span>

<span data-ttu-id="4285d-194"><OrgID>:<LocalID></span><span class="sxs-lookup"><span data-stu-id="4285d-194"><OrgID>:<LocalID></span></span>

<span data-ttu-id="4285d-195">Dabei <OrgID> <LocalID> sind und durch einen Doppelpunkt (:) und wobei <OrgID> ein urheberrechtlich geschütztes, mit einem oder ein oder anderweitig eindeutiger Name enthalten muss, der der Geschäfts Entität entspricht, die die InstanceId erstellt oder definiert, oder die eine registrierte ID ist, die der Geschäfts Entität von einer anerkannten globalen Autorität zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="4285d-195">Where <OrgID> and <LocalID> are separated by a colon (:), and where <OrgID> must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="4285d-196">(Diese Anforderung ähnelt der <Schema Name> \_ <Class Name> Struktur von Schema Klassennamen.) Außerdem <OrgID> darf keine Doppelpunkte (:) enthalten, um die Eindeutigkeit sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="4285d-196">(This requirement is similar to the <Schema Name>\_<Class Name> structure of Schema class names.) In addition, to ensure uniqueness, <OrgID> must not contain a colon (:).</span></span> <span data-ttu-id="4285d-197">Wenn dieser Algorithmus verwendet wird, muss der erste Doppelpunkt, der in InstanceId angezeigt wird, zwischen und angezeigt werden <OrgID> <LocalID> .</span><span class="sxs-lookup"><span data-stu-id="4285d-197">When using this algorithm, the first colon to appear in InstanceID must appear between <OrgID> and <LocalID>.</span></span>

<span data-ttu-id="4285d-198"><LocalID> wird von der Business-Entität gewählt und sollte nicht wieder verwendet werden, um verschiedene zugrunde liegende (reale) Elemente zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="4285d-198"><LocalID> is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="4285d-199">Wenn not NULL und der oben genannte "bevorzugte" Algorithmus nicht verwendet wird, muss die definierende Entität sicherstellen, dass die resultierende InstanceId nicht in allen instanceids wieder verwendet wird, die von diesem oder anderen Anbietern für den Namespace dieser Instanz erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4285d-199">If not null and the above "preferred" algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span>

<span data-ttu-id="4285d-200">Wenn für von DMTF definierte Instanzen nicht auf NULL festgelegt ist, muss der "bevorzugte" Algorithmus verwendet werden, wobei <OrgID> auf CIM festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4285d-200">If not set to null for DMTF-defined instances, the "preferred" algorithm must be used with the <OrgID> set to CIM.</span></span>

> [!Note]  
> <span data-ttu-id="4285d-201">In Windows 10 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4285d-201">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="4285d-202">**Integrationservicesversionstate**</span><span class="sxs-lookup"><span data-stu-id="4285d-202">**IntegrationServicesVersionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-203">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4285d-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4285d-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4285d-205">Gibt an, ob die auf dem virtuellen Computer installierten Integrationsdienste auf dem neuesten Stand sind.</span><span class="sxs-lookup"><span data-stu-id="4285d-205">Indicates whether the integration services installed in the virtual machine are up to date.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4285d-206">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="4285d-206">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="UpToDate"></span><span id="uptodate"></span><span id="UPTODATE"></span>

<span data-ttu-id="4285d-207">**Update** (1)</span><span class="sxs-lookup"><span data-stu-id="4285d-207">**UpToDate** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Mismatch"></span><span id="mismatch"></span><span id="MISMATCH"></span>

<span data-ttu-id="4285d-208">Nicht **überein** stimmende (2)</span><span class="sxs-lookup"><span data-stu-id="4285d-208">**Mismatch** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4285d-209">**Memoryavailable**</span><span class="sxs-lookup"><span data-stu-id="4285d-209">**MemoryAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-210">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4285d-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4285d-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4285d-212">Der Prozentsatz des aktuellen Arbeitsspeichers, der für den virtuellen Computer verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="4285d-212">The percentage of the current memory available to the virtual machine.</span></span> <span data-ttu-id="4285d-213">Wenn dynamischer Arbeitsspeicher für eine virtuelle Maschine aktiviert ist, stellt diese Eigenschaft das Verhältnis zwischen dem verfügbaren Arbeitsspeicher des virtuellen Computers und dem gesamten physischen Arbeitsspeicher dar, der dem virtuellen Computer zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="4285d-213">When dynamic memory is enabled for a virtual machine, this property represents the ratio of available memory of the virtual machine to the total physical memory assigned to the virtual machine.</span></span> <span data-ttu-id="4285d-214">Wenn für eine virtuelle Maschine kein Arbeitsspeicher verfügbar ist, ist diese Eigenschaft negativ und enthält das Verhältnis des Arbeitsspeichers, der für die virtuelle Maschine benötigt wird, zum gesamten physischen Arbeitsspeicher, der der virtuellen Maschine zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="4285d-214">When a virtual machine has no available memory, this property will be negative, and it will contain the ratio of memory needed for the virtual machine to the total physical memory assigned to the virtual machine.</span></span>

<span data-ttu-id="4285d-215">Diese Eigenschaft ist für Instanzen der **MSVM-Klasse " \_ SummaryInformation** " ungültig, die virtuelle Computer darstellt, für die der dynamische Arbeitsspeicher nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4285d-215">This property is not valid for instances of the **Msvm\_SummaryInformation** class that represent virtual machines for which dynamic memory is not enabled.</span></span>

<span data-ttu-id="4285d-216">Diese Eigenschaft ist für Instanzen der **MSVM \_ SummaryInformation** -Klasse, die eine Momentaufnahme eines virtuellen Computers darstellen, ungültig.</span><span class="sxs-lookup"><span data-stu-id="4285d-216">This property is not valid for instances of the **Msvm\_SummaryInformation** class that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="4285d-217">**Memoryspansphysicalnumanodes**</span><span class="sxs-lookup"><span data-stu-id="4285d-217">**MemorySpansPhysicalNumaNodes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-218">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4285d-218">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4285d-219">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4285d-220">Gibt an, ob der Arbeitsspeicher eines oder mehrerer der virtuellen NUMA-Knoten (nicht einheitlicher Speicherzugriff) der virtuellen Maschine mehrere physische NUMA-Knoten des hostingcomputersystems umfasst.</span><span class="sxs-lookup"><span data-stu-id="4285d-220">Indicates whether the memory of the one or more of the virtual nonuniform memory access (NUMA) nodes of the virtual machine spans multiple physical NUMA nodes of the hosting computer system.</span></span> <span data-ttu-id="4285d-221">Enthält **true** , wenn der Arbeitsspeicher mehrere physische NUMA-Knoten umfasst, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="4285d-221">Contains **True** if the memory spans multiple physical NUMA nodes or **False** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="4285d-222">**MemoryUsage**</span><span class="sxs-lookup"><span data-stu-id="4285d-222">**MemoryUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-223">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4285d-223">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4285d-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4285d-225">Die aktuelle Speicherauslastung (in Megabyte) der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="4285d-225">The current memory usage, in megabytes, of the virtual machine.</span></span> <span data-ttu-id="4285d-226">Diese Eigenschaft ist für Instanzen von **MSVM \_ SummaryInformation** , die eine Momentaufnahme eines virtuellen Computers darstellen, ungültig.</span><span class="sxs-lookup"><span data-stu-id="4285d-226">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="4285d-227">**Name**</span><span class="sxs-lookup"><span data-stu-id="4285d-227">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-228">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4285d-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4285d-229">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4285d-230">Der eindeutige Name für den virtuellen Computer oder die Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="4285d-230">The unique name for the virtual machine or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="4285d-231">**Hinweise**</span><span class="sxs-lookup"><span data-stu-id="4285d-231">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-232">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4285d-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4285d-233">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4285d-234">Die Anmerkungen, die dem virtuellen Computer oder der Momentaufnahme zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="4285d-234">The notes associated with the virtual machine or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="4285d-235">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="4285d-235">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-236">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4285d-236">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4285d-237">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4285d-238">Die Gesamtanzahl der virtuellen Prozessoren, die dem virtuellen Computer oder der Momentaufnahme zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="4285d-238">The total number of virtual processors allocated to the virtual machine or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="4285d-239">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="4285d-239">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-240">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="4285d-240">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4285d-241">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4285d-242">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="4285d-242">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="4285d-243">Der aktuelle Betriebsstatus der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="4285d-243">The current operational statuses of the virtual machine.</span></span> <span data-ttu-id="4285d-244">Mögliche Werte finden Sie unter der **OperationalStatus** -Eigenschaft der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="4285d-244">See the **OperationalStatus** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

</dd> <dt>

<span data-ttu-id="4285d-245">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="4285d-245">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-246">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4285d-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4285d-247">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4285d-248">Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4285d-248">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1.</span></span> <span data-ttu-id="4285d-249">Diese Eigenschaft wird auf **null** festgelegt, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="4285d-249">This property will be set to **Null** when **EnabledState** is any value other than 1.</span></span>

</dd> <dt>

<span data-ttu-id="4285d-250">**Processorload**</span><span class="sxs-lookup"><span data-stu-id="4285d-250">**ProcessorLoad**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-251">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4285d-251">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4285d-252">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4285d-253">Die aktuelle Prozessorauslastung der virtuellen Maschine (in Prozent).</span><span class="sxs-lookup"><span data-stu-id="4285d-253">The current processor usage of the virtual machine, in percentage.</span></span> <span data-ttu-id="4285d-254">Diese Eigenschaft ist für Instanzen von **MSVM \_ SummaryInformation** , die eine Momentaufnahme eines virtuellen Computers darstellen, ungültig.</span><span class="sxs-lookup"><span data-stu-id="4285d-254">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="4285d-255">**Processorloadhistory**</span><span class="sxs-lookup"><span data-stu-id="4285d-255">**ProcessorLoadHistory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-256">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="4285d-256">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4285d-257">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4285d-258">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="4285d-258">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="4285d-259">Ein Array der vorherigen 100-Stichproben der Prozessorauslastung in Prozent für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="4285d-259">An array of the previous 100 samples of the processor usage, in percentage, for the virtual machine.</span></span> <span data-ttu-id="4285d-260">Diese Eigenschaft ist für Instanzen von **MSVM \_ SummaryInformation** , die eine Momentaufnahme eines virtuellen Computers darstellen, ungültig.</span><span class="sxs-lookup"><span data-stu-id="4285d-260">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="4285d-261">**ReplicationHealth**</span><span class="sxs-lookup"><span data-stu-id="4285d-261">**ReplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-262">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4285d-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4285d-263">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4285d-264">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**MSVM \_ SummaryInformation**.**Replicationhealthex**")</span><span class="sxs-lookup"><span data-stu-id="4285d-264">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**Msvm\_SummaryInformation**.**ReplicationHealthEx**")</span></span>
</dt> </dl>

<span data-ttu-id="4285d-265">Die Replikations Integrität für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="4285d-265">The replication health for the virtual machine.</span></span> <span data-ttu-id="4285d-266">Mögliche Werte finden Sie unter der **ReplicationHealth** -Eigenschaft der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="4285d-266">See the **ReplicationHealth** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

> [!Note]  
> <span data-ttu-id="4285d-267">Diese Eigenschaft ist ab Windows 8.1 veraltet. Verwenden Sie stattdessen " **replicationhealthex**".</span><span class="sxs-lookup"><span data-stu-id="4285d-267">This property is deprecated starting with Windows 8.1; instead, use the **ReplicationHealthEx**.</span></span>

 

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="4285d-268">**Nicht zutreffend** (0)</span><span class="sxs-lookup"><span data-stu-id="4285d-268">**Not applicable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

<span data-ttu-id="4285d-269">**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="4285d-269">**Ok** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="4285d-270">**Warnung** (2)</span><span class="sxs-lookup"><span data-stu-id="4285d-270">**Warning** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="4285d-271">**Kritisch** (3)</span><span class="sxs-lookup"><span data-stu-id="4285d-271">**Critical** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4285d-272">**Replicationhealthex**</span><span class="sxs-lookup"><span data-stu-id="4285d-272">**ReplicationHealthEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-273">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="4285d-273">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4285d-274">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4285d-275">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="4285d-275">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="4285d-276">Das Array der Replikations Integritäts Werte für die verschiedenen Replikations Beziehungen der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="4285d-276">The array of replication health values for the various replication relationships of the virtual machine.</span></span> <span data-ttu-id="4285d-277">Mögliche Werte finden Sie unter der **ReplicationHealth** -Eigenschaft der [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="4285d-277">See the **ReplicationHealth** property of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class for possible values.</span></span>

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="4285d-278">**Nicht zutreffend** (0)</span><span class="sxs-lookup"><span data-stu-id="4285d-278">**Not applicable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

<span data-ttu-id="4285d-279">**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="4285d-279">**Ok** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="4285d-280">**Warnung** (2)</span><span class="sxs-lookup"><span data-stu-id="4285d-280">**Warning** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="4285d-281">**Kritisch** (3)</span><span class="sxs-lookup"><span data-stu-id="4285d-281">**Critical** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4285d-282">**ReplicationMode**</span><span class="sxs-lookup"><span data-stu-id="4285d-282">**ReplicationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-283">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4285d-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4285d-284">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4285d-285">Der Replikationstyp für die virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="4285d-285">The replication type for the virtual machine.</span></span> <span data-ttu-id="4285d-286">Mögliche Werte finden Sie unter der **replicationmode** -Eigenschaft der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="4285d-286">See the **ReplicationMode** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="4285d-287">**Keine** (0)</span><span class="sxs-lookup"><span data-stu-id="4285d-287">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="4285d-288">**Primär** (1)</span><span class="sxs-lookup"><span data-stu-id="4285d-288">**Primary** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

<span data-ttu-id="4285d-289">**Replikat** (2)</span><span class="sxs-lookup"><span data-stu-id="4285d-289">**Replica** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

<span data-ttu-id="4285d-290">**Test Replikat** (3)</span><span class="sxs-lookup"><span data-stu-id="4285d-290">**Test Replica** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>

<span data-ttu-id="4285d-291">**Erweitertes Replikat** (4)</span><span class="sxs-lookup"><span data-stu-id="4285d-291">**Extended Replica** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4285d-292">**ReplicationProviderId**</span><span class="sxs-lookup"><span data-stu-id="4285d-292">**ReplicationProviderId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-293">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="4285d-293">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4285d-294">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4285d-295">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="4285d-295">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="4285d-296">Für den primären oder erweiterten virtuellen Replikat Computer ist dies die primäre Replikations Anbieter-ID.</span><span class="sxs-lookup"><span data-stu-id="4285d-296">For the primary or extended replica virtual machine, this is the primary replication provider ID.</span></span> <span data-ttu-id="4285d-297">Bei einem virtuellen Replikat Computer und bei aktivierter erweiterter Replikation ist dies die Anbieter-ID für die erweiterte Beziehung.</span><span class="sxs-lookup"><span data-stu-id="4285d-297">For a replica virtual machine and if extended replication is enabled, this is the provider ID for extended relationship.</span></span>

<span data-ttu-id="4285d-298">**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4285d-298">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="4285d-299">**ReplicationState**</span><span class="sxs-lookup"><span data-stu-id="4285d-299">**ReplicationState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-300">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4285d-300">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4285d-301">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4285d-302">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**MSVM \_ SummaryInformation**.**Replicationstateex**")</span><span class="sxs-lookup"><span data-stu-id="4285d-302">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**Msvm\_SummaryInformation**.**ReplicationStateEx**")</span></span>
</dt> </dl>

<span data-ttu-id="4285d-303">Der Replikations Status für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="4285d-303">The replication state for the virtual machine.</span></span> <span data-ttu-id="4285d-304">Mögliche Werte finden Sie unter der **replicationstate** -Eigenschaft der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="4285d-304">See the **ReplicationState** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

> [!Note]  
> <span data-ttu-id="4285d-305">Diese Eigenschaft ist ab Windows 8.1 veraltet. Verwenden Sie stattdessen **replicationstateex**.</span><span class="sxs-lookup"><span data-stu-id="4285d-305">This property is deprecated starting with Windows 8.1; instead, use the **ReplicationStateEx**.</span></span>

 

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4285d-306">**Deaktiviert** (0)</span><span class="sxs-lookup"><span data-stu-id="4285d-306">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="4285d-307">**Bereit für Replikation** (1)</span><span class="sxs-lookup"><span data-stu-id="4285d-307">**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="4285d-308">**Warten auf Abschluss der ersten Replikation** (2)</span><span class="sxs-lookup"><span data-stu-id="4285d-308">**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="4285d-309">**Replizieren** (3)</span><span class="sxs-lookup"><span data-stu-id="4285d-309">**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="4285d-310">**Synchronisierungs Replikation beendet** (4)</span><span class="sxs-lookup"><span data-stu-id="4285d-310">**Synced replication complete** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="4285d-311">**Wieder hergestellt** (5)</span><span class="sxs-lookup"><span data-stu-id="4285d-311">**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="4285d-312">Commit **ausgeführt (6** )</span><span class="sxs-lookup"><span data-stu-id="4285d-312">**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="4285d-313">Angeh **alten (7** )</span><span class="sxs-lookup"><span data-stu-id="4285d-313">**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="4285d-314">**Kritisch** (8)</span><span class="sxs-lookup"><span data-stu-id="4285d-314">**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="4285d-315">**Warten auf den Start der erneuten Synchronisierung** (9)</span><span class="sxs-lookup"><span data-stu-id="4285d-315">**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="4285d-316">**Neusynchronisierung** (10)</span><span class="sxs-lookup"><span data-stu-id="4285d-316">**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span data-ttu-id="4285d-317">**Neusynchronisierung** angehalten (11)</span><span class="sxs-lookup"><span data-stu-id="4285d-317">**Resynchronization suspended** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span data-ttu-id="4285d-318">**Failover** wird ausgeführt (12)</span><span class="sxs-lookup"><span data-stu-id="4285d-318">**Failover in progress** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4285d-319">**Replicationstateex**</span><span class="sxs-lookup"><span data-stu-id="4285d-319">**ReplicationStateEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-320">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="4285d-320">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4285d-321">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4285d-322">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="4285d-322">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="4285d-323">Das Array von Replikations Zustands Werten für die verschiedenen Replikations Beziehungen der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="4285d-323">The array of replication state values for the various replication relationships of the virtual machine.</span></span> <span data-ttu-id="4285d-324">Mögliche Werte finden Sie unter der **replicationstate** -Eigenschaft der [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="4285d-324">See the **ReplicationState** property of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class for possible values.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4285d-325"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (0)</span><span class="sxs-lookup"><span data-stu-id="4285d-325"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="4285d-326"><span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Bereit für Replikation** (1)</span><span class="sxs-lookup"><span data-stu-id="4285d-326"><span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="4285d-327"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Warten auf Abschluss der ersten Replikation** (2)</span><span class="sxs-lookup"><span data-stu-id="4285d-327"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="4285d-328"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replizieren** (3)</span><span class="sxs-lookup"><span data-stu-id="4285d-328"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="4285d-329"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synchronisierungs Replikation beendet** (4)</span><span class="sxs-lookup"><span data-stu-id="4285d-329"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synced replication complete** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="4285d-330"><span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Wieder hergestellt** (5)</span><span class="sxs-lookup"><span data-stu-id="4285d-330"><span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="4285d-331"><span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>Commit **ausgeführt (6** )</span><span class="sxs-lookup"><span data-stu-id="4285d-331"><span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="4285d-332"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>Angeh **alten (7** )</span><span class="sxs-lookup"><span data-stu-id="4285d-332"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="4285d-333"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Kritisch** (8)</span><span class="sxs-lookup"><span data-stu-id="4285d-333"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="4285d-334"><span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**Warten auf den Start der erneuten Synchronisierung** (9)</span><span class="sxs-lookup"><span data-stu-id="4285d-334"><span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="4285d-335"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Neusynchronisierung** (10)</span><span class="sxs-lookup"><span data-stu-id="4285d-335"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span data-ttu-id="4285d-336"><span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Neusynchronisierung** angehalten (11)</span><span class="sxs-lookup"><span data-stu-id="4285d-336"><span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Resynchronization suspended** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span data-ttu-id="4285d-337"><span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Failover** wird ausgeführt (12)</span><span class="sxs-lookup"><span data-stu-id="4285d-337"><span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Failover in progress** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

<span data-ttu-id="4285d-338"><span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Failback** wird ausgeführt (13)</span><span class="sxs-lookup"><span data-stu-id="4285d-338"><span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Failback in progress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

<span data-ttu-id="4285d-339"><span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Failback ist beendet** (14)</span><span class="sxs-lookup"><span data-stu-id="4285d-339"><span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Failback complete** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>

<span data-ttu-id="4285d-340"><span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>Datenträger **Update läuft** (15)</span><span class="sxs-lookup"><span data-stu-id="4285d-340"><span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**Disk update in progress** (15)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="4285d-341">In Windows 10, Version 1703 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4285d-341">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>

<span data-ttu-id="4285d-342"><span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>Datenträger **Update kritisch** (16)</span><span class="sxs-lookup"><span data-stu-id="4285d-342"><span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**Disk update critical** (16)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="4285d-343">In Windows 10, Version 1703 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4285d-343">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4285d-344"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (17)</span><span class="sxs-lookup"><span data-stu-id="4285d-344"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (17)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="4285d-345">In Windows 10, Version 1703 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4285d-345">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>

<span data-ttu-id="4285d-346"><span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Repurpose Replication in Progress** (18)</span><span class="sxs-lookup"><span data-stu-id="4285d-346"><span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Repurpose replication in progress** (18)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="4285d-347">In Windows 10, Version 1703 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4285d-347">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>

<span data-ttu-id="4285d-348"><span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Vorbereitet für Synchronisierungs Replikation** (19)</span><span class="sxs-lookup"><span data-stu-id="4285d-348"><span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Prepared for sync replication** (19)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="4285d-349">In Windows 10, Version 1703 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4285d-349">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>

<span data-ttu-id="4285d-350"><span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Vorbereitet für Gruppen umgekehrte Replikation** (20)</span><span class="sxs-lookup"><span data-stu-id="4285d-350"><span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Prepared for group reverse replication** (20)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="4285d-351">In Windows 10, Version 1703 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4285d-351">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>

<span data-ttu-id="4285d-352"><span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Firedrill läuft** (21)</span><span class="sxs-lookup"><span data-stu-id="4285d-352"><span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Firedrill in progress** (21)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="4285d-353">In Windows 10, Version 1703 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4285d-353">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4285d-354">**Geschützt**</span><span class="sxs-lookup"><span data-stu-id="4285d-354">**Shielded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-355">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4285d-355">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4285d-356">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4285d-357">Gibt an, ob der Schutz für die virtuelle Maschine konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="4285d-357">Indicates whether or not shielding is configured for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="4285d-358">In Windows 10, Version 1703 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4285d-358">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="4285d-359">**Momentaufnahmen**</span><span class="sxs-lookup"><span data-stu-id="4285d-359">**Snapshots**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-360">Datentyp: **CIM \_ virtualsystemsettingdata** -Array</span><span class="sxs-lookup"><span data-stu-id="4285d-360">Data type: **CIM\_VirtualSystemSettingData** array</span></span>
</dt> <dt>

<span data-ttu-id="4285d-361">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4285d-362">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="4285d-362">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="4285d-363">Ein Array von [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) -Instanzen, die die Momentaufnahmen für den virtuellen Computer darstellen.</span><span class="sxs-lookup"><span data-stu-id="4285d-363">An array of [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) instances that represent the snapshots for the virtual machine.</span></span> <span data-ttu-id="4285d-364">Diese Eigenschaft ist für Instanzen von **MSVM \_ SummaryInformation** , die eine Momentaufnahme eines virtuellen Computers darstellen, ungültig.</span><span class="sxs-lookup"><span data-stu-id="4285d-364">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="4285d-365">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="4285d-365">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-366">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="4285d-366">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4285d-367">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4285d-368">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="4285d-368">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="4285d-369">Zeichen folgen, die die entsprechenden **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="4285d-369">Strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="4285d-370">Dies entspricht der Eigenschaft **Status Beschreibungen** der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="4285d-370">This corresponds to the **StatusDescriptions** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="4285d-371">**Austauschen von Dateien**</span><span class="sxs-lookup"><span data-stu-id="4285d-371">**SwapFilesInUse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-372">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4285d-372">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4285d-373">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4285d-374">Gibt an, ob Paging auf zweiter Ebene aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="4285d-374">Indicates whether second level paging is active.</span></span> <span data-ttu-id="4285d-375">Enthält **true** , wenn Paging auf zweiter Ebene aktiv ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="4285d-375">Contains **True** if second level paging is active or **False** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="4285d-376">**Testreplicasystem**</span><span class="sxs-lookup"><span data-stu-id="4285d-376">**TestReplicaSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-377">Datentyp: **CIM \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="4285d-377">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="4285d-378">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4285d-379">Verweis auf eine [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Instanz, die den virtuellen Computer des virtuellen Computers für den virtuellen Computer darstellt.</span><span class="sxs-lookup"><span data-stu-id="4285d-379">Reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the test replica virtual machine for the virtual machine.</span></span> <span data-ttu-id="4285d-380">Diese Eigenschaft ist für Instanzen von **MSVM \_ SummaryInformation** , die eine Momentaufnahme eines virtuellen Computers darstellen, ungültig.</span><span class="sxs-lookup"><span data-stu-id="4285d-380">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="4285d-381">**Thumbnailimage**</span><span class="sxs-lookup"><span data-stu-id="4285d-381">**ThumbnailImage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-382">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="4285d-382">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="4285d-383">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4285d-384">**Qualifizierer: octetstring**, [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**MSVM \_ SummaryInformation**.**ThumbnailImageWidth**","**MSVM \_ SummaryInformation**.**Thumbnailimageheight**")</span><span class="sxs-lookup"><span data-stu-id="4285d-384">Qualifiers: **OctetString**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm\_SummaryInformation**.**ThumbnailImageWidth**", "**Msvm\_SummaryInformation**.**ThumbnailImageHeight**")</span></span>
</dt> </dl>

<span data-ttu-id="4285d-385">Ein Array, das ein kleines Bild des Desktops für die Miniaturansicht des Desktops für den virtuellen Computer oder die Momentaufnahme im RGB565-Format enthält.</span><span class="sxs-lookup"><span data-stu-id="4285d-385">An array that contains a small, thumbnail-sized image of the desktop for the virtual machine or snapshot in RGB565 format.</span></span>

</dd> <dt>

<span data-ttu-id="4285d-386">**Thumbnailimageheight**</span><span class="sxs-lookup"><span data-stu-id="4285d-386">**ThumbnailImageHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-387">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4285d-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4285d-388">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4285d-389">Qualifizierer: [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**MSVM \_ SummaryInformation**.**Thumbnailimage**")</span><span class="sxs-lookup"><span data-stu-id="4285d-389">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm\_SummaryInformation**.**ThumbnailImage**")</span></span>
</dt> </dl>

<span data-ttu-id="4285d-390">Die Höhe des Bilds in der thumbnailimage-Eigenschaft in Pixel.</span><span class="sxs-lookup"><span data-stu-id="4285d-390">The height in pixels of the image in the ThumbnailImage property.</span></span>

> [!Note]  
> <span data-ttu-id="4285d-391">In Windows 10 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4285d-391">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="4285d-392">**ThumbnailImageWidth**</span><span class="sxs-lookup"><span data-stu-id="4285d-392">**ThumbnailImageWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-393">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4285d-393">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4285d-394">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4285d-395">Qualifizierer: [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**MSVM \_ SummaryInformation**.**Thumbnailimage**")</span><span class="sxs-lookup"><span data-stu-id="4285d-395">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm\_SummaryInformation**.**ThumbnailImage**")</span></span>
</dt> </dl>

<span data-ttu-id="4285d-396">Die Breite des Bilds in der thumbnailimage-Eigenschaft in Pixel.</span><span class="sxs-lookup"><span data-stu-id="4285d-396">The width in pixels of the image in the ThumbnailImage property.</span></span>

> [!Note]  
> <span data-ttu-id="4285d-397">In Windows 10 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4285d-397">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="4285d-398">**Betriebszeit**</span><span class="sxs-lookup"><span data-stu-id="4285d-398">**UpTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-399">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4285d-399">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4285d-400">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4285d-401">Die Zeitspanne seit dem letzten Starten des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="4285d-401">The amount of time since the virtual machine was last booted.</span></span> <span data-ttu-id="4285d-402">Diese Eigenschaft ist für Instanzen von **MSVM \_ SummaryInformation** , die eine Momentaufnahme eines virtuellen Computers darstellen, ungültig.</span><span class="sxs-lookup"><span data-stu-id="4285d-402">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="4285d-403">**Version**</span><span class="sxs-lookup"><span data-stu-id="4285d-403">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-404">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4285d-404">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4285d-405">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4285d-406">Die Version des virtuellen Systems im Format "Major. Minor", z. b. "2,0".</span><span class="sxs-lookup"><span data-stu-id="4285d-406">The version of the virtual system in a format of "major.minor", for example "2.0".</span></span>

> [!Note]  
> <span data-ttu-id="4285d-407">In Windows 10 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4285d-407">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="4285d-408">**Virtualswitchnames**</span><span class="sxs-lookup"><span data-stu-id="4285d-408">**VirtualSwitchNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-409">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="4285d-409">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4285d-410">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4285d-411">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="4285d-411">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="4285d-412">Zeichen folgen, die die anzeigen amen der virtuellen Switches angeben, mit denen der virtuelle Computer verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="4285d-412">Strings that specify the friendly names of the virtual switches the virtual machine is connected to.</span></span>

<span data-ttu-id="4285d-413">**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4285d-413">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="4285d-414">**VirtualSystemSubType**</span><span class="sxs-lookup"><span data-stu-id="4285d-414">**VirtualSystemSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4285d-415">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4285d-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4285d-416">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4285d-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4285d-417">Der Untertyp des virtuellen Systems.</span><span class="sxs-lookup"><span data-stu-id="4285d-417">The subtype of the virtual system.</span></span>

<span data-ttu-id="4285d-418">**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4285d-418">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

<span data-ttu-id="4285d-419">**Microsoft: Hyper-V: Untertyp: 1** ()</span><span class="sxs-lookup"><span data-stu-id="4285d-419">**Microsoft:Hyper-V:SubType:1** ()</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

<span data-ttu-id="4285d-420">**Microsoft: Hyper-V: Untertyp: 2** ()</span><span class="sxs-lookup"><span data-stu-id="4285d-420">**Microsoft:Hyper-V:SubType:2** ()</span></span>


<span data-ttu-id="4285d-421"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="4285d-421"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="4285d-422">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4285d-422">Remarks</span></span>

<span data-ttu-id="4285d-423">Der Zugriff auf die **MSVM-Klasse " \_ SummaryInformation** " kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="4285d-423">Access to the **Msvm\_SummaryInformation** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4285d-424">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="4285d-424">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="4285d-425">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4285d-425">Requirements</span></span>



| <span data-ttu-id="4285d-426">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4285d-426">Requirement</span></span> | <span data-ttu-id="4285d-427">Wert</span><span class="sxs-lookup"><span data-stu-id="4285d-427">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4285d-428">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4285d-428">Minimum supported client</span></span><br/> | <span data-ttu-id="4285d-429">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4285d-429">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4285d-430">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4285d-430">Minimum supported server</span></span><br/> | <span data-ttu-id="4285d-431">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4285d-431">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4285d-432">Namespace</span><span class="sxs-lookup"><span data-stu-id="4285d-432">Namespace</span></span><br/>                | <span data-ttu-id="4285d-433">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="4285d-433">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4285d-434">MOF</span><span class="sxs-lookup"><span data-stu-id="4285d-434">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4285d-435"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4285d-435"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4285d-436">DLL</span><span class="sxs-lookup"><span data-stu-id="4285d-436">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4285d-437"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4285d-437"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4285d-438">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4285d-438">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4285d-439">**MSVM \_ summaryinformationbase**</span><span class="sxs-lookup"><span data-stu-id="4285d-439">**Msvm\_SummaryInformationBase**</span></span>](msvm-summaryinformationbase.md)
</dt> <dt>

[<span data-ttu-id="4285d-440">Klassen des virtuellen Systems</span><span class="sxs-lookup"><span data-stu-id="4285d-440">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

