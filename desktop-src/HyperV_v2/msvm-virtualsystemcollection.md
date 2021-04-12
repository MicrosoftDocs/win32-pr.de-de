---
description: Stellt eine Sammlung virtueller Systeme dar.
ms.assetid: acf51beb-1103-43a4-8dc5-1a7f2a0482be
title: Msvm_VirtualSystemCollection-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemCollection
- Msvm_VirtualSystemCollection.CollectionID
- Msvm_VirtualSystemCollection.ElementName
- Msvm_VirtualSystemCollection.LastApplyConsistencyLevel
- Msvm_VirtualSystemCollection.LastApplyVirtualMachineIds
- Msvm_VirtualSystemCollection.LastApplyTime
- Msvm_VirtualSystemCollection.FailedOverReplicationType
- Msvm_VirtualSystemCollection.ReplicationMode
- Msvm_VirtualSystemCollection.ReplicationState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a9746356744f2743a8d6656ef4c61044223be113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393422"
---
# <a name="msvm_virtualsystemcollection-class"></a><span data-ttu-id="efdbd-103">MSVM \_ virtualsystemcollection-Klasse</span><span class="sxs-lookup"><span data-stu-id="efdbd-103">Msvm\_VirtualSystemCollection class</span></span>

<span data-ttu-id="efdbd-104">Stellt eine Sammlung virtueller Systeme dar.</span><span class="sxs-lookup"><span data-stu-id="efdbd-104">Represents a collection of virtual systems.</span></span>

<span data-ttu-id="efdbd-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="efdbd-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="efdbd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="efdbd-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemCollection : CIM_CollectionOfMSEs
{
  string   CollectionID;
  string   ElementName;
  uint16   LastApplyConsistencyLevel;
  String   LastApplyVirtualMachineIds[];
  DateTime LastApplyTime;
  uint16   FailedOverReplicationType;
  uint16   ReplicationMode;
  uint16   ReplicationState;
};
```

## <a name="members"></a><span data-ttu-id="efdbd-107">Member</span><span class="sxs-lookup"><span data-stu-id="efdbd-107">Members</span></span>

<span data-ttu-id="efdbd-108">Die **MSVM \_ virtualsystemcollection** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="efdbd-108">The **Msvm\_VirtualSystemCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="efdbd-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="efdbd-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="efdbd-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="efdbd-110">Properties</span></span>

<span data-ttu-id="efdbd-111">Die **MSVM \_ virtualsystemcollection** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="efdbd-111">The **Msvm\_VirtualSystemCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="efdbd-112">**Sammlungs**</span><span class="sxs-lookup"><span data-stu-id="efdbd-112">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efdbd-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="efdbd-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efdbd-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="efdbd-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efdbd-115">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionId"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="efdbd-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="efdbd-116">Die eindeutige Identifikation des Auflistungs Objekts.</span><span class="sxs-lookup"><span data-stu-id="efdbd-116">The unique identification of the collection object.</span></span>

</dd> <dt>

<span data-ttu-id="efdbd-117">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="efdbd-117">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efdbd-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="efdbd-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efdbd-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="efdbd-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efdbd-120">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Elementname")</span><span class="sxs-lookup"><span data-stu-id="efdbd-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="efdbd-121">Ein benutzerdefinierter Name für die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="efdbd-121">An user-defined name for the collection.</span></span> <span data-ttu-id="efdbd-122">Beachten Sie, dass dies nicht unbedingt eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="efdbd-122">Note this is not guaranteed to be unique.</span></span>

</dd> <dt>

<span data-ttu-id="efdbd-123">**Failedoverreplicationtype**</span><span class="sxs-lookup"><span data-stu-id="efdbd-123">**FailedOverReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efdbd-124">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="efdbd-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="efdbd-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="efdbd-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="efdbd-126">Typ des Failovers, der für die virtuelle System Sammlung ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="efdbd-126">Type of failover that was performed for the virtual system collection.</span></span>

> [!Note]  
> <span data-ttu-id="efdbd-127">Hinzugefügt in Windows 10, Version 1703.</span><span class="sxs-lookup"><span data-stu-id="efdbd-127">Added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="efdbd-128">**Keine** (0)</span><span class="sxs-lookup"><span data-stu-id="efdbd-128">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="efdbd-129">**Regulär** (1)</span><span class="sxs-lookup"><span data-stu-id="efdbd-129">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="efdbd-130">**Geplant** (2)</span><span class="sxs-lookup"><span data-stu-id="efdbd-130">**Planned** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="efdbd-131">**LastApplyConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="efdbd-131">**LastApplyConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efdbd-132">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="efdbd-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="efdbd-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="efdbd-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="efdbd-134">Die Konsistenz Ebene des zuletzt angewendeten Deltas.</span><span class="sxs-lookup"><span data-stu-id="efdbd-134">Consistency level of the last applied delta.</span></span>

> [!Note]  
> <span data-ttu-id="efdbd-135">Hinzugefügt in Windows 10, Version 1703.</span><span class="sxs-lookup"><span data-stu-id="efdbd-135">Added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="efdbd-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="efdbd-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="efdbd-137"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Anwendungs konsistent** (1)</span><span class="sxs-lookup"><span data-stu-id="efdbd-137"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Application Consistent** (1)</span></span>


</dt> <dd>

<span data-ttu-id="efdbd-138">Das zuletzt angewendete Delta zeigt einen Zeitpunkt an, zu dem sich das virtuelle System im Anwendungs konsistenten Zustand befunden hat.</span><span class="sxs-lookup"><span data-stu-id="efdbd-138">The last applied delta indicates a point in time when the virtual system was in application consistent state.</span></span>

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="efdbd-139"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Absturz konsistent** (2)</span><span class="sxs-lookup"><span data-stu-id="efdbd-139"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Crash Consistent** (2)</span></span>


</dt> <dd>

<span data-ttu-id="efdbd-140">Das zuletzt angewendete Delta zeigt einen Zeitpunkt an, zu dem sich das virtuelle System in einem Absturz konsistenten Zustand befunden hat.</span><span class="sxs-lookup"><span data-stu-id="efdbd-140">The last applied delta indicates a point in time when the virtual system was in crash consistent state.</span></span>

</dd> <dt>

<span id="Group_Crash_Consistent"></span><span id="group_crash_consistent"></span><span id="GROUP_CRASH_CONSISTENT"></span>

<span data-ttu-id="efdbd-141"><span id="Group_Crash_Consistent"></span><span id="group_crash_consistent"></span><span id="GROUP_CRASH_CONSISTENT"></span>**Gruppen Absturz konsistent** (3)</span><span class="sxs-lookup"><span data-stu-id="efdbd-141"><span id="Group_Crash_Consistent"></span><span id="group_crash_consistent"></span><span id="GROUP_CRASH_CONSISTENT"></span>**Group Crash Consistent** (3)</span></span>


</dt> <dd>

<span data-ttu-id="efdbd-142">Das zuletzt angewendete Delta gibt einen Zeitpunkt an, zu dem die Gruppe einen Absturz konsistenten Zustand hatte.</span><span class="sxs-lookup"><span data-stu-id="efdbd-142">The last applied delta indicates a point in time when the group was in crash consistent state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="efdbd-143">**Lastapplytime**</span><span class="sxs-lookup"><span data-stu-id="efdbd-143">**LastApplyTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efdbd-144">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="efdbd-144">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="efdbd-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="efdbd-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="efdbd-146">Der Zeitpunkt, zu dem die letzte Replikation auf die Wiederherstellung für die virtuelle System Sammlung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="efdbd-146">The time at which the last replication is applied on recovery for the virtual system collection.</span></span>

> [!Note]  
> <span data-ttu-id="efdbd-147">Hinzugefügt in Windows 10, Version 1703.</span><span class="sxs-lookup"><span data-stu-id="efdbd-147">Added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="efdbd-148">**Lastapplyvirtualmachineids**</span><span class="sxs-lookup"><span data-stu-id="efdbd-148">**LastApplyVirtualMachineIds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efdbd-149">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="efdbd-149">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="efdbd-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="efdbd-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="efdbd-151">Array von VM-IDs, die im letzten Apply-Cycle erfolgreich angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="efdbd-151">Array of Virtual Machine Ids which were successfully applied in last apply cycle.</span></span>

> [!Note]  
> <span data-ttu-id="efdbd-152">Hinzugefügt in Windows 10, Version 1703.</span><span class="sxs-lookup"><span data-stu-id="efdbd-152">Added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="efdbd-153">**ReplicationMode**</span><span class="sxs-lookup"><span data-stu-id="efdbd-153">**ReplicationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efdbd-154">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="efdbd-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="efdbd-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="efdbd-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="efdbd-156">Der Replikationstyp für die virtuelle System Sammlung.</span><span class="sxs-lookup"><span data-stu-id="efdbd-156">Replication type for the virtual system collection.</span></span>

> [!Note]  
> <span data-ttu-id="efdbd-157">Hinzugefügt in Windows 10, Version 1703.</span><span class="sxs-lookup"><span data-stu-id="efdbd-157">Added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="efdbd-158">**Keine** (0)</span><span class="sxs-lookup"><span data-stu-id="efdbd-158">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="efdbd-159">**Primär** (1)</span><span class="sxs-lookup"><span data-stu-id="efdbd-159">**Primary** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

<span data-ttu-id="efdbd-160">**Replikat** (2)</span><span class="sxs-lookup"><span data-stu-id="efdbd-160">**Replica** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

<span data-ttu-id="efdbd-161">**Test Replikat** (3)</span><span class="sxs-lookup"><span data-stu-id="efdbd-161">**Test Replica** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="efdbd-162">**ReplicationState**</span><span class="sxs-lookup"><span data-stu-id="efdbd-162">**ReplicationState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efdbd-163">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="efdbd-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="efdbd-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="efdbd-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="efdbd-165">Replikations Status für die virtuelle System Sammlung.</span><span class="sxs-lookup"><span data-stu-id="efdbd-165">Replication state for the virtual system collection.</span></span>

> [!Note]  
> <span data-ttu-id="efdbd-166">Hinzugefügt in Windows 10, Version 1703.</span><span class="sxs-lookup"><span data-stu-id="efdbd-166">Added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="efdbd-167">**Deaktiviert** (0)</span><span class="sxs-lookup"><span data-stu-id="efdbd-167">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="efdbd-168">**Bereit für Replikation** (1)</span><span class="sxs-lookup"><span data-stu-id="efdbd-168">**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="efdbd-169">**Warten auf Abschluss der ersten Replikation** (2)</span><span class="sxs-lookup"><span data-stu-id="efdbd-169">**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="efdbd-170">**Replizieren** (3)</span><span class="sxs-lookup"><span data-stu-id="efdbd-170">**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_initiated"></span><span id="failover_initiated"></span><span id="FAILOVER_INITIATED"></span>

<span data-ttu-id="efdbd-171">**Initiiertes Failover** (4)</span><span class="sxs-lookup"><span data-stu-id="efdbd-171">**Failover initiated** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="efdbd-172">**Wieder hergestellt** (5)</span><span class="sxs-lookup"><span data-stu-id="efdbd-172">**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="efdbd-173">Commit **ausgeführt (6** )</span><span class="sxs-lookup"><span data-stu-id="efdbd-173">**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="efdbd-174">Angeh **alten (7** )</span><span class="sxs-lookup"><span data-stu-id="efdbd-174">**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="efdbd-175">**Kritisch** (8)</span><span class="sxs-lookup"><span data-stu-id="efdbd-175">**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="efdbd-176">**Warten auf den Start der erneuten Synchronisierung** (9)</span><span class="sxs-lookup"><span data-stu-id="efdbd-176">**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="efdbd-177">**Neusynchronisierung** (10)</span><span class="sxs-lookup"><span data-stu-id="efdbd-177">**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned_failover_initiatedRepurpose_initiatedTest_failover_initiatedPartially_enabled"></span><span id="planned_failover_initiatedrepurpose_initiatedtest_failover_initiatedpartially_enabled"></span><span id="PLANNED_FAILOVER_INITIATEDREPURPOSE_INITIATEDTEST_FAILOVER_INITIATEDPARTIALLY_ENABLED"></span>

<span data-ttu-id="efdbd-178">**Geplantes Failover initiatedrepurpose initiatedtest Failover initiatedteilweise aktiviert** (11)</span><span class="sxs-lookup"><span data-stu-id="efdbd-178">**Planned failover initiatedRepurpose initiatedTest failover initiatedPartially enabled** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_disabled"></span><span id="partially_disabled"></span><span id="PARTIALLY_DISABLED"></span>

<span data-ttu-id="efdbd-179">**Teilweise deaktiviert** (12)</span><span class="sxs-lookup"><span data-stu-id="efdbd-179">**Partially disabled** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_recovered"></span><span id="partially_recovered"></span><span id="PARTIALLY_RECOVERED"></span>

<span data-ttu-id="efdbd-180">**Teilweise wieder hergestellt** (13)</span><span class="sxs-lookup"><span data-stu-id="efdbd-180">**Partially recovered** (13)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="efdbd-181">(14)</span><span class="sxs-lookup"><span data-stu-id="efdbd-181">(14)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="efdbd-182">(15)</span><span class="sxs-lookup"><span data-stu-id="efdbd-182">(15)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="efdbd-183">(16)</span><span class="sxs-lookup"><span data-stu-id="efdbd-183">(16)</span></span>


<span data-ttu-id="efdbd-184"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="efdbd-184"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="efdbd-185">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="efdbd-185">Requirements</span></span>



| <span data-ttu-id="efdbd-186">Anforderung</span><span class="sxs-lookup"><span data-stu-id="efdbd-186">Requirement</span></span> | <span data-ttu-id="efdbd-187">Wert</span><span class="sxs-lookup"><span data-stu-id="efdbd-187">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efdbd-188">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="efdbd-188">Minimum supported client</span></span><br/> | <span data-ttu-id="efdbd-189">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="efdbd-189">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="efdbd-190">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="efdbd-190">Minimum supported server</span></span><br/> | <span data-ttu-id="efdbd-191">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="efdbd-191">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="efdbd-192">Namespace</span><span class="sxs-lookup"><span data-stu-id="efdbd-192">Namespace</span></span><br/>                | <span data-ttu-id="efdbd-193">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="efdbd-193">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="efdbd-194">MOF</span><span class="sxs-lookup"><span data-stu-id="efdbd-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="efdbd-195"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="efdbd-195"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="efdbd-196">DLL</span><span class="sxs-lookup"><span data-stu-id="efdbd-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efdbd-197"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="efdbd-197"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="efdbd-198">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="efdbd-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efdbd-199">**CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="efdbd-199">**CIM\_CollectionOfMSEs**</span></span>](cim-collectionofmses.md)
</dt> </dl>

 

