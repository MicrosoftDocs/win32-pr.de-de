---
description: 'Weitere Informationen finden Sie hier: JetCommitTransaction2-Funktion'
title: JetCommitTransaction2-Funktion
TOCTitle: JetCommitTransaction2 Function
ms:assetid: 55b89f8e-7073-4fc2-bf97-103b4bc45e1c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835041(v=EXCHG.10)
ms:contentKeyID: 49894663
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCommitTransaction2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 24dfecd091de027f51ed8f69c0441fbc7cbd57af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373318"
---
# <a name="jetcommittransaction2-function"></a>JetCommitTransaction2-Funktion


_**Gilt für:** Windows | Windows Server_

Die **JetCommitTransaction2** -Funktion führt einen Commit für die Änderungen aus, die an den Zustand der Datenbank während des aktuellen Speicher Punkts vorgenommen werden, und migriert Sie zum vorherigen Sicherungspunkt. Wenn für den äußersten Speicherpunkt ein Commit ausgeführt wird, werden die während dieses Speicher Punkts vorgenommenen Änderungen an den Status der Datenbank übertragen, und die Sitzung wird beendet.

Die **JetCommitTransaction2** -Funktion wurde im Windows 8-Betriebssystem eingeführt.

``` c++
JET_ERR JET_API JetCommitTransaction2(
  __in          JET_SESID sesid,
  __in          JET_GRBIT grbit,
  __in          DWORD cmsecDurableCommit,
  __out         JET_COMMIT_ID pCommitID
);
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*grbit*

Eine Gruppe von Bits, die NULL oder mehr der in der folgenden Tabelle aufgeführten Werte angeben.

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
<td><p>JET_bitCommitLazyFlush</p></td>
<td><p>Die Transaktion wird normal ausgeführt, aber diese API wartet nicht, bis die Transaktion in die Transaktionsprotokoll Datei geleert wurde, bevor Sie an den Aufrufer zurückgegeben wird. Dadurch wird die Dauer eines Commitvorgangs drastisch reduziert und die Dauerhaftigkeit beeinträchtigt. Alle Transaktionen, die vor einem Absturz nicht in das Protokoll geschrieben werden, werden während des nächsten Aufrufens der <a href="gg294068(v=exchg.10).md">jetinit</a> -Funktion automatisch abgebrochen.</p>
<p>Wenn JET_bitWaitLastLevel0Commit oder JET_bitWaitAllLevel0Commit angegeben werden, wird diese Option ignoriert.</p>
<p>Wenn dieser <strong>JetCommitTransaction2</strong> -Aufrufvorgang nicht mit dem ersten Aufrufen der <a href="gg294083(v=exchg.10).md">jetbegintransaction</a> -Funktion für diese Sitzung identisch ist, wird diese Option ignoriert. Dies liegt daran, dass die letzte Aktion, die auf dem äußersten Speicherpunkt auftritt, der bestimmende Faktor ist, der angibt, ob die gesamte Transaktion tatsächlich auf den Datenträger übertragen wird</p></td>
</tr>
<tr class="even">
<td><p>JET_bitWaitAllLevel0Commit</p></td>
<td><p>Alle Transaktionen, für die zuvor von einer Sitzung ein Commit ausgeführt wurde und die noch nicht in die Transaktionsprotokoll Datei geleert wurden, werden sofort geleert. Diese API wartet, bis die Transaktionen geleert wurden, bevor Sie an den Aufrufer zurückgegeben werden.</p>
<p>Diese Option kann auch verwendet werden, wenn sich die Sitzung derzeit nicht in einer Transaktion befindet.</p>
<p>Diese Option kann nicht in Kombination mit anderen Optionen verwendet werden.</p>
<p>Diese Option ist ab Windows Server 2003 in Versionen des Windows Server-Betriebssystems verfügbar.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitWaitLastLevel0Commit</p></td>
<td><p>Wenn für die Sitzung bereits ein Commit für Transaktionen ausgeführt wurde und diese noch nicht in die Transaktionsprotokoll Datei geleert wurden, sollten Sie sofort geleert werden. Diese API wartet, bis die Transaktionen geleert wurden, bevor Sie an den Aufrufer zurückgegeben werden. Dies ist nützlich, wenn die Anwendung zuvor mehrere Transaktionen mit JET_bitCommitLazyFlush committet hat und diese nun auf den Datenträger leeren möchte.</p>
<p>Diese Option kann auch verwendet werden, wenn sich die Sitzung derzeit nicht in einer Transaktion befindet.</p>
<p>Diese Option kann nicht in Kombination mit anderen Optionen verwendet werden.</p></td>
</tr>
</tbody>
</table>


*cmsecdurablecommit*

Die Dauer für das Commit einer verzögerten Transaktion.

*pcomentschärd*

Die Commit-ID, die diesem Commitdatensatz zugeordnet ist.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) -Datentyp mit einem der in der folgenden Tabelle aufgelisteten Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern (Extensible Storage Engine) finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Fehler Behandlungsparameter](./error-handling-parameters.md).

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
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens der <a href="gg269240(v=exchg.10).md">jetstopservice</a> -Funktion beendet wurden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</p>
<p>Dieser Fehler wird nur von Versionen des Windows-Betriebssystems ab Windows XP zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Eine der angeforderten Optionen war ungültig oder nicht implementiert. Dieser Fehler wird von der <strong>JetCommitTransaction2</strong> -Funktion zurückgegeben, wenn Folgendes geschieht:</p>
<ul>
<li><p>Es wurde ein ungültiges <em>grbit</em> angegeben.</p></li>
<li><p>JET_bitWaitLastLevel0Commit wurde in Kombination mit einem anderen <em>grbit</em>angegeben.</p></li>
<li><p>JET_bitWaitAllLevel0Commit wurde in Kombination mit einem anderen <em>grbit</em>angegeben.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInTransaction</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da die angegebene Sitzung nicht in einer Transaktion ausgeführt wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</p>
<p>Dieser Fehler wird nur von Versionen des Windows-Betriebssystems ab Windows XP zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg werden alle Änderungen, die während des aktuellen Speicher Punkts für die jeweilige Sitzung an der Datenbank vorgenommen wurden, committet, und der Sicherungspunkt wird beendet. Wenn der letzte Sicherungspunkt für die Sitzung beendet wurde, wird die Transaktion optional in die Transaktionsprotokoll Datei geleert, und die Sitzung wird beendet.

Bei einem Fehler bleibt der Transaktionsstatus der Sitzung unverändert. Es erfolgt keine Änderung des Daten Bank Status. Die Anwendung sollte die [jetrollback](./jetrollback-function.md) -Funktion anrufen, um die Transaktion abzubrechen.

#### <a name="remarks"></a>Bemerkungen

Es muss ein **JetCommitTransaction2** -oder [jetrollback](./jetrollback-function.md) -Rückruf vorhanden sein, um jeden Aufrufen von [jetbegintransaction](./jetbegintransaction-function.md) für eine bestimmte Sitzung abzugleichen.

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2012.</p></td>
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


#### <a name="see-also"></a>Siehe auch

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[Jetbegintransaction](./jetbegintransaction-function.md)  
[Jetcommittransaction](./jetcommittransaction-function.md)  
[Jetrollback](./jetrollback-function.md)  
[Jetstopservice](./jetstopservice-function.md)
