---
description: Enthält Informationen zu den synthetischen 3D-Grafik Verarbeitungseinheiten (GPUs), die auf dem Host System verfügbar sind.
ms.assetid: 771A42C3-4888-49DF-A389-161A2D0E3DBD
title: Msvm_Synth3dVideoPool-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synth3dVideoPool
- Msvm_Synth3dVideoPool.InstanceID
- Msvm_Synth3dVideoPool.Caption
- Msvm_Synth3dVideoPool.Description
- Msvm_Synth3dVideoPool.ElementName
- Msvm_Synth3dVideoPool.InstallDate
- Msvm_Synth3dVideoPool.Name
- Msvm_Synth3dVideoPool.OperationalStatus
- Msvm_Synth3dVideoPool.StatusDescriptions
- Msvm_Synth3dVideoPool.Status
- Msvm_Synth3dVideoPool.HealthState
- Msvm_Synth3dVideoPool.CommunicationStatus
- Msvm_Synth3dVideoPool.DetailedStatus
- Msvm_Synth3dVideoPool.OperatingStatus
- Msvm_Synth3dVideoPool.PrimaryStatus
- Msvm_Synth3dVideoPool.PoolID
- Msvm_Synth3dVideoPool.Primordial
- Msvm_Synth3dVideoPool.Capacity
- Msvm_Synth3dVideoPool.Reserved
- Msvm_Synth3dVideoPool.ResourceType
- Msvm_Synth3dVideoPool.OtherResourceType
- Msvm_Synth3dVideoPool.ResourceSubType
- Msvm_Synth3dVideoPool.AllocationUnits
- Msvm_Synth3dVideoPool.ConsumedResourceUnits
- Msvm_Synth3dVideoPool.CurrentlyConsumedResource
- Msvm_Synth3dVideoPool.MaxConsumableResource
- Msvm_Synth3dVideoPool.Is3dVideoSupported
- Msvm_Synth3dVideoPool.IsSLATCapable
- Msvm_Synth3dVideoPool.IsGPUCapable
- Msvm_Synth3dVideoPool.DirectXVersion
- Msvm_Synth3dVideoPool.RequiredMinimumDirectXVersion
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1afad0f1b2e80a747bb518cb3eafc75d494de62a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959399"
---
# <a name="msvm_synth3dvideopool-class"></a><span data-ttu-id="81959-103">MSVM \_ Synth3dVideoPool-Klasse</span><span class="sxs-lookup"><span data-stu-id="81959-103">Msvm\_Synth3dVideoPool class</span></span>

<span data-ttu-id="81959-104">Enthält Informationen zu den synthetischen 3D-Grafik Verarbeitungseinheiten (GPUs), die auf dem Host System verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="81959-104">Contains information about the synthetic 3-D video graphics processing units (GPUs) available on the host system.</span></span> <span data-ttu-id="81959-105">Diese Klasse wird nur für Host Systeme verwendet, von denen remotefx unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="81959-105">This class is only used with host systems that support RemoteFX.</span></span>

<span data-ttu-id="81959-106">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="81959-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="81959-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="81959-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Synth3dVideoPool : CIM_ResourcePool
{
  string   InstanceID;
  string   Caption = "3D Display Controller Resource Pool";
  string   Description = "Resource pool used to allocate synthetic 3D video controller resources to a virtual machine.";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[] = {"OK"};
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   PoolID;
  boolean  Primordial = True;
  uint64   Capacity;
  uint64   Reserved = 0;
  uint16   ResourceType;
  string   OtherResourceType;
  string   ResourceSubType = "Microsoft:Hyper-V:Synthetic 3D Display Controller";
  string   AllocationUnits = "count";
  string   ConsumedResourceUnits = "count";
  uint64   CurrentlyConsumedResource;
  uint64   MaxConsumableResource;
  boolean  Is3dVideoSupported;
  boolean  IsSLATCapable;
  boolean  IsGPUCapable;
  string   DirectXVersion;
  string   RequiredMinimumDirectXVersion;
};
```

## <a name="members"></a><span data-ttu-id="81959-108">Member</span><span class="sxs-lookup"><span data-stu-id="81959-108">Members</span></span>

<span data-ttu-id="81959-109">Die **MSVM \_ Synth3dVideoPool** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="81959-109">The **Msvm\_Synth3dVideoPool** class has these types of members:</span></span>

-   [<span data-ttu-id="81959-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="81959-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="81959-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="81959-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="81959-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="81959-112">Methods</span></span>

<span data-ttu-id="81959-113">Die **MSVM- \_ Synth3dVideoPool** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="81959-113">The **Msvm\_Synth3dVideoPool** class has these methods.</span></span>



| <span data-ttu-id="81959-114">Methode</span><span class="sxs-lookup"><span data-stu-id="81959-114">Method</span></span>                                                                                             | <span data-ttu-id="81959-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="81959-115">Description</span></span>                                                                               |
|:---------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81959-116">**Calculatevideomemoryrequirements**</span><span class="sxs-lookup"><span data-stu-id="81959-116">**CalculateVideoMemoryRequirements**</span></span>](msvm-synth3dvideopool-calculatevideomemoryrequirements.md) | <span data-ttu-id="81959-117">Berechnet die Menge an Video Arbeitsspeicher, der für einen virtuellen remotefx-Computer erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="81959-117">Calculates the amount of video memory required for a RemoteFX virtual machine.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="81959-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="81959-118">Properties</span></span>

<span data-ttu-id="81959-119">Die **MSVM- \_ Synth3dVideoPool** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="81959-119">The **Msvm\_Synth3dVideoPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="81959-120">**Zuordnung von Einheiten**</span><span class="sxs-lookup"><span data-stu-id="81959-120">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81959-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="81959-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81959-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81959-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81959-123">Die Zuordnungs Einheiten, die vom Ressourcenpool verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="81959-123">The units of allocation used by the resource pool.</span></span> <span data-ttu-id="81959-124">Diese Eigenschaft wird von [**CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="81959-124">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="81959-125">**Capacity**</span><span class="sxs-lookup"><span data-stu-id="81959-125">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81959-126">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="81959-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="81959-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81959-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81959-128">Der maximale Betrag (in Einheiten von " **Zuweisung**") der aktiven Reservierungen, die der Ressourcenpool unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="81959-128">The maximum amount (in units of **AllocationUnits**) of active reservations that the resource pool can support.</span></span> <span data-ttu-id="81959-129">Diese Eigenschaft wird von [**CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="81959-129">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="81959-130">**Caption**</span><span class="sxs-lookup"><span data-stu-id="81959-130">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81959-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="81959-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81959-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81959-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81959-133">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="81959-133">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="81959-134">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="81959-134">A short description of the object.</span></span> <span data-ttu-id="81959-135">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="81959-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="81959-136">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="81959-136">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81959-137">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81959-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81959-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81959-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81959-139">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="81959-139">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="81959-140">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="81959-140">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="81959-141">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="81959-141">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="81959-142"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="81959-142"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="81959-143"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="81959-143"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="81959-144"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="81959-144"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="81959-145"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="81959-145"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="81959-146"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="81959-146"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="81959-147"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="81959-147"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="81959-148"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="81959-148"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="81959-149">)</span><span class="sxs-lookup"><span data-stu-id="81959-149">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="81959-150">**Consumedresourceunits**</span><span class="sxs-lookup"><span data-stu-id="81959-150">**ConsumedResourceUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81959-151">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="81959-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81959-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81959-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81959-153">Gibt die Einheiten für die Eigenschaften " **maxconsumableresource** " und " **currentlyconsumedresource** " an.</span><span class="sxs-lookup"><span data-stu-id="81959-153">Specifies the units for the **MaxConsumableResource** and the **CurrentlyConsumedResource** properties.</span></span> <span data-ttu-id="81959-154">Diese Eigenschaft wird von [**CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="81959-154">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="81959-155">**Currentlyconsumedresource**</span><span class="sxs-lookup"><span data-stu-id="81959-155">**CurrentlyConsumedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81959-156">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="81959-156">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="81959-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81959-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81959-158">Gibt die Menge an Ressourcen an, die der Ressourcenpool aktuell für Consumer darstellt.</span><span class="sxs-lookup"><span data-stu-id="81959-158">Specifies the amount of resource that the resource pool currently presents to consumers.</span></span> <span data-ttu-id="81959-159">Diese Eigenschaft unterscheidet sich von der **reservierten** Eigenschaft darin, dass Sie die Consumer-Ansicht der Ressource beschreibt, während die **reservierte** Eigenschaft die Producer-Ansicht der Ressource beschreibt.</span><span class="sxs-lookup"><span data-stu-id="81959-159">This property is different from the **Reserved** property in that it describes the consumers view of the resource, while the **Reserved** property describes the producers view of the resource.</span></span> <span data-ttu-id="81959-160">Diese Eigenschaft wird von [**CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="81959-160">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="81959-161">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="81959-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81959-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="81959-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81959-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81959-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81959-164">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="81959-164">A description of the object.</span></span> <span data-ttu-id="81959-165">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="81959-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="81959-166">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="81959-166">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81959-167">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81959-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81959-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81959-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81959-169">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="81959-169">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="81959-170">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="81959-170">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="81959-171">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="81959-171">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="81959-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="81959-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="81959-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="81959-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="81959-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="81959-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="81959-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="81959-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="81959-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="81959-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="81959-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="81959-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="81959-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="81959-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="81959-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="81959-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="81959-180">)</span><span class="sxs-lookup"><span data-stu-id="81959-180">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="81959-181">**Directxversion**</span><span class="sxs-lookup"><span data-stu-id="81959-181">**DirectXVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81959-182">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="81959-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81959-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81959-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81959-184">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="81959-184">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="81959-185">Gibt die niedrigste Version von DirectX an, die von den Karten innerhalb des Ressourcenpools unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="81959-185">Specifies the lowest version of DirectX that is supported by the cards within the resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="81959-186">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="81959-186">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81959-187">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="81959-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81959-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81959-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81959-189">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="81959-189">A display name for the object.</span></span> <span data-ttu-id="81959-190">Mit dieser Eigenschaft kann jede Instanz zusätzlich zu ihren Schlüsseleigenschaften, Identitätsdaten und Beschreibungs Informationen einen anzeigen Amen definieren.</span><span class="sxs-lookup"><span data-stu-id="81959-190">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="81959-191">Die [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) -Eigenschaft der **CIM \_ ManagedSystemElement** -Klasse wird auch als Anzeige Name definiert, aber Sie wird häufig als ein Schlüssel eingestuft.</span><span class="sxs-lookup"><span data-stu-id="81959-191">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name, but it is often subclassed to be a Key.</span></span> <span data-ttu-id="81959-192">Es ist nicht sinnvoll, dass dieselbe Eigenschaft ohne Inkonsistenzen sowohl Identität als auch einen anzeigen Amen vermitteln kann.</span><span class="sxs-lookup"><span data-stu-id="81959-192">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="81959-193">Wenn [**Name**](msvm-keyboard.md) vorhanden und kein Schlüssel ist (z. b. für Instanzen von LogicalDevice), können dieselben Informationen in den Eigenschaften **Name** und **ElementName** vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="81959-193">Where [**Name**](msvm-keyboard.md) exists and is not a Key (such as for instances of LogicalDevice), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="81959-194">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="81959-194">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="81959-195">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="81959-195">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81959-196">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81959-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81959-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81959-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81959-198">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="81959-198">The current health of the element.</span></span> <span data-ttu-id="81959-199">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 5 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="81959-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="81959-200">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="81959-200">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81959-201">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="81959-201">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="81959-202">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81959-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81959-203">Das Datum und die Uhrzeit der Erstellung der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="81959-203">The date and time at which the virtual machine was created.</span></span> <span data-ttu-id="81959-204">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="81959-204">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="81959-205">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="81959-205">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81959-206">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="81959-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81959-207">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81959-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81959-208">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="81959-208">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="81959-209">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="81959-209">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="81959-210">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="81959-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="81959-211">**Is3dVideoSupported**</span><span class="sxs-lookup"><span data-stu-id="81959-211">**Is3dVideoSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81959-212">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="81959-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="81959-213">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81959-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81959-214">Gibt an, ob das Host System 3D-Videos unterstützt.</span><span class="sxs-lookup"><span data-stu-id="81959-214">Specifies whether 3-D video is supported by the host system.</span></span> <span data-ttu-id="81959-215">Enthält einen Wert ungleich 0 (null), wenn 3D-Videos unterstützt werden, andernfalls 0 (null).</span><span class="sxs-lookup"><span data-stu-id="81959-215">Contains a nonzero value if 3-D video is supported, or zero otherwise.</span></span> <span data-ttu-id="81959-216">Zur Unterstützung von 3D-Videos muss der remotefx-Host über slat (Second Level Address Translation)-Funktionen verfügen und über mindestens eine physische GPU verfügen, die remotefx unterstützt.</span><span class="sxs-lookup"><span data-stu-id="81959-216">To support 3-D video, the RemoteFX host must have second level address translation (SLAT) capabilities and have at least one physical GPU that supports RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="81959-217">**Isgpufähig**</span><span class="sxs-lookup"><span data-stu-id="81959-217">**IsGPUCapable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81959-218">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="81959-218">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="81959-219">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81959-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81959-220">Gibt an, ob der Host über GPUs verfügt, die remotefx unterstützen, und ob die DirectX-Versionen die Mindestanforderungen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="81959-220">Specifies whether the host has GPUs that support RemoteFX and whether their DirectX versions meet the minimum requirement.</span></span>

</dd> <dt>

<span data-ttu-id="81959-221">**Isslatfähig**</span><span class="sxs-lookup"><span data-stu-id="81959-221">**IsSLATCapable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81959-222">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="81959-222">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="81959-223">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81959-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81959-224">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("kein Wert")</span><span class="sxs-lookup"><span data-stu-id="81959-224">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="81959-225">Gibt an, ob der Host über eine slat (Second Level Address Translation)-fähige CPU verfügt.</span><span class="sxs-lookup"><span data-stu-id="81959-225">Specifies whether the host has a second level address translation (SLAT) capable CPU.</span></span>

> [!Note]  
> <span data-ttu-id="81959-226">Veraltet in Windows 10, Version 1703 und Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="81959-226">Deprecated in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="81959-227">**Maxconsumableresource**</span><span class="sxs-lookup"><span data-stu-id="81959-227">**MaxConsumableResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81959-228">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="81959-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="81959-229">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81959-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81959-230">Gibt die maximale Menge an nutzbaren Ressourcen an, die der Ressourcenpool für Consumer aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="81959-230">Specifies the maximum amount of consumable resource that the resource pool can present to consumers.</span></span> <span data-ttu-id="81959-231">Diese Eigenschaft unterscheidet sich von der **Capacity** -Eigenschaft darin, dass Sie die Consumer-Ansicht der Ressource beschreibt, während die **Capacity** -Eigenschaft die Producer-Ansicht der Ressource beschreibt.</span><span class="sxs-lookup"><span data-stu-id="81959-231">This property is different from the **Capacity** property in that it describes the consumers view of the resource, while the **Capacity** property describes the producers view of the resource.</span></span> <span data-ttu-id="81959-232">Diese Eigenschaft wird von [**CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="81959-232">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="81959-233">**Name**</span><span class="sxs-lookup"><span data-stu-id="81959-233">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81959-234">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="81959-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81959-235">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81959-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81959-236">Qualifizierer: **maxlen** (1024)</span><span class="sxs-lookup"><span data-stu-id="81959-236">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="81959-237">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="81959-237">The label by which the object is known.</span></span> <span data-ttu-id="81959-238">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="81959-238">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="81959-239">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="81959-239">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="81959-240">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="81959-240">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81959-241">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81959-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81959-242">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81959-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81959-243">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="81959-243">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="81959-244">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="81959-244">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="81959-245">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="81959-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="81959-246"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="81959-246"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="81959-247"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="81959-247"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="81959-248"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="81959-248"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="81959-249"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="81959-249"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="81959-250"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="81959-250"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="81959-251"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="81959-251"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="81959-252"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="81959-252"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="81959-253"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="81959-253"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="81959-254"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="81959-254"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="81959-255"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="81959-255"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="81959-256"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="81959-256"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="81959-257"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="81959-257"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="81959-258"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="81959-258"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="81959-259"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="81959-259"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="81959-260"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="81959-260"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="81959-261"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="81959-261"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="81959-262"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="81959-262"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="81959-263"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="81959-263"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="81959-264"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="81959-264"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="81959-265">)</span><span class="sxs-lookup"><span data-stu-id="81959-265">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="81959-266">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="81959-266">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81959-267">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="81959-267">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="81959-268">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81959-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81959-269">Der aktuelle Status des Elements.</span><span class="sxs-lookup"><span data-stu-id="81959-269">The current status of the element.</span></span> <span data-ttu-id="81959-270">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 2 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="81959-270">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 (OK).</span></span> <span data-ttu-id="81959-271">Hyper-V verwendet nur das erste Element dieses Arrays.</span><span class="sxs-lookup"><span data-stu-id="81959-271">Hyper-V will only ever use the first element of this array.</span></span>

</dd> <dt>

<span data-ttu-id="81959-272">**Otherresourcetype**</span><span class="sxs-lookup"><span data-stu-id="81959-272">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81959-273">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="81959-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81959-274">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81959-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81959-275">Eine Zeichenfolge, die den Ressourcentyp beschreibt, wenn ein klar definierter Wert nicht verfügbar ist und [**ResourceType**](msvm-processorpool.md) auf 0 ("Other") festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="81959-275">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorpool.md) is set to 0 ("Other").</span></span> <span data-ttu-id="81959-276">Diese Eigenschaft wird von [**CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85))geerbt und ist auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="81959-276">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="81959-277">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="81959-277">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81959-278">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="81959-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81959-279">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81959-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81959-280">Auf diesen Wert wird von den [**CIM \_ resourcezugewiescationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) -Instanzen verwiesen, die von diesem Pool zugeordnet wurden.</span><span class="sxs-lookup"><span data-stu-id="81959-280">This value is referenced by the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) instances which were allocated from this pool.</span></span> <span data-ttu-id="81959-281">Diese Eigenschaft wird von [**CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85))geerbt und ist immer auf "Microsoft:*GUID* \\ root" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="81959-281">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is always set to "Microsoft:*GUID*\\Root".</span></span>

</dd> <dt>

<span data-ttu-id="81959-282">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="81959-282">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81959-283">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81959-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81959-284">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81959-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81959-285">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="81959-285">Provides high level status information.</span></span> <span data-ttu-id="81959-286">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="81959-286">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="81959-287">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="81959-287">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="81959-288">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="81959-288">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="81959-289"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="81959-289"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="81959-290"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="81959-290"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="81959-291"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="81959-291"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="81959-292"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="81959-292"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="81959-293"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="81959-293"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="81959-294"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="81959-294"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="81959-295">)</span><span class="sxs-lookup"><span data-stu-id="81959-295">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="81959-296">**Ursprünglich**</span><span class="sxs-lookup"><span data-stu-id="81959-296">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81959-297">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="81959-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="81959-298">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81959-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81959-299">**True** , wenn dieser Ressourcenpool die Basis ist, aus der Ressourcen in der Aktivität der Ressourcenverwaltung gezeichnet und zurückgegeben werden. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="81959-299">**True** if this resource pool is the base from which resources are drawn and returned in the activity of resource management; otherwise, **False**.</span></span> <span data-ttu-id="81959-300">"Primordial" bedeutet, dass dieser Ressourcenpool von Consumern dieses Modells nicht erstellt oder gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="81959-300">Being primordial means that this resource pool cannot be created or deleted by consumers of this model.</span></span> <span data-ttu-id="81959-301">Andere Aktionen, die modelliert werden, können sich jedoch auf die Merkmale oder die Größe von ursprünglichen Ressourcenpools auswirken.</span><span class="sxs-lookup"><span data-stu-id="81959-301">However, other actions, modeled or not, may affect the characteristics or size of primordial resource pools.</span></span> <span data-ttu-id="81959-302">Diese Eigenschaft wird von [**CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="81959-302">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="81959-303">**Requirements dminimumdirectxversion**</span><span class="sxs-lookup"><span data-stu-id="81959-303">**RequiredMinimumDirectXVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81959-304">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="81959-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81959-305">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81959-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81959-306">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="81959-306">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="81959-307">Gibt die niedrigste Version von DirectX an, die für die Karten innerhalb des Ressourcenpools erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="81959-307">Specifies the lowest version of DirectX that is required by the cards within the resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="81959-308">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="81959-308">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81959-309">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="81959-309">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="81959-310">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81959-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81959-311">Die aktuellen Reservierungen (in Einheiten von **allocationunits**) werden auf alle aktiven Zuweisungen aus diesem Pool verteilt.</span><span class="sxs-lookup"><span data-stu-id="81959-311">The current reservations (in units of **AllocationUnits**) spread across all active allocations from this pool.</span></span> <span data-ttu-id="81959-312">In einer hierarchischen Konfiguration stellt dies die Summe aller aktuellen Reservierungen des untergeordneten Ressourcenpools dar.</span><span class="sxs-lookup"><span data-stu-id="81959-312">In a hierarchical configuration, this represents the sum of all descendant resource pool current reservations.</span></span> <span data-ttu-id="81959-313">Diese Eigenschaft wird von [**CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="81959-313">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="81959-314">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="81959-314">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81959-315">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="81959-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81959-316">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81959-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81959-317">Eine Zeichenfolge, die einen Implementierungs spezifischen Untertyp für diesen Pool beschreibt.</span><span class="sxs-lookup"><span data-stu-id="81959-317">A string that describes an implementation specific subtype for this pool.</span></span> <span data-ttu-id="81959-318">Dies kann z. b. verwendet werden, um unterschiedliche Modelle desselben Ressourcentyps zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="81959-318">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="81959-319">Diese Eigenschaft wird von [**CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="81959-319">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="81959-320">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="81959-320">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81959-321">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81959-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81959-322">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81959-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81959-323">Der Typ der Ressource, die dieser Ressourcenpool zuordnen kann.</span><span class="sxs-lookup"><span data-stu-id="81959-323">The type of resource this resource pool can allocate.</span></span> <span data-ttu-id="81959-324">Diese Eigenschaft wird von [**CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85))geerbt und ist immer auf 4 ("Memory") festgelegt.</span><span class="sxs-lookup"><span data-stu-id="81959-324">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is always set to 4 ("Memory").</span></span>

</dd> <dt>

<span data-ttu-id="81959-325">**Status**</span><span class="sxs-lookup"><span data-stu-id="81959-325">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81959-326">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="81959-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81959-327">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81959-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81959-328">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="81959-328">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="81959-329">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="81959-329">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81959-330">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="81959-330">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="81959-331">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="81959-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81959-332">Zeichen folgen, die die verschiedenen [**OperationalStatus**](msvm-bioselement.md) -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="81959-332">Strings that describe the various [**OperationalStatus**](msvm-bioselement.md) array values.</span></span> <span data-ttu-id="81959-333">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf "OK" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="81959-333">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span> <span data-ttu-id="81959-334">Hyper-V verwendet nur das erste Element dieses Arrays.</span><span class="sxs-lookup"><span data-stu-id="81959-334">Hyper-V will only ever use the first element of this array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="81959-335">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81959-335">Requirements</span></span>



| <span data-ttu-id="81959-336">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81959-336">Requirement</span></span> | <span data-ttu-id="81959-337">Wert</span><span class="sxs-lookup"><span data-stu-id="81959-337">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81959-338">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="81959-338">Minimum supported client</span></span><br/> | <span data-ttu-id="81959-339">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81959-339">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="81959-340">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="81959-340">Minimum supported server</span></span><br/> | <span data-ttu-id="81959-341">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81959-341">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="81959-342">Namespace</span><span class="sxs-lookup"><span data-stu-id="81959-342">Namespace</span></span><br/>                | <span data-ttu-id="81959-343">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="81959-343">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="81959-344">MOF</span><span class="sxs-lookup"><span data-stu-id="81959-344">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81959-345"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="81959-345"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="81959-346">DLL</span><span class="sxs-lookup"><span data-stu-id="81959-346">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81959-347"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="81959-347"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="81959-348">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81959-348">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81959-349">**CIM- \_ resourcepool**</span><span class="sxs-lookup"><span data-stu-id="81959-349">**CIM\_ResourcePool**</span></span>](cim-resourcepool.md)
</dt> </dl>

 

