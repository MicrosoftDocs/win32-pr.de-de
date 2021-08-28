---
description: 'Weitere Informationen zu: JetCommitTransaction2-Funktion'
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
ms.openlocfilehash: 6080380fd8326504e7b1182b439571e3904f0d53
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986063"
---
# <a name="jetcommittransaction2-function"></a>JetCommitTransaction2-Funktion


_**Gilt für:** Windows | Windows Server_

Die **JetCommitTransaction2-Funktion** committet die Änderungen, die während des aktuellen Speicherpunkts am Zustand der Datenbank vorgenommen wurden, und migriert sie zum vorherigen Sicherungspunkt. Wenn für den äußersten Sicherungspunkt ein Commit ausgeführt wird, wird für die während dieses Speicherpunkts vorgenommenen Änderungen ein Commit in den Zustand der Datenbank ausgeführt, und die Sitzung beendet die Transaktion.

Die **JetCommitTransaction2-Funktion** wurde im Windows 8 Betriebssystem eingeführt.

``` c++
JET_ERR JET_API JetCommitTransaction2(
  __in          JET_SESID sesid,
  __in          JET_GRBIT grbit,
  __in          DWORD cmsecDurableCommit,
  __out         JET_COMMIT_ID pCommitID
);
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*grbit*

Eine Gruppe von Bits, die null oder mehr der in der folgenden Tabelle aufgeführten Werte angeben.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitCommitLazyFlush</p> | <p>Für die Transaktion wird normal ein Commit ausgeführt, aber diese API wartet nicht, bis die Transaktion in die Transaktionsprotokolldatei geleert wird, bevor sie an den Aufrufer zurückgegeben wird. Dadurch wird die Dauer eines Commitvorgangs auf Kosten der Dauerhaftigkeit drastisch reduziert. Jede Transaktion, die vor einem Absturz nicht in das Protokoll geleert wird, wird während der Absturzwiederherstellung beim nächsten Aufruf der <a href="gg294068(v=exchg.10).md">JetInit-Funktion</a> automatisch abgebrochen.</p><p>Wenn JET_bitWaitLastLevel0Commit oder JET_bitWaitAllLevel0Commit angegeben sind, wird diese Option ignoriert.</p><p>Wenn dieser Aufruf von <strong>JetCommitTransaction2</strong> nicht mit dem ersten Aufruf der <a href="gg294083(v=exchg.10).md">JetBeginTransaction-Funktion</a> für diese Sitzung übereinstimmt, wird diese Option ignoriert. Dies liegt daran, dass die letzte Aktion, die am äußersten Sicherungspunkt ausgeführt wird, der bestimmende Faktor ist, ob für die gesamte Transaktion tatsächlich ein Commit auf den Datenträger ausgeführt wird.</p> | 
| <p>JET_bitWaitAllLevel0Commit</p> | <p>Alle Transaktionen, für die zuvor von einer Sitzung ein Commit ausgeführt wurde, die noch nicht in die Transaktionsprotokolldatei geleert wurden, werden sofort geleert. Diese API wartet, bis die Transaktionen geleert wurden, bevor sie an den Aufrufer zurückgegeben wird.</p><p>Diese Option kann auch dann verwendet werden, wenn sich die Sitzung derzeit nicht in einer Transaktion befindet.</p><p>Diese Option kann nicht in Kombination mit einer anderen Option verwendet werden.</p><p>Diese Option ist ab Windows Server 2003 in Versionen des Betriebssystems Windows Server verfügbar.</p> | 
| <p>JET_bitWaitLastLevel0Commit</p> | <p>Wenn für die Sitzung zuvor ein Commit für Transaktionen ausgeführt wurde und sie noch nicht in die Transaktionsprotokolldatei geleert wurden, sollten sie sofort geleert werden. Diese API wartet, bis die Transaktionen geleert wurden, bevor sie an den Aufrufer zurückgegeben wird. Dies ist nützlich, wenn die Anwendung zuvor mithilfe von JET_bitCommitLazyFlush mehrere Transaktionen ausgeführt hat und nun alle Transaktionen auf den Datenträger leeren möchte.</p><p>Diese Option kann auch dann verwendet werden, wenn sich die Sitzung derzeit nicht in einer Transaktion befindet.</p><p>Diese Option kann nicht in Kombination mit einer anderen Option verwendet werden.</p> | 



*cmsecDurableCommit*

Die Dauer des Commits einer verzögerten Transaktion.

*pCommitID*

Die Commit-ID, die diesem Commitdatensatz zugeordnet ist.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der in der folgenden Tabelle aufgeführten Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern (Extensible Storage Engine) finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs der <a href="gg269240(v=exchg.10).md">JetStopService-Funktion</a> ausgeführt wurden.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da für die instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p>Dieser Fehler wird nur von Versionen des Windows Betriebssystems zurückgegeben, die mit Windows XP beginnen.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Eine der angeforderten Optionen war ungültig oder nicht implementiert. Dieser Fehler wird von der <strong>JetCommitTransaction2-Funktion</strong> zurückgegeben, wenn Folgendes auftritt:</p><ul><li><p>Ein ungültiges <em>Grbit</em> wird angegeben.</p></li><li><p>JET_bitWaitLastLevel0Commit wurde in Kombination mit einem anderen <em>grbit</em>angegeben.</p></li><li><p>JET_bitWaitAllLevel0Commit wurde in Kombination mit einem anderen <em>grbit</em>angegeben.</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errNotInTransaction</p> | <p>Fehler beim Vorgang, weil sich die angegebene Sitzung nicht in einer Transaktion befindet.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht für mehrere Threads gleichzeitig verwendet werden.</p><p>Dieser Fehler wird nur von Versionen des Windows Betriebssystems zurückgegeben, die mit Windows XP beginnen.</p> | 
| <p>JET_errTermInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Bei Erfolg wird für alle Änderungen, die während des aktuellen Speicherpunkts für die angegebene Sitzung an der Datenbank vorgenommen wurden, ein Commit ausgeführt, und dieser Sicherungspunkt wird beendet. Wenn der letzte Sicherungspunkt für die Sitzung beendet wurde, wird die Transaktion optional in die Transaktionsprotokolldatei geleert, und die Sitzung beendet die Transaktion.

Bei einem Fehler bleibt der Transaktionsstatus der Sitzung unverändert. Es wird keine Änderung am Datenbankzustand vorgenommen. Die Anwendung sollte die [JetRollback-Funktion](./jetrollback-function.md) aufrufen, um die Transaktion abzubricht.

#### <a name="remarks"></a>Bemerkungen

Es muss einen Aufruf von **JetCommitTransaction2** oder [JetRollback](./jetrollback-function.md) geben, damit jeder Aufruf von [JetBeginTransaction](./jetbegintransaction-function.md) für eine bestimmte Sitzung übereinstimmt.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows 8.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2012.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Siehe auch

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)
