---
description: 'Weitere Informationen: jetgetlock-Funktion'
title: Jetgetlock-Funktion
TOCTitle: JetGetLock Function
ms:assetid: cebf0789-3d31-4ae8-9b23-dcf5e34e98fc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294094(v=EXCHG.10)
ms:contentKeyID: 32765709
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLock
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5757616214336de25ce30ca49755ac229b10afbe
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104132433"
---
# <a name="jetgetlock-function"></a>Jetgetlock-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetlock-function"></a>Jetgetlock-Funktion

Die **jetgetlock** -Funktion bietet die Möglichkeit, die Möglichkeit zum Aktualisieren von Zeilen, Schreiben einer Sperre oder explizit zu verhindern, dass eine Zeile von einer anderen Sitzung (Lesesperre) aktualisiert wird. Normalerweise werden Zeilen Schreib Sperren implizit durch das Aktualisieren von Zeilen abgerufen. Lese Sperren sind in der Regel aufgrund von Daten Satz Versionsverwaltung nicht erforderlich. In einigen Fällen möchte eine Transaktion jedoch möglicherweise eine Zeile explizit sperren, um die Serialisierung zu erzwingen, oder um sicherzustellen, dass ein nachfolgender Vorgang erfolgreich ausgeführt wird, da die erforderlichen Sperren bereits übernommen wurden.

```cpp
JET_ERR JET_API JetGetLock(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet wird.

*TableID*

Der Cursor, der für diesen-Befehl verwendet wird.

*grbit*

Eine Gruppe von Bits, die die für diesen-Befehl zu verwendenden Optionen enthalten, die NULL oder mehr der folgenden Elemente enthalten:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Wert</p></th>
<th><p>Bedeutung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitReadLock</p></td>
<td><p>Dieses Flag bewirkt, dass eine Lesesperre für den aktuellen Datensatz abgerufen wird. Lese Sperren sind nicht kompatibel mit Schreib sperren, die bereits von anderen Sitzungen gehalten wurden, aber mit Lese Sperren von anderen Sitzungen kompatibel sind.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitWriteLock</p></td>
<td><p>Dieses Flag bewirkt, dass eine Schreibsperre für den aktuellen Datensatz abgerufen wird. Schreib Sperren sind nicht kompatibel mit Schreib-oder Lese sperren, die von anderen Sitzungen aufrechterhalten werden, aber mit Lese Sperren in derselben Sitzung kompatibel sind.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Rückgabecode</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Der Vorgang wurde erfolgreich abgeschlossen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Das angegebene <em>grbit</em> ist weder JET_bitReadLock noch JET_bitWriteLock. Dabei muss es sich um eines dieser beiden Flags handeln.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Der Cursor muss sich in einem Datensatz befinden, um eine Sperre zu erhalten. Sperren sind Always on-Datensätze.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInTransaction</p></td>
<td><p>Sperren können nur von Sitzungen in einer Transaktion abgerufen werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPermissionDenied</p></td>
<td><p>Der Cursor kann nicht schreibgeschützt sein und eine Schreibsperre erhalten.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransReadOnly</p></td>
<td><p>Die Sitzung muss über Schreibberechtigungen verfügen, um eine Schreibsperre zu erhalten.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict</p></td>
<td><p>Der Fehler, der zurückgegeben wird, wenn eine widersprüchliche Sperre angefordert wird.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg hat die Sitzung die angeforderte Sperre erhalten.

Bei einem Fehler hat die Sitzung die angeforderte Sperre nicht abgerufen.

#### <a name="remarks"></a>Bemerkungen

Schreib Sperren können nicht mit Sitzungen oder Cursorn mit schreibgeschützten Berechtigungen abgerufen werden, auch wenn die Sitzung und der Cursor letztendlich keinen Aktualisierungs Vorgang ausführen. Sowohl die Sitzung als auch der Cursor müssen über Schreibberechtigungen verfügen, um eine Schreibsperre zu erhalten.

Lese-und Schreib Sperren sind eine Möglichkeit der pessimistischen Sperrung. Das pessimistische sperren erwartet, dass mehrere gleichzeitige Sitzungen in Konflikt stehen und Sperren im Voraus erhalten, um sicherzustellen, dass Ihre Vorgänge erfolgreich

Die meisten Vorgänge werden aufgrund von implizit ergriffene Sperren serialisierbar sein. Bei einigen Vorgängen wird dies jedoch nicht der Fall sein. Um dies zu veranschaulichen, sehen Sie sich die beiden Transaktionen an:

T1: R (a), U (B)

T2: R (B), U (a)

Durch die Versionsverwaltung auf Datensatzebene wird sichergestellt, dass jede Transaktion bei gleichzeitiger Ausführung die ursprünglichen Werte für A und B angezeigt wird. Es gibt keine serielle Reihenfolge der Ausführung, die dieselben Ergebnisse für A und B erzielen kann, wenn die Ergebnisse von den gelesenen Daten abhängig sind. Damit die Anwendung diese Transaktion serialisierbar macht, sollte Sie eine explizite Lesesperre für A und B in jeder Transaktion erhalten, wenn der Wert gelesen wird.

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothek</strong></p></td>
<td><p>Verwenden Sie ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Erfordert ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[Jetprepareupdate](./jetprepareupdate-function.md)  
[Jetstopservice](./jetstopservice-function.md)  
[Jetupdate](./jetupdate-function.md)
