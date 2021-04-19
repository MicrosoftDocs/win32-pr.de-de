---
description: Weitere Informationen finden Sie in der jetgetcurrsorinfo-Funktion
title: Jetgetcurrsorinfo-Funktion
TOCTitle: JetGetCursorInfo Function
ms:assetid: e779fa5d-1d7e-46f1-80c9-f7c819279188
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294126(v=EXCHG.10)
ms:contentKeyID: 32765740
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetCursorInfo
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7201c37f79f68deead837cdcdd90402e4b2bf1e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366506"
---
# <a name="jetgetcursorinfo-function"></a>Jetgetcurrsorinfo-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetcursorinfo-function"></a>Jetgetcurrsorinfo-Funktion

Die **jetgetcursorinfo** -Funktion wird verwendet, um zu bestimmen, ob ein Update des aktuellen Datensatzes eines Cursors basierend auf dem aktuellen Update Status des Datensatzes zu einem Schreib Konflikt führt. Es ist möglich, dass ein Schreib Konflikt letztendlich zurückgegeben wird, auch wenn **jetgetcurrsorinfo** JET_errSuccess zurückgibt, da eine andere Sitzung den Datensatz aktualisieren kann, bevor die aktuelle Sitzung denselben Datensatz aktualisieren kann.

```cpp
    JET_ERR JET_API JetGetCursorInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet wird.

*TableID*

Der Cursor, der für diesen-Befehl verwendet wird.

*pvresult*

Für die zukünftige Verwendung reserviert.

*cbmax*

Muss auf 0 (null) festgelegt werden, andernfalls nicht verwendet. Es ist für zukünftige Funktionen vorhanden.

*Infolevel*

Muss auf 0 (null) festgelegt werden, andernfalls nicht verwendet. Es ist für zukünftige Funktionen vorhanden.

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
<td><p>JET_errInvalidParameter</p></td>
<td><p><em>Cbmax</em> ist nicht 0 (null), oder <em>infolevel</em> ist nicht 0 (null).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Der Cursor befindet sich derzeit nicht in einem Datensatz, und die Informationen zu einem logischen Datensatz können nicht als Ergebnis zurückgegeben werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
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
<td><p>JET_errWriteConflict</p></td>
<td><p>Der aktuelle Datensatz des Cursors wurde von einer anderen Sitzung aktualisiert, und ein Update dieses Datensatzes durch diese Sitzung führt zu einem Schreib Konflikt.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg hat dieser Vorgang keine Auswirkung auf die Position des Cursors, sondern gibt nur an, dass dieser Datensatz zurzeit von keiner anderen Sitzung aktualisiert wurde.

Bei einem Fehler gibt es keine Auswirkung auf den Cursor oder die Datenbank, wenn ein negativer Fehlercode zurückgegeben wird.

#### <a name="remarks"></a>Bemerkungen

Dieser Vorgang wirkt sich nicht auf den Status des Cursors oder der Daten aus. Es wird nur ein Fehlercode zurückgegeben, der beschreibt, ob ein Update des aktuellen Datensatzes durch die aufrufende Sitzung bekanntermaßen zu einer JET_errWriteConflict führt oder unbekannt ist, JET_errWriteConflict zurückzugeben. Wenn dieser Datensatz bereits von einer anderen Sitzung aktualisiert wurde, um ihn zu verwenden, ist sicherzustellen, dass ein Update dieses Datensatzes durch diese Sitzung zu einem Schreib Konflikt führt. Dies gilt, bis diese Sitzung einen Commit oder Rollback der Transaktionen auf die Transaktionsebene 0 (null) ausführt. Wenn **jetgetcursor Info** jedoch JET_errSuccess zurückgibt, ist es weiterhin möglich, dass eine andere Sitzung diesen Datensatz vor der aktuellen Sitzung aktualisiert. Folglich ist es weiterhin möglich, dass ein Update des aktuellen Datensatzes durch diese Sitzung in der aktuellen Transaktion zu einem Schreib Konflikt führt.

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
[Jetgetlock](./jetgetlock-function.md)  
[Jetprepareupdate](./jetprepareupdate-function.md)  
[Jetstopservice](./jetstopservice-function.md)  
[Jetupdate](./jetupdate-function.md)
