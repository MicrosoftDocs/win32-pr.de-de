---
description: Aggregiert die Prozessorressourcen, die einem virtuellen Computer zugeordnet werden können.
ms.assetid: 73424568-fa6c-4ed8-9640-a67a6d2829f0
title: Msvm_ProcessorPool-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProcessorPool
- Msvm_ProcessorPool.InstanceID
- Msvm_ProcessorPool.Caption
- Msvm_ProcessorPool.Description
- Msvm_ProcessorPool.ElementName
- Msvm_ProcessorPool.InstallDate
- Msvm_ProcessorPool.Name
- Msvm_ProcessorPool.OperationalStatus
- Msvm_ProcessorPool.StatusDescriptions
- Msvm_ProcessorPool.Status
- Msvm_ProcessorPool.HealthState
- Msvm_ProcessorPool.CommunicationStatus
- Msvm_ProcessorPool.DetailedStatus
- Msvm_ProcessorPool.OperatingStatus
- Msvm_ProcessorPool.PrimaryStatus
- Msvm_ProcessorPool.PoolID
- Msvm_ProcessorPool.Primordial
- Msvm_ProcessorPool.Capacity
- Msvm_ProcessorPool.Reserved
- Msvm_ProcessorPool.ResourceType
- Msvm_ProcessorPool.OtherResourceType
- Msvm_ProcessorPool.ResourceSubType
- Msvm_ProcessorPool.AllocationUnits
- Msvm_ProcessorPool.ConsumedResourceUnits
- Msvm_ProcessorPool.CurrentlyConsumedResource
- Msvm_ProcessorPool.MaxConsumableResource
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 93927483c23147fd387e24cdc5a550a1771457cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358497"
---
# <a name="msvm_processorpool-class"></a><span data-ttu-id="980cb-103">MSVM \_ processorpool-Klasse</span><span class="sxs-lookup"><span data-stu-id="980cb-103">Msvm\_ProcessorPool class</span></span>

<span data-ttu-id="980cb-104">Aggregiert die Prozessorressourcen, die einem virtuellen Computer zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="980cb-104">Aggregates the processor resources that may be allocated to a virtual machine.</span></span>

<span data-ttu-id="980cb-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="980cb-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="980cb-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="980cb-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ProcessorPool : CIM_ResourcePool
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
  string   PoolID = "Microsoft:GUID\Root";
  boolean  Primordial = False;
  uint64   Capacity;
  uint64   Reserved;
  uint16   ResourceType = 4;
  string   OtherResourceType;
  string   ResourceSubType;
  string   AllocationUnits = "Megabyte";
  string   ConsumedResourceUnits = "count";
  uint64   CurrentlyConsumedResource;
  uint64   MaxConsumableResource;
};
```

## <a name="members"></a><span data-ttu-id="980cb-107">Member</span><span class="sxs-lookup"><span data-stu-id="980cb-107">Members</span></span>

<span data-ttu-id="980cb-108">Die **MSVM \_ processorpool** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="980cb-108">The **Msvm\_ProcessorPool** class has these types of members:</span></span>

-   [<span data-ttu-id="980cb-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="980cb-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="980cb-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="980cb-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="980cb-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="980cb-111">Methods</span></span>

<span data-ttu-id="980cb-112">Die **MSVM \_ processorpool** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="980cb-112">The **Msvm\_ProcessorPool** class has these methods.</span></span>



| <span data-ttu-id="980cb-113">Methode</span><span class="sxs-lookup"><span data-stu-id="980cb-113">Method</span></span>                                                                          | <span data-ttu-id="980cb-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="980cb-114">Description</span></span>                                           |
|:--------------------------------------------------------------------------------|:------------------------------------------------------|
| [<span data-ttu-id="980cb-115">**Calculatepossiblereserve**</span><span class="sxs-lookup"><span data-stu-id="980cb-115">**CalculatePossibleReserve**</span></span>](calculatepossiblereserve-msvm-processorpool.md) | <span data-ttu-id="980cb-116">Wird verwendet, um die tatsächliche Prozessor Reserve zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="980cb-116">Used to find the actual processor reserve.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="980cb-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="980cb-117">Properties</span></span>

<span data-ttu-id="980cb-118">Die **MSVM \_ processorpool** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="980cb-118">The **Msvm\_ProcessorPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="980cb-119">**Zuordnung von Einheiten**</span><span class="sxs-lookup"><span data-stu-id="980cb-119">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980cb-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="980cb-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980cb-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980cb-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980cb-122">Die Zuordnungs Einheiten, die vom Ressourcenpool verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="980cb-122">The units of allocation used by the resource pool.</span></span> <span data-ttu-id="980cb-123">Diese Eigenschaft wird von [**CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85))geerbt und auf "Megabyte" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="980cb-123">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to "Megabyte".</span></span>

</dd> <dt>

<span data-ttu-id="980cb-124">**Capacity**</span><span class="sxs-lookup"><span data-stu-id="980cb-124">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980cb-125">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="980cb-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="980cb-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980cb-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980cb-127">Der maximale Betrag (in Einheiten von " **Zuweisung**") der aktiven Reservierungen, die der Ressourcenpool unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="980cb-127">The maximum amount (in units of **AllocationUnits**) of active reservations that the resource pool can support.</span></span> <span data-ttu-id="980cb-128">Diese Eigenschaft wird von [**CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="980cb-128">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="980cb-129">**Caption**</span><span class="sxs-lookup"><span data-stu-id="980cb-129">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980cb-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="980cb-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980cb-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980cb-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980cb-132">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="980cb-132">A short description of the object.</span></span> <span data-ttu-id="980cb-133">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="980cb-133">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="980cb-134">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="980cb-134">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980cb-135">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="980cb-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="980cb-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980cb-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980cb-137">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="980cb-137">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="980cb-138">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="980cb-138">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="980cb-139">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="980cb-139">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="980cb-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="980cb-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-141"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="980cb-141"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-142"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="980cb-142"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-143"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="980cb-143"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-144"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="980cb-144"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-145"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="980cb-145"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-146"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="980cb-146"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="980cb-147">)</span><span class="sxs-lookup"><span data-stu-id="980cb-147">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="980cb-148">**Consumedresourceunits**</span><span class="sxs-lookup"><span data-stu-id="980cb-148">**ConsumedResourceUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980cb-149">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="980cb-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980cb-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980cb-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980cb-151">Gibt die Einheiten für die Eigenschaften " **maxconsumableresource** " und " **currentlyconsumedresource** " an.</span><span class="sxs-lookup"><span data-stu-id="980cb-151">Specifies the units for the **MaxConsumableResource** and the **CurrentlyConsumedResource** properties.</span></span> <span data-ttu-id="980cb-152">Diese Eigenschaft wird von [**CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="980cb-152">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="980cb-153">**Currentlyconsumedresource**</span><span class="sxs-lookup"><span data-stu-id="980cb-153">**CurrentlyConsumedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980cb-154">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="980cb-154">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="980cb-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980cb-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980cb-156">Gibt die Menge an Ressourcen an, die der Ressourcenpool aktuell für Consumer darstellt.</span><span class="sxs-lookup"><span data-stu-id="980cb-156">Specifies the amount of resource that the resource pool currently presents to consumers.</span></span> <span data-ttu-id="980cb-157">Diese Eigenschaft unterscheidet sich von der **reservierten** Eigenschaft darin, dass Sie die Consumer-Ansicht der Ressource beschreibt, während die **reservierte** Eigenschaft die Producer-Ansicht der Ressource beschreibt.</span><span class="sxs-lookup"><span data-stu-id="980cb-157">This property is different from the **Reserved** property in that it describes the consumers view of the resource, while the **Reserved** property describes the producers view of the resource.</span></span> <span data-ttu-id="980cb-158">Diese Eigenschaft wird von [**CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="980cb-158">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="980cb-159">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="980cb-159">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980cb-160">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="980cb-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980cb-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980cb-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980cb-162">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="980cb-162">A description of the object.</span></span> <span data-ttu-id="980cb-163">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="980cb-163">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="980cb-164">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="980cb-164">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980cb-165">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="980cb-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="980cb-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980cb-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980cb-167">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="980cb-167">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="980cb-168">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="980cb-168">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="980cb-169">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="980cb-169">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="980cb-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="980cb-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-171"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="980cb-171"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-172"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="980cb-172"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-173"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="980cb-173"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-174"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="980cb-174"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-175"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="980cb-175"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="980cb-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="980cb-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="980cb-178">)</span><span class="sxs-lookup"><span data-stu-id="980cb-178">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="980cb-179">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="980cb-179">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980cb-180">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="980cb-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980cb-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980cb-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980cb-182">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="980cb-182">A display name for the object.</span></span> <span data-ttu-id="980cb-183">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="980cb-183">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="980cb-184">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="980cb-184">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980cb-185">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="980cb-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="980cb-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980cb-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980cb-187">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="980cb-187">The current health of the element.</span></span> <span data-ttu-id="980cb-188">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="980cb-188">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="980cb-189">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="980cb-189">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980cb-190">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="980cb-190">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="980cb-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980cb-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980cb-192">Das Datum und die Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="980cb-192">The date and time when the object was installed.</span></span> <span data-ttu-id="980cb-193">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="980cb-193">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="980cb-194">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="980cb-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="980cb-195">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="980cb-195">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980cb-196">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="980cb-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980cb-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980cb-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="980cb-198">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="980cb-198">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="980cb-199">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="980cb-199">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="980cb-200">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="980cb-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="980cb-201">**Maxconsumableresource**</span><span class="sxs-lookup"><span data-stu-id="980cb-201">**MaxConsumableResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980cb-202">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="980cb-202">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="980cb-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980cb-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980cb-204">Gibt die maximale Menge an nutzbaren Ressourcen an, die der Ressourcenpool für Consumer aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="980cb-204">Specifies the maximum amount of consumable resource that the resource pool can present to consumers.</span></span> <span data-ttu-id="980cb-205">Diese Eigenschaft unterscheidet sich von der **Capacity** -Eigenschaft darin, dass Sie die Consumer-Ansicht der Ressource beschreibt, während die **Capacity** -Eigenschaft die Producer-Ansicht der Ressource beschreibt.</span><span class="sxs-lookup"><span data-stu-id="980cb-205">This property is different from the **Capacity** property in that it describes the consumers view of the resource, while the **Capacity** property describes the producers view of the resource.</span></span> <span data-ttu-id="980cb-206">Diese Eigenschaft wird von [**CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="980cb-206">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="980cb-207">**Name**</span><span class="sxs-lookup"><span data-stu-id="980cb-207">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980cb-208">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="980cb-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980cb-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980cb-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980cb-210">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="980cb-210">The label by which the object is known.</span></span> <span data-ttu-id="980cb-211">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="980cb-211">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="980cb-212">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="980cb-212">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980cb-213">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="980cb-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="980cb-214">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980cb-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980cb-215">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="980cb-215">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="980cb-216">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="980cb-216">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="980cb-217">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="980cb-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="980cb-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="980cb-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="980cb-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-220"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="980cb-220"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-221"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="980cb-221"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-222"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="980cb-222"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-223"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="980cb-223"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-224"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="980cb-224"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-225"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="980cb-225"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-226"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="980cb-226"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-227"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="980cb-227"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-228"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="980cb-228"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-229"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="980cb-229"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-230"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="980cb-230"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-231"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="980cb-231"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-232"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="980cb-232"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-233"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="980cb-233"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-234"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="980cb-234"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-235"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="980cb-235"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-236"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="980cb-236"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="980cb-237">)</span><span class="sxs-lookup"><span data-stu-id="980cb-237">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="980cb-238">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="980cb-238">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980cb-239">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="980cb-239">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="980cb-240">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980cb-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980cb-241">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="980cb-241">The current statuses of the object.</span></span> <span data-ttu-id="980cb-242">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="980cb-242">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="980cb-243">**Otherresourcetype**</span><span class="sxs-lookup"><span data-stu-id="980cb-243">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980cb-244">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="980cb-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980cb-245">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980cb-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980cb-246">Eine Zeichenfolge, die den Ressourcentyp beschreibt, wenn ein klar definierter Wert nicht verfügbar ist und **ResourceType** auf 0 ("Other") festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="980cb-246">A string that describes the resource type when a well-defined value is not available and **ResourceType** is set to 0 ("Other").</span></span> <span data-ttu-id="980cb-247">Diese Eigenschaft wird von [**CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85))geerbt und ist auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="980cb-247">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="980cb-248">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="980cb-248">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980cb-249">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="980cb-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980cb-250">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980cb-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980cb-251">Auf diesen Wert wird von den [**CIM \_ resourcezugewiescationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) -Instanzen verwiesen, die von diesem Pool zugeordnet wurden.</span><span class="sxs-lookup"><span data-stu-id="980cb-251">This value is referenced by the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) instances which were allocated from this pool.</span></span> <span data-ttu-id="980cb-252">Diese Eigenschaft wird von [**CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85))geerbt und ist immer auf "Microsoft:*GUID* \\ root" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="980cb-252">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is always set to "Microsoft:*GUID*\\Root".</span></span>

</dd> <dt>

<span data-ttu-id="980cb-253">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="980cb-253">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980cb-254">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="980cb-254">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="980cb-255">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980cb-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980cb-256">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="980cb-256">Provides high level status information.</span></span> <span data-ttu-id="980cb-257">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="980cb-257">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="980cb-258">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="980cb-258">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="980cb-259">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="980cb-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="980cb-260"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="980cb-260"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-261"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="980cb-261"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-262"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="980cb-262"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-263"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="980cb-263"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="980cb-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="980cb-265"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="980cb-265"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="980cb-266">)</span><span class="sxs-lookup"><span data-stu-id="980cb-266">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="980cb-267">**Ursprünglich**</span><span class="sxs-lookup"><span data-stu-id="980cb-267">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980cb-268">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="980cb-268">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="980cb-269">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980cb-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980cb-270">**True** , wenn dieser Ressourcenpool die Basis ist, aus der Ressourcen in der Aktivität der Ressourcenverwaltung gezeichnet und zurückgegeben werden. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="980cb-270">**True** if this resource pool is the base from which resources are drawn and returned in the activity of resource management; otherwise, **False**.</span></span> <span data-ttu-id="980cb-271">"Primordial" bedeutet, dass dieser Ressourcenpool von Consumern dieses Modells nicht erstellt oder gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="980cb-271">Being primordial means that this resource pool cannot be created or deleted by consumers of this model.</span></span> <span data-ttu-id="980cb-272">Andere Aktionen, die modelliert werden, können sich jedoch auf die Merkmale oder die Größe von ursprünglichen Ressourcenpools auswirken.</span><span class="sxs-lookup"><span data-stu-id="980cb-272">However, other actions, modeled or not, may affect the characteristics or size of primordial resource pools.</span></span> <span data-ttu-id="980cb-273">Diese Eigenschaft wird von [**CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="980cb-273">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="980cb-274">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="980cb-274">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980cb-275">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="980cb-275">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="980cb-276">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980cb-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980cb-277">Die aktuellen Reservierungen (in Einheiten von **allocationunits**) werden auf alle aktiven Zuweisungen aus diesem Pool verteilt.</span><span class="sxs-lookup"><span data-stu-id="980cb-277">The current reservations (in units of **AllocationUnits**) spread across all active allocations from this pool.</span></span> <span data-ttu-id="980cb-278">In einer hierarchischen Konfiguration stellt dies die Summe aller aktuellen Reservierungen des untergeordneten Ressourcenpools dar.</span><span class="sxs-lookup"><span data-stu-id="980cb-278">In a hierarchical configuration, this represents the sum of all descendant resource pool current reservations.</span></span> <span data-ttu-id="980cb-279">Diese Eigenschaft wird von [**CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="980cb-279">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="980cb-280">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="980cb-280">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980cb-281">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="980cb-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980cb-282">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980cb-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980cb-283">Eine Zeichenfolge, die einen Implementierungs spezifischen Untertyp für diesen Pool beschreibt.</span><span class="sxs-lookup"><span data-stu-id="980cb-283">A string that describes an implementation specific sub-type for this pool.</span></span> <span data-ttu-id="980cb-284">Dies kann z. b. verwendet werden, um unterschiedliche Modelle desselben Ressourcentyps zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="980cb-284">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="980cb-285">Diese Eigenschaft wird von [**CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="980cb-285">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="980cb-286">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="980cb-286">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980cb-287">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="980cb-287">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="980cb-288">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980cb-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980cb-289">Der Ressourcentyp, der von diesem Ressourcenpool möglicherweise zugeteilt wird.</span><span class="sxs-lookup"><span data-stu-id="980cb-289">The type of resource this resource pool may allocate.</span></span> <span data-ttu-id="980cb-290">Diese Eigenschaft wird von [**CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85))geerbt und ist auf 4 ("Memory") festgelegt.</span><span class="sxs-lookup"><span data-stu-id="980cb-290">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to 4 ("Memory").</span></span>

</dd> <dt>

<span data-ttu-id="980cb-291">**Status**</span><span class="sxs-lookup"><span data-stu-id="980cb-291">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980cb-292">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="980cb-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="980cb-293">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980cb-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980cb-294">Der aktuelle Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="980cb-294">The current status of the object.</span></span> <span data-ttu-id="980cb-295">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="980cb-295">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="980cb-296">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="980cb-296">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="980cb-297">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="980cb-297">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="980cb-298">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="980cb-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="980cb-299">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="980cb-299">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="980cb-300">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="980cb-300">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="980cb-301">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="980cb-301">Remarks</span></span>

<span data-ttu-id="980cb-302">Der Zugriff auf die **MSVM \_ processorpool** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="980cb-302">Access to the **Msvm\_ProcessorPool** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="980cb-303">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="980cb-303">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="980cb-304">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="980cb-304">Requirements</span></span>



| <span data-ttu-id="980cb-305">Anforderung</span><span class="sxs-lookup"><span data-stu-id="980cb-305">Requirement</span></span> | <span data-ttu-id="980cb-306">Wert</span><span class="sxs-lookup"><span data-stu-id="980cb-306">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="980cb-307">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="980cb-307">Minimum supported client</span></span><br/> | <span data-ttu-id="980cb-308">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="980cb-308">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="980cb-309">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="980cb-309">Minimum supported server</span></span><br/> | <span data-ttu-id="980cb-310">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="980cb-310">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="980cb-311">Namespace</span><span class="sxs-lookup"><span data-stu-id="980cb-311">Namespace</span></span><br/>                | <span data-ttu-id="980cb-312">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="980cb-312">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="980cb-313">MOF</span><span class="sxs-lookup"><span data-stu-id="980cb-313">MOF</span></span><br/>                      | <dl> <span data-ttu-id="980cb-314"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="980cb-314"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="980cb-315">DLL</span><span class="sxs-lookup"><span data-stu-id="980cb-315">DLL</span></span><br/>                      | <dl> <span data-ttu-id="980cb-316"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="980cb-316"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="980cb-317">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="980cb-317">See also</span></span>

<dl> <dt>

[<span data-ttu-id="980cb-318">**CIM- \_ resourcepool**</span><span class="sxs-lookup"><span data-stu-id="980cb-318">**CIM\_ResourcePool**</span></span>](cim-resourcepool.md)
</dt> <dt>

<span data-ttu-id="980cb-319">[**CIM- \_ resourcepool**](/previous-versions//cc136903(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="980cb-319">[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="980cb-320">Prozessor Klassen</span><span class="sxs-lookup"><span data-stu-id="980cb-320">Processor Classes</span></span>](processor-classes.md)
</dt> </dl>

 

