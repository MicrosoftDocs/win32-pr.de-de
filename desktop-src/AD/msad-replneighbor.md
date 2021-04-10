---
title: MSAD_ReplNeighbor-Klasse
description: Stellt die DS- \_ repl \_ -Nachbar Struktur dar, die die eingehenden Replikations Zustandsinformationen für einen bestimmten namens Kontext (NC) und das Quell Server Paar enthält.
ms.assetid: fdd3934b-a3f6-49ad-827b-077bcd21cf23
ms.tgt_platform: multiple
keywords:
- MSAD_ReplNeighbor-Klasse Active Directory
- MSAD_ReplNeighbor Klasse Active Directory, beschrieben
topic_type:
- apiref
api_name:
- MSAD_ReplNeighbor
- MSAD_ReplNeighbor.NamingContextDN
- MSAD_ReplNeighbor.SourceDsaObjGuid
- MSAD_ReplNeighbor.NamingContextObjGuid
- MSAD_ReplNeighbor.SourceDsaDN
- MSAD_ReplNeighbor.SourceDsaAddress
- MSAD_ReplNeighbor.SourceDsaInvocationID
- MSAD_ReplNeighbor.AsyncIntersiteTransportDN
- MSAD_ReplNeighbor.AsyncIntersiteTransportObjGuid
- MSAD_ReplNeighbor.USNLastObjChangeSynced
- MSAD_ReplNeighbor.USNAttributeFilter
- MSAD_ReplNeighbor.TimeOfLastSyncSuccess
- MSAD_ReplNeighbor.TimeOfLastSyncAttempt
- MSAD_ReplNeighbor.LastSyncResult
- MSAD_ReplNeighbor.NumConsecutiveSyncFailures
- MSAD_ReplNeighbor.ReplicaFlags
- MSAD_ReplNeighbor.Writeable
- MSAD_ReplNeighbor.SyncOnStartup
- MSAD_ReplNeighbor.DoScheduledSyncs
- MSAD_ReplNeighbor.UseAsyncIntersiteTransport
- MSAD_ReplNeighbor.TwoWaySync
- MSAD_ReplNeighbor.FullSyncInProgress
- MSAD_ReplNeighbor.FullSyncNextPacket
- MSAD_ReplNeighbor.NeverSynced
- MSAD_ReplNeighbor.IgnoreChangeNotifications
- MSAD_ReplNeighbor.DisableScheduledSync
- MSAD_ReplNeighbor.CompressChanges
- MSAD_ReplNeighbor.NoChangeNotifications
- MSAD_ReplNeighbor.SourceDsaSite
- MSAD_ReplNeighbor.SourceDsaCN
- MSAD_ReplNeighbor.Domain
- MSAD_ReplNeighbor.IsDeletedSourceDsa
- MSAD_ReplNeighbor.ModifiedNumConsecutiveSyncFailures
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9554c73c7fb84aad10ae6dda51480a7644d8434a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956512"
---
# <a name="msad_replneighbor-class"></a><span data-ttu-id="8f1d5-105">MSAD \_ ReplNeighbor-Klasse</span><span class="sxs-lookup"><span data-stu-id="8f1d5-105">MSAD\_ReplNeighbor class</span></span>

<span data-ttu-id="8f1d5-106">Stellt die [**DS- \_ repl- \_ Nachbar**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw) Struktur dar, die die eingehenden Replikations Zustandsinformationen für einen bestimmten namens Kontext (NC) und das Quell Server Paar enthält, wie von der [**dsreplicagetinfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-106">Represents the [**DS\_REPL\_NEIGHBOR**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw) structure, which contains the inbound replication state information for a particular naming context (NC) and source server pair, as returned by the [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f1d5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f1d5-107">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplNeighbor
{
  String   NamingContextDN;
  String   SourceDsaObjGuid;
  String   NamingContextObjGuid;
  String   SourceDsaDN;
  String   SourceDsaAddress;
  String   SourceDsaInvocationID;
  String   AsyncIntersiteTransportDN;
  String   AsyncIntersiteTransportObjGuid;
  uint64   USNLastObjChangeSynced;
  uint64   USNAttributeFilter;
  datetime TimeOfLastSyncSuccess;
  datetime TimeOfLastSyncAttempt;
  uint32   LastSyncResult;
  uint32   NumConsecutiveSyncFailures;
  uint32   ReplicaFlags;
  boolean  Writeable = FALSE;
  boolean  SyncOnStartup = FALSE;
  boolean  DoScheduledSyncs = FALSE;
  boolean  UseAsyncIntersiteTransport = FALSE;
  boolean  TwoWaySync = FALSE;
  boolean  FullSyncInProgress = FALSE;
  boolean  FullSyncNextPacket = FALSE;
  boolean  NeverSynced = FALSE;
  boolean  IgnoreChangeNotifications = FALSE;
  boolean  DisableScheduledSync = FALSE;
  boolean  CompressChanges = FALSE;
  boolean  NoChangeNotifications = FALSE;
  String   SourceDsaSite;
  String   SourceDsaCN;
  String   Domain;
  boolean  IsDeletedSourceDsa = FALSE;
  uint32   ModifiedNumConsecutiveSyncFailures;
};
```

## <a name="members"></a><span data-ttu-id="8f1d5-108">Member</span><span class="sxs-lookup"><span data-stu-id="8f1d5-108">Members</span></span>

<span data-ttu-id="8f1d5-109">Die **MSAD \_ ReplNeighbor** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8f1d5-109">The **MSAD\_ReplNeighbor** class has these types of members:</span></span>

-   [<span data-ttu-id="8f1d5-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="8f1d5-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="8f1d5-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8f1d5-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8f1d5-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="8f1d5-112">Methods</span></span>

<span data-ttu-id="8f1d5-113">Die **MSAD \_ ReplNeighbor** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-113">The **MSAD\_ReplNeighbor** class has these methods.</span></span>



| <span data-ttu-id="8f1d5-114">Methode</span><span class="sxs-lookup"><span data-stu-id="8f1d5-114">Method</span></span>                                                           | <span data-ttu-id="8f1d5-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f1d5-115">Description</span></span>                                                                   |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="8f1d5-116">**Syncnamingcontext**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-116">**SyncNamingContext**</span></span>](syncnamingcontext-msad-replneighbor.md) | <span data-ttu-id="8f1d5-117">Synchronisiert einen Ziel namens Kontext mit einer seiner Quellen.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-117">Synchronizes a destination naming context with one of its sources.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8f1d5-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8f1d5-118">Properties</span></span>

<span data-ttu-id="8f1d5-119">Die **MSAD \_ ReplNeighbor** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-119">The **MSAD\_ReplNeighbor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8f1d5-120">**Asyncintersitetransportdn**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-120">**AsyncIntersiteTransportDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f1d5-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-121">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f1d5-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f1d5-123">Ruft den X. 500-Pfad des [**interSiteTransport**](/windows/desktop/ADSchema/c-intersitetransport) -Objekts ab, das dem Transport entspricht, über den die Replikation ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-123">Gets the X.500 path of the [**interSiteTransport**](/windows/desktop/ADSchema/c-intersitetransport) object that corresponds to the transport over which replication is performed.</span></span> <span data-ttu-id="8f1d5-124">Legen Sie für die RPC/IP-Replikation auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-124">Set to **NULL** for RPC/IP replication.</span></span>

</dd> <dt>

<span data-ttu-id="8f1d5-125">**Asyncintersitetransportobjguid**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-125">**AsyncIntersiteTransportObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f1d5-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-126">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f1d5-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f1d5-128">Ruft die GUID des standortübergreifenden Transport Objekts ab, das der **asyncintersitetransportdn** -Eigenschaft entspricht.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-128">Gets the GUID of the intersite transport object that corresponds to the **AsyncIntersiteTransportDN** property.</span></span>

</dd> <dt>

<span data-ttu-id="8f1d5-129">**Compresschanges**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-129">**CompressChanges**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f1d5-130">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8f1d5-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f1d5-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f1d5-132">Ruft den Wert ab, der angibt, ob das **DS- \_ repl- \_ NBR \_ \_** -Flag zum Komprimieren von Änderungen in der **replicaflags** -Eigenschaft festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-132">Gets the value that indicates whether the **DS\_REPL\_NBR\_COMPRESS\_CHANGES** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="8f1d5-133">**Disablescheduledsync**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-133">**DisableScheduledSync**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f1d5-134">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8f1d5-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f1d5-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f1d5-136">Ruft den Wert ab, der angibt, ob das Flag zum **\_ \_ \_ Deaktivieren \_ geplanter \_ Synchronisierung in DS repl** in der **replicaflags** -Eigenschaft festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-136">Gets the value that indicates whether the **DS\_REPL\_NBR\_DISABLE\_SCHEDULED\_SYNC** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="8f1d5-137">**Domäne**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-137">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f1d5-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-138">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f1d5-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f1d5-140">Ruft den kanonischen Namen der Domäne des replizierten NC ab.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-140">Gets the canonical name of the domain of the replicated NC.</span></span>

</dd> <dt>

<span data-ttu-id="8f1d5-141">**Doscheduledsyncs**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-141">**DoScheduledSyncs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f1d5-142">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8f1d5-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f1d5-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f1d5-144">Ruft den Wert ab, der angibt, ob das Flag " **DS \_ repl \_ NBR \_ do \_ Scheduled \_ syncs** " in der **replicaflags** -Eigenschaft festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-144">Gets the value that indicates whether the **DS\_REPL\_NBR\_DO\_SCHEDULED\_SYNCS** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="8f1d5-145">**Fullsyncinprogress**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-145">**FullSyncInProgress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f1d5-146">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8f1d5-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f1d5-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f1d5-148">Ruft den Wert ab, der angibt, ob in der **replicaflags** -Eigenschaft das Flag **\_ für die \_ \_ vollständige Synchronisierung von DS repl NBR \_ \_ in \_ Progress** festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-148">Gets the value that indicates whether the **DS\_REPL\_NBR\_FULL\_SYNC\_IN\_PROGRESS** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="8f1d5-149">**Fullsyncnextpacket**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-149">**FullSyncNextPacket**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f1d5-150">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8f1d5-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f1d5-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f1d5-152">Ruft den Wert ab, der angibt, ob das Flag für die **\_ vollständige Synchronisierung der DS-repl- \_ \_ voll \_ Synchronisierung des \_ nächsten \_ Pakets** in der **replicaflags** -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8f1d5-152">Gets the value that indicates whether the **DS\_REPL\_NBR\_FULL\_SYNC\_NEXT\_PACKET** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="8f1d5-153">**Ignorechangenotifications**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-153">**IgnoreChangeNotifications**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f1d5-154">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8f1d5-154">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f1d5-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f1d5-156">Ruft den Wert ab, der angibt, ob das Flag " **DS \_ repl \_ NBR- \_ \_ Änderungs \_ Benachrichtigungen ignorieren** " in der **replicaflags** -Eigenschaft festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-156">Gets the value that indicates whether the **DS\_REPL\_NBR\_IGNORE\_CHANGE\_NOTIFICATIONS** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="8f1d5-157">**Isdeletedsourcedsa**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-157">**IsDeletedSourceDsa**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f1d5-158">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8f1d5-158">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f1d5-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f1d5-160">Ruft den-Wert ab, der angibt, ob diese Verbindung einen Quell-DC darstellt, der gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-160">Gets the value that indicates whether this connection represents a source DC that has been deleted.</span></span> <span data-ttu-id="8f1d5-161">**True** , wenn diese Verbindung einen Quell-DC darstellt, der gelöscht wurde. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-161">**TRUE** if this connection represents a source DC that has been deleted; otherwise, **FALSE**.</span></span> <span data-ttu-id="8f1d5-162">In der Entwurfszeit repliziert die DS diese Verbindungen für einige Zeit nach dem Löschen des Quell Domänen Controllers.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-162">By design, the DS will continue to replicate these connections for some time for some time after the source DC is deleted.</span></span>

</dd> <dt>

<span data-ttu-id="8f1d5-163">**Lastsynkresult**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-163">**LastSyncResult**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f1d5-164">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f1d5-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f1d5-166">Ruft den **HRESULT** -Fehlercode für den letzten Replikations Versuch ab.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-166">Gets the **HRESULT** error code for the last replication attempt.</span></span>

</dd> <dt>

<span data-ttu-id="8f1d5-167">**ModifiedNumConsecutiveSyncFailures**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-167">**ModifiedNumConsecutiveSyncFailures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f1d5-168">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f1d5-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f1d5-170">Ruft die Anzahl der aufeinander folgenden fehlgeschlagenen Replikations Versuche ab, ohne die Verbindungen, für die ein Fehler erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-170">Gets the number of consecutive failed replication attempts, not including the connections that are expected to fail.</span></span> <span data-ttu-id="8f1d5-171">Wenn z. b. die **isdeletedsourcedsa** -Eigenschaft auf **true** festgelegt ist, wird erwartet, dass Sie fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-171">For example, if the **IsDeletedSourceDsa** property is set to **TRUE**, it is expected to fail.</span></span>

</dd> <dt>

<span data-ttu-id="8f1d5-172">**Namingcontextdn**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-172">**NamingContextDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f1d5-173">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-173">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f1d5-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-175">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8f1d5-175">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8f1d5-176">Ruft den X. 500-Pfad für den NC ab, der von dieser Verbindung repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-176">Gets the X.500 path for the NC that is replicated by this connection.</span></span>

</dd> <dt>

<span data-ttu-id="8f1d5-177">**Namingcontextobjguid**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-177">**NamingContextObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f1d5-178">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-178">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f1d5-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f1d5-180">Ruft die GUID für den replizierten NC ab.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-180">Gets the GUID for the replicated NC.</span></span>

</dd> <dt>

<span data-ttu-id="8f1d5-181">**Nicht synchronisiert**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-181">**NeverSynced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f1d5-182">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8f1d5-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f1d5-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f1d5-184">Ruft den Wert ab, der angibt, ob das Flag " **DS \_ repl \_ NBR \_ nie \_ synchronisiert** " in der **replicaflags** -Eigenschaft festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-184">Gets the value that indicates whether the **DS\_REPL\_NBR\_NEVER\_SYNCED** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="8f1d5-185">**Nochangenotifications**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-185">**NoChangeNotifications**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f1d5-186">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8f1d5-186">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f1d5-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f1d5-188">Ruft den Wert ab, der angibt, ob das Flag " **DS \_ repl \_ NBR \_ No \_ Change \_** Notification" in der **replicaflags** -Eigenschaft festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-188">Gets the value that indicates whether the **DS\_REPL\_NBR\_NO\_CHANGE\_NOTIFICATIONS** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="8f1d5-189">**Numaufeinanderfolgende tivesyncfailure**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-189">**NumConsecutiveSyncFailures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f1d5-190">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f1d5-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f1d5-192">Ruft die Anzahl der aufeinanderfolgenden fehlgeschlagenen Replikations Versuche ab.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-192">Gets the number of consecutive failed replication attempts.</span></span>

</dd> <dt>

<span data-ttu-id="8f1d5-193">**Replicaflags**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-193">**ReplicaFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f1d5-194">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f1d5-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f1d5-196">Ruft den Satz von Flags ab, die Attribute und Optionen für die Replikations Daten angeben.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-196">Gets the set of flags that specify attributes and options for the replication data.</span></span> <span data-ttu-id="8f1d5-197">Diese Eigenschaft kann NULL sein oder eine Kombination aus einem oder mehreren der folgenden Flags aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-197">This property can be zero or a combination of one or more of the following flags.</span></span>

<dt>

<span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>

<span data-ttu-id="8f1d5-198"><span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>**DS \_ \_ \_ Beschreibbares repl-NBR** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="8f1d5-198"><span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>**DS\_REPL\_NBR\_WRITEABLE** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="8f1d5-199">Die lokale Kopie des Namenskontexts ist nicht schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-199">The local copy of the naming context is writable.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>

<span data-ttu-id="8f1d5-200"><span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>**DS \_ REPL- \_ NBR- \_ Synchronisierung \_ beim \_ Start** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="8f1d5-200"><span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>**DS\_REPL\_NBR\_SYNC\_ON\_STARTUP** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="8f1d5-201">Beim Starten des Zielservers wird versucht, diesen namens Kontext aus dieser Quelle zu replizieren.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-201">Replication of this naming context from this source is attempted when the destination server is booted.</span></span> <span data-ttu-id="8f1d5-202">Dieses Flag gilt normalerweise nur für Standort interne Nachbarn.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-202">This flag usually only applies to intra-site neighbors.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>

<span data-ttu-id="8f1d5-203"><span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>**DS \_ REPL \_ NBR \_ \_ geplante \_ Synchronisierungen** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="8f1d5-203"><span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>**DS\_REPL\_NBR\_DO\_SCHEDULED\_SYNCS** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="8f1d5-204">Die Replikation nach einem Zeitplan ausführen.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-204">Perform replication on a schedule.</span></span> <span data-ttu-id="8f1d5-205">Dieses Flag wird normalerweise festgelegt, es sei denn, der Zeitplan für diesen namens Kontext oder diese Quelle ist "Never", d. h. der leere Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-205">This flag is usually set unless the schedule for this naming context or source is "never", that is, the empty schedule.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>

<span data-ttu-id="8f1d5-206"><span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>**DS \_ REPL \_ NBR \_ verwendet \_ Async- \_ standortübergreifenden \_ Transport** (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="8f1d5-206"><span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>**DS\_REPL\_NBR\_USE\_ASYNC\_INTERSITE\_TRANSPORT** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="8f1d5-207">Die Replikation indirekt über den standortübergreifenden Meldungsdienst ausführen.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-207">Perform replication indirectly through the Inter-Site Messaging Service.</span></span> <span data-ttu-id="8f1d5-208">Dieses Flag wird nur festgelegt, wenn über SMTP repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-208">This flag is set only when replicating over SMTP.</span></span> <span data-ttu-id="8f1d5-209">Dieses Flag wird nicht festgelegt, wenn über standortübergreifendes RPC/IP repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-209">This flag is not set when replicating over inter-site RPC/IP.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>

<span data-ttu-id="8f1d5-210"><span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>**DS \_ REPL NBR bidirektionale \_ \_ \_ \_ Synchronisierung** (512 (0x200))</span><span class="sxs-lookup"><span data-stu-id="8f1d5-210"><span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>**DS\_REPL\_NBR\_TWO\_WAY\_SYNC** (512 (0x200))</span></span>


</dt> <dd>

<span data-ttu-id="8f1d5-211">Wenn festgelegt, wird angegeben, dass der Zielserver nach Abschluss der eingehenden Replikation den Quell Server in umgekehrter Richtung synchronisieren muss.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-211">If set, indicates that when inbound replication is complete, the destination server must tell the source server to synchronize in the reverse direction.</span></span> <span data-ttu-id="8f1d5-212">Dieses Feature wird in DFÜ-Szenarien verwendet, in denen nur einer der beiden Server eine DFÜ-Verbindung initiieren kann.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-212">This feature is used in dial-up scenarios where only one of the two servers can initiate a dial-up connection.</span></span> <span data-ttu-id="8f1d5-213">Diese Option kann z. b. in einer Unternehmenszentrale und Filiale verwendet werden, in der die Zweigstelle mithilfe einer DFÜ-ISP-Verbindung eine Verbindung mit dem Unternehmens Hauptsitz über das Internet herstellt.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-213">For example, this option could be used in a corporate headquarters and branch office, where the branch office connects to the corporate headquarters over the Internet by means of a dial-up ISP connection.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>

<span data-ttu-id="8f1d5-214"><span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>**DS \_ REPL \_ NBR \_ Rückgabe \_ Objekt \_** -übergeordnete Elemente (2048 (0x800))</span><span class="sxs-lookup"><span data-stu-id="8f1d5-214"><span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>**DS\_REPL\_NBR\_RETURN\_OBJECT\_PARENTS** (2048 (0x800))</span></span>


</dt> <dd>

<span data-ttu-id="8f1d5-215">Dieser Nachbar befindet sich in einem Zustand, in dem er vor untergeordneten Objekten übergeordnete Objekte zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-215">This neighbor is in a state where it returns parent objects before children objects.</span></span> <span data-ttu-id="8f1d5-216">Der Nachbar wechselt in diesen Zustand, nachdem er ein untergeordnetes Element vor dem zugehörigen übergeordneten Element empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-216">It goes into this state after it receives a child object before its parent.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>

<span data-ttu-id="8f1d5-217"><span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>**DS \_ \_ \_ Vollständige \_ Synchronisierung \_ der \_ repl NBR** wird ausgeführt (65536 (0x10000))</span><span class="sxs-lookup"><span data-stu-id="8f1d5-217"><span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>**DS\_REPL\_NBR\_FULL\_SYNC\_IN\_PROGRESS** (65536 (0x10000))</span></span>


</dt> <dd>

<span data-ttu-id="8f1d5-218">Der Zielserver führt eine vollständige Synchronisierung vom Quellserver aus.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-218">The destination server is performing a full synchronization from the source server.</span></span> <span data-ttu-id="8f1d5-219">Vollständige Synchronisierung verwenden keine Vektoren, die Aktualisierungen (z. b. [**DS- \_ repl- \_ Cursors**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)) zum Filtern von Aktualisierungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-219">Full synchronizations do not use vectors that create updates (such as [**DS\_REPL\_CURSORS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)) for filtering updates.</span></span> <span data-ttu-id="8f1d5-220">Vollständige Synchronisierung wird nicht als Teil des standardmäßigen Replikations Protokolls verwendet.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-220">Full synchronizations are not used as a part of the default replication protocol.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>

<span data-ttu-id="8f1d5-221"><span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>**DS \_ REPL \_ NBR- \_ vollständige \_ Synchronisierung \_ Nächster \_ Paket** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="8f1d5-221"><span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>**DS\_REPL\_NBR\_FULL\_SYNC\_NEXT\_PACKET** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="8f1d5-222">Das letzte Paket aus der Quelle hat eine Änderung eines Objekts angegeben, das vom Zielserver noch nicht erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-222">The last packet from the source indicated a modification of an object that the destination server has not yet created.</span></span> <span data-ttu-id="8f1d5-223">Das nächste Paket, das angefordert werden soll, weist den Quell Server an, alle Attribute des geänderten Objekts in das Paket einzufügen.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-223">The next packet to be requested instructs the source server to put all attributes of the modified object into the packet.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>

<span data-ttu-id="8f1d5-224"><span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>**DS \_ REPL \_ NBR \_ nie \_ synchronisiert** (2097152 (0x200000))</span><span class="sxs-lookup"><span data-stu-id="8f1d5-224"><span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>**DS\_REPL\_NBR\_NEVER\_SYNCED** (2097152 (0x200000))</span></span>


</dt> <dd>

<span data-ttu-id="8f1d5-225">Eine Synchronisierung ist von dieser Quelle nie erfolgreich abgeschlossen worden.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-225">A synchronization has never been successfully completed from this source.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>

<span data-ttu-id="8f1d5-226"><span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>**DS \_ REPL \_ NBR \_ vorzeitig** entfernt (16777216 (0x1000000))</span><span class="sxs-lookup"><span data-stu-id="8f1d5-226"><span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>**DS\_REPL\_NBR\_PREEMPTED** (16777216 (0x1000000))</span></span>


</dt> <dd>

<span data-ttu-id="8f1d5-227">Die Replikations-Engine hat die Verarbeitung dieses Nachbarn vorübergehend beendet, um einen anderen Nachbar mit höherer Priorität zu verarbeiten, entweder für diese Partition oder für eine andere Partition.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-227">The replication engine has temporarily stopped processing this neighbor in order to service another higher-priority neighbor, either for this partition or for another partition.</span></span> <span data-ttu-id="8f1d5-228">Die Replikations-Engine fährt mit der Verarbeitung dieses Nachbarn fort, nachdem die Arbeit mit der höheren Priorität abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-228">The replication engine will resume processing this neighbor after the higher-priority work is completed.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>

<span data-ttu-id="8f1d5-229"><span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>**DS \_ REPL \_ NBR \_ - \_ Änderungs \_ Benachrichtigungen ignorieren** (67108864 (0x4000000))</span><span class="sxs-lookup"><span data-stu-id="8f1d5-229"><span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>**DS\_REPL\_NBR\_IGNORE\_CHANGE\_NOTIFICATIONS** (67108864 (0x4000000))</span></span>


</dt> <dd>

<span data-ttu-id="8f1d5-230">Dieser Nachbar ist darauf festgelegt, Benachrichtigungs basierte Synchronisierung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-230">This neighbor is set to disable notification-based synchronizations.</span></span> <span data-ttu-id="8f1d5-231">Innerhalb eines Standorts werden Domänencontroller bei Vornahme von Änderungen auf Grundlage von Benachrichtigungen miteinander synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-231">Within a site, domain controllers synchronize with each other based on notifications when changes occur.</span></span> <span data-ttu-id="8f1d5-232">Diese Einstellung verhindert, dass dieser Nachbar Synchronisierung durchführt, die von Benachrichtigungen ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-232">This setting prevents this neighbor from performing synchronizations that are triggered by notifications.</span></span> <span data-ttu-id="8f1d5-233">Der Nachbar führt weiterhin Synchronisierung basierend auf dem Zeitplan oder als Reaktion auf manuell angeforderte Synchronisierung durch.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-233">The neighbor will still do synchronizations based on its schedule, or in response to manually requested synchronizations.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>

<span data-ttu-id="8f1d5-234"><span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>**DS \_ REPL \_ NBR \_ , \_ geplante \_ Synchronisierung deaktivieren** (134217728 (0x8000000))</span><span class="sxs-lookup"><span data-stu-id="8f1d5-234"><span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>**DS\_REPL\_NBR\_DISABLE\_SCHEDULED\_SYNC** (134217728 (0x8000000))</span></span>


</dt> <dd>

<span data-ttu-id="8f1d5-235">Dieser Nachbar ist so festgelegt, dass keine Synchronisierung basierend auf dem Zeitplan durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-235">This neighbor is set to not perform synchronizations based on its schedule.</span></span> <span data-ttu-id="8f1d5-236">Die einzige Möglichkeit, mit der die Synchronisierung durchgeführt wird, ist die Antwort auf Änderungs Benachrichtigungen oder manuell angeforderte Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-236">The only way this neighbor will perform synchronizations is in response to change notifications or to manually requested synchronizations.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>

<span data-ttu-id="8f1d5-237"><span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>**DS \_ Änderungen an der \_ NBR- \_ Komprimierung \_** (268435456 (0x10000000))</span><span class="sxs-lookup"><span data-stu-id="8f1d5-237"><span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>**DS\_REPL\_NBR\_COMPRESS\_CHANGES** (268435456 (0x10000000))</span></span>


</dt> <dd>

<span data-ttu-id="8f1d5-238">Die von dieser Quelle empfangenen Änderungen müssen komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-238">Changes received from this source are to be compressed.</span></span> <span data-ttu-id="8f1d5-239">Die Komprimierung erfolgt in der Regel nur, wenn sich der Quell Server an einem anderen Standort befindet.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-239">Compression usually occurs only if the source server is in a different site.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>

<span data-ttu-id="8f1d5-240"><span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>**DS \_ REPL \_ NBR \_ keine \_ Änderungs \_ Benachrichtigungen** (536870912 (0x20000000))</span><span class="sxs-lookup"><span data-stu-id="8f1d5-240"><span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>**DS\_REPL\_NBR\_NO\_CHANGE\_NOTIFICATIONS** (536870912 (0x20000000))</span></span>


</dt> <dd>

<span data-ttu-id="8f1d5-241">Von dieser Quelle sollten keine Änderungsbenachrichtigungen empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-241">No change notifications should be received from this source.</span></span> <span data-ttu-id="8f1d5-242">Wird normalerweise nur dann festgelegt, wenn sich der Quell Server an einem anderen Standort befindet.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-242">Usually set only if the source server is in a different site.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>

<span data-ttu-id="8f1d5-243"><span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>**DS \_ \_ \_ Teil \_ Attribut \_ Satz für repl-NBR** (1073741824 (0x40000000))</span><span class="sxs-lookup"><span data-stu-id="8f1d5-243"><span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>**DS\_REPL\_NBR\_PARTIAL\_ATTRIBUTE\_SET** (1073741824 (0x40000000))</span></span>


</dt> <dd>

<span data-ttu-id="8f1d5-244">Dieser Nachbar befindet sich in einem Zustand, in dem er den Inhalt dieses Replikats aufgrund einer Änderung im Teilattributsatz neu erstellt.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-244">This neighbor is in a state where it is rebuilding the contents of this replica because of a change in the partial attribute set.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f1d5-245">**Sourcedsaaddress**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-245">**SourceDsaAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f1d5-246">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-246">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-247">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f1d5-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f1d5-248">Ruft die DNS-Adresse des Quell Domänen Controllers ab.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-248">Gets the DNS address of the source DC.</span></span>

> [!Note]  
> <span data-ttu-id="8f1d5-249">Diese Zeichenfolge enthält eine geänderte GUID, nicht den häufig verwendeten kanonischen DNS-Namen.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-249">This string contains a modified GUID, not the commonly used canonical DNS name.</span></span>

 

</dd> <dt>

<span data-ttu-id="8f1d5-250">**SourceDsaCN**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-250">**SourceDsaCN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f1d5-251">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-251">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-252">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f1d5-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f1d5-253">Ruft die Objekt Pfadkomponente für das DSA ab, das den Quell Domänen Controller darstellt.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-253">Gets the object path component for the DSA that represents the source DC.</span></span> <span data-ttu-id="8f1d5-254">Diese Zeichenfolge ähnelt häufig dem Computernamen, ist aber nicht immer identisch.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-254">This string is often similar to the computer name but is not always identical.</span></span>

</dd> <dt>

<span data-ttu-id="8f1d5-255">**Sourcedsadn**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-255">**SourceDsaDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f1d5-256">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-256">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-257">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f1d5-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f1d5-258">Ruft den X. 500-Pfad für das DSA ab, das den Quell Domänen Controller darstellt.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-258">Gets the X.500 path for the DSA that represents the source DC.</span></span>

</dd> <dt>

<span data-ttu-id="8f1d5-259">**Sourcedsainvocationid**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-259">**SourceDsaInvocationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f1d5-260">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-260">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-261">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f1d5-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f1d5-262">Ruft die Aufruf-ID ab, die vom Quell Server bei der letzten Replikation verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-262">Gets the invocation ID that was used by the source server as of the last replication.</span></span>

</dd> <dt>

<span data-ttu-id="8f1d5-263">**Sourcedsaobjguid**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-263">**SourceDsaObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f1d5-264">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-264">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-265">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f1d5-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-266">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8f1d5-266">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8f1d5-267">Ruft die GUID für den Verzeichnisdienst-Agent (DSA) ab, der den Quell Domänen Controller (DC) darstellt.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-267">Gets the GUID for the directory service agent (DSA) that represents the source domain controller (DC).</span></span>

</dd> <dt>

<span data-ttu-id="8f1d5-268">**Sourcedsasite**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-268">**SourceDsaSite**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f1d5-269">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-269">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-270">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f1d5-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f1d5-271">Ruft die Site ab, die den Quell Domänen Controller enthält.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-271">Gets the site that contains the source DC.</span></span>

</dd> <dt>

<span data-ttu-id="8f1d5-272">**Synchronisierungs Start**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-272">**SyncOnStartup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f1d5-273">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8f1d5-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-274">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f1d5-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f1d5-275">Ruft den Wert ab, der angibt, ob das Flag **DS \_ repl \_ NBR \_ Sync \_ on \_ Startup** in der **replicaflags** -Eigenschaft festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-275">Gets the value that indicates whether the **DS\_REPL\_NBR\_SYNC\_ON\_STARTUP** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="8f1d5-276">**Timeoflastsyncatcher**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-276">**TimeOfLastSyncAttempt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f1d5-277">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-277">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-278">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f1d5-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f1d5-279">Ruft den Zeitstempel für den letzten Replikations Versuch ab.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-279">Gets the timestamp for the last replication attempt.</span></span>

</dd> <dt>

<span data-ttu-id="8f1d5-280">**TimeOfLastSyncSuccess**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-280">**TimeOfLastSyncSuccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f1d5-281">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-281">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-282">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f1d5-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f1d5-283">Ruft den Zeitstempel für den letzten erfolgreichen Replikations Versuch ab.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-283">Gets the timestamp for the last successful replication attempt.</span></span>

</dd> <dt>

<span data-ttu-id="8f1d5-284">**Twowaysync**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-284">**TwoWaySync**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f1d5-285">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8f1d5-285">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-286">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f1d5-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f1d5-287">Ruft den Wert ab, der angibt, ob das Flag für die bidirektionale **\_ \_ \_ \_ \_ Synchronisierung von DS repl NBR** in der **replicaflags** -Eigenschaft festgelegt wurde</span><span class="sxs-lookup"><span data-stu-id="8f1d5-287">Gets the value that indicates whether the **DS\_REPL\_NBR\_TWO\_WAY\_SYNC** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="8f1d5-288">**Useasyncintersitetransport**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-288">**UseAsyncIntersiteTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f1d5-289">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8f1d5-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-290">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f1d5-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f1d5-291">Ruft den Wert ab, der angibt, ob das **DS \_ repl-NBR-Transport Flag für die \_ \_ \_ \_ Standort \_ übergreifende Verwendung** in der **replicaflags** -Eigenschaft festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-291">Gets the value that indicates whether the **DS\_REPL\_NBR\_USE\_ASYNC\_INTERSITE\_TRANSPORT** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="8f1d5-292">**"", "".**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-292">**USNAttributeFilter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f1d5-293">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-293">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-294">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f1d5-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f1d5-295">Ruft den Wert der Eigenschaft "Wert der Eigenschaft" "für" " **für das Ende** des letzten erfolgreichen abgeschlossenen Replikations Prozesses ab.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-295">Gets the **USNLastObjChangeSynced** property value at the end of the last successful completed replication cycle.</span></span> <span data-ttu-id="8f1d5-296">NULL, wenn keine erfolgreich abgeschlossenen Replikations Zyklen vorhanden waren.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-296">Zero if there were no successfully completed replication cycles.</span></span>

</dd> <dt>

<span data-ttu-id="8f1d5-297">**"" Für "" "" ".**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-297">**USNLastObjChangeSynced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f1d5-298">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-298">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-299">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f1d5-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f1d5-300">Ruft den [**unveränderten**](/windows/desktop/ADSchema/a-usnchanged) Attribut Wert des letzten empfangenen Objekt Updates ab.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-300">Gets the [**unchanged**](/windows/desktop/ADSchema/a-usnchanged) attribute value of the last object update that was received.</span></span>

</dd> <dt>

<span data-ttu-id="8f1d5-301">**Schreibbar**</span><span class="sxs-lookup"><span data-stu-id="8f1d5-301">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f1d5-302">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="8f1d5-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f1d5-303">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f1d5-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f1d5-304">Ruft den Wert ab, der angibt, ob das Flag zum Schreiben von **DS- \_ repl \_ NBR \_** in der **replicaflags** -Eigenschaft festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="8f1d5-304">Gets the value that indicates whether the **DS\_REPL\_NBR\_WRITEABLE** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8f1d5-305">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8f1d5-305">Requirements</span></span>



| <span data-ttu-id="8f1d5-306">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8f1d5-306">Requirement</span></span> | <span data-ttu-id="8f1d5-307">Wert</span><span class="sxs-lookup"><span data-stu-id="8f1d5-307">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f1d5-308">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8f1d5-308">Minimum supported client</span></span><br/> | <span data-ttu-id="8f1d5-309">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8f1d5-309">None supported</span></span><br/>                                                               |
| <span data-ttu-id="8f1d5-310">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8f1d5-310">Minimum supported server</span></span><br/> | <span data-ttu-id="8f1d5-311">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f1d5-311">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8f1d5-312">Namespace</span><span class="sxs-lookup"><span data-stu-id="8f1d5-312">Namespace</span></span><br/>                | <span data-ttu-id="8f1d5-313">\\Microsoftactivedirectory-Stammverzeichnis</span><span class="sxs-lookup"><span data-stu-id="8f1d5-313">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="8f1d5-314">MOF</span><span class="sxs-lookup"><span data-stu-id="8f1d5-314">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f1d5-315"><dt>ReplProv. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8f1d5-315"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f1d5-316">DLL</span><span class="sxs-lookup"><span data-stu-id="8f1d5-316">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f1d5-317"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f1d5-317"><dt>Replprov.dll</dt></span></span> </dl> |



 

