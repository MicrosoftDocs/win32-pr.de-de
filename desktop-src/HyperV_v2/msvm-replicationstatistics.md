---
description: Stellt Replikations Statistiken für eine virtuelle Maschine bereit.
ms.assetid: 52d944a7-9309-4b56-97b7-e050a9501c57
title: Msvm_ReplicationStatistics-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationStatistics
- Msvm_ReplicationStatistics.InstanceID
- Msvm_ReplicationStatistics.Caption
- Msvm_ReplicationStatistics.Description
- Msvm_ReplicationStatistics.ElementName
- Msvm_ReplicationStatistics.StartStatisticTime
- Msvm_ReplicationStatistics.EndStatisticTime
- Msvm_ReplicationStatistics.ReplicationSuccessCount
- Msvm_ReplicationStatistics.ReplicationSize
- Msvm_ReplicationStatistics.MaxReplicationSize
- Msvm_ReplicationStatistics.ReplicationLatency
- Msvm_ReplicationStatistics.ReplicationMissCount
- Msvm_ReplicationStatistics.MaxReplicationLatency
- Msvm_ReplicationStatistics.NetworkFailureCount
- Msvm_ReplicationStatistics.ReplicationFailureCount
- Msvm_ReplicationStatistics.PendingReplicationSize
- Msvm_ReplicationStatistics.ApplicationConsistentSnapshotFailureCount
- Msvm_ReplicationStatistics.ReplicationHealth
- Msvm_ReplicationStatistics.LastTestFailoverTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3f18501c2da875a9c3514549271fbc91620abef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349304"
---
# <a name="msvm_replicationstatistics-class"></a><span data-ttu-id="e6e54-103">MSVM \_ replicationstatistics-Klasse</span><span class="sxs-lookup"><span data-stu-id="e6e54-103">Msvm\_ReplicationStatistics class</span></span>

<span data-ttu-id="e6e54-104">Stellt Replikations Statistiken für eine virtuelle Maschine bereit.</span><span class="sxs-lookup"><span data-stu-id="e6e54-104">Provides replication statistics for a virtual machine.</span></span> <span data-ttu-id="e6e54-105">Diese Statistiken decken den Zeitraum ab, der durch die Eigenschaften **monitoringstarttime** und **monitoringinterval** der [**MSVM \_ replicationservicesettingdata**](msvm-replicationservicesettingdata.md) -Klasse festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="e6e54-105">These statistics cover the duration specified by the **MonitoringStartTime** and **MonitoringInterval** properties of the [**Msvm\_ReplicationServiceSettingData**](msvm-replicationservicesettingdata.md) class.</span></span>

<span data-ttu-id="e6e54-106">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e6e54-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6e54-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6e54-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationStatistics : CIM_ManagedElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime StartStatisticTime;
  datetime EndStatisticTime;
  uint32   ReplicationSuccessCount;
  uint64   ReplicationSize;
  uint64   MaxReplicationSize;
  uint32   ReplicationLatency;
  uint32   ReplicationMissCount;
  uint32   MaxReplicationLatency;
  uint32   NetworkFailureCount;
  uint32   ReplicationFailureCount;
  uint64   PendingReplicationSize;
  uint32   ApplicationConsistentSnapshotFailureCount;
  uint32   ReplicationHealth;
  datetime LastTestFailoverTime;
};
```

## <a name="members"></a><span data-ttu-id="e6e54-108">Member</span><span class="sxs-lookup"><span data-stu-id="e6e54-108">Members</span></span>

<span data-ttu-id="e6e54-109">Die **MSVM \_ replicationstatistics** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e6e54-109">The **Msvm\_ReplicationStatistics** class has these types of members:</span></span>

-   [<span data-ttu-id="e6e54-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e6e54-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e6e54-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e6e54-111">Properties</span></span>

<span data-ttu-id="e6e54-112">Die **MSVM \_ replicationstatistics** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e6e54-112">The **Msvm\_ReplicationStatistics** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e6e54-113">**Applicationkonsistentsnapshotfailucomplete**</span><span class="sxs-lookup"><span data-stu-id="e6e54-113">**ApplicationConsistentSnapshotFailureCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6e54-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e6e54-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e6e54-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6e54-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6e54-116">Die Gesamtanzahl der VSS-Momentaufnahme Fehler.</span><span class="sxs-lookup"><span data-stu-id="e6e54-116">The total number of VSS snapshot failures.</span></span>

</dd> <dt>

<span data-ttu-id="e6e54-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e6e54-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6e54-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e6e54-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6e54-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6e54-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6e54-120">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="e6e54-120">A short description of the object.</span></span> <span data-ttu-id="e6e54-121">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e6e54-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e6e54-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e6e54-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6e54-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e6e54-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6e54-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6e54-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6e54-125">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="e6e54-125">A description of the object.</span></span> <span data-ttu-id="e6e54-126">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e6e54-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e6e54-127">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e6e54-127">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6e54-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e6e54-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6e54-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6e54-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6e54-130">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e6e54-130">A display name for the object.</span></span> <span data-ttu-id="e6e54-131">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e6e54-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e6e54-132">**Endstatistictime**</span><span class="sxs-lookup"><span data-stu-id="e6e54-132">**EndStatisticTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6e54-133">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="e6e54-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e6e54-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6e54-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6e54-135">Die Zeit in UTC, zu der der Hyper-V-Replikat Dienst das Sammeln von Replikations Statistikdaten beendet hat.</span><span class="sxs-lookup"><span data-stu-id="e6e54-135">The time, in UTC, when the Hyper-V Replica service stopped gathering replication statistics data.</span></span> <span data-ttu-id="e6e54-136">Zu diesem Zeitpunkt wird ein neuer Replikations Statistik-Cycle gestartet.</span><span class="sxs-lookup"><span data-stu-id="e6e54-136">At this time, a new replication statistics cycle starts.</span></span>

</dd> <dt>

<span data-ttu-id="e6e54-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e6e54-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6e54-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e6e54-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6e54-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6e54-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6e54-140">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="e6e54-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e6e54-141">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="e6e54-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e6e54-142">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e6e54-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e6e54-143">**Lasttestfailovertime**</span><span class="sxs-lookup"><span data-stu-id="e6e54-143">**LastTestFailoverTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6e54-144">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="e6e54-144">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e6e54-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6e54-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6e54-146">Gibt den letzten Zeitpunkt an, zu dem ein Test Replikat System für einen Replikations fähigen virtuellen Computer auf dem Wiederherstellungs Server erstellt wurde</span><span class="sxs-lookup"><span data-stu-id="e6e54-146">Indicates the last time a test replica system was created for a replication enabled virtual machine on the recovery server.</span></span>

</dd> <dt>

<span data-ttu-id="e6e54-147">**Maxreplicationlatency**</span><span class="sxs-lookup"><span data-stu-id="e6e54-147">**MaxReplicationLatency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6e54-148">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e6e54-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e6e54-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6e54-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6e54-150">Die maximale Zeitspanne in Sekunden, die für einen einzelnen Replikations Vorgang benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="e6e54-150">The maximum amount of time taken to complete a single replication cycle, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="e6e54-151">**Maxreplicationsize**</span><span class="sxs-lookup"><span data-stu-id="e6e54-151">**MaxReplicationSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6e54-152">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e6e54-152">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e6e54-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6e54-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6e54-154">Maximale Anzahl an Replikations Daten, die an das Wiederherstellungs Host System übertragen werden</span><span class="sxs-lookup"><span data-stu-id="e6e54-154">Maximum replication data transferred to the recovery host system, in bytes.</span></span> <span data-ttu-id="e6e54-155">Dies stellt die maximale Größe von Replikations Daten dar, die für dieses Intervall in einem einzelnen Intervall gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6e54-155">This represents the maximum size of replication data sent over a single cycle for this interval.</span></span>

</dd> <dt>

<span data-ttu-id="e6e54-156">**Networkfailudie**</span><span class="sxs-lookup"><span data-stu-id="e6e54-156">**NetworkFailureCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6e54-157">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e6e54-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e6e54-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6e54-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6e54-159">Die Gesamtanzahl der Netzwerkfehler, die für den Replikations Kanal mit dem Wiederherstellungs Host System aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="e6e54-159">The total number of network errors encountered for the replication channel with recovery host system.</span></span>

</dd> <dt>

<span data-ttu-id="e6e54-160">**"Pdingreplicationsize"**</span><span class="sxs-lookup"><span data-stu-id="e6e54-160">**PendingReplicationSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6e54-161">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e6e54-161">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e6e54-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6e54-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6e54-163">Die Größe der Daten für eine ausstehende Replikation in Bytes.</span><span class="sxs-lookup"><span data-stu-id="e6e54-163">The size of the data for a pending replication, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e6e54-164">**Replicationfailuder**</span><span class="sxs-lookup"><span data-stu-id="e6e54-164">**ReplicationFailureCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6e54-165">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e6e54-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e6e54-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6e54-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6e54-167">Die Gesamtanzahl der Replikations Fehler.</span><span class="sxs-lookup"><span data-stu-id="e6e54-167">The total number of replication failures.</span></span> <span data-ttu-id="e6e54-168">Dies schließt Fehler für den Replikations Vorgang ein.</span><span class="sxs-lookup"><span data-stu-id="e6e54-168">This includes errors for replication operation.</span></span>

</dd> <dt>

<span data-ttu-id="e6e54-169">**ReplicationHealth**</span><span class="sxs-lookup"><span data-stu-id="e6e54-169">**ReplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6e54-170">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e6e54-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e6e54-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6e54-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6e54-172">Die Replikations Integrität für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="e6e54-172">The replication health for the virtual machine.</span></span> <span data-ttu-id="e6e54-173">Dabei handelt es sich um einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="e6e54-173">This will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e6e54-174"><span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (0)</span><span class="sxs-lookup"><span data-stu-id="e6e54-174"><span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not applicable** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e6e54-175"><span id="Ok"></span><span id="ok"></span><span id="OK"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="e6e54-175"><span id="Ok"></span><span id="ok"></span><span id="OK"></span>**Ok** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e6e54-176"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (2)</span><span class="sxs-lookup"><span data-stu-id="e6e54-176"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e6e54-177"><span id="Critical_________________"></span><span id="critical_________________"></span><span id="CRITICAL_________________"></span>**Kritisch** (3)</span><span class="sxs-lookup"><span data-stu-id="e6e54-177"><span id="Critical_________________"></span><span id="critical_________________"></span><span id="CRITICAL_________________"></span>**Critical** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e6e54-178">**ReplicationLatency**</span><span class="sxs-lookup"><span data-stu-id="e6e54-178">**ReplicationLatency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6e54-179">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e6e54-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e6e54-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6e54-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6e54-181">Gesamt Replikations Latenz beim Übertragen der Daten an das Wiederherstellungs Host System in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="e6e54-181">Total replication latency while transferring the data to the recovery host system, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="e6e54-182">**Replicationmisscount**</span><span class="sxs-lookup"><span data-stu-id="e6e54-182">**ReplicationMissCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6e54-183">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e6e54-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e6e54-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6e54-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6e54-185">Die Anzahl der verpassten Replikations Zyklen.</span><span class="sxs-lookup"><span data-stu-id="e6e54-185">The number of missed replication cycles.</span></span> <span data-ttu-id="e6e54-186">Dies kann auf hohe Arbeitsauslastung, Netzwerkprobleme oder Replikations Fehler liegen.</span><span class="sxs-lookup"><span data-stu-id="e6e54-186">This can be because of heavy workload, network issues, or replication errors.</span></span>

</dd> <dt>

<span data-ttu-id="e6e54-187">**Replicationsize**</span><span class="sxs-lookup"><span data-stu-id="e6e54-187">**ReplicationSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6e54-188">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e6e54-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e6e54-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6e54-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6e54-190">Die Gesamtmenge der Replikations Daten, die auf das Wiederherstellungs Host System übertragen werden (in Bytes)</span><span class="sxs-lookup"><span data-stu-id="e6e54-190">The total amount of replication data transferred to the recovery host system, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e6e54-191">**Replicationerfolgreiches count**</span><span class="sxs-lookup"><span data-stu-id="e6e54-191">**ReplicationSuccessCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6e54-192">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e6e54-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e6e54-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6e54-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6e54-194">Die Gesamtanzahl der erfolgreichen Replikationen für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="e6e54-194">The total number of successful replications for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="e6e54-195">**Startstatistictime**</span><span class="sxs-lookup"><span data-stu-id="e6e54-195">**StartStatisticTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6e54-196">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="e6e54-196">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e6e54-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e6e54-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6e54-198">Die Zeit in UTC, zu der der Hyper-V-Replikat Dienst mit dem Sammeln von Replikations Statistikdaten begonnen hat</span><span class="sxs-lookup"><span data-stu-id="e6e54-198">The time, in UTC, when the Hyper-V Replica service started gathering replication statistics data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e6e54-199">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6e54-199">Requirements</span></span>



| <span data-ttu-id="e6e54-200">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6e54-200">Requirement</span></span> | <span data-ttu-id="e6e54-201">Wert</span><span class="sxs-lookup"><span data-stu-id="e6e54-201">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6e54-202">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e6e54-202">Minimum supported client</span></span><br/> | <span data-ttu-id="e6e54-203">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6e54-203">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e6e54-204">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e6e54-204">Minimum supported server</span></span><br/> | <span data-ttu-id="e6e54-205">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6e54-205">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e6e54-206">Namespace</span><span class="sxs-lookup"><span data-stu-id="e6e54-206">Namespace</span></span><br/>                | <span data-ttu-id="e6e54-207">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="e6e54-207">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e6e54-208">MOF</span><span class="sxs-lookup"><span data-stu-id="e6e54-208">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6e54-209"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e6e54-209"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e6e54-210">DLL</span><span class="sxs-lookup"><span data-stu-id="e6e54-210">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6e54-211"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e6e54-211"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

