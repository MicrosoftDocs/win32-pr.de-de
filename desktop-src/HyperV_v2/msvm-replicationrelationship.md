---
description: Stellt den Replikations Status einer Replikations Beziehung dar
ms.assetid: F11EFF86-5CC9-4310-8254-B310C54B561D
title: Msvm_ReplicationRelationship-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationRelationship
- Msvm_ReplicationRelationship.InstanceID
- Msvm_ReplicationRelationship.ReplicationState
- Msvm_ReplicationRelationship.ReplicationHealth
- Msvm_ReplicationRelationship.FailedOverReplicationType
- Msvm_ReplicationRelationship.LastReplicationType
- Msvm_ReplicationRelationship.LastApplicationConsistentReplicationTime
- Msvm_ReplicationRelationship.LastReplicationTime
- Msvm_ReplicationRelationship.LastApplyTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 04665f96f4ec77501ee0b161d816c84943ca2c98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362263"
---
# <a name="msvm_replicationrelationship-class"></a><span data-ttu-id="9dfe0-103">MSVM \_ replicationrelationship-Klasse</span><span class="sxs-lookup"><span data-stu-id="9dfe0-103">Msvm\_ReplicationRelationship class</span></span>

<span data-ttu-id="9dfe0-104">Stellt den Replikations Status einer Replikations Beziehung dar</span><span class="sxs-lookup"><span data-stu-id="9dfe0-104">Represents replication status for a replication relationship.</span></span> <span data-ttu-id="9dfe0-105">Da für jeden virtuellen Replikat Computer mehrere Replizierungen möglich sind, können Sie diese Klasse verwenden, um jede Replikations Beziehung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-105">Because you can have multiple replications for each replica virtual machine, you can use this class to identify each replication relationship.</span></span>

<span data-ttu-id="9dfe0-106">Die folgende Syntax wird aus dem MOF-Code vereinfacht und enthält diese geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-106">The following syntax is simplified from MOF code and includes these inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dfe0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9dfe0-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationRelationship : CIM_ManagedSystemElement
{
  string   InstanceID;
  uint16   ReplicationState;
  uint16   ReplicationHealth;
  uint16   FailedOverReplicationType;
  uint16   LastReplicationType;
  datetime LastApplicationConsistentReplicationTime;
  datetime LastReplicationTime;
  datetime LastApplyTime;
};
```

## <a name="members"></a><span data-ttu-id="9dfe0-108">Member</span><span class="sxs-lookup"><span data-stu-id="9dfe0-108">Members</span></span>

<span data-ttu-id="9dfe0-109">Die **MSVM- \_ replicationrelationship** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9dfe0-109">The **Msvm\_ReplicationRelationship** class has these types of members:</span></span>

-   [<span data-ttu-id="9dfe0-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9dfe0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9dfe0-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9dfe0-111">Properties</span></span>

<span data-ttu-id="9dfe0-112">Die **MSVM- \_ replicationrelationship** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-112">The **Msvm\_ReplicationRelationship** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9dfe0-113">**Failedoverreplicationtype**</span><span class="sxs-lookup"><span data-stu-id="9dfe0-113">**FailedOverReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dfe0-114">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9dfe0-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9dfe0-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9dfe0-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9dfe0-116">Der Typ des Failovers, der für die Replikations Beziehung ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-116">The type of failover that was performed for the replication relationship.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="9dfe0-117">**Keine** (0)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-117">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="9dfe0-118">**Regulär** (1)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-118">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="9dfe0-119">**Anwendungs konsistent** (2)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-119">**Application consistent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="9dfe0-120">**Geplant** (3)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-120">**Planned** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9dfe0-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9dfe0-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dfe0-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9dfe0-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9dfe0-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9dfe0-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9dfe0-124">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")</span><span class="sxs-lookup"><span data-stu-id="9dfe0-124">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="9dfe0-125">Identifiziert die Replikations Beziehung.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-125">Identifies replication relationship.</span></span> <span data-ttu-id="9dfe0-126">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="9dfe0-127">Diese Eigenschaft hat folgendes Format:</span><span class="sxs-lookup"><span data-stu-id="9dfe0-127">This property has this format:</span></span>

<span data-ttu-id="9dfe0-128">**Microsoft: <vmid> \\ HVR \\<0/1>**</span><span class="sxs-lookup"><span data-stu-id="9dfe0-128">**Microsoft:<vmid>\\HVR\\<0/1>**</span></span>

<span data-ttu-id="9dfe0-129">0 gibt Primär und 1 die [Erweiterte Replikation](#extended-replication)an.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-129">0 indicates primary and 1 indicates [extended replication](#extended-replication).</span></span>

</dd> <dt>

<span data-ttu-id="9dfe0-130">**Lastapplicationkonsistentreplicationtime**</span><span class="sxs-lookup"><span data-stu-id="9dfe0-130">**LastApplicationConsistentReplicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dfe0-131">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="9dfe0-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9dfe0-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9dfe0-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9dfe0-133">Das Datum und die Uhrzeit, zu der die letzte Anwendungs konsistente Replikation bei der Wiederherstellung für die Replikations Beziehung empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-133">The date and time at which the last application consistent replication is received on recovery for the replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="9dfe0-134">**Lastapplytime**</span><span class="sxs-lookup"><span data-stu-id="9dfe0-134">**LastApplyTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dfe0-135">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="9dfe0-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9dfe0-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9dfe0-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9dfe0-137">Das Datum und die Uhrzeit, zu der die letzte Replikation bei der Wiederherstellung für die Replikations Beziehung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-137">The date and time at which the last replication is applied on recovery for the replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="9dfe0-138">**Lastreplicationtime**</span><span class="sxs-lookup"><span data-stu-id="9dfe0-138">**LastReplicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dfe0-139">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="9dfe0-139">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9dfe0-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9dfe0-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9dfe0-141">Das Datum und die Uhrzeit, zu der die letzte Replikation bei der Wiederherstellung für die Replikations Beziehung empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-141">The date and time at which the last replication is received on recovery for the replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="9dfe0-142">**Lastreplicationtype**</span><span class="sxs-lookup"><span data-stu-id="9dfe0-142">**LastReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dfe0-143">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9dfe0-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9dfe0-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9dfe0-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9dfe0-145">Der Typ der letzten Replikation, die für die Replikations Beziehung empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-145">The type of the last replication that was received for the replication relationship.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="9dfe0-146">**Keine** (0)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-146">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="9dfe0-147">**Regulär** (1)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-147">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="9dfe0-148">**Anwendungs konsistent** (2)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-148">**Application consistent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="9dfe0-149">**Geplant** (3)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-149">**Planned** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9dfe0-150">**ReplicationHealth**</span><span class="sxs-lookup"><span data-stu-id="9dfe0-150">**ReplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dfe0-151">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9dfe0-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9dfe0-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9dfe0-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9dfe0-153">Replikations Integrität für die Replikations Beziehung.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-153">Replication health for the replication relationship.</span></span>

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9dfe0-154">**Nicht zutreffend** (0)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-154">**Not applicable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

<span data-ttu-id="9dfe0-155">**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-155">**Ok** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="9dfe0-156">**Warnung** (2)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-156">**Warning** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="9dfe0-157">**Kritisch** (3)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-157">**Critical** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9dfe0-158">**ReplicationState**</span><span class="sxs-lookup"><span data-stu-id="9dfe0-158">**ReplicationState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dfe0-159">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9dfe0-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9dfe0-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9dfe0-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9dfe0-161">Replikations Status für die Replikations Beziehung.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-161">Replication state for the replication relationship.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9dfe0-162"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (0)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-162"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="9dfe0-163"><span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Bereit für Replikation** (1)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-163"><span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="9dfe0-164"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Warten auf Abschluss der ersten Replikation** (2)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-164"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="9dfe0-165"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replizieren** (3)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-165"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="9dfe0-166"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synchronisierungs Replikation beendet** (4)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-166"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synced replication complete** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="9dfe0-167"><span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Wieder hergestellt** (5)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-167"><span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="9dfe0-168"><span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>Commit **ausgeführt (6** )</span><span class="sxs-lookup"><span data-stu-id="9dfe0-168"><span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="9dfe0-169"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>Angeh **alten (7** )</span><span class="sxs-lookup"><span data-stu-id="9dfe0-169"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="9dfe0-170"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Kritisch** (8)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-170"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="9dfe0-171"><span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**Warten auf den Start der erneuten Synchronisierung** (9)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-171"><span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="9dfe0-172"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Neusynchronisierung** (10)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-172"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span data-ttu-id="9dfe0-173"><span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Neusynchronisierung** angehalten (11)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-173"><span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Resynchronization suspended** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span data-ttu-id="9dfe0-174"><span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Failover** wird ausgeführt (12)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-174"><span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Failover in progress** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

<span data-ttu-id="9dfe0-175"><span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Failback** wird ausgeführt (13)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-175"><span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Failback in progress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

<span data-ttu-id="9dfe0-176"><span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Failback ist beendet** (14)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-176"><span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Failback complete** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>

<span data-ttu-id="9dfe0-177"><span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>Datenträger **Update läuft** (15)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-177"><span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**Disk update in progress** (15)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="9dfe0-178">Diese Eigenschaft wurde in Windows 10, Version 1703, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-178">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>

<span data-ttu-id="9dfe0-179"><span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>Datenträger **Update kritisch** (16)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-179"><span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**Disk update critical** (16)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="9dfe0-180">Diese Eigenschaft wurde in Windows 10, Version 1703, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-180">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9dfe0-181"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (17)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-181"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (17)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="9dfe0-182">Diese Eigenschaft wurde in Windows 10, Version 1703, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-182">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>

<span data-ttu-id="9dfe0-183"><span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Repurpose Replication in Progress** (18)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-183"><span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Repurpose replication in progress** (18)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="9dfe0-184">Diese Eigenschaft wurde in Windows 10, Version 1703, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-184">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>

<span data-ttu-id="9dfe0-185"><span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Vorbereitet für Synchronisierungs Replikation** (19)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-185"><span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Prepared for sync replication** (19)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="9dfe0-186">Diese Eigenschaft wurde in Windows 10, Version 1703, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-186">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>

<span data-ttu-id="9dfe0-187"><span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Vorbereitet für Gruppen umgekehrte Replikation** (20)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-187"><span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Prepared for group reverse replication** (20)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="9dfe0-188">Diese Eigenschaft wurde in Windows 10, Version 1703, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-188">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>

<span data-ttu-id="9dfe0-189"><span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Firedrill läuft** (21)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-189"><span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Firedrill in progress** (21)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="9dfe0-190">Diese Eigenschaft wurde in Windows 10, Version 1703, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-190">This property was added in Windows 10, version 1703.</span></span>

 

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9dfe0-191">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9dfe0-191">Remarks</span></span>

### <a name="extended-replication"></a><span data-ttu-id="9dfe0-192">Erweiterte Replikation</span><span class="sxs-lookup"><span data-stu-id="9dfe0-192">Extended replication</span></span>

<span data-ttu-id="9dfe0-193">Das Hyper-v-Replikations Feature in Windows 8 ermöglicht das effiziente Replizieren von virtuellen Computern, die auf einem Hyper-v-Server am primären Standort ausgeführt werden, auf einem anderen Hyper-v-Server am sekundären Standort.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-193">The Hyper-V replication feature in Windows 8 allows virtual machines that run on a Hyper-V server at the primary site to be efficiently replicated to another Hyper-V server at the secondary site.</span></span>

<span data-ttu-id="9dfe0-194">Das Hyper-V-Replikations Feature in Windows 8.1 ermöglicht einem Benutzer, die Replikations Beziehung zwischen dem sekundären Standort und einem dritten Standort zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-194">The Hyper-V replication feature in Windows 8.1 enables a user to extend the replication relationship from the secondary site onwards to a third site.</span></span> <span data-ttu-id="9dfe0-195">Beim dritten Standort kann es sich um einen Hyper-V-Host handeln, der vorab als Wiederherstellungs Server oder externer Replikations Anbieter bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="9dfe0-195">The third site can be a Hyper-V host pre-provisioned as a recovery server or external replication provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="9dfe0-196">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9dfe0-196">Requirements</span></span>



| <span data-ttu-id="9dfe0-197">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9dfe0-197">Requirement</span></span> | <span data-ttu-id="9dfe0-198">Wert</span><span class="sxs-lookup"><span data-stu-id="9dfe0-198">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dfe0-199">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-199">Minimum supported client</span></span><br/> | <span data-ttu-id="9dfe0-200">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="9dfe0-200">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="9dfe0-201">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9dfe0-201">Minimum supported server</span></span><br/> | <span data-ttu-id="9dfe0-202">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9dfe0-202">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9dfe0-203">Namespace</span><span class="sxs-lookup"><span data-stu-id="9dfe0-203">Namespace</span></span><br/>                | <span data-ttu-id="9dfe0-204">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="9dfe0-204">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9dfe0-205">MOF</span><span class="sxs-lookup"><span data-stu-id="9dfe0-205">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9dfe0-206"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9dfe0-206"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9dfe0-207">DLL</span><span class="sxs-lookup"><span data-stu-id="9dfe0-207">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9dfe0-208"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9dfe0-208"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9dfe0-209">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9dfe0-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dfe0-210">**CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="9dfe0-210">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dt>

[<span data-ttu-id="9dfe0-211">**CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="9dfe0-211">**CIM\_ManagedSystemElement**</span></span>](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)
</dt> </dl>

 

