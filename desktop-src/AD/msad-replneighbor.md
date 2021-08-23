---
title: MSAD_ReplNeighbor-Klasse
description: Stellt die DS REPL NEIGHBOR-Struktur dar, die die eingehenden Replikationszustandsinformationen für ein bestimmtes \_ \_ Benennungskontext-/Quellserverpaar enthält.
ms.assetid: fdd3934b-a3f6-49ad-827b-077bcd21cf23
ms.tgt_platform: multiple
keywords:
- MSAD_ReplNeighbor Active Directory-Klasse
- MSAD_ReplNeighbor Active Directory-Klasse , beschrieben
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
ms.openlocfilehash: 0598116413d34334e0610895a9c3b0629399fed8bb482e0d08cdae9cafb17fe4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025758"
---
# <a name="msad_replneighbor-class"></a>MSAD \_ ReplNeighbor-Klasse

Stellt die [**DS \_ REPL \_ NEIGHBOR-Struktur**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw) dar, die die eingehenden Replikationsstatusinformationen für einen bestimmten Benennungskontext (NC) und ein Quellserverpaar enthält, wie von der [**DsReplicaGetInfo-Funktion**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) zurückgegeben.

## <a name="syntax"></a>Syntax

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

## <a name="members"></a>Member

Die **MSAD \_ ReplNeighbor-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MSAD \_ ReplNeighbor-Klasse** verfügt über diese Methoden.



| Methode                                                           | BESCHREIBUNG                                                                   |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**SyncNamingContext**](syncnamingcontext-msad-replneighbor.md) | Synchronisiert einen Zielnamenskontext mit einer seiner Quellen.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **MSAD \_ ReplNeighbor-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AsyncIntersiteTransportDN**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den X.500-Pfad des [**interSiteTransport-Objekts**](/windows/desktop/ADSchema/c-intersitetransport) ab, das dem Transport entspricht, über den die Replikation ausgeführt wird. Legen Sie für **die** RPC/IP-Replikation auf NULL fest.

</dd> <dt>

**AsyncIntersiteTransportObjGuid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft die GUID des standortübergreifenden Transportobjekts ab, das der **AsyncIntersiteTransportDN-Eigenschaft** entspricht.

</dd> <dt>

**CompressChanges**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert ab, der angibt, ob das **DS \_ REPL \_ NBR \_ COMPRESS \_ CHANGES-Flag** in der **ReplicaFlags-Eigenschaft festgelegt** wurde.

</dd> <dt>

**DisableScheduledSync**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert ab, der angibt, ob das **Flag DS \_ REPL \_ NBR \_ DISABLE SCHEDULED \_ \_ SYNC** in der **ReplicaFlags-Eigenschaft festgelegt** wurde.

</dd> <dt>

**Domain**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den kanonischen Namen der Domäne des replizierten NC ab.

</dd> <dt>

**DoScheduledSyncs**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert ab, der angibt, ob das **Flag DS \_ REPL \_ NBR \_ DO SCHEDULED \_ \_ SYNCS** in der **ReplicaFlags-Eigenschaft festgelegt** wurde.

</dd> <dt>

**FullSyncInProgress**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert ab, der angibt, ob das **Flag DS \_ REPL \_ NBR \_ FULL SYNC \_ \_ IN \_ PROGRESS** in der **ReplicaFlags-Eigenschaft festgelegt** wurde.

</dd> <dt>

**FullSyncNextPacket**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert ab, der angibt, ob das **Flag DS \_ REPL \_ NBR \_ FULL SYNC \_ \_ NEXT \_ PACKET** in der **ReplicaFlags-Eigenschaft festgelegt** wurde.

</dd> <dt>

**IgnoreChangeNotifications**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert ab, der angibt, ob das **Flag DS \_ REPL \_ NBR \_ IGNORE CHANGE \_ \_ NOTIFICATIONS** in der **ReplicaFlags-Eigenschaft festgelegt** wurde.

</dd> <dt>

**IsDeletedSourceDsa**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert ab, der angibt, ob diese Verbindung einen gelöschten Quelldomänencontroller darstellt. **TRUE,** wenn diese Verbindung einen gelöschten Quelldomänencontroller darstellt; andernfalls **FALSE**. Standardmäßig repliziert der DS diese Verbindungen nach dem Löschen des Quelldomänencontrollers noch einige Zeit.

</dd> <dt>

**LastSyncResult**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den **HRESULT-Fehlercode** für den letzten Replikationsversuch ab.

</dd> <dt>

**ModifiedNumConsecutiveSyncFailures**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft die Anzahl der aufeinanderfolgenden fehlgeschlagenen Replikationsversuche ab, einschließlich der Verbindungen, bei denen ein Fehler erwartet wird. Wenn die **IsDeletedSourceDsa-Eigenschaft** beispielsweise auf **TRUE** festgelegt ist, wird ein Fehler erwartet.

</dd> <dt>

**NamingContextDN**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ruft den X.500-Pfad für den NC ab, der von dieser Verbindung repliziert wird.

</dd> <dt>

**NamingContextObjGuid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft die GUID für den replizierten NC ab.

</dd> <dt>

**NeverSynced**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert ab, der angibt, ob das **DS \_ REPL \_ NBR \_ NEVER \_ SYNCED-Flag** in der **ReplicaFlags-Eigenschaft festgelegt** wurde.

</dd> <dt>

**NoChangeNotifications**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert ab, der angibt, ob das **DS \_ REPL \_ NBR \_ NO CHANGE \_ \_ NOTIFICATIONS-Flag** in der **ReplicaFlags-Eigenschaft festgelegt** wurde.

</dd> <dt>

**NumConsecutiveSyncFailures**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft die Anzahl der aufeinanderfolgenden fehlgeschlagenen Replikationsversuche ab.

</dd> <dt>

**ReplicaFlags**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Satz von Flags ab, die Attribute und Optionen für die Replikationsdaten angeben. Diese Eigenschaft kann 0 (null) oder eine Kombination aus mindestens einem der folgenden Flags sein.

<dt>

<span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>

<span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>**DS \_ REPL \_ NBR \_ WRITEABLE** (16 (0x10))


</dt> <dd>

Die lokale Kopie des Namenskontexts ist nicht schreibgeschützt.

</dd> <dt>

<span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>

<span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>**DS \_ REPL \_ NBR \_ SYNC BEIM \_ \_ START** (32 (0x20))


</dt> <dd>

Die Replikation dieses Namenskontexts aus dieser Quelle wird versucht, wenn der Zielserver gestartet wird. Dieses Flag gilt in der Regel nur für standortinterne Nachbarn.

</dd> <dt>

<span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>

<span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>**DS \_ REPL \_ NBR \_ DO SCHEDULED \_ \_ SYNCS** (64 (0x40))


</dt> <dd>

Die Replikation nach einem Zeitplan ausführen. Dieses Flag wird in der Regel festgelegt, es sei denn, der Zeitplan für diesen Benennungskontext oder die Quelle ist "never", d.&a; der leere Zeitplan.

</dd> <dt>

<span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>

<span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>**DS \_ REPL \_ NBR \_ USE \_ ASYNC \_ INTERSITE \_ TRANSPORT** (128 (0x80))


</dt> <dd>

Die Replikation indirekt über den standortübergreifenden Meldungsdienst ausführen. Dieses Flag wird nur festgelegt, wenn über SMTP repliziert wird. Dieses Flag wird nicht festgelegt, wenn über standortübergreifendes RPC/IP repliziert wird.

</dd> <dt>

<span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>

<span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>**DS \_ REPL \_ NBR \_ TWO WAY \_ \_ SYNC** (512 (0x200))


</dt> <dd>

Wenn festgelegt, gibt an, dass der Zielserver nach Abschluss der eingehenden Replikation dem Quellserver mitteilen muss, dass die Synchronisierung in umgekehrter Richtung ausgeführt werden soll. Dieses Feature wird in DFÜ-Szenarien verwendet, in denen nur einer der beiden Server eine DFÜ-Verbindung initiieren kann. Diese Option kann beispielsweise in einem Hauptsitz und einer Filiale des Unternehmens verwendet werden, wo die Zweigstelle über das Internet über eine DFÜ-ISP-Verbindung eine Verbindung mit dem Hauptsitz des Unternehmens herstellt.

</dd> <dt>

<span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>

<span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>**DS \_ REPL \_ NBR \_ RETURN OBJECT \_ \_ PARENTS** (2048 (0x800))


</dt> <dd>

Dieser Nachbar befindet sich in einem Zustand, in dem er vor untergeordneten Objekten übergeordnete Objekte zurückgibt. Der Nachbar wechselt in diesen Zustand, nachdem er ein untergeordnetes Element vor dem zugehörigen übergeordneten Element empfangen hat.

</dd> <dt>

<span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>

<span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>**DS \_ REPL \_ NBR \_ FULL SYNC \_ IN \_ \_ PROGRESS** (65536 (0x10000))


</dt> <dd>

Der Zielserver führt eine vollständige Synchronisierung vom Quellserver aus. Vollständige Synchronisierungen verwenden keine Vektoren, die Updates (z. B. [**DS \_ REPL \_ CURSORS)**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)zum Filtern von Updates erstellen. Vollständige Synchronisierungen werden nicht als Teil des Standardreplikationsprotokolls verwendet.

</dd> <dt>

<span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>

<span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>**DS \_ REPL \_ NBR \_ FULL SYNC \_ NEXT \_ \_ PACKET** (131072 (0x20000))


</dt> <dd>

Das letzte Paket aus der Quelle hat eine Änderung eines Objekts angegeben, das der Zielserver noch nicht erstellt hat. Das nächste angeforderte Paket weist den Quellserver an, alle Attribute des geänderten Objekts in das Paket zu setzen.

</dd> <dt>

<span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>

<span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>**DS \_ REPL \_ NBR \_ NEVER \_ SYNCED** (2097152 (0x200000))


</dt> <dd>

Eine Synchronisierung ist von dieser Quelle nie erfolgreich abgeschlossen worden.

</dd> <dt>

<span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>

<span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>**DS \_ REPL \_ NBR \_ PREEMPTED** (16777216 (0x1000000))


</dt> <dd>

Die Replikations-Engine hat die Verarbeitung dieses Nachbarn vorübergehend beendet, um einen anderen Nachbarn mit höherer Priorität zu verarbeiten, entweder für diese Partition oder für eine andere Partition. Die Replikations-Engine fährt mit der Verarbeitung dieses Nachbarn fort, nachdem die Arbeit mit der höheren Priorität abgeschlossen wurde.

</dd> <dt>

<span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>

<span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>**DS \_ REPL \_ NBR \_ IGNORE CHANGE \_ \_ NOTIFICATIONS** (67108864 (0x4000000))


</dt> <dd>

Dieser Nachbar ist so festgelegt, dass benachrichtigungsbasierte Synchronisierungen deaktiviert werden. Innerhalb eines Standorts werden Domänencontroller bei Vornahme von Änderungen auf Grundlage von Benachrichtigungen miteinander synchronisiert. Diese Einstellung verhindert, dass dieser Nachbar Synchronisierungen durchführen kann, die durch Benachrichtigungen ausgelöst werden. Der Nachbar wird weiterhin Synchronisierungen basierend auf seinem Zeitplan oder als Reaktion auf manuell angeforderte Synchronisierungen durchführen.

</dd> <dt>

<span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>

<span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>**DS \_ REPL \_ NBR \_ DISABLE SCHEDULED \_ \_ SYNC** (134217728 (0x8000000))


</dt> <dd>

Dieser Nachbar ist so festgelegt, dass keine Synchronisierungen basierend auf seinem Zeitplan ausgeführt werden. Der Nachbar führt Synchronisierungen nur als Reaktion auf Änderungsbenachrichtigungen oder manuell angeforderte Synchronisierungen durch.

</dd> <dt>

<span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>

<span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>**DS \_ REPL \_ NBR \_ COMPRESS \_ CHANGES** (268435456 (0x10000000))


</dt> <dd>

Die von dieser Quelle empfangenen Änderungen müssen komprimiert werden. Die Komprimierung erfolgt in der Regel nur, wenn sich der Quellserver an einem anderen Standort befindet.

</dd> <dt>

<span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>

<span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>**DS \_ REPL \_ NBR \_ NO CHANGE \_ \_ NOTIFICATIONS** (536870912 (0x20000000))


</dt> <dd>

Von dieser Quelle sollten keine Änderungsbenachrichtigungen empfangen werden. Wird normalerweise nur festgelegt, wenn sich der Quellserver an einem anderen Standort befindet.

</dd> <dt>

<span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>

<span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>**DS \_ REPL \_ NBR \_ PARTIAL ATTRIBUTE \_ \_ SET** (1073741824 (0x40000000))


</dt> <dd>

Dieser Nachbar befindet sich in einem Zustand, in dem er den Inhalt dieses Replikats aufgrund einer Änderung im Teilattributsatz neu erstellt.

</dd> </dl>

</dd> <dt>

**SourceDsaAddress**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft die DNS-Adresse des Quelldomänencontrollers ab.

> [!Note]  
> Diese Zeichenfolge enthält eine geänderte GUID, nicht den häufig verwendeten kanonischen DNS-Namen.

 

</dd> <dt>

**SourceDsaCN**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft die Objektpfadkomponente für das DSA ab, das den Quelldomänencontroller darstellt. Diese Zeichenfolge ähnelt häufig dem Computernamen, ist aber nicht immer identisch.

</dd> <dt>

**SourceDsaDN**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den X.500-Pfad für das DSA ab, das den Quelldomänencontroller darstellt.

</dd> <dt>

**SourceDsaInvocationID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft die Aufruf-ID ab, die seit der letzten Replikation vom Quellserver verwendet wurde.

</dd> <dt>

**SourceDsaObjGuid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ruft die GUID für den Verzeichnisdienst-Agent (DSA) ab, der den Quelldomänencontroller (DC) darstellt.

</dd> <dt>

**SourceDsaSite**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Standort ab, der den Quelldomänencontroller enthält.

</dd> <dt>

**SyncOnStartup**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert ab, der angibt, ob das **Flag DS \_ REPL \_ NBR \_ SYNC ON \_ \_ STARTUP** in der **ReplicaFlags-Eigenschaft festgelegt** wurde.

</dd> <dt>

**TimeOfLastSyncAttempt**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Zeitstempel für den letzten Replikationsversuch ab.

</dd> <dt>

**TimeOfLastSyncSuccess**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Zeitstempel für den letzten erfolgreichen Replikationsversuch ab.

</dd> <dt>

**TwoWaySync**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert ab, der angibt, ob das **DS \_ REPL \_ NBR \_ TWO WAY \_ \_ SYNC-Flag** in der **ReplicaFlags-Eigenschaft festgelegt** wurde.

</dd> <dt>

**UseAsyncIntersiteTransport**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert ab, der angibt, ob das **DS \_ REPL \_ NBR \_ USE \_ ASYNC \_ INTERSITE \_ TRANSPORT-Flag** in der **ReplicaFlags-Eigenschaft festgelegt** wurde.

</dd> <dt>

**USNAttributeFilter**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den **USNLastObjChangeSynced-Eigenschaftswert** am Ende des letzten erfolgreich abgeschlossenen Replikationszyklus ab. 0 (null), wenn keine erfolgreich abgeschlossenen Replikationszyklen durchgeführt wurden.

</dd> <dt>

**USNLastObjChangeSynced**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den [**unveränderten**](/windows/desktop/ADSchema/a-usnchanged) Attributwert des letzten empfangenen Objektupdates ab.

</dd> <dt>

**Schreibbar**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Wert ab, der angibt, ob das **DS \_ REPL \_ NBR \_ WRITEABLE-Flag** in der **ReplicaFlags-Eigenschaft** festgelegt wurde.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\MicrosoftActiveDirectory-Stammverzeichnis<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



 

