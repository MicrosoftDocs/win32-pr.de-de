---
description: Stellt einen Non-Uniform Memory Access (NUMA)-Knoten eines virtuellen Systems dar.
ms.assetid: a2e9aa74-15e5-4a78-b7f8-ffe2883a31d0
title: Msvm_NumaNode-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_NumaNode
- Msvm_NumaNode.RequestStateChange
- Msvm_NumaNode.InstanceID
- Msvm_NumaNode.Caption
- Msvm_NumaNode.Description
- Msvm_NumaNode.ElementName
- Msvm_NumaNode.InstallDate
- Msvm_NumaNode.Name
- Msvm_NumaNode.OperationalStatus
- Msvm_NumaNode.StatusDescriptions
- Msvm_NumaNode.Status
- Msvm_NumaNode.HealthState
- Msvm_NumaNode.CommunicationStatus
- Msvm_NumaNode.DetailedStatus
- Msvm_NumaNode.OperatingStatus
- Msvm_NumaNode.PrimaryStatus
- Msvm_NumaNode.EnabledState
- Msvm_NumaNode.OtherEnabledState
- Msvm_NumaNode.RequestedState
- Msvm_NumaNode.EnabledDefault
- Msvm_NumaNode.TimeOfLastStateChange
- Msvm_NumaNode.AvailableRequestedStates
- Msvm_NumaNode.TransitioningToState
- Msvm_NumaNode.SystemCreationClassName
- Msvm_NumaNode.SystemName
- Msvm_NumaNode.CreationClassName
- Msvm_NumaNode.NodeID
- Msvm_NumaNode.NumberOfProcessorCores
- Msvm_NumaNode.NumberOfLogicalProcessors
- Msvm_NumaNode.CurrentlyConsumableMemoryBlocks
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4bdbd600cd4a78f66376f21ee264b2dfe9854147
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363391"
---
# <a name="msvm_numanode-class"></a><span data-ttu-id="d2a79-103">MSVM- \_ numanode-Klasse</span><span class="sxs-lookup"><span data-stu-id="d2a79-103">Msvm\_NumaNode class</span></span>

<span data-ttu-id="d2a79-104">Stellt einen Non-Uniform Memory Access (NUMA)-Knoten eines virtuellen Systems dar.</span><span class="sxs-lookup"><span data-stu-id="d2a79-104">Represents a Non-Uniform Memory Access (NUMA) node of a virtual system.</span></span>

<span data-ttu-id="d2a79-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d2a79-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2a79-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2a79-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_NumaNode : CIM_EnabledLogicalElement
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
  uint16   HealthState = 5;
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
  string   CreationClassName;
  string   NodeID;
  uint32   NumberOfProcessorCores;
  uint32   NumberOfLogicalProcessors;
  uint64   CurrentlyConsumableMemoryBlocks;
};
```

## <a name="members"></a><span data-ttu-id="d2a79-107">Member</span><span class="sxs-lookup"><span data-stu-id="d2a79-107">Members</span></span>

<span data-ttu-id="d2a79-108">Die **MSVM- \_ numanode** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d2a79-108">The **Msvm\_NumaNode** class has these types of members:</span></span>

-   [<span data-ttu-id="d2a79-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="d2a79-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="d2a79-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d2a79-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d2a79-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="d2a79-111">Methods</span></span>

<span data-ttu-id="d2a79-112">Die **MSVM- \_ numanode** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="d2a79-112">The **Msvm\_NumaNode** class has these methods.</span></span>



| <span data-ttu-id="d2a79-113">Methode</span><span class="sxs-lookup"><span data-stu-id="d2a79-113">Method</span></span>                 | <span data-ttu-id="d2a79-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2a79-114">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="d2a79-115">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="d2a79-115">**RequestStateChange**</span></span> | <span data-ttu-id="d2a79-116">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d2a79-116">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d2a79-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d2a79-117">Properties</span></span>

<span data-ttu-id="d2a79-118">Die **MSVM- \_ numanode** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d2a79-118">The **Msvm\_NumaNode** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d2a79-119">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="d2a79-119">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2a79-120">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="d2a79-120">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2a79-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2a79-122">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="d2a79-122">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="d2a79-123">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="d2a79-123">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d2a79-124">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d2a79-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2a79-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2a79-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2a79-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2a79-127">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="d2a79-127">A short description of the object.</span></span> <span data-ttu-id="d2a79-128">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d2a79-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2a79-129">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="d2a79-129">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2a79-130">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2a79-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2a79-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2a79-132">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="d2a79-132">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="d2a79-133">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="d2a79-133">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d2a79-134">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d2a79-134">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d2a79-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="d2a79-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-136"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="d2a79-136"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-137"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="d2a79-137"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-138"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="d2a79-138"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-139"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="d2a79-139"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-140"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="d2a79-140"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-141"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="d2a79-141"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d2a79-142">)</span><span class="sxs-lookup"><span data-stu-id="d2a79-142">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d2a79-143">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="d2a79-143">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2a79-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2a79-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2a79-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-146">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="d2a79-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d2a79-147">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="d2a79-147">The scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="d2a79-148">**Currentlyconsumablememoryblocks**</span><span class="sxs-lookup"><span data-stu-id="d2a79-148">**CurrentlyConsumableMemoryBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2a79-149">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d2a79-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2a79-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2a79-151">Die Anzahl der Speicherblöcke, die derzeit für die Verwendung durch virtuelle Maschinen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="d2a79-151">The number of memory blocks currently available for consumption by virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="d2a79-152">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d2a79-152">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2a79-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2a79-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2a79-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2a79-155">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="d2a79-155">A description of the object.</span></span> <span data-ttu-id="d2a79-156">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d2a79-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2a79-157">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="d2a79-157">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2a79-158">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2a79-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2a79-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2a79-160">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="d2a79-160">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="d2a79-161">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="d2a79-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d2a79-162">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d2a79-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d2a79-163"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="d2a79-163"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-164"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="d2a79-164"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-165"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="d2a79-165"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-166"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="d2a79-166"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-167"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="d2a79-167"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-168"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="d2a79-168"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-169"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="d2a79-169"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-170"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="d2a79-170"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d2a79-171">)</span><span class="sxs-lookup"><span data-stu-id="d2a79-171">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d2a79-172">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d2a79-172">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2a79-173">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2a79-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2a79-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2a79-175">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d2a79-175">A display name for the object.</span></span> <span data-ttu-id="d2a79-176">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d2a79-176">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2a79-177">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="d2a79-177">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2a79-178">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2a79-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2a79-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2a79-180">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="d2a79-180">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="d2a79-181">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="d2a79-181">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d2a79-182">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="d2a79-182">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2a79-183">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2a79-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2a79-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2a79-185">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="d2a79-185">The enabled and disabled states of an element.</span></span> <span data-ttu-id="d2a79-186">Sie kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben.</span><span class="sxs-lookup"><span data-stu-id="d2a79-186">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="d2a79-187">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="d2a79-187">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="d2a79-188">Wert</span><span class="sxs-lookup"><span data-stu-id="d2a79-188">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="d2a79-189">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d2a79-189">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="d2a79-190"><dt>**Unbekannter**</dt> Wert <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d2a79-190"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="d2a79-191">Der Zustand des Elements konnte nicht bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="d2a79-191">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="d2a79-192"><dt>**Sonstige**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d2a79-192"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="d2a79-193"><dt>**Aktiviert**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d2a79-193"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="d2a79-194">Das-Element wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d2a79-194">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="d2a79-195"><dt>**Deaktiviert**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d2a79-195"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="d2a79-196">Das Element ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d2a79-196">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="d2a79-197"><dt>4</dt> wird <dt>**heruntergefahren**</dt></span><span class="sxs-lookup"><span data-stu-id="d2a79-197"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="d2a79-198">Das Element wird gerade in den deaktivierten Zustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="d2a79-198">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="d2a79-199"><dt>**Nicht zutreffend**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="d2a79-199"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="d2a79-200">Das Element unterstützt das Aktivieren oder Deaktivieren des Elements nicht.</span><span class="sxs-lookup"><span data-stu-id="d2a79-200">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="d2a79-201"><dt>**Aktiviert, aber offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="d2a79-201"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="d2a79-202">Das Element kann Befehle abschließen und löscht alle neuen Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="d2a79-202">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="d2a79-203"><dt>**In Test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="d2a79-203"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="d2a79-204">Das-Element befindet sich in einem Testzustand.</span><span class="sxs-lookup"><span data-stu-id="d2a79-204">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="d2a79-205"><dt></dt> Verzögert <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="d2a79-205"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="d2a79-206">Das Element kann Befehle abschließen, aber alle neuen Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="d2a79-206">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="d2a79-207"><dt>**Inesce**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="d2a79-207"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="d2a79-208">Das-Element ist aktiviert, befindet sich jedoch in einem eingeschränkten Modus.</span><span class="sxs-lookup"><span data-stu-id="d2a79-208">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="d2a79-209">Das Verhalten des-Elements ähnelt dem aktivierten Status (2), aber es verarbeitet nur einen eingeschränkten Satz von Befehlen.</span><span class="sxs-lookup"><span data-stu-id="d2a79-209">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="d2a79-210">Alle anderen Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="d2a79-210">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="d2a79-211"><dt>**Start**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="d2a79-211"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="d2a79-212">Das Element wechselt in den Zustand "aktiviert" (2).</span><span class="sxs-lookup"><span data-stu-id="d2a79-212">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="d2a79-213">Neue Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="d2a79-213">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="d2a79-214">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="d2a79-214">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2a79-215">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2a79-215">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-216">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2a79-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2a79-217">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="d2a79-217">The current health of the element.</span></span> <span data-ttu-id="d2a79-218">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="d2a79-218">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="d2a79-219">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="d2a79-219">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="d2a79-220">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 5 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2a79-220">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="d2a79-221">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d2a79-221">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2a79-222">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="d2a79-222">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-223">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2a79-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2a79-224">Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="d2a79-224">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="d2a79-225">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d2a79-225">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2a79-226">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d2a79-226">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2a79-227">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2a79-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-228">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2a79-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-229">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="d2a79-229">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d2a79-230">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="d2a79-230">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d2a79-231">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d2a79-231">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2a79-232">**Name**</span><span class="sxs-lookup"><span data-stu-id="d2a79-232">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2a79-233">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2a79-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-234">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2a79-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2a79-235">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="d2a79-235">The label by which the object is known.</span></span> <span data-ttu-id="d2a79-236">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d2a79-236">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2a79-237">**NodeId**</span><span class="sxs-lookup"><span data-stu-id="d2a79-237">**NodeID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2a79-238">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2a79-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-239">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2a79-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-240">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d2a79-240">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d2a79-241">Der NUMA-Knoten Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="d2a79-241">The NUMA node identifier.</span></span>

</dd> <dt>

<span data-ttu-id="d2a79-242">**"Numoflogicalprocessor"**</span><span class="sxs-lookup"><span data-stu-id="d2a79-242">**NumberOfLogicalProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2a79-243">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d2a79-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-244">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2a79-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2a79-245">Die Gesamtanzahl der logischen Prozessorkerne in diesem Knoten.</span><span class="sxs-lookup"><span data-stu-id="d2a79-245">The total number of logical processor cores in this node.</span></span>

</dd> <dt>

<span data-ttu-id="d2a79-246">**NumberOfProcessorCores**</span><span class="sxs-lookup"><span data-stu-id="d2a79-246">**NumberOfProcessorCores**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2a79-247">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d2a79-247">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-248">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2a79-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2a79-249">Die Gesamtanzahl der Prozessorkerne in diesem NUMA-Knoten.</span><span class="sxs-lookup"><span data-stu-id="d2a79-249">The total number of processor cores in this NUMA node.</span></span> <span data-ttu-id="d2a79-250">Dies kann sich von der Anzahl der [**MSVM- \_ Prozessor**](msvm-processor.md) Objekte unterscheiden, die diesem Knoten zugeordnet sind, wenn die einzelnen Prozessorkerne mehrere computethreads unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d2a79-250">This may differ from the number of [**Msvm\_Processor**](msvm-processor.md) objects associated to this node if each processor core supports multiple compute threads.</span></span>

</dd> <dt>

<span data-ttu-id="d2a79-251">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="d2a79-251">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2a79-252">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2a79-252">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-253">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2a79-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2a79-254">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d2a79-254">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="d2a79-255">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="d2a79-255">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d2a79-256">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d2a79-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d2a79-257"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="d2a79-257"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-258"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="d2a79-258"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-259"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="d2a79-259"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-260"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="d2a79-260"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-261"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="d2a79-261"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-262"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="d2a79-262"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-263"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="d2a79-263"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-264"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="d2a79-264"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-265"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="d2a79-265"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-266"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="d2a79-266"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-267"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="d2a79-267"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-268"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="d2a79-268"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-269"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="d2a79-269"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-270"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="d2a79-270"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-271"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="d2a79-271"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-272"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="d2a79-272"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-273"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="d2a79-273"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-274"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="d2a79-274"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-275"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="d2a79-275"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d2a79-276">)</span><span class="sxs-lookup"><span data-stu-id="d2a79-276">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d2a79-277">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="d2a79-277">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2a79-278">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="d2a79-278">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-279">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2a79-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2a79-280">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="d2a79-280">The current statuses of the object.</span></span> <span data-ttu-id="d2a79-281">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d2a79-281">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2a79-282">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="d2a79-282">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2a79-283">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2a79-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-284">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2a79-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2a79-285">Der aktivierte oder deaktivierte Status des Elements, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d2a79-285">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="d2a79-286">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="d2a79-286">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="d2a79-287">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2a79-287">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d2a79-288">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="d2a79-288">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2a79-289">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2a79-289">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-290">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2a79-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2a79-291">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="d2a79-291">Provides high level status information.</span></span> <span data-ttu-id="d2a79-292">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d2a79-292">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="d2a79-293">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="d2a79-293">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d2a79-294">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d2a79-294">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d2a79-295"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="d2a79-295"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-296"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="d2a79-296"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-297"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="d2a79-297"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-298"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="d2a79-298"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-299"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="d2a79-299"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-300"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="d2a79-300"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d2a79-301">)</span><span class="sxs-lookup"><span data-stu-id="d2a79-301">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d2a79-302">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="d2a79-302">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2a79-303">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2a79-303">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-304">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2a79-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2a79-305">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="d2a79-305">The last requested or desired state for the element.</span></span> <span data-ttu-id="d2a79-306">Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d2a79-306">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="d2a79-307">Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuell aktivierten oder deaktivierten Zustände zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="d2a79-307">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="d2a79-308">Eine bestimmte Instanz von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) unterstützt möglicherweise nicht die **requestStateChange** -Methode.</span><span class="sxs-lookup"><span data-stu-id="d2a79-308">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="d2a79-309">Wenn dies auftritt, wird der Wert 12 (nicht zutreffend) verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2a79-309">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="d2a79-310">Diese Eigenschaft wird von **CIM \_ enabledlogicalelement** geerbt.</span><span class="sxs-lookup"><span data-stu-id="d2a79-310">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="d2a79-311">**Status**</span><span class="sxs-lookup"><span data-stu-id="d2a79-311">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2a79-312">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2a79-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-313">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2a79-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2a79-314">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2a79-314">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2a79-315">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="d2a79-315">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2a79-316">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="d2a79-316">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-317">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2a79-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2a79-318">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="d2a79-318">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="d2a79-319">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d2a79-319">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2a79-320">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="d2a79-320">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2a79-321">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2a79-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-322">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2a79-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-323">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**")</span><span class="sxs-lookup"><span data-stu-id="d2a79-323">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="d2a79-324">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="d2a79-324">The scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="d2a79-325">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="d2a79-325">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2a79-326">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2a79-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-327">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2a79-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-328">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ System**](cim-system.md).**Name**")</span><span class="sxs-lookup"><span data-stu-id="d2a79-328">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="d2a79-329">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="d2a79-329">The scoping system's name.</span></span>

</dd> <dt>

<span data-ttu-id="d2a79-330">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="d2a79-330">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2a79-331">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="d2a79-331">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-332">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2a79-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2a79-333">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="d2a79-333">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="d2a79-334">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf "Null" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2a79-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to "NULL".</span></span>

</dd> <dt>

<span data-ttu-id="d2a79-335">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="d2a79-335">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2a79-336">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2a79-336">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2a79-337">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2a79-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2a79-338">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="d2a79-338">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="d2a79-339">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="d2a79-339">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d2a79-340">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2a79-340">Requirements</span></span>



| <span data-ttu-id="d2a79-341">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2a79-341">Requirement</span></span> | <span data-ttu-id="d2a79-342">Wert</span><span class="sxs-lookup"><span data-stu-id="d2a79-342">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2a79-343">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d2a79-343">Minimum supported client</span></span><br/> | <span data-ttu-id="d2a79-344">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2a79-344">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d2a79-345">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d2a79-345">Minimum supported server</span></span><br/> | <span data-ttu-id="d2a79-346">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2a79-346">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d2a79-347">Namespace</span><span class="sxs-lookup"><span data-stu-id="d2a79-347">Namespace</span></span><br/>                | <span data-ttu-id="d2a79-348">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="d2a79-348">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d2a79-349">MOF</span><span class="sxs-lookup"><span data-stu-id="d2a79-349">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2a79-350"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d2a79-350"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2a79-351">DLL</span><span class="sxs-lookup"><span data-stu-id="d2a79-351">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2a79-352"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d2a79-352"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

