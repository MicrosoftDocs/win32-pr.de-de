---
description: Beschreibt einen virtuellen Ressourcentyp, der für die Verwendung auf virtuellen Computern verfügbar ist.
ms.assetid: A93D990E-D921-4113-8D88-218D0F84EFA0
title: Msvm_ResourcePool-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePool
- Msvm_ResourcePool.InstanceID
- Msvm_ResourcePool.Caption
- Msvm_ResourcePool.Description
- Msvm_ResourcePool.ElementName
- Msvm_ResourcePool.InstallDate
- Msvm_ResourcePool.Name
- Msvm_ResourcePool.OperationalStatus
- Msvm_ResourcePool.StatusDescriptions
- Msvm_ResourcePool.Status
- Msvm_ResourcePool.HealthState
- Msvm_ResourcePool.CommunicationStatus
- Msvm_ResourcePool.DetailedStatus
- Msvm_ResourcePool.OperatingStatus
- Msvm_ResourcePool.PrimaryStatus
- Msvm_ResourcePool.PoolID
- Msvm_ResourcePool.Primordial
- Msvm_ResourcePool.Capacity
- Msvm_ResourcePool.Reserved
- Msvm_ResourcePool.ResourceType
- Msvm_ResourcePool.OtherResourceType
- Msvm_ResourcePool.ResourceSubType
- Msvm_ResourcePool.AllocationUnits
- Msvm_ResourcePool.ConsumedResourceUnits
- Msvm_ResourcePool.CurrentlyConsumedResource
- Msvm_ResourcePool.MaxConsumableResource
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7c45f67a3e1b7c2b4b5291b24beddcdd4cf5e964
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216574"
---
# <a name="msvm_resourcepool-class"></a><span data-ttu-id="7ba3d-103">MSVM \_ resourcepool-Klasse</span><span class="sxs-lookup"><span data-stu-id="7ba3d-103">Msvm\_ResourcePool class</span></span>

<span data-ttu-id="7ba3d-104">Beschreibt einen virtuellen Ressourcentyp, der für die Verwendung auf virtuellen Computern verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-104">Describes a type of virtual resource available for use in virtual machines.</span></span> <span data-ttu-id="7ba3d-105">Der Ressourcenpool aggregiert physische Ressourcen und wird zum Zuordnen von Ressourcen zu virtuellen Computern verwendet.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-105">The resource pool aggregates physical resources and is used to allocate resources to virtual machines.</span></span> <span data-ttu-id="7ba3d-106">In Hyper-V sind alle Ressourcenpools ursprünglicher, und es gibt genau einen Pool für jeden bestimmten Ressourcentyp, der einem virtuellen Computer zugewiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-106">In Hyper-V, all resource pools are primordial, and there is exactly one pool for each specific type of resource which may be allocated to a virtual machine.</span></span>

<span data-ttu-id="7ba3d-107">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ba3d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ba3d-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourcePool : CIM_ResourcePool
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

## <a name="members"></a><span data-ttu-id="7ba3d-109">Member</span><span class="sxs-lookup"><span data-stu-id="7ba3d-109">Members</span></span>

<span data-ttu-id="7ba3d-110">Die **MSVM \_ resourcepool** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7ba3d-110">The **Msvm\_ResourcePool** class has these types of members:</span></span>

-   [<span data-ttu-id="7ba3d-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7ba3d-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7ba3d-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7ba3d-112">Properties</span></span>

<span data-ttu-id="7ba3d-113">Die **MSVM \_ resourcepool** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-113">The **Msvm\_ResourcePool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7ba3d-114">**Zuordnung von Einheiten**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-114">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba3d-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ba3d-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ba3d-117">Die Zuordnungs Einheiten, die vom Ressourcenpool verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-117">The units of allocation used by the resource pool.</span></span> <span data-ttu-id="7ba3d-118">Diese Eigenschaft wird von [**CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85))geerbt und auf "Megabyte" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-118">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to "Megabyte".</span></span>

</dd> <dt>

<span data-ttu-id="7ba3d-119">**Capacity**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-119">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba3d-120">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ba3d-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ba3d-122">Der maximale Betrag (in Einheiten von " **Zuweisung**") der aktiven Reservierungen, die der Ressourcenpool unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-122">The maximum amount (in units of **AllocationUnits**) of active reservations that the resource pool can support.</span></span> <span data-ttu-id="7ba3d-123">Diese Eigenschaft wird von [**CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-123">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7ba3d-124">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba3d-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ba3d-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ba3d-127">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-127">A short description of the object.</span></span> <span data-ttu-id="7ba3d-128">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7ba3d-129">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-129">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba3d-130">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ba3d-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ba3d-132">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-132">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="7ba3d-133">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-133">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7ba3d-134">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-134">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="7ba3d-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-136"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-136"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-137"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-137"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-138"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-138"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-139"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-139"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-140"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-140"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-141"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="7ba3d-141"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="7ba3d-142">)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-142">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7ba3d-143">**Consumedresourceunits**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-143">**ConsumedResourceUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba3d-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ba3d-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ba3d-146">Gibt die Einheiten für die Eigenschaften " **maxconsumableresource** " und " **currentlyconsumedresource** " an.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-146">Specifies the units for the **MaxConsumableResource** and the **CurrentlyConsumedResource** properties.</span></span>

</dd> <dt>

<span data-ttu-id="7ba3d-147">**Currentlyconsumedresource**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-147">**CurrentlyConsumedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba3d-148">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-148">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ba3d-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ba3d-150">Gibt die Menge an Ressourcen an, die der Ressourcenpool aktuell für Consumer darstellt.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-150">Specifies the amount of resource that the resource pool currently presents to consumers.</span></span> <span data-ttu-id="7ba3d-151">Diese Eigenschaft unterscheidet sich von der **reservierten** Eigenschaft darin, dass Sie die Consumer-Ansicht der Ressource beschreibt, während die **reservierte** Eigenschaft die Producer-Ansicht der Ressource beschreibt.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-151">This property is different from the **Reserved** property in that it describes the consumers view of the resource, while the **Reserved** property describes the producers view of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="7ba3d-152">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-152">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba3d-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ba3d-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ba3d-155">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-155">A description of the object.</span></span> <span data-ttu-id="7ba3d-156">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7ba3d-157">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-157">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba3d-158">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ba3d-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ba3d-160">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-160">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="7ba3d-161">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7ba3d-162">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="7ba3d-163"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-163"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-164"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-164"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-165"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-165"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-166"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-166"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-167"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-167"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-168"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-168"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-169"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-169"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-170"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="7ba3d-170"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="7ba3d-171">)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-171">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7ba3d-172">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-172">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba3d-173">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ba3d-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ba3d-175">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-175">A display name for the object.</span></span> <span data-ttu-id="7ba3d-176">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-176">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7ba3d-177">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-177">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba3d-178">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ba3d-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ba3d-180">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-180">The current health of the element.</span></span> <span data-ttu-id="7ba3d-181">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-181">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7ba3d-182">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-182">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba3d-183">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-183">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ba3d-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ba3d-185">Das Datum und die Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-185">The date and time when the object was installed.</span></span> <span data-ttu-id="7ba3d-186">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-186">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="7ba3d-187">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-187">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7ba3d-188">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-188">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba3d-189">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ba3d-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-191">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-191">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="7ba3d-192">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-192">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="7ba3d-193">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-193">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7ba3d-194">**Maxconsumableresource**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-194">**MaxConsumableResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba3d-195">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-195">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-196">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ba3d-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ba3d-197">Gibt die maximale Menge an nutzbaren Ressourcen an, die der Ressourcenpool für Consumer aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-197">Specifies the maximum amount of consumable resource that the resource pool can present to consumers.</span></span> <span data-ttu-id="7ba3d-198">Diese Eigenschaft unterscheidet sich von der **Capacity** -Eigenschaft darin, dass Sie die Consumer-Ansicht der Ressource beschreibt, während die **Capacity** -Eigenschaft die Producer-Ansicht der Ressource beschreibt.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-198">This property is different from the **Capacity** property in that it describes the consumers view of the resource, while the **Capacity** property describes the producers view of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="7ba3d-199">**Name**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-199">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba3d-200">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-201">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ba3d-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ba3d-202">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-202">The label by which the object is known.</span></span> <span data-ttu-id="7ba3d-203">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-203">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7ba3d-204">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-204">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba3d-205">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-206">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ba3d-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ba3d-207">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-207">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="7ba3d-208">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-208">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7ba3d-209">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-209">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="7ba3d-210"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-210"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-211"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-211"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-212"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-212"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-213"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-213"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-214"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="7ba3d-214"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-215"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-215"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-216"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-216"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-217"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-217"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-218"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-218"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-219"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-219"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-220"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-220"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-221"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-221"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-222"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-222"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-223"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-223"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-224"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-224"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-225"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-225"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-226"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-226"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-228"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="7ba3d-228"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="7ba3d-229">)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-229">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7ba3d-230">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-230">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba3d-231">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="7ba3d-231">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-232">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ba3d-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-233">Qualifizierer: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="7ba3d-233">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="7ba3d-234">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-234">The current statuses of the object.</span></span> <span data-ttu-id="7ba3d-235">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-235">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="7ba3d-236">Wenn keine QoS-bezogenen Bedingungen erkannt wurden, wird der primäre Status (OperationalStatus \[ 0 \] ) auf OK (2) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-236">If no QoS related conditions have been detected, the primary status (OperationalStatus\[0\]) is set to OK (2).</span></span> <span data-ttu-id="7ba3d-237">Andernfalls wird der primäre Status auf "heruntergestuft" (3) festgelegt, und mindestens ein sekundärer Statuswert wird in das Array eingefügt, beginnend bei Index 1, der nach dieser Tabelle spezifischere Bedingungen meldet.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-237">Otherwise, the primary status is set to Degraded (3), and one or more secondary status values is filled in the array, starting at index 1, which report more specific conditions, according to this table.</span></span>



| <span data-ttu-id="7ba3d-238">Wert</span><span class="sxs-lookup"><span data-stu-id="7ba3d-238">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="7ba3d-239">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7ba3d-239">Description</span></span>                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ba3d-240"><span id="_Insufficient_Throughput___32788_"></span><span id="_insufficient_throughput___32788_"></span><span id="_INSUFFICIENT_THROUGHPUT___32788_"></span> Unzureichender Durchsatz (32788)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-240"><span id="_Insufficient_Throughput___32788_"></span><span id="_insufficient_throughput___32788_"></span><span id="_INSUFFICIENT_THROUGHPUT___32788_"></span> Insufficient Throughput  (32788)</span></span><br/> | <span data-ttu-id="7ba3d-241">Mindestens eine der vom Pool zugewiesenen virtuellen Datenträger meldet derzeit einen unzureichenden Durchsatz Status.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-241">At least one of the virtual disks allocated from the pool is currently reporting an  Insufficient Throughput  status.</span></span><br/> |



 

<span data-ttu-id="7ba3d-242">Der Hyper-V-WMI-Anbieter löst jedes Mal ein [**MSVM \_ storagealert**](msvm-storagealert.md) -Ereignis aus, wenn sich der OperationalStatus der **MSVM \_ resourcepool** -Klasse ändert.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-242">The Hyper-V WMI provider raises an [**Msvm\_StorageAlert**](msvm-storagealert.md) event each time the OperationalStatus of the **Msvm\_ResourcePool** class changes.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7ba3d-243">**OK** (2)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-243">**OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7ba3d-244">Herunter **gestuft (3** )</span><span class="sxs-lookup"><span data-stu-id="7ba3d-244">**Degraded** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="7ba3d-245">**Nicht BEHEB barer Fehler** (7)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-245">**Non-Recoverable Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7ba3d-246">**Kein Kontakt** (12)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-246">**No Contact** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="7ba3d-247">**Verlorene Kommunikation** (13)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-247">**Lost Communication** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>

<span data-ttu-id="7ba3d-248">**Protokoll** Konflikt (32775)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-248">**Protocol Mismatch** (32775)</span></span>


</dt> <dd></dd> <dt>

<span id="Insufficient_Throughput"></span><span id="insufficient_throughput"></span><span id="INSUFFICIENT_THROUGHPUT"></span>

<span data-ttu-id="7ba3d-249">**Unzureichender Durchsatz** (32788)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-249">**Insufficient Throughput** (32788)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7ba3d-250">**Otherresourcetype**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-250">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba3d-251">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-252">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ba3d-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ba3d-253">Eine Zeichenfolge, die den Ressourcentyp beschreibt, wenn ein klar definierter Wert nicht verfügbar ist und [**ResourceType**](msvm-processorpool.md) auf 0 ("Other") festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-253">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorpool.md) is set to 0 ("Other").</span></span> <span data-ttu-id="7ba3d-254">Diese Eigenschaft wird von [**CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85)) geerbt und ist auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-254">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)) and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7ba3d-255">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-255">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba3d-256">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-257">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ba3d-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ba3d-258">Auf diesen Wert wird von den [**CIM \_ resourcezugewiescationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) -Instanzen verwiesen, die von diesem Pool zugeordnet wurden.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-258">This value is referenced by the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) instances which were allocated from this pool.</span></span> <span data-ttu-id="7ba3d-259">Diese Eigenschaft wird von [**CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85))geerbt und ist immer auf "Microsoft:*GUID* \\ root" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-259">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is always set to "Microsoft:*GUID*\\Root".</span></span>

</dd> <dt>

<span data-ttu-id="7ba3d-260">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-260">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba3d-261">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-261">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-262">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ba3d-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ba3d-263">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-263">Provides high level status information.</span></span> <span data-ttu-id="7ba3d-264">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-264">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="7ba3d-265">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-265">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7ba3d-266">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-266">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="7ba3d-267"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-267"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-268"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-268"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-269"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="7ba3d-269"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-270"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-270"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-271"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-271"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-272"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="7ba3d-272"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="7ba3d-273">)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-273">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7ba3d-274">**Ursprünglich**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-274">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba3d-275">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="7ba3d-275">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-276">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ba3d-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ba3d-277">**True** , wenn dieser Ressourcenpool die Basis ist, aus der Ressourcen in der Aktivität der Ressourcenverwaltung gezeichnet und zurückgegeben werden. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-277">**True** if this resource pool is the base from which resources are drawn and returned in the activity of resource management; otherwise, **False**.</span></span> <span data-ttu-id="7ba3d-278">"Primordial" bedeutet, dass dieser Ressourcenpool von Consumern dieses Modells nicht erstellt oder gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-278">Being primordial means that this resource pool cannot be created or deleted by consumers of this model.</span></span> <span data-ttu-id="7ba3d-279">Andere Aktionen, die modelliert werden, können sich jedoch auf die Merkmale oder die Größe von ursprünglichen Ressourcenpools auswirken.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-279">However, other actions, modeled or not, may affect the characteristics or size of primordial resource pools.</span></span> <span data-ttu-id="7ba3d-280">Diese Eigenschaft wird von [**CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-280">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7ba3d-281">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-281">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba3d-282">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-282">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-283">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ba3d-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ba3d-284">Die aktuellen Reservierungen (in Einheiten von **allocationunits**) werden auf alle aktiven Zuweisungen aus diesem Pool verteilt.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-284">The current reservations (in units of **AllocationUnits**) spread across all active allocations from this pool.</span></span> <span data-ttu-id="7ba3d-285">In einer hierarchischen Konfiguration stellt dies die Summe aller aktuellen Reservierungen des untergeordneten Ressourcenpools dar.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-285">In a hierarchical configuration, this represents the sum of all descendant resource pool current reservations.</span></span> <span data-ttu-id="7ba3d-286">Diese Eigenschaft wird von [**CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-286">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7ba3d-287">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-287">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba3d-288">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-289">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ba3d-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ba3d-290">Eine Zeichenfolge, die einen Implementierungs spezifischen Untertyp für diesen Pool beschreibt.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-290">A string that describes an implementation specific sub-type for this pool.</span></span> <span data-ttu-id="7ba3d-291">Dies kann z. b. verwendet werden, um unterschiedliche Modelle desselben Ressourcentyps zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-291">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="7ba3d-292">Diese Eigenschaft wird von [**CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-292">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7ba3d-293">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-293">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba3d-294">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-294">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-295">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ba3d-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ba3d-296">Der Ressourcentyp, der von diesem Ressourcenpool möglicherweise zugeteilt wird.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-296">The type of resource this resource pool may allocate.</span></span> <span data-ttu-id="7ba3d-297">Diese Eigenschaft wird von [**CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85))geerbt und ist auf 4 ("Memory") festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-297">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to 4 ("Memory").</span></span>

</dd> <dt>

<span data-ttu-id="7ba3d-298">**Status**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-298">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba3d-299">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-300">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ba3d-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ba3d-301">Der aktuelle Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-301">The current status of the object.</span></span> <span data-ttu-id="7ba3d-302">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-302">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7ba3d-303">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-303">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba3d-304">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="7ba3d-304">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7ba3d-305">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ba3d-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ba3d-306">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-306">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="7ba3d-307">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-307">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7ba3d-308">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ba3d-308">Remarks</span></span>

<span data-ttu-id="7ba3d-309">Der Zugriff auf die **MSVM \_ resourcepool** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="7ba3d-309">Access to the **Msvm\_ResourcePool** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="7ba3d-310">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="7ba3d-310">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="7ba3d-311">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ba3d-311">Requirements</span></span>



| <span data-ttu-id="7ba3d-312">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7ba3d-312">Requirement</span></span> | <span data-ttu-id="7ba3d-313">Wert</span><span class="sxs-lookup"><span data-stu-id="7ba3d-313">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ba3d-314">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-314">Minimum supported client</span></span><br/> | <span data-ttu-id="7ba3d-315">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7ba3d-315">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7ba3d-316">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7ba3d-316">Minimum supported server</span></span><br/> | <span data-ttu-id="7ba3d-317">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7ba3d-317">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7ba3d-318">Namespace</span><span class="sxs-lookup"><span data-stu-id="7ba3d-318">Namespace</span></span><br/>                | <span data-ttu-id="7ba3d-319">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="7ba3d-319">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7ba3d-320">MOF</span><span class="sxs-lookup"><span data-stu-id="7ba3d-320">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7ba3d-321"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7ba3d-321"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7ba3d-322">DLL</span><span class="sxs-lookup"><span data-stu-id="7ba3d-322">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ba3d-323"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7ba3d-323"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7ba3d-324">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ba3d-324">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ba3d-325">**CIM- \_ resourcepool**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-325">**CIM\_ResourcePool**</span></span>](cim-resourcepool.md)
</dt> <dt>

<span data-ttu-id="7ba3d-326">[**CIM- \_ resourcepool**](/previous-versions//cc136903(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7ba3d-326">[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7ba3d-327">**MSVM- \_ resourcepool (v1)**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-327">**Msvm\_ResourcePool (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-resourcepool)
</dt> <dt>

[<span data-ttu-id="7ba3d-328">**MSVM \_ storagealert**</span><span class="sxs-lookup"><span data-stu-id="7ba3d-328">**Msvm\_StorageAlert**</span></span>](msvm-storagealert.md)
</dt> <dt>

[<span data-ttu-id="7ba3d-329">Ressourcen Verwaltungs Klassen</span><span class="sxs-lookup"><span data-stu-id="7ba3d-329">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

